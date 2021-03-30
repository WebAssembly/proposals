# Creating and Managing a Wasm Proposal Repository

## 0. CG Approval

First, you need to get the CG on board.

1. Present the proposal at a [CG meeting](https://github.com/WebAssembly/meetings).

2. Have a successful poll for moving it to phase 1.


## 1. Creating the Repository

You need admin rights for the GitHub WebAsssembly organisation to execute this step. If you don’t have that, you will need to ask one of the maintainers (@binji, @rossberg, @lukewagner) to do it for you.

1. Pick a repository name for the proposal, e.g., `multi-bulklets`

   * in the rest of this document, replace all occurrences of `<<proposal>>` with that name

2. Create the repository on GitHub:

   1. Go to https://github.com/WebAssembly

   2. Click “New”

   3. Enter "Repository name": `<<proposal>>`

   4. Enter “Description”: the repository title, e.g., `Multiple Bulklets Proposal`

   5. Click "Create repository”

3. If you are a maintainer and not the champion, make the champion an admin for this repo:

   1. Click "Settings”

   2. Go to the "Manage Access" settings

   3. Click "Invite teams or people" and enter the champion’s GitHub user name

   4. Select the "Admin" role and add the champion to the repository


## Populating the Repository

Every proposal repository is supposed to be a fork of the main `spec` repo. Unfortunately, GitHub does not allow to fork within the same organisation (for whatever reason), so this has to be wired up manually.

1. Set spec as upstream repository:

   1. Run:
      ```
      git clone https://github.com/WebAssembly/<<proposal>>.git
      cd <<proposal>>
      git remote add upstream https://github.com/WebAssembly/spec.git
      git fetch upstream
      git merge upstream/master
      ```

2. If your proposal has dependencies on another active proposal, whose repository is named `<<parent-proposal>>`, then add that as an additional remote repository:

   1. Run:
      ```
      git remote add <<parent-proposal>> https://github.com/WebAssembly/<<parent-proposal>>.git
      git fetch <<parent-proposal>>
      git merge <<parent-proposal>>/master
      ```

Note: If you connect to github using SSH, and run into authentication failures, use the [SSH url](https://docs.github.com/en/github/getting-started-with-github/about-remote-repositories#about-remote-repositories) for the repository instead of the HTTPS url above.

3. Create Overview:

   1. Run
      ```
      mkdir proposals/<<proposal>>
      touch proposals/<<proposal>>/Overview.md
      git add proposals/<<proposal>>/Overview.md
      ```

   2. Edit `proposals/<<proposal>>/Overview.md`, e.g., with contents as follows:
      ```
      # Multiple Bulklets Proposal

      ## Summary

      This proposal extends Wasm with the ability to define multiple bulklets within a module.

      ## Motivation

      * Bulklets are very cool.

      * They are even better when they come in multiples.

      ## Overview

      Here is a sketch of what we wanna add.
      ```

4. Adjust toplevel readme:

   1. Edit `README.md`, replacing the first line with the following:
      ```
      [![Build Status](https://travis-ci.org/WebAssembly/<<proposal>>.svg?branch=master)](https://travis-ci.org/WebAssembly/<<proposal>>)

      # <<Title>> Proposal for WebAssembly

      This repository is a clone of [github.com/WebAssembly/spec/](https://github.com/WebAssembly/spec/).
      It is meant for discussion, prototype specification and implementation of a proposal to
      add support for <<Feature Description>> to WebAssembly.

      * See the [overview](proposals/<<proposal>>/Overview.md) for a summary of the proposal.

      * See the [modified spec](https://webassembly.github.io/<<proposal>>/) for details.

      Original `README` from upstream repository follows…
      ```
      where `<<Title>>` is the title picked for the repository and `<<Feature Description>>` a healf-sentence summary

5. Adjust spec doc front matters:

   1. Edit `document/core/index.rst`, changing the Release line to say:
      ```
         | Release |release| + <<proposal>> (Draft, |today|)
      ```

   2. If your proposal has another proposal as a dependency, then the Release line should include that as well:
      ```
         | Release |release| + <<parent-proposal>> + <<proposal>> (Draft, |today|)
      ```

6. Adjust links in spec:

   1. Edit `document/core/util/macros.def`

      * in the paths defining `WasmDraft` and `WasmIssues`, replace `.../spec/…` with `…/<<proposal>>/…` (4 places)

7. Commit (`README.md`, `proposals/<<proposal>>/Overview.md`, `document/core/index.rst`, `document/core/util/macros.def`):

   1. Run:
      ```
      git commit -am "Inital setup and overview"
      git push
      ```


## Update Proposals List

Add the proposal to the list of active proposals by creating a respective PR.

1. Go to https://github.com/WebAssembly/proposals

2. Edit `README.md` in UI:

   1. Add line for the proposal in table for Phase 0

   2. Create a PR


## Setting up Travis and GitHub Page

This step makes sure that every commit runs through Travis continuous integration tests. The spec CI scripts also automatically rebuild the spec document and publish it on the repo’s github.io page.

Note: Our Travis setup loosely follows the recipe decribed at https://gist.github.com/domenic/ec8b0fc8ab45f39403dd#get-encrypted-credentials

1. Generate new deploy key:

   1. Run:
      ```
      ssh-keygen -t rsa -b 4096 -C ""
      ```

   2. Save to: `deploy_key`

   3. Enter empty pass phrase (twice)

   This generates files `deploy_key` and `deploy_key.pub`

2. Add deploy key to repository:

   1. Go to `https://github.com/WebAssembly/<<proposal>>/settings/keys`

   2. Click "Add deploy key"

   3. Enter “Title": `Travis CI`

   4. Enter “Key": `<<contents of deploy_key.pub>>`

   5. Check "Allow write access"

   6. Click "Add key"

3. Install the [Travis Command Line Client](https://github.com/travis-ci/travis.rb#installation), if you do not have it already

4. If you are using 2FA on GitHub and (like me) can’t figure out how to use something like YubiKey with the Travis command line client, you may need to generate a GitHub token to perform the Travis login in the next step:

   1. Go to https://github.com/settings/tokens

   2. Click "Generate new token"

   3. Enter “Description”, e.g., `Setup token`

   4. Check the authorisation boxes specified at `https://docs.travis-ci.com/user/github-oauth-scopes/#travis-ci-for-open-source-projects`

      1. The following seem to suffice:

         * `repo/*`
         * `admin:org/read:org`
         * `user/user:email`

   5. Take note of the generated token string

5. Log into Travis from command line:

   1. If you don’t have GitHub 2FA activated or know how it works, run:
      ```
      travis login --org
      ```

   2. Otherwise, if you have created a GitHub token `<<gh-token>>` in the previous step, run:
      ```
      travis login --org --github-token <<gh-token>>
      ```

   3. If this is the first time you log into Travis from the command line, you may have to accept the request through the Travis web site:

      1. Go to `https://travis-ci.org/account/preferences`

      2. Log in with your GitHub account, if necessary

      3. Accept the request

      4. Repeat the travis command line login

6. Encrypt deploy key:

   1. Run:
      ```
      travis encrypt-file deploy_key
      ```
      
      Note: There is a bug in travis version 1.8.11 where this command will fail with the error:
      ```
      wrong number of arguments (given 1, expected 2)
      ```
      See `https://github.com/travis-ci/travis.rb/issues/711`. Version 1.10.0 seems to work fine.

   2. Confirm override with `yes`

   3. The output includes a line like
      ```
      openssl aes-256-cbc -K $encrypted_<<label>>_key -iv $encrypted_<<label>>_iv -in deploy_key.enc -out deploy_key -d
      ```
      where `<<label>>` is some hex value

7. Add encryption label to Travis configuration:

   1. Edit `.travis.yml`

   2. Change definition of `env/global/ENCRYPTION_LABEL` to `<<label>>`:
   ```
   env:
     global:
       - ENCRYPTION_LABEL: "<<label>>"
   ```

8. Commit (`deploy_key.enc`, `.travis.yml`):

   1. Run:
      ```
      git commit -am "Set up Travis"
      git push
      ```

9. Turn on builds for the new repository

   1. Go to `https://travis-ci.org/organizations/WebAssembly/repositories`

   2. Select "Current" tab

   3. Click "Activate repository"

10. Watch build progress at `https://travis-ci.org/WebAssembly/<<proposal>>/builds`

   1. You may have to retrigger the build:

      1. Click on "More options" pull down
      2. Select "Trigger build"
      3. Click “Trigger custom build” (you can leave the text boxes empty)

11. Point repository to GitHub IO

   1. Go to `https://github.com/WebAssembly/<<proposal>>`

   2. Click the settings icon next to “About” on the right of the page

   3. Enter “Website": `https://webassembly.github.io/<<proposal>>/`

   4. Click "Save"


## Syncing with Upstream Changes

Once in a while you will need to merge in changes from the main spec repo.
(Merging changes from possible parent proposals works the same way, but with `upstream` replaced by `<<parent-proposal>>`.)

1. Merge upstream:

   1. Make sure you are on the `master` branch

   2. Run:
      ```
      git fetch upstream
      git merge upstream/master
      ```

   3. Resolve merge conflicts if necessary

   4. Run:
      ```
      git push
      ```
      
If the merge conflicts are complex, you may want to have it reviewed. In that case:

1. Merge upstream with code review:

   1. Make sure you are on the `master` branch

   2. Pick a new `<<branch-name>>` for performing the merge and run:
      ```
      git checkout -b <<branch-name>>
      git fetch upstream
      git merge upstream/master
      ```
      
   3. Resolve merge conflicts
   
   4. Run:
      ```
      git commit -m "Merge from upstream spec"
      git push
      ```

   5. Create a nicer diff:

      The GitHub UI will display this as a list of all the changes added from the spec to this repo, which is not very easy to review. Instead, you can create a diff between this repo and the spec [merge base](https://git-scm.com/docs/git-merge-base).
   
      1. Run:
         ```
         git diff upstream/master..origin/<<branch-name>> > <<branch-name>>.diff
         ```
      
      2. Go to gist.github.com
   
      3. Paste the contents of `<<branch-name>>.diff` into the edit box
   
      4. Name the file `<<branch-name>>.diff`.
         This will make the diff have proper syntax highlighting.
   
      5. Click "Create public gist"
   
      6. Copy the URL
   
   6. Create a new pull request

      1. Go to `https://github.com/WebAssembly/<<proposal>>/compare`
   
      2. Click the right branch button and choose `<<branch-name>>`
   
      3. Click "Create pull request"
   
      4. Fill out the details, and make sure to include the URL of your gist

   7. Once approved, commit

      1. Do **not** use GitHub's "Squash and merge" option for committing upstream changes!
         That will ruin the history and reiterate all merge conflicts the next time.

      2. Instead, select "Merge pull request" (or "Create a merge commit") in GitHub!

         ![Select "Create a merge commit" from the dropdown](/create-merge-commit.png)

      3. Alternatively, you can push manually:
         ```
         git checkout master
         git merge --ff-only <<branch-name>>
         git push
         ```
         This assumes that `master` has not changed in the mean time.
         If it has, you will have to merge `master` into `<<branch-name>>` first.


## Progressing a Proposal Stages

Progress needs to be voted on by the Wasm [CG meeting](https://WebAssembly/meetings).
When the CG agrees to advance a proposal, update its status by creating a respective PR modifying `README.md` on the https://github.com/WebAssembly/proposals repo.


## Merging a Proposal into the Spec

Once a proposal has progressed to Stage 5, it is ready to be merged into the main spec.
Before doing so:

1. Make sure that all possible parent proposals have been merged.

2. Sync with upstream changes, as described above.

3. Undo the changes to `README.md`, `document/core/index.rst`, and `document/core/util/macros.def` that have been made when populating the repo.

4. Make sure that Travis is green.

5. Make sure that the changes to the document are rendered correctly.
