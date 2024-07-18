# [WebAssembly][webassembly_specification] proposals

- [Finished Proposals](finished-proposals.md)
- [Inactive Proposals](inactive-proposals.md)

## Active proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/main/process/phases.md).

### Phase 5 - The Feature is Standardized (WG)

_These proposals have not yet been merged to the spec. Merged proposals are listed in [Finished Proposals](finished-proposals.md)._

| Proposal                                                   | Champion                 |
| -----------------------------------------------------------| ------------------------ |
| [Tail call][tail_call]                                     | Andreas Rossberg         |
| [Extended Constant Expressions][extended-const]            | Sam Clegg                |
| [Typed Function References][function_references]           | Andreas Rossberg         |
| [Garbage collection][garbage_collection]                   | Andreas Rossberg         |
| [Multiple memories][multi-memory]                          | Andreas Rossberg         |
| [Relaxed SIMD][relaxed-simd]                               | Marat Dukhan & Zhi An Ng |
| [Custom Annotation Syntax in the Text Format][annotations] | Andreas Rossberg         |
| [Branch Hinting][branch-hinting]                           | Yuri Iozzelli            |

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                   | Champion                 |
| -----------------------------------------------------------| -------------------------|
| [Threads][threads]                                         | Conrad Watt              |
| [Exception handling][exception_handling]                   | Heejin Ahn & Ben Titzer  |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                                   | Champion                             |
| -----------------------------------------------------------| ------------------------------------ |
| [Memory64][memory64]                                       | Sam Clegg                            |
| [Web Content Security Policy][content-security-policy]     | Francis McCabe                       |
| [JS Promise Integration][js-promise-integration]           | Ross Tate and Francis McCabe         |
| [Type Reflection for WebAssembly JavaScript API][js-types] | Ilya Rezvov                          |
| [ESM Integration][ecmascript_module_integration]           | Asumu Takikawa, Ms2ger & Guy Bedford |
| [JS String Builtins][js-string-builtins]                   | Ryan Hunt                            |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                       | Champion                     |
| ---------------------------------------------------------------| -----------------------------|
| [Relaxed dead code validation][relaxed-dead-code-validation]   | Conrad Watt and Ross Tate    |
| [Numeric Values in WAT Data Segments][numeric-values-in-wat]   | Ezzat Chamudi                |
| [Instrument and Tracing Technology][instrument-tracing]        | Richard Winterton            |
| [Extended Name Section][extended-name-section]                 | Ashley Nelson                |

### Phase 1 - Feature Proposal (CG)

| Proposal                                               | Champion                                                                          |
| ------------------------------------------------------ | --------------------------------------------------------------------------------- |
| [Type Imports][type-imports]                           | Andreas Rossberg                                                                  |
| [Component Model][component-model]                     | Luke Wagner                                                                       |
| [WebAssembly C and C++ API][wasm_c_api]                | Andreas Rossberg                                                                  |
| [Flexible Vectors][flexible-vectors]                   | Petr Penzin & Tal Garfinkel                                                       |
| [Call Tags][call-tags]                                 | Ross Tate                                                                         |
| [Stack Switching][stack-switching]                     | Francis McCabe & Sam Lindley                                                      |
| [Constant Time][constant-time]                         | Sunjay Cauligi, Garrett Gu, John Renner, Hovav Shacham, Deian Stefan, Conrad Watt |
| [JS Customization for GC Objects][gc-js-customization] | Asumu Takikawa                                                                    |
| [Memory control][memory-control]                       | Deepti Gandluri & Ben Visness                                                     |
| [Reference-Typed Strings][stringref]                   | Andy Wingo                                                                        |
| [Profiles][profiles]                                   | Andreas Rossberg                                                                  |
| [Rounding Variants][rounding-mode-control]             | Kloud Koder                                                                       |
| [Shared-Everything Threads][shared-everything-threads] | Andrew Brown, Conrad Watt, and Thomas Lively                                      |
| [Frozen Values][frozen-values]                         | Léo Andrès and Pierre Chambart                                                    |
| [Compilation Hints][compilation-hints]                 | Emanuel Ziegler                                                                   |
| [Custom Page Sizes][custom-page-sizes]                 | Nick Fitzgerald                                                                   |
| [Half Precision][half-precision]                       | Ilya Rezvov                                                                       |
| [Compact Import Section][compact-import-section]       | Ryan Hunt                                                                         |

### Phase 0 - Pre-Proposal (CG)

| Proposal                                                    | Champion                         |
| ----------------------------------------------------------- | -------------------------------- |

## Implementation status

Implementation status of most proposals in various wasm engines is available on https://webassembly.org/features/

## Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/main/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[annotations]: https://github.com/WebAssembly/annotations
[ecmascript_module_integration]: https://github.com/WebAssembly/esm-integration
[exception_handling]: https://github.com/WebAssembly/exception-handling
[feature_detection]: https://github.com/WebAssembly/feature-detection
[function_references]: https://github.com/WebAssembly/function-references
[type-imports]: https://github.com/WebAssembly/proposal-type-imports
[garbage_collection]: https://github.com/WebAssembly/gc
[component-model]: https://github.com/WebAssembly/component-model
[multi-memory]: https://github.com/WebAssembly/multi-memory
[tail_call]: https://github.com/WebAssembly/tail-call
[threads]: https://github.com/webassembly/threads
[js-types]: https://github.com/WebAssembly/js-types
[wasm_c_api]: https://github.com/WebAssembly/wasm-c-api
[content-security-policy]: https://github.com/WebAssembly/content-security-policy
[webassembly_specification]: https://github.com/WebAssembly/spec
[extended-name-section]: https://github.com/WebAssembly/extended-name-section
[constant-time]: https://github.com/WebAssembly/constant-time
[memory64]: https://github.com/WebAssembly/memory64
[flexible-vectors]: https://github.com/WebAssembly/flexible-vectors
[numeric-values-in-wat]: https://github.com/WebAssembly/wat-numeric-values
[instrument-tracing]: https://github.com/WebAssembly/instrument-tracing
[call-tags]: https://github.com/WebAssembly/call-tags
[relaxed-dead-code-validation]: https://github.com/WebAssembly/relaxed-dead-code-validation
[branch-hinting]: https://github.com/WebAssembly/branch-hinting
[extended-const]: https://github.com/WebAssembly/extended-const
[relaxed-simd]: https://github.com/WebAssembly/relaxed-simd
[stack-switching]: https://github.com/WebAssembly/stack-switching
[js-promise-integration]: https://github.com/WebAssembly/js-promise-integration
[gc-js-customization]: https://github.com/WebAssembly/gc-js-customization
[memory-control]: https://github.com/WebAssembly/memory-control
[stringref]: https://github.com/WebAssembly/stringref
[profiles]: https://github.com/WebAssembly/profiles
[js-string-builtins]: https://github.com/WebAssembly/js-string-builtins
[rounding-mode-control]: https://github.com/WebAssembly/rounding-mode-control
[shared-everything-threads]: https://github.com/WebAssembly/shared-everything-threads
[frozen-values]: https://github.com/WebAssembly/frozen-values
[compilation-hints]: https://github.com/WebAssembly/compilation-hints
[custom-page-sizes]: https://github.com/WebAssembly/custom-page-sizes
[half-precision]: https://github.com/WebAssembly/half-precision
[compact-import-section]: https://github.com/WebAssembly/compact-import-section
