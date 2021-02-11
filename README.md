# [WebAssembly][webassembly_specification] proposals

- [Finished Proposals](finished-proposals.md)
- [Inactive Proposals](inactive-proposals.md)

## Active proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/master/process/phases.md).

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                                       | Champion         |
| ------------------------------------------------------------------------------ | ---------------- |
| [Reference Types][reference_types]                                             | Andreas Rossberg |
| [Bulk memory operations][bulk_memory_operations]                               | Ben Smith        |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                                                                             | Champion                               |
| ---------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Tail call][tail_call]                                                                               | Andreas Rossberg                       |
| [Fixed-width SIMD][fixed-width_simd]                                                                 | Deepti Gandluri and Arun Purushan      |
| [Multiple memories][multi-memory]                                                                    | Andreas Rossberg                       |
| [Custom Annotation Syntax in the Text Format][custom_annotation_syntax_in_the_text_format]           | Andreas Rossberg                       |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                                                             | Champion                               |
| ---------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Threads][threads]                                                                                   | Ben Smith                              |
| [ECMAScript module integration][ecmascript_module_integration]                                       | Lin Clark & Daniel Ehrenberg           |
| [Exception handling][exception_handling]                                                             | Heejin Ahn                             |
| [Type Reflection for WebAssembly JavaScript API][type_reflection_for_webassembly_javascript_api]     | Till Schneidereit                      |
| [Typed Function References][function_references]                                                     | Andreas Rossberg                       |
| [Memory64][memory64]                                                                                 | Wouter van Oortmerssen                 |
| [Relaxed dead code validation][relaxed-dead-code-validation]                                         | Conrad Watt and Ross Tate              |
| [Numeric Values in WAT Data Segments][numeric-values-in-wat]                                         | Ezzat Chamudi                          |

### Phase 1 - Feature Proposal (CG)

| Proposal                                                                                         | Champion                         |
| ------------------------------------------------------------------------------------------------ | -------------------------------- |
| [Type Imports][type-imports]                                                                     | Andreas Rossberg                 |
| [Garbage collection][garbage_collection]                                                         | Andreas Rossberg                 |
| [Interface Types][interface_types]                                                               | Luke Wagner and Francis McCabe   |
| [WebAssembly C and C++ API][wasm_c_api]                                                          | Andreas Rossberg                 |
| [Feature Detection][feature_detection]                                                           | Thomas Lively                    |
| [Extended Name Section][extended-name-section]                                                   | Andrew Scheidecker               |
| [Flexible Vectors][flexible-vectors]                                                             | Petr Penzin                      |
| [Instrument and Tracing Technology][instrument-tracing]                                          | Richard Winterton                |
| [Call Tags][call-tags]                                                                           | Ross Tate                        |
| [Module Linking][module_linking]                                                                 | Luke Wagner and Andreas Rossberg |
| [Branch Hinting][branch-hinting]                                                                 | Yuri Iozzelli                    |
| [Extended Constant Expressions][extended-const]                                               | Sam Clegg                        |

### Phase 0 - Pre-Proposal (CG)

| Proposal                                                   | Champion                         |
| ---------------------------------------------------------- | -------------------------------- |
| [Web Content Security Policy][web_content_security_policy] | Francis McCabe                   |
| [Funclets: Flexible Intraprocedural Control Flow][funclets]| Dan Gohman                       |
| [Constant Time][constant-time]                             | John Renner, Hovav Shacham, Deian Stefan, Conrad Watt|


### Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/master/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[bulk_memory_operations]: https://github.com/WebAssembly/bulk-memory-operations
[custom_annotation_syntax_in_the_text_format]: https://github.com/WebAssembly/annotations
[ecmascript_module_integration]: https://github.com/WebAssembly/esm-integration
[exception_handling]: https://github.com/WebAssembly/exception-handling
[feature_detection]: https://github.com/WebAssembly/feature-detection
[fixed-width_simd]: https://github.com/webassembly/simd
[function_references]: https://github.com/WebAssembly/function-references
[type-imports]: https://github.com/WebAssembly/proposal-type-imports
[garbage_collection]: https://github.com/WebAssembly/gc
[interface_types]: https://github.com/WebAssembly/interface-types
[multi-memory]: https://github.com/WebAssembly/multi-memory
[reference_types]: https://github.com/WebAssembly/reference-types
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
