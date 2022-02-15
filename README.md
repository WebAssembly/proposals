# [WebAssembly][webassembly_specification] proposals

- [Finished Proposals](finished-proposals.md)
- [Inactive Proposals](inactive-proposals.md)

## Active proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/main/process/phases.md).

### Phase 5 - The Feature is Standardized (WG)

_These proposals have not yet been merged to the spec. Merged proposals are listed in [Finished Proposals](finished-proposals.md)._

| Proposal                                                                       | Champion         |
| ------------------------------------------------------------------------------ | ---------------- |

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                                       | Champion         |
| ------------------------------------------------------------------------------ | ---------------- |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                                                                             | Champion                               |
| ---------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Tail call][tail_call]                                                                               | Andreas Rossberg                       |
| [Multiple memories][multi-memory]                                                                    | Andreas Rossberg                       |
| [Custom Annotation Syntax in the Text Format][custom_annotation_syntax_in_the_text_format]           | Andreas Rossberg                       |
| [Memory64][memory64]                                                                                 | Wouter van Oortmerssen                 |
| [Exception handling][exception_handling]                                                             | Heejin Ahn                             |
| [Web Content Security Policy][web_content_security_policy]                                           | Francis McCabe                         |
| [Branch Hinting][branch-hinting]                                                                     | Yuri Iozzelli                          |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                                                             | Champion                               |
| ---------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Threads][threads]                                                                                   | Conrad Watt                            |
| [ECMAScript module integration][ecmascript_module_integration]                                       | Lin Clark & Daniel Ehrenberg           |
| [Type Reflection for WebAssembly JavaScript API][type_reflection_for_webassembly_javascript_api]     | Till Schneidereit                      |
| [Typed Function References][function_references]                                                     | Andreas Rossberg                       |
| [Relaxed dead code validation][relaxed-dead-code-validation]                                         | Conrad Watt and Ross Tate              |
| [Numeric Values in WAT Data Segments][numeric-values-in-wat]                                         | Ezzat Chamudi                          |
| [Instrument and Tracing Technology][instrument-tracing]                                              | Richard Winterton                      |
| [Relaxed SIMD][relaxed-simd]                                                                         | Marat Dukhan & Zhi An Ng               |
| [Garbage collection][garbage_collection]                                                             | Andreas Rossberg                       |

### Phase 1 - Feature Proposal (CG)

| Proposal                                                   | Champion                                                                          |
|------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Type Imports][type-imports]                               | Andreas Rossberg                                                                  |
| [Interface Types][interface_types]                         | Luke Wagner and Francis McCabe                                                    |
| [WebAssembly C and C++ API][wasm_c_api]                    | Andreas Rossberg                                                                  |
| [Feature Detection][feature_detection]                     | Thomas Lively                                                                     |
| [Extended Name Section][extended-name-section]             | Andrew Scheidecker                                                                |
| [Flexible Vectors][flexible-vectors]                       | Petr Penzin                                                                       |
| [Call Tags][call-tags]                                     | Ross Tate                                                                         |
| [Module Linking][module_linking]                           | Luke Wagner and Andreas Rossberg                                                  |
| [Extended Constant Expressions][extended-const]            | Sam Clegg                                                                         |
| [Stack Switching][stack-switching]                         | Francis McCabe & Sam Lindley                                                      |
| [Constant Time][constant-time]                             | Sunjay Cauligi, Garrett Gu, John Renner, Hovav Shacham, Deian Stefan, Conrad Watt |
| [JS Promise Integration][js-promise-integration]           | Ross Tate and Francis McCabe                                                      |

### Phase 0 - Pre-Proposal (CG)

| Proposal                                                   | Champion                         |
| ---------------------------------------------------------- | -------------------------------- |
| [Funclets: Flexible Intraprocedural Control Flow][funclets]| Dan Gohman                       |

## Implementation status

Roadmap is available on https://webassembly.org/roadmap/

## Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/main/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[custom_annotation_syntax_in_the_text_format]: https://github.com/WebAssembly/annotations
[ecmascript_module_integration]: https://github.com/WebAssembly/esm-integration
[exception_handling]: https://github.com/WebAssembly/exception-handling
[feature_detection]: https://github.com/WebAssembly/feature-detection
[function_references]: https://github.com/WebAssembly/function-references
[type-imports]: https://github.com/WebAssembly/proposal-type-imports
[garbage_collection]: https://github.com/WebAssembly/gc
[interface_types]: https://github.com/WebAssembly/interface-types
[multi-memory]: https://github.com/WebAssembly/multi-memory
[tail_call]: https://github.com/WebAssembly/tail-call
[threads]: https://github.com/webassembly/threads
[type_reflection_for_webassembly_javascript_api]: https://github.com/WebAssembly/js-types
[wasm_c_api]: https://github.com/WebAssembly/wasm-c-api
[web_content_security_policy]: https://github.com/WebAssembly/content-security-policy
[webassembly_specification]: https://github.com/WebAssembly/spec
[funclets]: https://github.com/WebAssembly/funclets
[extended-name-section]: https://github.com/WebAssembly/extended-name-section
[module_linking]: https://github.com/WebAssembly/module-linking
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
