# [WebAssembly][webassembly_specification] proposals

- [Finished Proposals](finished-proposals.md)
- [Inactive Proposals](inactive-proposals.md)

## Active proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/master/process/phases.md).

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                                       | Champion   |
| ------------------------------------------------------------------------------ | ---------- |
| [Non-trapping float-to-int conversions][non-trapping_float-to-int_conversions] | Dan Gohman |
| [Sign-extension operators][sign-extension_operators]                           | Ben Smith  |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                         | Champion         |
| ------------------------------------------------ | ---------------- |
| [Multi-value][multi-value]                       | Andreas Rossberg |
| [Reference Types][reference_types]               | Andreas Rossberg |
| [Tail call][tail_call]                           | Andreas Rossberg |
| [Bulk memory operations][bulk_memory_operations] | Ben Smith        |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                                                             | Champion                       |
| ---------------------------------------------------------------------------------------------------- | ------------------------------ |
| [JavaScript BigInt to WebAssembly i64 integration][javascript_bigint_to_webassembly_i64_integration] | Dan Ehrenberg                  |
| [Threads][threads]                                                                                   | Ben Smith                      |
| [ECMAScript module integration][ecmascript_module_integration]                                       | Lin Clark & Daniel Ehrenberg   |
| [Fixed-width SIMD][fixed-width_simd]                                                                 | Peter Jensen and Arun Purushan |

### Phase 1 - Feature Proposal (CG)

| Proposal                                                                                         | Champion                         |
| ------------------------------------------------------------------------------------------------ | -------------------------------- |
| [Custom Annotation Syntax in the Text Format][custom_annotation_syntax_in_the_text_format]       | Andreas Rossberg                 |
| [Exception handling][exception_handling]                                                         | Heejin Ahn                       |
| [Type Imports][type-imports]                                                                     | Andreas Rossberg         |
| [Garbage collection][garbage_collection]                                                         | Andreas Rossberg                 |
| [Web IDL Bindings][webidl_bindings]                                                              | Luke Wagner                      |
| [Type Reflection for WebAssembly JavaScript API][type_reflection_for_webassembly_javascript_api] | Till Schneidereit                |
| [WebAssembly C and C++ API][wasm_c_api]                                                          | Andreas Rossberg                 |
| [Typed Function References][function_references]                                                 | Andreas Rossberg                 |
| [Feature Detection][feature_detection]                                                           | Thomas Lively                    |
| [Extended Name Section][extended-name-section]                                                   | Andrew Scheidecker               |

### Phase 0 - Pre-Proposal (CG)

| Proposal                                                   | Champion         |
| ---------------------------------------------------------- | ---------------- |
| [Web Content Security Policy][web_content_security_policy] | Ben Titzer       |
| [Funclets: Flexible Intraprocedural Control Flow][funclets]| Dan Gohman       |

### Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/master/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[bulk_memory_operations]: https://github.com/webassembly/bulk-memory-operations
[custom_annotation_syntax_in_the_text_format]: https://github.com/WebAssembly/annotations/blob/master/proposals/annotations/Overview.md
[ecmascript_module_integration]: https://github.com/webassembly/esm-integration
[exception_handling]: https://github.com/WebAssembly/exception-handling/blob/master/proposals/Exceptions.md
[fixed-width_simd]: https://github.com/webassembly/simd/blob/master/proposals/simd/SIMD.md
[function_references]: https://github.com/WebAssembly/function-references
[type-imports]: https://github.com/WebAssembly/proposal-type-imports
[garbage_collection]: https://github.com/webassembly/gc/blob/master/proposals/gc/Overview.md
[webidl_bindings]: https://github.com/WebAssembly/webidl-bindings/blob/master/proposals/webidl-bindings/Explainer.md
[javascript_bigint_to_webassembly_i64_integration]: https://github.com/WebAssembly/JS-BigInt-integration
[non-trapping_float-to-int_conversions]: https://github.com/WebAssembly/nontrapping-float-to-int-conversions
[multi-value]: https://github.com/WebAssembly/multi-value
[reference_types]: https://github.com/WebAssembly/reference-types
[sign-extension_operators]: https://github.com/WebAssembly/sign-extension-ops/blob/master/proposals/sign-extension-ops/Overview.md
[tail_call]: https://github.com/webassembly/tail-call
[threads]: https://github.com/webassembly/threads/blob/master/proposals/threads/Overview.md
[type_reflection_for_webassembly_javascript_api]: https://github.com/webassembly/js-types/blob/master/proposals/js-types/Overview.md
[wasm_c_api]: https://github.com/WebAssembly/wasm-c-api
[web_content_security_policy]: https://github.com/WebAssembly/content-security-policy/blob/master/proposals/CSP.md
[webassembly_specification]: https://github.com/WebAssembly/spec
[funclets]: https://github.com/WebAssembly/funclets
[feature_detection]: https://github.com/WebAssembly/feature-detection
[extended-name-section]: https://github.com/WebAssembly/extended-name-section/blob/master/proposals/extended-name-section/Overview.md
