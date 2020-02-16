# [WebAssembly][webassembly_specification] proposals

- [Finished Proposals](finished-proposals.md)
- [Inactive Proposals](inactive-proposals.md)

## Active proposals

Proposals follow [this process document](https://github.com/WebAssembly/meetings/blob/master/process/phases.md).

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                                       | Champion         |
| ------------------------------------------------------------------------------ | ---------------- |
| [Non-trapping float-to-int conversions][non-trapping_float-to-int_conversions] | Dan Gohman       |
| [Sign-extension operators][sign-extension_operators]                           | Ben Smith        |
| [Multi-value][multi-value]                                                     | Andreas Rossberg |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                                                                             | Champion                               |
| ---------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Reference Types][reference_types]                                                                   | Andreas Rossberg                       |
| [Tail call][tail_call]                                                                               | Andreas Rossberg                       |
| [Bulk memory operations][bulk_memory_operations]                                                     | Ben Smith                              |
| [JavaScript BigInt to WebAssembly i64 integration][javascript_bigint_to_webassembly_i64_integration] | Dan Ehrenberg & Sven Sauleau           |
| [Fixed-width SIMD][fixed-width_simd]                                                                 | Deepti Gandluri and Arun Purushan      |
| [Multiple memories][multi-memory]                                                                    | Andreas Rossberg                       |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                                                             | Champion                               |
| ---------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Threads][threads]                                                                                   | Ben Smith                              |
| [ECMAScript module integration][ecmascript_module_integration]                                       | Lin Clark & Daniel Ehrenberg           |
| [Exception handling][exception_handling]                                                             | Heejin Ahn                             |
| [Custom Annotation Syntax in the Text Format][custom_annotation_syntax_in_the_text_format]           | Andreas Rossberg                       |
| [Type Reflection for WebAssembly JavaScript API][type_reflection_for_webassembly_javascript_api]     | Till Schneidereit                      |

### Phase 1 - Feature Proposal (CG)

| Proposal                                                                                         | Champion                         |
| ------------------------------------------------------------------------------------------------ | -------------------------------- |
| [Type Imports][type-imports]                                                                     | Andreas Rossberg                 |
| [Garbage collection][garbage_collection]                                                         | Andreas Rossberg                 |
| [Interface Types][interface_types]                                                               | Luke Wagner                      |
| [WebAssembly C and C++ API][wasm_c_api]                                                          | Andreas Rossberg                 |
| [Typed Function References][function_references]                                                 | Andreas Rossberg                 |
| [Conditional Sections][conditional_sections]                                                     | Thomas Lively                    |
| [Extended Name Section][extended-name-section]                                                   | Andrew Scheidecker               |

### Phase 0 - Pre-Proposal (CG)

| Proposal                                                   | Champion                         |
| ---------------------------------------------------------- | -------------------------------- |
| [Web Content Security Policy][web_content_security_policy] | Ben Titzer                       |
| [Funclets: Flexible Intraprocedural Control Flow][funclets]| Dan Gohman                       |
| [Module Types][module_types]                               | Luke Wagner and Andreas Rossberg |

### Contributing new proposals

Please see [Contributing to WebAssembly](https://github.com/WebAssembly/design/blob/master/Contributing.md) for the most up-to-date information on contributing proposals to standard.

[bulk_memory_operations]: https://github.com/WebAssembly/bulk-memory-operations
[custom_annotation_syntax_in_the_text_format]: https://github.com/WebAssembly/annotations
[ecmascript_module_integration]: https://github.com/WebAssembly/esm-integration
[exception_handling]: https://github.com/WebAssembly/exception-handling
[fixed-width_simd]: https://github.com/webassembly/simd
[function_references]: https://github.com/WebAssembly/function-references
[type-imports]: https://github.com/WebAssembly/proposal-type-imports
[garbage_collection]: https://github.com/WebAssembly/gc
[interface_types]: https://github.com/WebAssembly/interface-types
[javascript_bigint_to_webassembly_i64_integration]: https://github.com/WebAssembly/JS-BigInt-integration
[non-trapping_float-to-int_conversions]: https://github.com/WebAssembly/nontrapping-float-to-int-conversions
[multi-value]: https://github.com/WebAssembly/multi-value
[multi-memory]: https://github.com/WebAssembly/multi-memory
[reference_types]: https://github.com/WebAssembly/reference-types
[sign-extension_operators]: https://github.com/WebAssembly/sign-extension-ops
[tail_call]: https://github.com/WebAssembly/tail-call
[threads]: https://github.com/webassembly/threads
[type_reflection_for_webassembly_javascript_api]: https://github.com/WebAssembly/js-types
[wasm_c_api]: https://github.com/WebAssembly/wasm-c-api
[web_content_security_policy]: https://github.com/WebAssembly/content-security-policy
[webassembly_specification]: https://github.com/WebAssembly/spec
[funclets]: https://github.com/WebAssembly/funclets
[conditional_sections]: https://github.com/WebAssembly/conditional-sections
[extended-name-section]: https://github.com/WebAssembly/extended-name-section
[module_types]: https://github.com/WebAssembly/module-types
