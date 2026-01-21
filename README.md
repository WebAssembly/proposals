# [WebAssembly][webassembly_specification] proposals

- [Finished Proposals](finished-proposals.md)
- [Inactive Proposals](inactive-proposals.md)

## Active proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/main/process/phases.md).

### Phase 5 - The Feature is Standardized (WG)

_These proposals have not yet been merged to the spec. Merged proposals are listed in [Finished Proposals](finished-proposals.md)._

| Proposal                                                   | Champion                 |
| -----------------------------------------------------------| ------------------------ |

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                   | Champion                 |
| -----------------------------------------------------------| -------------------------|
| [Threads][threads]                                         | Conrad Watt              |
| [JS Promise Integration][js-promise-integration]           | Francis McCabe           |
| [Web Content Security Policy][content-security-policy]     | Francis McCabe           |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                                   | Champion                             |
| -----------------------------------------------------------| ------------------------------------ |
| [Type Reflection for WebAssembly JavaScript API][js-types] | Ilya Rezvov                          |
| [ESM Integration][ecmascript_module_integration]           | Asumu Takikawa, Ms2ger & Guy Bedford |
| [Wide Arithmetic][wide-arithmetic]                         | Alex Crichton and Jamey Sharp        |
| [Stack Switching][stack-switching]                         | Francis McCabe & Sam Lindley         |
| [Compact Import Section][compact-import-section]               | Ryan Hunt                    |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                       | Champion                     |
| ---------------------------------------------------------------| -----------------------------|
| [Relaxed dead code validation][relaxed-dead-code-validation]   | Conrad Watt and Ross Tate    |
| [Numeric Values in WAT Data Segments][numeric-values-in-wat]   | Ezzat Chamudi                |
| [Extended Name Section][extended-name-section]                 | Ben Visness                  |
| [Custom Page Sizes][custom-page-sizes]                         | Nick Fitzgerald              |
| [Rounding Variants][rounding-mode-control]                     | Kloud Koder                  |
| [Compilation Hints][compilation-hints]                         | Emanuel Ziegler              |
| [Custom Descriptors and JS Interop][custom-descs]              | Thomas Lively                |
| [JS Primitive Builtins][js-primitive-builtins]                 | Sébastien Doeraene           |

### Phase 1 - Feature Proposal (CG)

| Proposal                                               | Champion                                                                          |
| ------------------------------------------------------ | --------------------------------------------------------------------------------- |
| [Type Imports][type-imports]                           | Andreas Rossberg                                                                  |
| [Component Model][component-model]                     | Luke Wagner                                                                       |
| [WebAssembly C and C++ API][wasm_c_api]                | Andreas Rossberg                                                                  |
| [Flexible Vectors][flexible-vectors]                   | Petr Penzin & Tal Garfinkel                                                       |
| [Memory control][memory-control]                       | Deepti Gandluri & Ben Visness                                                     |
| [Reference-Typed Strings][stringref]                   | Andy Wingo                                                                        |
| [Profiles][profiles]                                   | Andreas Rossberg                                                                  |
| [Shared-Everything Threads][shared-everything-threads] | Andrew Brown, Conrad Watt, and Thomas Lively                                      |
| [Frozen Values][frozen-values]                         | Léo Andrès and Pierre Chambart                                                    |
| [Half Precision][half-precision]                       | Ilya Rezvov                                                                       |
| [More Array Constructors][more-array-constructors]     | Nick Fitzgerald                                                                   |
| [JIT Interface][jit-interface]                         | Ben Titzer                                                                        |
| [Multibyte Array Access][multibyte-array-access]       | Brendan Dahl                                                                      |

### Phase 0 - Pre-Proposal (CG)

Phase 0 proposals are tracked in the [design repository issue tracker].

[design repository issue tracker]: https://github.com/WebAssembly/design/issues

## Implementation status

Implementation status of most proposals in various wasm engines is available on https://webassembly.org/features/

## Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/main/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[ecmascript_module_integration]: https://github.com/WebAssembly/esm-integration
[feature_detection]: https://github.com/WebAssembly/feature-detection
[type-imports]: https://github.com/WebAssembly/proposal-type-imports
[component-model]: https://github.com/WebAssembly/component-model
[threads]: https://github.com/webassembly/threads
[js-primitive-builtins]: https://github.com/WebAssembly/js-primitive-builtins
[js-types]: https://github.com/WebAssembly/js-types
[wasm_c_api]: https://github.com/WebAssembly/wasm-c-api
[content-security-policy]: https://github.com/WebAssembly/content-security-policy
[webassembly_specification]: https://github.com/WebAssembly/spec
[extended-name-section]: https://github.com/WebAssembly/extended-name-section
[flexible-vectors]: https://github.com/WebAssembly/flexible-vectors
[numeric-values-in-wat]: https://github.com/WebAssembly/wat-numeric-values
[relaxed-dead-code-validation]: https://github.com/WebAssembly/relaxed-dead-code-validation
[stack-switching]: https://github.com/WebAssembly/stack-switching
[js-promise-integration]: https://github.com/WebAssembly/js-promise-integration
[memory-control]: https://github.com/WebAssembly/memory-control
[stringref]: https://github.com/WebAssembly/stringref
[profiles]: https://github.com/WebAssembly/profiles
[rounding-mode-control]: https://github.com/WebAssembly/rounding-mode-control
[shared-everything-threads]: https://github.com/WebAssembly/shared-everything-threads
[frozen-values]: https://github.com/WebAssembly/frozen-values
[compilation-hints]: https://github.com/WebAssembly/compilation-hints
[custom-page-sizes]: https://github.com/WebAssembly/custom-page-sizes
[custom-descs]: https://github.com/WebAssembly/custom-descriptors
[half-precision]: https://github.com/WebAssembly/half-precision
[compact-import-section]: https://github.com/WebAssembly/compact-import-section
[wide-arithmetic]: https://github.com/WebAssembly/wide-arithmetic
[more-array-constructors]: https://github.com/WebAssembly/more-array-constructors/
[jit-interface]: https://github.com/WebAssembly/jit-interface
[multibyte-array-access]: https://github.com/WebAssembly/multibyte-array-access
