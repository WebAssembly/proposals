# Finished Proposals

Finished proposals are proposals that have reached phase 4, and are included in the latest draft of [the specification](http://webassembly.github.io/spec/).

| Proposal                                                             | Champion         | Meeting notes        | Affected specs | Spec Version |
| -------------------------------------------------------------------- | ---------------- | ---------------------|----------------|---------|
| [MVP][mvp]                                                           | The Wasm CG      | [WG 2017-12-06][WG-2017-12-06] | core, js-api, web-api | 1.0 |
| [Import/Export of Mutable Globals][import_export_of_mutable_globals] | Ben Smith        | [WG 2018-06-06][WG-2018-06-06] | core, js-api | 1.0 |
| [Non-trapping float-to-int conversions][non-trapping_float-to-int_conversions] | Dan Gohman       | [WG 2020-03-11][WG-2020-03-11] | core | 2.0 |
| [Sign-extension operators][sign-extension_operators]                           | Ben Smith        | [WG 2020-03-11][WG-2020-03-11] | core | 2.0 |
| [Multi-value][multi-value]                                                     | Andreas Rossberg | [WG 2020-03-11][WG-2020-03-11] | core, js-api | 2.0 |
| [JavaScript BigInt to WebAssembly i64 integration][javascript_bigint_to_webassembly_i64_integration] | Dan Ehrenberg & Sven Sauleau           | [WG 2020-06-09][WG-2020-06-09] | js-api | - |
| [Reference Types][reference_types]                                             | Andreas Rossberg | [WG 2021-02-10][WG-2021-02-10] | core, js-api | 2.0 |
| [Bulk memory operations][bulk_memory_operations]                               | Ben Smith        | [WG 2021-02-10][WG-2021-02-10] | core | 2.0 |
| [Fixed-width SIMD][fixed-width_simd]                                           | Deepti Gandluri and Arun Purushan | [WG 2021-07-14][WG-2021-07-14] | core, js-api | 2.0 |
| [Tail call][tail_call]                                               | Andreas Rossberg         | [WG 2024-07-10][WG-2024-07-10] | core | 3.0 |
| [Extended Constant Expressions][extended-const]                      | Sam Clegg                | [WG 2024-07-10][WG-2024-07-10] | core | 3.0 |
| [Typed Function References][function_references]                     | Andreas Rossberg         | [WG 2024-07-10][WG-2024-07-10] | core, js-api | 3.0 |
| [Garbage collection][garbage_collection]                             | Andreas Rossberg         | [WG 2024-07-10][WG-2024-07-10] | core, js-api | 3.0 |
| [Multiple memories][multi-memory]                                    | Andreas Rossberg         | [WG 2024-07-10][WG-2024-07-10] | core, js-api | 3.0 |
| [Relaxed SIMD][relaxed-simd]                                         | Marat Dukhan & Zhi An Ng | [WG 2024-07-10][WG-2024-07-10] | core | 3.0 |
| [Custom Annotation Syntax in the Text Format][annotations]           | Andreas Rossberg         | [WG 2024-07-10][WG-2024-07-10] | core | 3.0 |
| [Branch Hinting][branch-hinting]                                     | Yuri Iozzelli            | [WG 2024-07-10][WG-2024-07-10] | core | 3.0 |
| [Exception handling][exception_handling]                             | Heejin Ahn & Ben Titzer  | [WG 2025-07-23][WG-2025-07-23] | core, js-api | 3.0 |
| [JS String Builtins][js-string-builtins]                             | Ryan Hunt                | [WG 2025-07-23][WG-2025-07-23] | core, js-api | 3.0 |
| [Memory64][memory64]                                                 | Sam Clegg                | [WG 2025-07-23][WG-2025-07-23] | core | 3.0 |

See also the [active proposals](README.md) and [inactive proposals](inactive-proposals.md) documents.

[mvp]: https://github.com/WebAssembly/design/blob/main/MVP.md
[import_export_of_mutable_globals]: https://github.com/WebAssembly/mutable-global
[non-trapping_float-to-int_conversions]: https://github.com/WebAssembly/nontrapping-float-to-int-conversions
[sign-extension_operators]: https://github.com/WebAssembly/sign-extension-ops
[multi-value]: https://github.com/WebAssembly/multi-value
[javascript_bigint_to_webassembly_i64_integration]: https://github.com/WebAssembly/JS-BigInt-integration
[reference_types]: https://github.com/WebAssembly/reference-types
[bulk_memory_operations]: https://github.com/WebAssembly/bulk-memory-operations
[fixed-width_simd]: https://github.com/webassembly/simd
[tail_call]: https://github.com/WebAssembly/tail-call
[extended-const]: https://github.com/WebAssembly/extended-const
[function_references]: https://github.com/WebAssembly/function-references
[garbage_collection]: https://github.com/WebAssembly/gc
[multi-memory]: https://github.com/WebAssembly/multi-memory
[relaxed-simd]: https://github.com/WebAssembly/relaxed-simd
[annotations]: https://github.com/WebAssembly/annotations
[branch-hinting]: https://github.com/WebAssembly/branch-hinting
[exception_handling]: https://github.com/WebAssembly/exception-handling
[js-string-builtins]: https://github.com/WebAssembly/js-string-builtins
[memory64]: https://github.com/WebAssembly/memory64
[WG-2017-12-06]: https://github.com/WebAssembly/meetings/blob/main/main/2017/WG-12-06.md
[WG-2018-06-06]: https://github.com/WebAssembly/meetings/blob/main/main/2018/WG-06-06.md#discussion-on-status-of-the-working-draft
[WG-2020-03-11]: https://github.com/WebAssembly/meetings/blob/main/main/2020/WG-03-11.md
[WG-2020-06-09]: https://lists.w3.org/Archives/Public/public-webassembly/2020Jun/0000.html
[WG-2021-02-10]: https://github.com/WebAssembly/meetings/blob/main/main/2021/WG-02-10.md
[WG-2021-07-14]: https://github.com/WebAssembly/meetings/blob/main/main/2021/WG-07-14.md
[WG-2024-07-10]: https://github.com/WebAssembly/meetings/blob/main/main/2024/WG-07-10.md
[WG-2025-07-23]: https://github.com/WebAssembly/meetings/blob/main/main/2025/WG-07-23.md
