# [WebAssembly](https://github.com/WebAssembly/spec) proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/master/process/phases.md).

## Standardized proposals

| Proposal                                                             | Champion  |
| -------------------------------------------------------------------- | --------- |
| [Import/Export of Mutable Globals][import_export_of_mutable_globals] | Ben Smith |

## Active proposals

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                                       | Champion   |
| ------------------------------------------------------------------------------ | ---------- |
| [Non-trapping float-to-int conversions][non-trapping_float-to-int_conversions] | Dan Gohman |
| [Sign-extension operators][sign-extension_operators]                           | Ben Smith  |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                           | Champion         |
| ---------------------------------- | ---------------- |
| [Multi-value][multi-value]         | Andreas Rossberg |
| [Reference Types][reference_types] | Andreas Rossberg |
| [Tail call][tail_call]             | Andreas Rossberg |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                                                             | Champion         |
| ---------------------------------------------------------------------------------------------------- | ---------------- |
| [JavaScript BigInt to WebAssembly i64 integration][javascript_bigint_to_webassembly_i64_integration] | Dan Ehrenberg    |
| [WebAssembly specification][webassembly_specification]                                               | Andreas Rossberg |
| [Bulk memory operations][bulk_memory_operations]                                                     | Ben Smith        |
| [Threads][threads]                                                                                   | Ben Smith        |

### Phase 1 - Feature Proposal (CG)

| Proposal                                                                                         | Champion                    |
| ------------------------------------------------------------------------------------------------ | --------------------------- |
| [Custom Annotation Syntax in the Text Format][custom_annotation_syntax_in_the_text_format]       | Andreas Rossberg            |
| [ECMAScript module integration][ecmascript_module_integration]                                   | Lin Clark                   |
| [Exception handling][exception_handling]                                                         | Heejin Ahn                  |
| [Fixed-width SIMD][fixed-width_simd]                                                             | Peter Jensen and Arun Purushan   |
| [Garbage collection][garbage_collection]                                                         | Andreas Rossberg            |
| [Host bindings][host_bindings]                                                                   | Luke Wagner                 |
| [Type Reflection for WebAssembly JavaScript API][type_reflection_for_webassembly_javascript_api] | Till Schneidereit           |
| [WebAssembly C and C++ API][wasm_c_api]                                                          | Andreas Rossberg            |

### Phase 0 - Pre-Proposal (CG)

| Proposal                                                   | Champion         |
| ---------------------------------------------------------- | ---------------- |
| [Unmanaged closures][unmanaged_closures]                   | Mark Miller      |
| [Web Content Security Policy][web_content_security_policy] |                  |
| [Funclets: Flexible Intraprocedural Control Flow][funclets]| Dan Gohman       |

### Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/master/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[bulk_memory_operations]: https://github.com/webassembly/bulk-memory-operations
[custom_annotation_syntax_in_the_text_format]: https://github.com/WebAssembly/annotations/blob/master/proposals/annotations/Overview.md
[ecmascript_module_integration]: https://github.com/webassembly/esm-integration
[exception_handling]: https://github.com/webassembly/exception-handling/blob/master/proposals/Level-1.md
[fixed-width_simd]: https://github.com/webassembly/simd/blob/master/proposals/simd/SIMD.md
[garbage_collection]: https://github.com/webassembly/gc/blob/master/proposals/gc/Overview.md
[host_bindings]: https://github.com/webassembly/host-bindings
[import_export_of_mutable_globals]: https://github.com/WebAssembly/mutable-global
[javascript_bigint_to_webassembly_i64_integration]: https://github.com/WebAssembly/JS-BigInt-integration
[non-trapping_float-to-int_conversions]: https://github.com/WebAssembly/nontrapping-float-to-int-conversions
[multi-value]: https://github.com/WebAssembly/multi-value
[reference_types]: https://github.com/WebAssembly/reference-types
[sign-extension_operators]: https://github.com/WebAssembly/sign-extension-ops/blob/master/proposals/sign-extension-ops/Overview.md
[tail_call]: https://github.com/webassembly/tail-call
[threads]: https://github.com/webassembly/threads/blob/master/proposals/threads/Overview.md
[type_reflection_for_webassembly_javascript_api]: https://github.com/webassembly/js-types/blob/master/proposals/js-types/Overview.md
[unmanaged_closures]: https://github.com/WebAssembly/design/issues/1182
[wasm_c_api]: https://github.com/rossberg/wasm-c-api
[web_content_security_policy]: https://github.com/WebAssembly/content-security-policy/blob/master/proposals/CSP.md
[webassembly_specification]: https://github.com/WebAssembly/spec
[funclets]: https://github.com/WebAssembly/funclets
