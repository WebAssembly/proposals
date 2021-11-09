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

   3. Click "Add people" and enter the champion’s GitHub user name

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
      git merge upstream/main
      ```

2. If your proposal has dependencies on another active proposal, whose repository is named `<<parent-proposal>>`, then add that as an additional remote repository:

   1. Run:
      ```
      git remote add <<parent-proposal>> https://github.com/WebAssembly/<<parent-proposal>>.git
      git fetch <<parent-proposal>>
      git merge <<parent-proposal>>/main
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
      ![Build Status](https://github.com/WebAssembly/<<proposal>>/actions/workflows/main.yml/badge.svg)

      # <<Title>> Proposal for WebAssembly

      This repository is a clone of [github.com/WebAssembly/spec/](https://github.com/WebAssembly/spec/).
      It is meant for discussion, prototype specification and implementation of a proposal to
      add support for <<Feature Description>> to WebAssembly.

      * See the [overview](proposals/<<proposal>>/Overview.md) for a summary of the proposal.

      * See the [modified spec](https://webassembly.github.io/<<proposal>>/) for details.

      Original `README` from upstream repository follows...
      ```
      where `<<Title>>` is the title picked for the repository and `<<Feature Description>>` a healf-sentence summary

5. Adjust document configuration:

   1. Edit `document/core/conf.py`, changing the line defining `proposal` to say:
      ```
      proposal = '<<proposal>>'
      ```

   2. If your proposal has another proposal as a dependency, then it should be included as well:
      ```
      proposal = '<<parent-proposal>> + <<proposal>>'
      ```

   3. Change the line defining `repo` to say:
      ```
      repo = '<<proposal>>'
      ```

6. Commit (`README.md`, `proposals/<<proposal>>/Overview.md`, `document/core/conf.py`):

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


## Setting up CI and GitHub Pages

This step makes sure that every commit runs through continuous integration tests. The spec CI scripts also automatically rebuild the spec document and publish it on the repo’s github.io page.

CI is currently done with Github Actions ([documentation](https://docs.github.com/en/actions)). When you merge from the upstream spec directory, git should also pull in yml files in `.github/workflows` that specify the CI behavior. These files should automatically set up CI actions that run on both commit and on pull requests.

While the CI action will automatically build the spec document and push it to the `gh-pages` branch, you may also need to configure the repository to publish this branch to the web:

 1. Click "Settings”.

 2. Go to the "Pages" settings.

 3. Under "Source", click the drop-down button and choose the `gh-pages` branch.

 4. Click "Save".

This should publish the document to `https://webassembly.github.io/<<proposal>>`.

On some pull requests, there may be an additional approval needed from a user with write-access to run the CI actions. See the [documentation page](https://docs.github.com/en/actions/managing-workflow-runs/approving-workflow-runs-from-public-forks) on this for details.

## Syncing with Upstream Changes

Once in a while you will need to merge in changes from the main spec repo.
(Merging changes from possible parent proposals works the same way, but with `upstream` replaced by `<<parent-proposal>>`.)

1. Merge upstream:

   1. Make sure you are on the `main` branch

   2. Run:
      ```
      git fetch upstream
      git merge upstream/main
      ```

   3. Resolve merge conflicts if necessary

   4. Run:
      ```
      git push
      ```
      
If the merge conflicts are complex, you may want to have it reviewed. In that case:

1. Merge upstream with code review:

   1. Make sure you are on the `main` branch

   2. Pick a new `<<branch-name>>` for performing the merge and run:
      ```
      git checkout -b <<branch-name>>
      git fetch upstream
      git merge upstream/main
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
         git diff upstream/main..origin/<<branch-name>> > <<branch-name>>.diff
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
         git checkout main
         git merge --ff-only <<branch-name>>
         git push
         ```
         This assumes that `main` has not changed in the mean time.
         If it has, you will have to merge `main` into `<<branch-name>>` first.


## Progressing a Proposal Stages

Progress needs to be voted on by the Wasm [CG meeting](https://WebAssembly/meetings).
When the CG agrees to advance a proposal, update its status by creating a respective PR modifying `README.md` on the https://github.com/WebAssembly/proposals repo.


## Merging a Proposal into the Spec

Once a proposal has progressed to Stage 5, it is ready to be merged into the main spec.
Before doing so:

1. Make sure that all possible parent proposals have been merged.

2. Sync with upstream changes, as described above.

3. Undo the changes to `README.md` and `document/core/conf.py` that have been made when populating the repo.

4. Make sure that Travis is green.

5. Make sure that the changes to the document are rendered correctly.

After merging, archive the proposal repository:

1. Go to "Settings" -> "Options"

2. Click "Archive repository" and follow instructions.

Finally, update the proposals list:

Add the proposal to the list of active proposals by creating a respective PR.

1. Go to https://github.com/WebAssembly/proposals

2. Edit `README.md` and `finished-proposals.md`:

   1. Move the proposal from the former to the latter.

   2. Create a PR
