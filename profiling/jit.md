
## 2to3

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.27% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.93% | `[JIT]` | `jit` | jit |
| 2.45% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.20% | `python` | `deduce_unreachable` | gc |
| 2.08% | `python` | `type_new` | memory |
| 2.04% | `python` | `gc_collect_region.isra.0` | gc |
| 1.79% | `python` | `tupledealloc` | memory |
| 1.66% | `python` | `visit_decref` | gc |
| 1.58% | `python` | `sre_ucs1_match` | library |
| 1.50% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.44% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.07% | `python` | `PyDict_GetItemRef` | dict |
| 1.00% | `python` | `_PyCode_New` | memory |
| 0.94% | `python` | `visit_reachable` | gc |
| 0.86% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.82% | `python` | `r_object` | import |
| 0.80% | `python` | `_PyPegen_fill_token` | interpreter |
| 0.77% | `python` | `list_dealloc` | memory |
| 0.74% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.66% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.64% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.63% | `python` | `gen_dealloc` | memory |
| 0.62% | `python` | `make_gen` | unknown |
| 0.61% | `python` | `siphash13` | str |
| 0.60% | `python` | `dict_dealloc` | memory |
| 0.58% | `python` | `PyUnicode_FromKindAndData` | str |
| 0.50% | `python` | `PyDict_SetItem` | dict |

## aiohttp

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 26.73% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.53% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.53% | `[JIT]` | `jit` | jit |
| 2.14% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.53% | `python` | `tupledealloc` | memory |
| 1.37% | `python` | `type_new` | memory |
| 1.23% | `python` | `deduce_unreachable` | gc |
| 1.03% | `python` | `visit_decref` | gc |
| 0.96% | `python` | `PyDict_GetItemRef` | dict |
| 0.95% | `python` | `gc_collect_region.isra.0` | gc |
| 0.77% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.70% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.69% | `python` | `visit_reachable` | gc |
| 0.68% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.66% | `python` | `unicode_dealloc` | memory |
| 0.65% | `python` | `subtype_dealloc` | memory |
| 0.63% | `python` | `find_name_in_mro` | lookup |
| 0.62% | `python` | `_PyCode_New` | memory |
| 0.61% | `python` | `dict_dealloc` | memory |
| 0.61% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.60% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.58% | `python` | `_PySuper_Lookup` | dynamic |
| 0.57% | `python` | `sre_ucs1_match` | library |
| 0.56% | `python` | `list_dealloc` | memory |
| 0.53% | `python` | `r_object` | import |
| 0.51% | `python` | `PyObject_GC_Del` | gc |
| 0.50% | `python` | `_PyObject_MakeTpCall` | dynamic |

## async_generators

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 22.43% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.97% | `python` | `_PyErr_SetObject` | exceptions |
| 4.58% | `python` | `BaseException_new` | memory |
| 4.47% | `python` | `StopIteration_dealloc` | memory |
| 3.63% | `[JIT]` | `jit` | jit |
| 3.23% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 2.64% | `python` | `gen_send_ex` | unknown |
| 2.50% | `python` | `StopIteration_init` | dynamic |
| 2.40% | `python` | `async_gen_asend_send` | unknown |
| 2.24% | `python` | `tupledealloc` | memory |
| 1.77% | `python` | `async_gen_asend_dealloc` | memory |
| 1.67% | `python` | `gen_send_ex2` | unknown |
| 1.65% | `python` | `async_gen_asend_new` | memory |
| 1.61% | `python` | `PyErr_ExceptionMatches` | exceptions |
| 1.47% | `python` | `PyErr_GivenExceptionMatches` | exceptions |
| 1.42% | `python` | `async_gen_wrapped_val_dealloc` | memory |
| 1.29% | `python` | `_PyAsyncGenValueWrapperNew` | memory |
| 1.24% | `python` | `async_gen_unwrap_value.isra.0` | unknown |
| 1.18% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.14% | `python` | `_Py_NewReference` | memory |
| 1.07% | `python` | `_PyLong_Add` | int |
| 1.00% | `python` | `_PyGen_FetchStopIterationValue.cold` | unknown |
| 0.92% | `python` | `type_call` | dynamic |
| 0.85% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.79% | `python` | `PyObject_CallFinalizerFromDealloc` | memory |
| 0.78% | `python` | `_PyEval_EvalFrameDefault.cold` | interpreter |
| 0.74% | `python` | `deduce_unreachable` | gc |
| 0.65% | `python` | `PyType_GenericAlloc` | memory |
| 0.62% | `python` | `_Py_Dealloc` | memory |
| 0.61% | `python` | `long_dealloc` | memory |
| 0.58% | `python` | `visit_decref` | gc |
| 0.56% | `python` | `_PyGen_SetStopIterationValue` | unknown |
| 0.54% | `python` | `range_subscript` | unknown |
| 0.52% | `python` | `subtype_dealloc` | memory |
| 0.50% | `python` | `visit_reachable` | gc |

## async_tree

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 22.15% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.81% | `python` | `deduce_unreachable` | gc |
| 4.27% | `python` | `visit_reachable` | gc |
| 4.11% | `python` | `visit_add_to_container` | gc |
| 4.09% | `python` | `visit_decref` | gc |
| 3.89% | `[JIT]` | `jit` | jit |
| 3.38% | `python` | `gc_collect_region.isra.0` | gc |
| 1.91% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.44% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.31% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 1.22% | `python` | `tupledealloc` | memory |
| 1.08% | `python` | `subtype_traverse` | gc |
| 1.02% | `python` | `_PyObject_GC_New` | gc |
| 1.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.97% | `python` | `PyObject_GC_Del` | gc |
| 0.96% | `python` | `PyDict_GetItemRef` | dict |
| 0.91% | `python` | `_PyGC_Collect` | gc |
| 0.91% | `python` | `meth_dealloc` | memory |
| 0.89% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.87% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.82% | `python` | `context_tp_dealloc` | memory |
| 0.78% | `python` | `insertdict` | dict |
| 0.77% | `python` | `slot_tp_init` | unknown |
| 0.74% | `python` | `list_dealloc` | memory |
| 0.70% | `python` | `gen_dealloc` | memory |
| 0.63% | `python` | `object_new` | memory |
| 0.60% | `python` | `dict_dealloc` | memory |
| 0.59% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |
| 0.57% | `python` | `gen_traverse` | gc |
| 0.56% | `python` | `dict_traverse` | gc |
| 0.55% | `python` | `type_new` | memory |
| 0.52% | `python` | `subtype_dealloc` | memory |
| 0.50% | `python` | `make_gen` | unknown |

## async_tree_cpu_io_mixed

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 19.10% | `python` | `k_mul` | int |
| 16.88% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.52% | `python` | `deduce_unreachable` | gc |
| 3.28% | `python` | `visit_reachable` | gc |
| 3.23% | `python` | `visit_decref` | gc |
| 3.04% | `python` | `visit_add_to_container` | gc |
| 2.89% | `[JIT]` | `jit` | jit |
| 2.56% | `python` | `gc_collect_region.isra.0` | gc |
| 2.50% | `python` | `long_dealloc` | memory |
| 1.34% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.26% | `python` | `_PyLong_New` | memory |
| 1.04% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.01% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.90% | `python` | `subtype_traverse` | gc |
| 0.88% | `python` | `tupledealloc` | memory |
| 0.88% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 0.71% | `python` | `PyDict_GetItemRef` | dict |
| 0.71% | `python` | `_PyGC_Collect` | gc |
| 0.69% | `python` | `context_tp_dealloc` | memory |
| 0.68% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.68% | `math.cpython-313-x86_64-linux-gnu.so` | `factorial_partial_product` | library |
| 0.65% | `python` | `meth_dealloc` | memory |
| 0.64% | `python` | `_PyObject_GC_New` | gc |
| 0.63% | `python` | `long_mul` | int |
| 0.60% | `python` | `PyObject_GC_Del` | gc |
| 0.59% | `python` | `gen_dealloc` | memory |
| 0.55% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.53% | `python` | `list_dealloc` | memory |

## async_tree_cpu_io_mixed_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 19.40% | `python` | `k_mul` | int |
| 15.64% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.91% | `python` | `deduce_unreachable` | gc |
| 4.40% | `python` | `visit_add_to_container` | gc |
| 3.96% | `python` | `visit_decref` | gc |
| 3.79% | `python` | `visit_reachable` | gc |
| 2.87% | `python` | `gc_collect_region.isra.0` | gc |
| 2.69% | `python` | `long_dealloc` | memory |
| 2.50% | `[JIT]` | `jit` | jit |
| 1.26% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.26% | `python` | `_PyLong_New` | memory |
| 1.03% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.02% | `python` | `subtype_traverse` | gc |
| 0.93% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.88% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 0.80% | `python` | `_PyGC_Collect` | gc |
| 0.79% | `python` | `tupledealloc` | memory |
| 0.78% | `python` | `gen_traverse` | gc |
| 0.75% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.70% | `math.cpython-313-x86_64-linux-gnu.so` | `factorial_partial_product` | library |
| 0.64% | `python` | `PyObject_GC_Del` | gc |
| 0.63% | `python` | `long_mul` | int |
| 0.58% | `python` | `PyDict_GetItemRef` | dict |
| 0.56% | `python` | `meth_dealloc` | memory |
| 0.56% | `python` | `set_traverse` | gc |
| 0.53% | `python` | `gen_dealloc` | memory |
| 0.53% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.52% | `python` | `slot_tp_init` | unknown |
| 0.52% | `python` | `make_gen` | unknown |
| 0.50% | `math.cpython-313-x86_64-linux-gnu.so` | `math_factorial` | library |

## async_tree_io

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 19.62% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 9.30% | `python` | `deduce_unreachable` | gc |
| 7.29% | `python` | `visit_add_to_container` | gc |
| 6.47% | `python` | `visit_reachable` | gc |
| 6.40% | `python` | `visit_decref` | gc |
| 5.79% | `python` | `gc_collect_region.isra.0` | gc |
| 3.01% | `[JIT]` | `jit` | jit |
| 1.73% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.53% | `python` | `_PyGC_Collect` | gc |
| 1.45% | `python` | `subtype_traverse` | gc |
| 1.31% | `python` | `gen_traverse` | gc |
| 1.02% | `python` | `slot_tp_richcompare` | dynamic |
| 0.94% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.89% | `python` | `tupledealloc` | memory |
| 0.77% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.74% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.74% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 0.69% | `python` | `meth_dealloc` | memory |
| 0.65% | `_heapq.cpython-313-x86_64-linux-gnu.so` | `_heapq_heappop` | library |
| 0.63% | `python` | `PyObject_GC_Del` | gc |
| 0.61% | `python` | `gen_dealloc` | memory |
| 0.60% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |
| 0.59% | `python` | `slot_tp_init` | unknown |
| 0.54% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.54% | `python` | `_PyObject_GC_New` | gc |
| 0.53% | `python` | `PyDict_GetItemRef` | dict |

## async_tree_io_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 18.83% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 9.21% | `python` | `deduce_unreachable` | gc |
| 8.20% | `python` | `visit_add_to_container` | gc |
| 6.99% | `python` | `visit_decref` | gc |
| 6.86% | `python` | `visit_reachable` | gc |
| 5.79% | `python` | `gc_collect_region.isra.0` | gc |
| 2.77% | `[JIT]` | `jit` | jit |
| 1.75% | `python` | `gen_traverse` | gc |
| 1.63% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.59% | `python` | `_PyGC_Collect` | gc |
| 1.54% | `python` | `subtype_traverse` | gc |
| 1.08% | `python` | `slot_tp_richcompare` | dynamic |
| 0.99% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.84% | `python` | `tupledealloc` | memory |
| 0.80% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.79% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.73% | `python` | `set_traverse` | gc |
| 0.71% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 0.67% | `python` | `gen_dealloc` | memory |
| 0.65% | `python` | `PyObject_GC_Del` | gc |
| 0.65% | `_heapq.cpython-313-x86_64-linux-gnu.so` | `_heapq_heappop` | library |
| 0.63% | `python` | `meth_dealloc` | memory |
| 0.60% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |
| 0.55% | `python` | `slot_tp_init` | unknown |
| 0.53% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.52% | `python` | `make_gen` | unknown |
| 0.50% | `python` | `PyObject_RichCompareBool` | dynamic |

## async_tree_memoization

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 22.32% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.01% | `python` | `deduce_unreachable` | gc |
| 4.89% | `python` | `visit_decref` | gc |
| 4.76% | `python` | `visit_reachable` | gc |
| 4.70% | `python` | `visit_add_to_container` | gc |
| 3.90% | `python` | `gc_collect_region.isra.0` | gc |
| 3.67% | `[JIT]` | `jit` | jit |
| 1.92% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.33% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.20% | `python` | `subtype_traverse` | gc |
| 1.13% | `python` | `tupledealloc` | memory |
| 1.12% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 1.06% | `python` | `_PyGC_Collect` | gc |
| 0.96% | `python` | `PyDict_GetItemRef` | dict |
| 0.92% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.92% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.91% | `python` | `context_tp_dealloc` | memory |
| 0.91% | `python` | `meth_dealloc` | memory |
| 0.83% | `python` | `_PyObject_GC_New` | gc |
| 0.79% | `python` | `PyObject_GC_Del` | gc |
| 0.70% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.67% | `python` | `slot_tp_init` | unknown |
| 0.64% | `python` | `gen_dealloc` | memory |
| 0.64% | `python` | `insertdict` | dict |
| 0.64% | `python` | `gen_traverse` | gc |
| 0.63% | `python` | `list_dealloc` | memory |
| 0.61% | `python` | `object_new` | memory |
| 0.59% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |
| 0.59% | `python` | `weakref_dealloc` | memory |
| 0.56% | `python` | `dict_traverse` | gc |
| 0.52% | `python` | `dict_dealloc` | memory |
| 0.50% | `python` | `set_lookkey` | miscobj |

## async_tree_memoization_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 21.43% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.94% | `python` | `deduce_unreachable` | gc |
| 6.03% | `python` | `visit_add_to_container` | gc |
| 5.56% | `python` | `visit_decref` | gc |
| 5.25% | `python` | `visit_reachable` | gc |
| 4.00% | `python` | `gc_collect_region.isra.0` | gc |
| 3.30% | `[JIT]` | `jit` | jit |
| 1.78% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.37% | `python` | `subtype_traverse` | gc |
| 1.27% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.11% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.11% | `python` | `tupledealloc` | memory |
| 1.08% | `python` | `gen_traverse` | gc |
| 1.07% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 1.06% | `python` | `_PyGC_Collect` | gc |
| 1.03% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.88% | `python` | `PyObject_GC_Del` | gc |
| 0.86% | `python` | `PyDict_GetItemRef` | dict |
| 0.86% | `python` | `meth_dealloc` | memory |
| 0.74% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.73% | `python` | `set_traverse` | gc |
| 0.67% | `python` | `slot_tp_init` | unknown |
| 0.66% | `python` | `gen_dealloc` | memory |
| 0.64% | `python` | `make_gen` | unknown |
| 0.62% | `python` | `set_lookkey` | miscobj |
| 0.61% | `python` | `object_new` | memory |
| 0.60% | `python` | `_PyObject_GC_New` | gc |
| 0.54% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |

## async_tree_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 20.30% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.24% | `python` | `deduce_unreachable` | gc |
| 5.85% | `python` | `visit_add_to_container` | gc |
| 4.96% | `python` | `visit_decref` | gc |
| 4.80% | `python` | `visit_reachable` | gc |
| 3.68% | `python` | `gc_collect_region.isra.0` | gc |
| 3.63% | `[JIT]` | `jit` | jit |
| 1.82% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.36% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.31% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 1.18% | `python` | `subtype_traverse` | gc |
| 1.16% | `python` | `tupledealloc` | memory |
| 1.16% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.15% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.07% | `python` | `gen_traverse` | gc |
| 1.02% | `python` | `PyObject_GC_Del` | gc |
| 0.94% | `python` | `_PyGC_Collect` | gc |
| 0.83% | `python` | `PyDict_GetItemRef` | dict |
| 0.82% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.82% | `python` | `set_traverse` | gc |
| 0.79% | `python` | `meth_dealloc` | memory |
| 0.74% | `python` | `slot_tp_init` | unknown |
| 0.73% | `python` | `make_gen` | unknown |
| 0.67% | `python` | `gen_dealloc` | memory |
| 0.67% | `python` | `_PyObject_GC_New` | gc |
| 0.61% | `python` | `object_new` | memory |
| 0.61% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |
| 0.59% | `python` | `type_new` | memory |
| 0.56% | `python` | `insertdict` | dict |
| 0.53% | `python` | `subtype_dealloc` | memory |

## asyncio_tcp

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 31.35% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 17.51% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 9.40% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.97% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.61% | `[kernel.kallsyms]` | `tcp_sendmsg_locked` | kernel |
| 0.51% | `[JIT]` | `jit` | jit |

## asyncio_tcp_ssl

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 39.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 25.74% | `libcrypto.so.1.1` | `CRYPTO_secure_actual_size` | libc |
| 10.83% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 3.61% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.86% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.90% | `libssl.so.1.1` | `SSL_rstate_string` | library |
| 0.56% | `[JIT]` | `jit` | jit |
| 0.55% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |

## asyncio_websockets

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 63.73% | `libz.so.1.2.11` | `crc32_combine64` | library |
| 20.13% | `libz.so.1.2.11` | `inflateBackEnd` | library |
| 2.90% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.72% | `python` | `_PyEval_EvalFrameDefault` | interpreter |

## chameleon

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 35.61% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.55% | `[JIT]` | `jit` | jit |
| 3.43% | `python` | `PyObject_Str` | dynamic |
| 2.50% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.30% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.17% | `python` | `sre_ucs2_charset.isra.0` | library |
| 2.15% | `python` | `PyUnicode_Format` | str |
| 2.01% | `python` | `dict_get` | dict |
| 1.77% | `python` | `_PyUnicode_JoinArray` | str |
| 1.66% | `python` | `type_new` | memory |
| 1.31% | `python` | `unicode_dealloc` | memory |
| 1.16% | `python` | `insertdict` | dict |
| 1.04% | `python` | `deduce_unreachable` | gc |
| 0.96% | `python` | `list_append` | list |
| 0.91% | `python` | `visit_decref` | gc |
| 0.84% | `python` | `list_dealloc` | memory |
| 0.79% | `python` | `gc_collect_region.isra.0` | gc |
| 0.75% | `python` | `state_init` | unknown |
| 0.74% | `python` | `PyUnicode_Concat` | str |
| 0.74% | `python` | `_PyUnicodeWriter_PrepareInternal` | str |
| 0.70% | `python` | `_PyCode_New` | memory |
| 0.63% | `python` | `PyObject_Vectorcall` | dynamic |
| 0.62% | `libc-2.31.so` | `malloc` | libc |
| 0.61% | `python` | `visit_reachable` | gc |
| 0.60% | `python` | `tupledealloc` | memory |
| 0.59% | `python` | `r_object` | import |
| 0.58% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.53% | `python` | `sre_search` | library |
| 0.51% | `python` | `method_vectorcall_FASTCALL` | calls |
| 0.51% | `python` | `dict_setdefault_ref_lock_held` | dict |

## chaos

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.43% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 18.71% | `[JIT]` | `jit` | jit |
| 2.65% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.17% | `python` | `_PyLong_Subtract` | int |
| 1.62% | `python` | `_PyLong_Add` | int |
| 1.48% | `python` | `subtype_dealloc` | memory |
| 1.42% | `python` | `PyType_GenericAlloc` | memory |
| 1.32% | `python` | `range_vectorcall` | unknown |
| 1.28% | `python` | `float_div` | float |
| 1.13% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.11% | `python` | `convert_to_double` | unknown |
| 0.95% | `python` | `type_new` | memory |
| 0.92% | `python` | `PyFloat_FromDouble` | float |
| 0.91% | `python` | `range_iter` | unknown |
| 0.90% | `python` | `float_sub` | float |
| 0.88% | `libm-2.31.so` | `f64xsubf128` | library |
| 0.86% | `python` | `PyObject_GC_Del` | gc |
| 0.79% | `python` | `float_dealloc` | memory |
| 0.73% | `python` | `float_richcompare` | float |
| 0.71% | `python` | `tupledealloc` | memory |
| 0.68% | `python` | `PyNumber_TrueDivide` | dynamic |
| 0.63% | `python` | `PyNumber_Subtract` | dynamic |
| 0.62% | `python` | `deduce_unreachable` | gc |
| 0.59% | `python` | `PyLong_FromLong` | int |
| 0.58% | `python` | `visit_decref` | gc |
| 0.55% | `python` | `range_dealloc` | memory |
| 0.54% | `python` | `vectorcall_maybe.constprop.0` | unknown |
| 0.54% | `python` | `gc_collect_region.isra.0` | gc |
| 0.54% | `python` | `float_pow` | float |
| 0.50% | `python` | `PyObject_RichCompare` | dynamic |

## comprehensions

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 29.62% | `[JIT]` | `jit` | jit |
| 14.81% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.28% | `python` | `dict_get` | dict |
| 2.69% | `python` | `PyFunction_NewWithQualName` | memory |
| 1.90% | `python` | `list_dealloc` | memory |
| 1.85% | `python` | `PyDict_GetItemRef` | dict |
| 1.64% | `python` | `unsafe_tuple_compare` | unknown |
| 1.56% | `python` | `list_iter` | list |
| 1.43% | `python` | `gen_dealloc` | memory |
| 1.39% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.28% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.25% | `python` | `_PyObject_Malloc` | memory |
| 1.16% | `python` | `listiter_dealloc` | memory |
| 1.10% | `python` | `type_new` | memory |
| 1.08% | `python` | `func_dealloc` | memory |
| 1.06% | `python` | `make_gen` | unknown |
| 0.99% | `python` | `PyObject_GC_Del` | gc |
| 0.97% | `python` | `tupledealloc` | memory |
| 0.89% | `python` | `insertdict` | dict |
| 0.88% | `python` | `long_hash` | int |
| 0.81% | `python` | `long_richcompare` | int |
| 0.75% | `python` | `PyObject_RichCompare` | dynamic |
| 0.71% | `python` | `deduce_unreachable` | gc |
| 0.70% | `python` | `_PyDict_SetItem_Take2` | dict |
| 0.68% | `python` | `_Py_type_getattro` | lookup |
| 0.67% | `python` | `_PyObject_Realloc` | memory |
| 0.60% | `python` | `gc_collect_region.isra.0` | gc |
| 0.58% | `python` | `visit_decref` | gc |
| 0.57% | `python` | `dictresize` | dict |
| 0.55% | `python` | `_PyList_AppendTakeRefListResize` | list |

## concurrent_imap

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.52% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.95% | `[JIT]` | `jit` | jit |
| 2.02% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.01% | `python` | `subtype_dealloc` | memory |
| 1.76% | `[kernel.kallsyms]` | `perf_event_alloc` | kernel |
| 1.61% | `[kernel.kallsyms]` | `memset_erms` | kernel |
| 1.27% | `python` | `tupledealloc` | memory |
| 1.24% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.18% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.12% | `python` | `PyObject_GC_Del` | gc |
| 0.99% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.84% | `python` | `long_dealloc` | memory |
| 0.63% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.62% | `python` | `_PySuper_Lookup` | dynamic |
| 0.61% | `python` | `list_dealloc` | memory |
| 0.60% | `python` | `meth_dealloc` | memory |
| 0.59% | `[kernel.kallsyms]` | `_raw_spin_lock_irqsave` | kernel |
| 0.58% | `python` | `slot_tp_init` | unknown |
| 0.57% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.57% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.55% | `python` | `PyObject_GetAttr` | dynamic |
| 0.54% | `[kernel.kallsyms]` | `copy_page` | kernel |
| 0.53% | `python` | `_Py_type_getattro` | lookup |
| 0.53% | `python` | `PyObject_Vectorcall` | dynamic |
| 0.51% | `[kernel.kallsyms]` | `kfree` | kernel |
| 0.50% | `python` | `method_dealloc` | memory |

## coroutines

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 40.18% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 14.00% | `python` | `gen_dealloc` | memory |
| 9.77% | `python` | `make_gen` | unknown |
| 6.38% | `python` | `_PyEval_EvalFrameDefault.cold` | interpreter |
| 4.81% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.51% | `python` | `_PyLong_Subtract` | int |
| 2.33% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.99% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.50% | `python` | `_PyLong_Add` | int |
| 1.29% | `python` | `_PyCoro_GetAwaitableIter` | unknown |
| 0.80% | `python` | `type_new` | memory |
| 0.51% | `python` | `_PyGen_yf` | unknown |
| 0.50% | `python` | `deduce_unreachable` | gc |

## coverage

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 18.90% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.31% | `tracer.cpython-313-x86_64-linux-gnu.so` | `CTracer_trace` | library |
| 4.71% | `python` | `call_instrumentation_vector` | unknown |
| 4.23% | `python` | `unicode_decode_utf8` | str |
| 4.15% | `python` | `PyObject_SetAttrString` | dynamic |
| 3.27% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 3.14% | `python` | `siphash13` | str |
| 2.62% | `python` | `frame_dealloc` | memory |
| 2.44% | `python` | `call_one_instrument` | unknown |
| 2.41% | `python` | `PyLong_FromLong` | int |
| 2.39% | `python` | `PySet_Add` | unknown |
| 2.34% | `python` | `_Py_dict_lookup` | lookup |
| 1.87% | `python` | `_PyObject_VectorcallTstate.lto_priv.5` | dynamic |
| 1.77% | `python` | `_PyFrame_MakeAndSetFrameObject` | unknown |
| 1.74% | `python` | `PyObject_SetAttr` | dynamic |
| 1.48% | `python` | `dict_getitem` | dict |
| 1.44% | `python` | `unicode_dealloc` | memory |
| 1.38% | `python` | `_PyDict_LoadGlobal` | dict |
| 1.35% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.18% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.16% | `python` | `_Py_hashtable_get` | unknown |
| 1.04% | `python` | `call_trace_func.isra.0` | unknown |
| 0.96% | `python` | `_PyUnicode_InternInPlace` | str |
| 0.92% | `python` | `type_new` | memory |
| 0.78% | `python` | `_Py_call_instrumentation_jump` | unknown |
| 0.62% | `python` | `deduce_unreachable` | gc |
| 0.61% | `python` | `visit_decref` | gc |
| 0.58% | `python` | `_PyCode_GetCode` | unknown |
| 0.54% | `python` | `PyEval_GetFrame` | interpreter |
| 0.54% | `python` | `gc_collect_region.isra.0` | gc |
| 0.52% | `[JIT]` | `jit` | jit |
| 0.51% | `tracer.cpython-313-x86_64-linux-gnu.so` | `CTracer_set_pdata_stack` | library |

## crypto_pyaes

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 26.26% | `[JIT]` | `jit` | jit |
| 11.22% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.05% | `python` | `long_dealloc` | memory |
| 6.92% | `python` | `long_bitwise` | int |
| 4.17% | `python` | `long_rshift` | int |
| 3.42% | `python` | `long_and` | int |
| 3.32% | `python` | `_PyLong_New` | memory |
| 3.13% | `python` | `long_mod` | int |
| 1.49% | `python` | `binary_op` | unknown |
| 1.32% | `python` | `_PyObject_Malloc` | memory |
| 1.12% | `python` | `PyNumber_And` | dynamic |
| 1.09% | `python` | `_PyLong_Add` | int |
| 1.05% | `python` | `PyObject_Free` | dynamic |
| 1.03% | `python` | `list_dealloc` | memory |
| 1.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.90% | `python` | `type_new` | memory |
| 0.79% | `python` | `long_xor` | int |
| 0.79% | `python` | `PyNumber_Rshift` | dynamic |
| 0.73% | `python` | `PyNumber_Remainder` | dynamic |
| 0.73% | `python` | `range_vectorcall` | unknown |
| 0.57% | `python` | `deduce_unreachable` | gc |
| 0.55% | `python` | `range_iter` | unknown |
| 0.54% | `python` | `visit_decref` | gc |
| 0.52% | `python` | `_PyEval_FrameClearAndPop` | interpreter |

## dask

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 25.05% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.61% | `python` | `visit_decref` | gc |
| 2.56% | `python` | `deduce_unreachable` | gc |
| 2.14% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.08% | `[JIT]` | `jit` | jit |
| 1.97% | `python` | `gc_collect_region.isra.0` | gc |
| 1.90% | `python` | `visit_reachable` | gc |
| 1.77% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.63% | `python` | `tupledealloc` | memory |
| 1.54% | `python` | `visit_add_to_container` | gc |
| 1.16% | `python` | `dict_dealloc` | memory |
| 1.09% | `python` | `PyDict_GetItemRef` | dict |
| 0.98% | `python` | `PyBytes_Repr` | str |
| 0.96% | `python` | `type_new` | memory |
| 0.78% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.64% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.64% | `python` | `list_dealloc` | memory |
| 0.63% | `python` | `insertdict` | dict |
| 0.57% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.53% | `python` | `PyObject_GC_Del` | gc |
| 0.52% | `python` | `siphash13` | str |

## deepcopy

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 43.65% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.28% | `python` | `dict_get` | dict |
| 4.20% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 3.65% | `[JIT]` | `jit` | jit |
| 2.28% | `python` | `_PyLong_New` | memory |
| 2.08% | `python` | `long_dealloc` | memory |
| 1.52% | `python` | `insertdict` | dict |
| 1.37% | `python` | `PySys_Audit` | unknown |
| 1.25% | `python` | `long_hash` | int |
| 1.14% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.11% | `python` | `builtin_id` | unknown |
| 1.06% | `python` | `PyDict_GetItemRef` | dict |
| 0.82% | `python` | `tupledealloc` | memory |
| 0.81% | `python` | `insert_to_emptydict` | dict |
| 0.76% | `python` | `list_dealloc` | memory |
| 0.73% | `python` | `type_new` | memory |
| 0.68% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.60% | `python` | `dict_dealloc` | memory |
| 0.60% | `python` | `list_append` | list |
| 0.56% | `python` | `list_resize` | list |
| 0.54% | `python` | `meth_dealloc` | memory |
| 0.53% | `python` | `long_richcompare` | int |

## deltablue

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 46.58% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 9.68% | `[JIT]` | `jit` | jit |
| 4.48% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.63% | `python` | `_PyObject_GetMethod` | dynamic |
| 1.43% | `python` | `deduce_unreachable` | gc |
| 1.35% | `python` | `gc_collect_region.isra.0` | gc |
| 1.27% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.14% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.07% | `python` | `type_new` | memory |
| 1.07% | `python` | `visit_decref` | gc |
| 1.04% | `python` | `_PySuper_Lookup` | dynamic |
| 0.73% | `python` | `_Py_type_getattro` | lookup |
| 0.70% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.70% | `python` | `method_dealloc` | memory |
| 0.62% | `python` | `PyObject_GC_Del` | gc |
| 0.58% | `python` | `cm_descr_get` | unknown |
| 0.57% | `python` | `visit_reachable` | gc |
| 0.55% | `python` | `PyObject_GetAttr` | dynamic |
| 0.52% | `python` | `_PyCode_New` | memory |

## django_template

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 33.98% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.33% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.82% | `python` | `_PyObject_Malloc (inlined)` | memory |
| 2.48% | `python` | `_PyObject_Free` | memory |
| 2.01% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.96% | `python` | `gc_collect_main` | gc |
| 1.68% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.52% | `python` | `_Py_dict_lookup` | lookup |
| 1.32% | `python` | `_PyType_Lookup` | lookup |
| 1.27% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 1.12% | `python` | `initialize_locals` | interpreter |
| 0.99% | `python` | `visit_decref` | gc |
| 0.91% | `python` | `tupledealloc` | memory |
| 0.76% | `python` | `replace` | str |
| 0.72% | `python` | `insertdict` | dict |
| 0.71% | `python` | `visit_reachable` | gc |
| 0.65% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.64% | `python` | `_PyObject_GC_New` | gc |
| 0.62% | `python` | `PyObject_GC_Del` | gc |
| 0.61% | `python` | `_Py_NewReference` | memory |
| 0.60% | `python` | `PyType_IsSubtype` | dynamic |
| 0.60% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.53% | `python` | `r_object` | import |
| 0.50% | `python` | `tuple_alloc` | memory |

## djangocms

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 17.57% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.74% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 4.91% | `python` | `gc_collect_main` | gc |
| 2.47% | `python` | `_PyObject_Malloc` | memory |
| 2.40% | `python` | `_Py_dict_lookup` | lookup |
| 2.05% | `python` | `visit_decref` | gc |
| 1.95% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.69% | `python` | `_PyType_Lookup` | lookup |
| 1.58% | `python` | `_PyObject_Free` | memory |
| 1.56% | `python` | `visit_reachable` | gc |
| 0.98% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.91% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.87% | `python` | `dict_traverse` | gc |
| 0.80% | `libsqlite3.so.0.8.6` | `sqlite3_exec` | library |
| 0.78% | `python` | `tupledealloc` | memory |
| 0.74% | `libz.so.1.2.11` | `inflateBackEnd` | library |
| 0.73% | `python` | `initialize_locals` | interpreter |
| 0.72% | `python` | `find_name_in_mro` | lookup |
| 0.72% | `python` | `_PyDict_GetItem_KnownHash` | dict |
| 0.66% | `python` | `advance` | interpreter |
| 0.62% | `python` | `update_one_slot` | lookup |
| 0.62% | `python` | `_PyPegen_is_memoized` | interpreter |
| 0.55% | `python` | `insertdict` | dict |
| 0.52% | `python` | `_PyFrame_ClearExceptCode` | interpreter |

## docutils

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 22.39% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.23% | `python` | `sre_ucs1_match` | library |
| 5.75% | `[JIT]` | `jit` | jit |
| 3.70% | `python` | `deduce_unreachable` | gc |
| 2.87% | `python` | `gc_collect_region.isra.0` | gc |
| 2.39% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 2.21% | `python` | `visit_add_to_container` | gc |
| 2.15% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.13% | `python` | `sre_ucs2_charset.isra.0` | library |
| 1.92% | `python` | `visit_decref` | gc |
| 1.88% | `python` | `list_dealloc` | memory |
| 1.87% | `python` | `find_name_in_mro` | lookup |
| 1.69% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.11% | `python` | `_PyObject_GetMethod` | dynamic |
| 1.04% | `python` | `dict_traverse` | gc |
| 0.98% | `python` | `visit_reachable` | gc |
| 0.91% | `python` | `PyDict_GetItemRef` | dict |
| 0.87% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.86% | `python` | `tupledealloc` | memory |
| 0.85% | `python` | `_PyUnicode_JoinArray` | str |
| 0.79% | `python` | `PyObject_SetAttr` | dynamic |
| 0.73% | `python` | `list_traverse` | gc |
| 0.72% | `python` | `object_isinstance` | dynamic |
| 0.69% | `python` | `PyMem_Free` | memory |
| 0.66% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.64% | `python` | `list_subscript` | list |
| 0.62% | `python` | `subtype_traverse` | gc |
| 0.60% | `python` | `dict_dealloc` | memory |
| 0.57% | `python` | `unicode_dealloc` | memory |
| 0.57% | `python` | `PyMem_Malloc` | memory |
| 0.54% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.54% | `python` | `PyObject_GetAttr` | dynamic |
| 0.52% | `python` | `PyObject_GC_Del` | gc |
| 0.51% | `python` | `PyUnicode_Format` | str |

## dulwich_log

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.57% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.10% | `[JIT]` | `jit` | jit |
| 2.93% | `libz.so.1.2.11` | `inflateCodesUsed` | library |
| 2.71% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.72% | `libz.so.1.2.11` | `inflateBackEnd` | library |
| 1.56% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.44% | `libz.so.1.2.11` | `inflate` | library |
| 1.25% | `python` | `PyBytes_FromStringAndSize` | str |
| 1.05% | `python` | `type_new` | memory |
| 0.94% | `python` | `tupledealloc` | memory |
| 0.93% | `python` | `PyObject_Free` | dynamic |
| 0.81% | `python` | `long_dealloc` | memory |
| 0.80% | `python` | `deduce_unreachable` | gc |
| 0.77% | `python` | `visit_decref` | gc |
| 0.76% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.73% | `python` | `list_dealloc` | memory |
| 0.58% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 0.58% | `python` | `gc_collect_region.isra.0` | gc |
| 0.55% | `python` | `unicode_dealloc` | memory |
| 0.52% | `python` | `_PyCode_New` | memory |

## fannkuch

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 36.36% | `[JIT]` | `jit` | jit |
| 10.09% | `python` | `list_subscript` | list |
| 6.63% | `python` | `list_dealloc` | memory |
| 6.60% | `python` | `list_ass_slice_lock_held` | list |
| 3.66% | `python` | `slice_dealloc` | memory |
| 2.66% | `python` | `_PyBuildSlice_ConsumeRefs` | miscobj |
| 2.65% | `python` | `_PyLong_Add` | int |
| 2.33% | `python` | `_PyObject_Malloc` | memory |
| 2.16% | `python` | `list_new_prealloc` | memory |
| 2.13% | `python` | `PySlice_New` | memory |
| 1.90% | `python` | `list_ass_subscript` | list |
| 1.61% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.59% | `python` | `PySlice_Unpack` | miscobj |
| 1.51% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 1.29% | `python` | `_PyEval_SliceIndex` | interpreter |
| 1.05% | `python` | `ins1` | unknown |
| 1.02% | `python` | `PyObject_GetItem` | dynamic |
| 0.86% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 0.81% | `python` | `list_pop` | list |
| 0.74% | `python` | `_PyLong_Subtract` | int |
| 0.71% | `python` | `PyMem_Malloc` | memory |
| 0.65% | `python` | `_Py_Dealloc` | memory |
| 0.56% | `python` | `PyObject_SetItem` | dynamic |

## float

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 25.33% | `[JIT]` | `jit` | jit |
| 14.35% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.81% | `libm-2.31.so` | `f64xsubf128` | library |
| 2.25% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.06% | `python` | `subtype_traverse` | gc |
| 1.88% | `python` | `object_new` | memory |
| 1.76% | `python` | `PyFloat_FromDouble` | float |
| 1.70% | `python` | `slot_tp_init` | unknown |
| 1.69% | `python` | `float_div` | float |
| 1.65% | `python` | `visit_decref` | gc |
| 1.61% | `python` | `visit_reachable` | gc |
| 1.53% | `python` | `deduce_unreachable` | gc |
| 1.53% | `python` | `_PyObject_Malloc` | memory |
| 1.40% | `python` | `clear_slots` | unknown |
| 1.30% | `python` | `_PyObject_Free` | memory |
| 1.21% | `python` | `PyFloat_AsDouble` | float |
| 1.11% | `python` | `visit_add_to_container` | gc |
| 1.01% | `python` | `float_dealloc` | memory |
| 0.97% | `python` | `gc_collect_region.isra.0` | gc |
| 0.97% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.94% | `python` | `tupledealloc` | memory |
| 0.88% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.87% | `python` | `subtype_dealloc` | memory |
| 0.83% | `python` | `type_new` | memory |
| 0.80% | `python` | `PyLong_FromLong` | int |
| 0.73% | `python` | `long_dealloc` | memory |
| 0.70% | `python` | `PyObject_GC_Del` | gc |
| 0.67% | `python` | `binary_op1` | unknown |
| 0.62% | `python` | `list_dealloc` | memory |

## gc_collect

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 17.99% | `python` | `gc_collect_region.isra.0` | gc |
| 14.47% | `python` | `visit_reachable` | gc |
| 13.25% | `python` | `visit_decref` | gc |
| 12.83% | `python` | `deduce_unreachable` | gc |
| 6.82% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.77% | `python` | `_PyGC_Collect` | gc |
| 4.58% | `python` | `dict_traverse` | gc |
| 2.64% | `python` | `subtype_traverse` | gc |
| 1.69% | `python` | `func_traverse` | gc |
| 1.35% | `python` | `set_traverse` | gc |
| 0.95% | `[JIT]` | `jit` | jit |
| 0.85% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.84% | `python` | `PyType_GenericAlloc` | memory |
| 0.79% | `python` | `tupletraverse` | tuple |
| 0.69% | `python` | `type_traverse` | gc |
| 0.65% | `python` | `list_traverse` | gc |
| 0.62% | `python` | `type_new` | memory |
| 0.60% | `libc-2.31.so` | `__nss_database_lookup` | libc |

## gc_traversal

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 30.95% | `python` | `visit_reachable` | gc |
| 20.63% | `python` | `visit_decref` | gc |
| 13.69% | `python` | `list_traverse` | gc |
| 7.47% | `python` | `gc_collect_region.isra.0` | gc |
| 5.08% | `python` | `deduce_unreachable` | gc |
| 2.51% | `[JIT]` | `jit` | jit |
| 2.31% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.12% | `python` | `dict_traverse` | gc |
| 0.76% | `python` | `func_traverse` | gc |
| 0.66% | `python` | `set_traverse` | gc |
| 0.66% | `python` | `subtype_traverse` | gc |
| 0.54% | `python` | `PyLong_FromLong` | int |
| 0.53% | `python` | `type_new` | memory |

## generators

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 52.40% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.99% | `python` | `gen_dealloc` | memory |
| 2.38% | `python` | `_PyLong_Add` | int |
| 2.23% | `python` | `make_gen` | unknown |
| 1.69% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.59% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.51% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.47% | `python` | `deduce_unreachable` | gc |
| 1.39% | `python` | `long_dealloc` | memory |
| 1.16% | `python` | `range_subscript` | unknown |
| 1.09% | `python` | `visit_decref` | gc |
| 0.93% | `python` | `subtype_dealloc` | memory |
| 0.92% | `python` | `PyType_GenericAlloc` | memory |
| 0.88% | `python` | `subtype_traverse` | gc |
| 0.87% | `python` | `visit_reachable` | gc |
| 0.79% | `python` | `make_range_object` | unknown |
| 0.74% | `python` | `type_new` | memory |
| 0.74% | `python` | `gc_collect_region.isra.0` | gc |
| 0.73% | `python` | `_PyObject_Malloc` | memory |
| 0.61% | `python` | `slot_tp_iter` | unknown |
| 0.54% | `python` | `visit_add_to_container` | gc |
| 0.53% | `python` | `range_dealloc` | memory |

## genshi

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 46.38% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.98% | `[JIT]` | `jit` | jit |
| 1.86% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.68% | `python` | `insertdict` | dict |
| 1.51% | `python` | `tupledealloc` | memory |
| 1.31% | `python` | `insert_to_emptydict` | dict |
| 1.30% | `python` | `PyObject_Str` | dynamic |
| 1.24% | `python` | `_PyObject_GC_New` | gc |
| 1.17% | `python` | `PyObject_GC_Del` | gc |
| 1.16% | `python` | `dict_dealloc` | memory |
| 1.08% | `python` | `dictresize` | dict |
| 1.07% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.00% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.92% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.84% | `python` | `type_new` | memory |
| 0.83% | `python` | `method_dealloc` | memory |
| 0.82% | `python` | `_Py_type_getattro` | lookup |
| 0.79% | `python` | `PyDict_GetItemRef` | dict |
| 0.70% | `python` | `cm_descr_get` | unknown |
| 0.66% | `python` | `PyDict_SetItem` | dict |
| 0.65% | `python` | `_PyDict_FromItems` | dict |
| 0.65% | `python` | `dict_get` | dict |
| 0.58% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.57% | `python` | `deduce_unreachable` | gc |
| 0.56% | `python` | `PyObject_IsTrue` | dynamic |

## go

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 47.15% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 17.51% | `[JIT]` | `jit` | jit |
| 3.37% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.22% | `python` | `_PyObject_GetMethod` | dynamic |
| 1.53% | `python` | `PyDict_GetItemRef` | dict |
| 1.12% | `python` | `long_dealloc` | memory |
| 1.06% | `python` | `PyDict_SetItem` | dict |
| 1.05% | `python` | `long_bitwise` | int |
| 0.95% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.85% | `python` | `type_new` | memory |
| 0.72% | `python` | `_PyLong_Add` | int |
| 0.63% | `python` | `deduce_unreachable` | gc |
| 0.58% | `python` | `PyObject_GC_Del` | gc |
| 0.56% | `python` | `gc_collect_region.isra.0` | gc |
| 0.54% | `python` | `list_iter` | list |
| 0.51% | `python` | `visit_decref` | gc |

## gunicorn

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 28.24% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.46% | `[JIT]` | `jit` | jit |
| 2.43% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.39% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.50% | `python` | `type_new` | memory |
| 1.45% | `python` | `tupledealloc` | memory |
| 1.20% | `python` | `deduce_unreachable` | gc |
| 1.03% | `python` | `PyDict_GetItemRef` | dict |
| 0.98% | `python` | `gc_collect_region.isra.0` | gc |
| 0.98% | `python` | `visit_decref` | gc |
| 0.81% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.78% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.75% | `python` | `subtype_dealloc` | memory |
| 0.71% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.65% | `python` | `visit_reachable` | gc |
| 0.64% | `python` | `unicode_dealloc` | memory |
| 0.63% | `python` | `_PyCode_New` | memory |
| 0.62% | `python` | `_PySuper_Lookup` | dynamic |
| 0.62% | `python` | `dict_dealloc` | memory |
| 0.61% | `python` | `r_object` | import |
| 0.59% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.58% | `python` | `find_name_in_mro` | lookup |
| 0.56% | `python` | `list_dealloc` | memory |
| 0.56% | `python` | `sre_ucs1_match` | library |
| 0.55% | `python` | `slot_tp_init` | unknown |
| 0.50% | `python` | `_PyObject_MakeTpCall` | dynamic |

## hexiom

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 34.55% | `[JIT]` | `jit` | jit |
| 19.77% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.03% | `python` | `list_contains` | list |
| 2.81% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.78% | `python` | `builtin_sum` | unknown |
| 1.76% | `python` | `long_richcompare` | int |
| 1.28% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.15% | `python` | `slot_mp_subscript` | unknown |
| 1.06% | `python` | `type_new` | memory |
| 0.91% | `python` | `gen_iternext` | unknown |
| 0.79% | `python` | `PyObject_Size` | dynamic |
| 0.76% | `python` | `list_dealloc` | memory |
| 0.76% | `python` | `deduce_unreachable` | gc |
| 0.74% | `python` | `PyLong_FromLong` | int |
| 0.68% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.62% | `python` | `gc_collect_region.isra.0` | gc |
| 0.57% | `python` | `visit_decref` | gc |
| 0.55% | `python` | `PyLong_FromSsize_t` | int |

## html5lib

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 34.77% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.11% | `python` | `sre_ucs2_charset.isra.0` | library |
| 3.31% | `[JIT]` | `jit` | jit |
| 2.02% | `python` | `deduce_unreachable` | gc |
| 1.78% | `python` | `PyDict_GetItemRef` | dict |
| 1.74% | `python` | `gc_collect_region.isra.0` | gc |
| 1.73% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.58% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.44% | `python` | `visit_decref` | gc |
| 1.13% | `python` | `type_new` | memory |
| 0.78% | `python` | `sre_ucs1_count` | library |
| 0.75% | `python` | `visit_reachable` | gc |
| 0.75% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.74% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.67% | `python` | `insertdict` | dict |
| 0.67% | `python` | `tupledealloc` | memory |
| 0.64% | `python` | `_sre_SRE_Pattern_match` | library |
| 0.61% | `python` | `list_dealloc` | memory |
| 0.60% | `python` | `unicode_dealloc` | memory |
| 0.57% | `python` | `long_dealloc` | memory |
| 0.57% | `python` | `_PyCode_New` | memory |
| 0.54% | `python` | `visit_add_to_container` | gc |
| 0.52% | `python` | `dict_dealloc` | memory |
| 0.52% | `python` | `list_contains` | list |
| 0.51% | `python` | `set_contains_lock_held` | miscobj |

## json

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 19.78% | `_json.cpython-313-x86_64-linux-gnu.so` | `_parse_object_unicode` | library |
| 7.77% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.87% | `python` | `PyUnicode_Substring` | str |
| 5.51% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 5.23% | `python` | `siphash13` | str |
| 4.84% | `python` | `PyDict_SetItem` | dict |
| 3.68% | `python` | `unicode_dealloc` | memory |
| 3.11% | `python` | `PyLong_FromString` | int |
| 2.99% | `python` | `dictresize` | dict |
| 2.25% | `python` | `dict_dealloc` | memory |
| 2.23% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.17% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 2.00% | `python` | `_sre_SRE_Pattern_match` | library |
| 1.43% | `_json.cpython-313-x86_64-linux-gnu.so` | `_match_number_unicode.isra.0` | library |
| 1.22% | `python` | `PyBytes_FromStringAndSize` | str |
| 0.99% | `[JIT]` | `jit` | jit |
| 0.96% | `python` | `PyObject_Free` | dynamic |
| 0.81% | `python` | `PyDict_GetItemRef` | dict |
| 0.75% | `python` | `type_new` | memory |
| 0.72% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.70% | `python` | `insert_to_emptydict` | dict |
| 0.67% | `python` | `tupledealloc` | memory |
| 0.60% | `python` | `deduce_unreachable` | gc |
| 0.60% | `python` | `long_dealloc` | memory |
| 0.59% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.54% | `python` | `sre_ucs1_match` | library |
| 0.51% | `libc-2.31.so` | `malloc` | libc |

## json_dumps

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 14.74% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.78% | `_json.cpython-313-x86_64-linux-gnu.so` | `encoder_encode_key_value` | library |
| 6.48% | `python` | `PyUnicode_New` | memory |
| 5.12% | `python` | `_PyUnicodeWriter_WriteStr` | str |
| 4.63% | `python` | `unicode_dealloc` | memory |
| 3.34% | `python` | `_PyUnicodeWriter_PrepareInternal` | str |
| 3.01% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.81% | `_json.cpython-313-x86_64-linux-gnu.so` | `py_encode_basestring_ascii` | library |
| 2.47% | `python` | `vgetargskeywords.constprop.0` | calls |
| 2.31% | `python` | `PyDict_GetItemRef` | dict |
| 1.62% | `python` | `resize_compact` | str |
| 1.61% | `python` | `long_to_decimal_string` | int |
| 1.55% | `python` | `tupledealloc` | memory |
| 1.37% | `python` | `_PyObject_Malloc` | memory |
| 1.31% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 1.29% | `python` | `PyDict_Next` | dict |
| 1.19% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.17% | `python` | `PyDict_SetItem` | dict |
| 0.92% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.91% | `[JIT]` | `jit` | jit |
| 0.80% | `python` | `_PyLong_New` | memory |
| 0.78% | `python` | `type_new` | memory |
| 0.77% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.73% | `python` | `long_hash` | int |
| 0.67% | `python` | `PyTuple_New` | memory |
| 0.67% | `python` | `func_dealloc` | memory |
| 0.66% | `python` | `dict_dealloc` | memory |
| 0.64% | `python` | `PyDict_DelItem` | dict |
| 0.64% | `python` | `deduce_unreachable` | gc |
| 0.64% | `python` | `long_dealloc` | memory |
| 0.60% | `python` | `_Py_dict_lookup` | lookup |
| 0.59% | `python` | `_Py_type_getattro` | lookup |
| 0.59% | `_json.cpython-313-x86_64-linux-gnu.so` | `encoder_listencode_obj` | library |
| 0.57% | `python` | `PyMem_Free` | memory |
| 0.55% | `python` | `PyDict_Contains` | dict |
| 0.52% | `python` | `PyObject_GetOptionalAttr` | dynamic |

## json_loads

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 20.93% | `_json.cpython-313-x86_64-linux-gnu.so` | `_parse_object_unicode` | library |
| 10.94% | `python` | `PyUnicode_Substring` | str |
| 6.40% | `python` | `siphash13` | str |
| 6.26% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.59% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 4.54% | `python` | `PyDict_SetItem` | dict |
| 4.32% | `python` | `unicode_dealloc` | memory |
| 3.18% | `python` | `PyLong_FromString` | int |
| 2.41% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.95% | `python` | `dictresize` | dict |
| 1.34% | `python` | `dict_dealloc` | memory |
| 1.29% | `_json.cpython-313-x86_64-linux-gnu.so` | `_match_number_unicode.isra.0` | library |
| 1.23% | `python` | `PyBytes_FromStringAndSize` | str |
| 1.10% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.99% | `python` | `_sre_SRE_Pattern_match` | library |
| 0.93% | `_json.cpython-313-x86_64-linux-gnu.so` | `_parse_array_unicode` | library |
| 0.89% | `python` | `PyObject_Free` | dynamic |
| 0.85% | `python` | `type_new` | memory |
| 0.66% | `python` | `deduce_unreachable` | gc |
| 0.59% | `python` | `unicode_hash` | str |
| 0.56% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.55% | `[JIT]` | `jit` | jit |
| 0.52% | `python` | `long_dealloc` | memory |
| 0.52% | `python` | `tupledealloc` | memory |
| 0.51% | `python` | `visit_decref` | gc |
| 0.50% | `python` | `gc_collect_region.isra.0` | gc |

## logging

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 45.54% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.25% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 3.16% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 2.89% | `[JIT]` | `jit` | jit |
| 2.20% | `python` | `PyDict_GetItemRef` | dict |
| 1.94% | `python` | `dict_dealloc` | memory |
| 1.81% | `python` | `PyCode_Addr2Line` | exceptions |
| 1.60% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.07% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.70% | `python` | `type_new` | memory |
| 0.69% | `python` | `meth_dealloc` | memory |
| 0.66% | `python` | `tupledealloc` | memory |
| 0.66% | `python` | `unicode_subscript` | str |
| 0.60% | `python` | `_PyObject_LookupSpecial` | dynamic |
| 0.59% | `python` | `unicode_dealloc` | memory |
| 0.57% | `python` | `method_get` | dynamic |
| 0.52% | `python` | `long_dealloc` | memory |
| 0.52% | `python` | `slot_tp_init` | unknown |

## mako

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.57% | `[JIT]` | `jit` | jit |
| 9.00% | `python` | `PyObject_Str` | dynamic |
| 8.50% | `python` | `unicode_replace` | str |
| 4.45% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.30% | `python` | `_PyUnicode_JoinArray` | str |
| 2.51% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.28% | `python` | `unicode_dealloc` | memory |
| 1.78% | `python` | `dequeiter_next_lock_held.isra.0` | miscobj |
| 1.62% | `python` | `deque_append_lock_held` | miscobj |
| 1.31% | `python` | `list_dealloc` | memory |
| 1.27% | `python` | `_list_extend` | unknown |
| 1.26% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.00% | `python` | `sre_ucs2_charset.isra.0` | library |
| 0.91% | `python` | `type_new` | memory |
| 0.82% | `python` | `deque_clear` | miscobj |
| 0.81% | `python` | `deque_append_impl` | miscobj |
| 0.76% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.73% | `python` | `deduce_unreachable` | gc |
| 0.68% | `python` | `PyLong_FromLong` | int |
| 0.56% | `python` | `visit_decref` | gc |
| 0.53% | `[kernel.kallsyms]` | `native_irq_return_iret` | kernel |
| 0.51% | `python` | `gc_collect_region.isra.0` | gc |

## mdp

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 36.53% | `python` | `tuplehash` | tuple |
| 13.18% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 12.46% | `python` | `long_hash` | int |
| 7.08% | `[JIT]` | `jit` | jit |
| 5.66% | `python` | `dict_subscript` | dict |
| 2.93% | `python` | `tuplerichcompare` | tuple |
| 1.29% | `python` | `insertdict` | dict |
| 1.19% | `python` | `_PyLong_GCD` | int |
| 1.11% | `python` | `PyDict_GetItemRef` | dict |
| 1.07% | `python` | `_PySuper_Lookup` | dynamic |
| 0.92% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.82% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.72% | `python` | `builtin_sum` | unknown |
| 0.62% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.60% | `python` | `func_dealloc` | memory |
| 0.52% | `python` | `_PySet_Contains` | unknown |

## meteor_contest

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 13.49% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 11.79% | `[JIT]` | `jit` | jit |
| 7.94% | `python` | `set_issubset_impl` | miscobj |
| 5.85% | `python` | `setiter_iternext` | miscobj |
| 5.05% | `python` | `set_lookkey` | miscobj |
| 4.91% | `python` | `set_difference` | miscobj |
| 4.03% | `python` | `set_dealloc` | memory |
| 3.12% | `python` | `builtin_min` | unknown |
| 2.24% | `python` | `list_dealloc` | memory |
| 1.85% | `python` | `set_add_entry` | miscobj |
| 1.60% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.32% | `python` | `list_subscript` | list |
| 1.32% | `python` | `PyObject_GC_Del` | gc |
| 1.15% | `python` | `long_richcompare` | int |
| 1.15% | `python` | `set_table_resize` | miscobj |
| 1.07% | `python` | `type_new` | memory |
| 1.05% | `python` | `PyObject_RichCompare` | dynamic |
| 1.04% | `python` | `make_new_set` | memory |
| 0.93% | `python` | `set_intersection` | miscobj |
| 0.86% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.74% | `python` | `PyIter_Next` | dynamic |
| 0.71% | `python` | `deduce_unreachable` | gc |
| 0.68% | `python` | `_PyObject_GC_New` | gc |
| 0.63% | `python` | `visit_decref` | gc |
| 0.62% | `python` | `gc_collect_region.isra.0` | gc |
| 0.61% | `python` | `list_iter` | list |
| 0.55% | `python` | `_PyCode_New` | memory |
| 0.55% | `python` | `set_merge_lock_held.part.0` | miscobj |

## mypy2

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 28.72% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.84% | `python` | `gc_collect_region.isra.0` | gc |
| 7.07% | `python` | `deduce_unreachable` | gc |
| 4.14% | `[JIT]` | `jit` | jit |
| 2.76% | `python` | `visit_decref` | gc |
| 2.62% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.55% | `python` | `subtype_traverse` | gc |
| 1.55% | `python` | `PyDict_GetItemRef` | dict |
| 1.46% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.38% | `python` | `visit_reachable` | gc |
| 1.21% | `python` | `_PySuper_Lookup` | dynamic |
| 1.21% | `python` | `object_isinstance` | dynamic |
| 1.19% | `_json.cpython-313-x86_64-linux-gnu.so` | `_parse_object_unicode` | library |
| 1.08% | `python` | `list_dealloc` | memory |
| 0.93% | `python` | `PyUnicode_Substring` | str |
| 0.91% | `python` | `clear_slots` | unknown |
| 0.90% | `python` | `subtype_dealloc` | memory |
| 0.87% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.86% | `python` | `siphash13` | str |
| 0.82% | `python` | `tupledealloc` | memory |
| 0.81% | `python` | `dict_dealloc` | memory |
| 0.78% | `python` | `slot_tp_init` | unknown |
| 0.77% | `python` | `PyObject_SetAttr` | dynamic |
| 0.77% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.76% | `python` | `PyObject_GC_Del` | gc |
| 0.67% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.66% | `python` | `unicode_dealloc` | memory |
| 0.62% | `python` | `object_new` | memory |
| 0.61% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.59% | `python` | `PyDict_SetItem` | dict |
| 0.56% | `python` | `list_traverse` | gc |
| 0.56% | `python` | `_PyGC_Collect` | gc |

## nbody

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 61.33% | `[JIT]` | `jit` | jit |
| 6.29% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.61% | `libm-2.31.so` | `f64xsubf128` | library |
| 4.57% | `python` | `PyFloat_FromDouble` | float |
| 2.22% | `python` | `float_dealloc` | memory |
| 1.27% | `python` | `_Py_Dealloc` | memory |
| 1.24% | `python` | `float_pow` | float |
| 0.73% | `python` | `type_new` | memory |
| 0.53% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.52% | `python` | `deduce_unreachable` | gc |

## nqueens

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 22.99% | `[JIT]` | `jit` | jit |
| 19.46% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.61% | `python` | `set_vectorcall` | miscobj |
| 2.76% | `python` | `list_dealloc` | memory |
| 2.55% | `python` | `PyFunction_NewWithQualName` | memory |
| 2.18% | `python` | `gen_iternext` | unknown |
| 1.98% | `python` | `set_dealloc` | memory |
| 1.76% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.73% | `python` | `func_dealloc` | memory |
| 1.48% | `python` | `list_subscript` | list |
| 1.30% | `python` | `_PyLong_Add` | int |
| 1.24% | `python` | `PyList_New` | memory |
| 1.20% | `python` | `_PyBuildSlice_ConsumeRefs` | miscobj |
| 1.20% | `python` | `make_gen` | unknown |
| 1.18% | `python` | `tupledealloc` | memory |
| 1.13% | `python` | `gen_dealloc` | memory |
| 0.93% | `python` | `list_ass_slice_lock_held` | list |
| 0.88% | `python` | `PyMem_Malloc` | memory |
| 0.74% | `python` | `PyLong_FromLong` | int |
| 0.70% | `python` | `type_new` | memory |
| 0.70% | `python` | `slice_dealloc` | memory |
| 0.66% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 0.64% | `python` | `PyObject_Free` | dynamic |
| 0.58% | `python` | `list_ass_subscript` | list |
| 0.57% | `python` | `method_get` | dynamic |
| 0.57% | `python` | `PySequence_Tuple` | dynamic |
| 0.53% | `python` | `deduce_unreachable` | gc |
| 0.53% | `python` | `meth_dealloc` | memory |
| 0.50% | `python` | `_PyEval_FrameClearAndPop` | interpreter |

## pathlib

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 15.05% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.20% | `[JIT]` | `jit` | jit |
| 2.19% | `python` | `long_dealloc` | memory |
| 1.58% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.39% | `[kernel.kallsyms]` | `__d_lookup_rcu` | kernel |
| 1.31% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.26% | `libpthread-2.31.so` | `__pthread_mutex_lock` | library |
| 1.23% | `python` | `_PySuper_Lookup` | dynamic |
| 1.18% | `python` | `k_mul` | int |
| 1.13% | `[kernel.kallsyms]` | `ext4_htree_store_dirent` | kernel |
| 1.13% | `libpthread-2.31.so` | `pthread_mutex_unlock` | library |
| 1.10% | `[kernel.kallsyms]` | `__ext4fs_dirhash` | kernel |
| 1.05% | `[kernel.kallsyms]` | `memset_erms` | kernel |
| 0.99% | `python` | `path_converter` | unknown |
| 0.96% | `python` | `_PyLong_New` | memory |
| 0.94% | `python` | `tupledealloc` | memory |
| 0.91% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.90% | `python` | `PyLong_FromLong` | int |
| 0.89% | `python` | `ScandirIterator_iternext` | unknown |
| 0.88% | `python` | `PyUnicode_FSConverter` | str |
| 0.82% | `python` | `type_new` | memory |
| 0.79% | `python` | `unicode_decode_utf8` | str |
| 0.79% | `[kernel.kallsyms]` | `filldir64` | kernel |
| 0.72% | `python` | `_sre_SRE_Pattern_match` | library |
| 0.72% | `python` | `_Py_type_getattro` | lookup |
| 0.70% | `python` | `PyEval_RestoreThread` | interpreter |
| 0.69% | `python` | `PyObject_GC_Del` | gc |
| 0.68% | `python` | `list_dealloc` | memory |
| 0.67% | `python` | `tp_new_wrapper` | memory |
| 0.67% | `python` | `x_add` | int |
| 0.66% | `python` | `vectorcall_method` | calls |
| 0.65% | `python` | `PyUnicode_DecodeFSDefault` | str |
| 0.63% | `python` | `deduce_unreachable` | gc |
| 0.62% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.62% | `python` | `slot_tp_init` | unknown |
| 0.61% | `[kernel.kallsyms]` | `link_path_walk.part.0` | kernel |
| 0.61% | `python` | `_Py_dict_lookup` | lookup |
| 0.61% | `[kernel.kallsyms]` | `strncpy_from_user` | kernel |
| 0.60% | `python` | `unicode_dealloc` | memory |
| 0.59% | `python` | `sre_ucs1_match` | library |
| 0.59% | `python` | `method_dealloc` | memory |
| 0.58% | `[kernel.kallsyms]` | `kmem_cache_alloc` | kernel |
| 0.56% | `python` | `_PyUnicode_JoinArray` | str |
| 0.56% | `python` | `get_type_attr_as_size` | unknown |
| 0.54% | `python` | `clear_slots` | unknown |
| 0.54% | `python` | `object_isinstance` | dynamic |
| 0.52% | `python` | `visit_decref` | gc |
| 0.51% | `[kernel.kallsyms]` | `__virt_addr_valid` | kernel |
| 0.50% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 0.50% | `python` | `method_vectorcall` | unknown |

## pickle

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.97% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `save` | library |
| 12.44% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_put.isra.0` | library |
| 6.95% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_write_bytes` | library |
| 4.27% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 4.21% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.70% | `python` | `PyDict_Next` | dict |
| 2.68% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pickler_dealloc` | library |
| 2.48% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_get.isra.0` | library |
| 1.81% | `python` | `PyUnicode_AsUTF8AndSize` | str |
| 1.68% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.49% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write` | library |
| 1.02% | `[JIT]` | `jit` | jit |
| 0.91% | `python` | `type_new` | memory |
| 0.64% | `python` | `deduce_unreachable` | gc |
| 0.62% | `python` | `find_name_in_mro` | lookup |
| 0.60% | `python` | `meth_dealloc` | memory |
| 0.59% | `python` | `visit_decref` | gc |
| 0.58% | `python` | `gc_collect_region.isra.0` | gc |
| 0.58% | `python` | `PyMem_Malloc` | memory |
| 0.55% | `python` | `tupledealloc` | memory |
| 0.55% | `python` | `PyDict_GetItemRef` | dict |
| 0.54% | `python` | `unicode_decode_utf8` | str |
| 0.53% | `python` | `PyMem_Free` | memory |
| 0.52% | `python` | `_PyCode_New` | memory |
| 0.51% | `python` | `dict_setdefault_ref_lock_held` | dict |

## pickle_dict

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 46.00% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `save` | library |
| 12.71% | `python` | `PyDict_Next` | dict |
| 10.83% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write` | library |
| 3.15% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.95% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_put.isra.0` | library |
| 2.89% | `python` | `PyLong_AsLongAndOverflow` | int |
| 1.11% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.72% | `python` | `type_new` | memory |
| 0.71% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pickler_dealloc` | library |
| 0.67% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005cd4` | library |
| 0.67% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005e54` | library |
| 0.55% | `python` | `deduce_unreachable` | gc |
| 0.54% | `[JIT]` | `jit` | jit |
| 0.51% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |

## pickle_list

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 42.62% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `save` | library |
| 11.19% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write` | library |
| 4.83% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_put.isra.0` | library |
| 4.66% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.58% | `python` | `PyLong_AsLongAndOverflow` | int |
| 2.00% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.13% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pickler_dealloc` | library |
| 1.10% | `python` | `type_new` | memory |
| 0.99% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.96% | `[JIT]` | `jit` | jit |
| 0.74% | `python` | `deduce_unreachable` | gc |
| 0.73% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005cd4` | library |
| 0.66% | `python` | `gc_collect_region.isra.0` | gc |
| 0.65% | `python` | `visit_decref` | gc |
| 0.64% | `python` | `PyList_Size` | list |
| 0.53% | `python` | `_PyCode_New` | memory |

## pickle_pure_python

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 47.20% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.63% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.34% | `python` | `dict_get` | dict |
| 2.27% | `python` | `bytes_concat` | str |
| 2.19% | `python` | `unicode_encode` | str |
| 2.02% | `python` | `PyObject_Free` | dynamic |
| 1.85% | `python` | `_PyLong_New` | memory |
| 1.81% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.59% | `[JIT]` | `jit` | jit |
| 1.52% | `python` | `long_dealloc` | memory |
| 1.42% | `python` | `insertdict` | dict |
| 1.29% | `python` | `PyDict_GetItemRef` | dict |
| 1.03% | `python` | `write_bytes` | unknown |
| 1.03% | `python` | `tupledealloc` | memory |
| 1.02% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.93% | `python` | `unicode_encode_utf8` | str |
| 0.91% | `python` | `PyType_GetModuleByDef` | dynamic |
| 0.80% | `python` | `PyDict_Contains` | dict |
| 0.74% | `python` | `long_hash` | int |
| 0.71% | `python` | `type_new` | memory |
| 0.66% | `python` | `PySys_Audit` | unknown |
| 0.57% | `python` | `builtin_id` | unknown |
| 0.50% | `_struct.cpython-313-x86_64-linux-gnu.so` | `s_pack` | library |

## pidigits

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.16% | `python` | `x_divrem` | int |
| 19.40% | `python` | `k_mul` | int |
| 15.44% | `python` | `x_add` | int |
| 7.71% | `python` | `x_sub` | int |
| 3.00% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.43% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.82% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.68% | `[JIT]` | `jit` | jit |
| 0.72% | `python` | `type_new` | memory |

## pprint

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.20% | `[JIT]` | `jit` | jit |
| 20.04% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.26% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 3.12% | `python` | `long_to_decimal_string` | int |
| 2.90% | `python` | `_Py_type_getattro_impl` | dynamic |
| 2.50% | `python` | `tupledealloc` | memory |
| 2.36% | `python` | `_Py_type_getattro` | lookup |
| 2.17% | `python` | `_PyUnicode_JoinArray` | str |
| 2.15% | `python` | `PyUnicode_Format` | str |
| 1.71% | `python` | `unicode_dealloc` | memory |
| 1.54% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.14% | `python` | `meth_dealloc` | memory |
| 1.12% | `python` | `_PyUnicodeWriter_PrepareInternal` | str |
| 1.03% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 1.02% | `python` | `_PyDict_SetItem_Take2` | dict |
| 1.01% | `python` | `_PySet_Contains` | unknown |
| 1.00% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.92% | `python` | `list_dealloc` | memory |
| 0.91% | `python` | `_PyObject_Malloc` | memory |
| 0.88% | `python` | `slot_tp_init` | unknown |
| 0.85% | `python` | `PyObject_GC_Del` | gc |
| 0.82% | `python` | `PyDict_Contains` | dict |
| 0.82% | `python` | `slot_tp_richcompare` | dynamic |
| 0.78% | `python` | `builtin_issubclass` | unknown |
| 0.76% | `python` | `object_new` | memory |
| 0.72% | `python` | `method_get` | dynamic |
| 0.67% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.66% | `python` | `_PyDict_LoadGlobal` | dict |
| 0.63% | `python` | `list_sort_impl` | list |
| 0.60% | `python` | `builtin_getattr` | lookup |
| 0.54% | `python` | `long_hash` | int |
| 0.54% | `python` | `_PyLong_New` | memory |

## pycparser

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 29.27% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 17.35% | `python` | `sre_ucs1_match` | library |
| 5.84% | `[JIT]` | `jit` | jit |
| 2.68% | `python` | `_sre_SRE_Pattern_match` | library |
| 2.58% | `python` | `PyDict_GetItemRef` | dict |
| 2.31% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 2.07% | `python` | `deduce_unreachable` | gc |
| 1.91% | `python` | `gc_collect_region.isra.0` | gc |
| 1.68% | `python` | `dict_get` | dict |
| 1.61% | `python` | `object_new` | memory |
| 1.43% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.15% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.07% | `python` | `list_ass_slice_lock_held` | list |
| 1.04% | `python` | `subtype_dealloc` | memory |
| 1.02% | `python` | `visit_decref` | gc |
| 0.96% | `python` | `subtype_traverse` | gc |
| 0.84% | `python` | `visit_add_to_container` | gc |
| 0.81% | `python` | `list_dealloc` | memory |
| 0.77% | `python` | `PyObject_GC_Del` | gc |
| 0.77% | `python` | `sre_ucs1_count` | library |
| 0.73% | `python` | `object_isinstance` | dynamic |
| 0.68% | `python` | `slot_mp_ass_subscript` | unknown |
| 0.59% | `python` | `PyDict_Contains` | dict |
| 0.56% | `python` | `visit_reachable` | gc |
| 0.54% | `python` | `sre_ucs2_charset.isra.0` | library |
| 0.50% | `python` | `list_subscript` | list |
| 0.50% | `python` | `PyObject_GenericGetAttr` | dynamic |

## pyflate

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 34.11% | `[JIT]` | `jit` | jit |
| 9.11% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.38% | `python` | `list_dealloc` | memory |
| 5.05% | `python` | `list_ass_slice_lock_held` | list |
| 2.68% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 2.56% | `python` | `long_dealloc` | memory |
| 2.45% | `python` | `bytes_subscript` | str |
| 2.42% | `python` | `list_subscript` | list |
| 2.05% | `python` | `_PyLong_Add` | int |
| 1.97% | `python` | `list_concat` | list |
| 1.80% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.67% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.27% | `python` | `_PyLong_Subtract` | int |
| 1.25% | `python` | `stringlib_bytes_join.lto_priv.1` | str |
| 1.21% | `python` | `long_lshift` | int |
| 1.08% | `python` | `PyObject_Free` | dynamic |
| 1.06% | `python` | `_PyLong_New` | memory |
| 0.91% | `python` | `PySlice_Unpack` | miscobj |
| 0.89% | `python` | `list_sort_impl` | list |
| 0.73% | `python` | `_PyObject_Malloc` | memory |
| 0.63% | `python` | `PyObject_GetItem` | dynamic |
| 0.63% | `python` | `unsafe_long_compare` | unknown |
| 0.61% | `python` | `long_rshift` | int |
| 0.56% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 0.53% | `python` | `long_and` | int |

## pylint

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.36% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.85% | `python` | `deduce_unreachable` | gc |
| 6.57% | `python` | `gc_collect_region.isra.0` | gc |
| 4.36% | `[JIT]` | `jit` | jit |
| 3.57% | `python` | `visit_decref` | gc |
| 2.82% | `python` | `visit_reachable` | gc |
| 1.76% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.62% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.54% | `python` | `PyDict_GetItemRef` | dict |
| 1.44% | `python` | `visit_add_to_container` | gc |
| 1.33% | `python` | `subtype_traverse` | gc |
| 1.29% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.88% | `python` | `tupledealloc` | memory |
| 0.88% | `python` | `dict_traverse` | gc |
| 0.84% | `python` | `object_isinstance` | dynamic |
| 0.82% | `python` | `find_name_in_mro` | lookup |
| 0.78% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.78% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.78% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.77% | `python` | `dict_dealloc` | memory |
| 0.76% | `python` | `list_traverse` | gc |
| 0.68% | `python` | `list_dealloc` | memory |
| 0.62% | `python` | `_PyLexer_update_fstring_expr` | unknown |
| 0.57% | `python` | `PyObject_SetAttr` | dynamic |
| 0.55% | `python` | `gen_dealloc` | memory |
| 0.54% | `python` | `PyObject_GC_Del` | gc |
| 0.51% | `python` | `type_new` | memory |
| 0.51% | `python` | `make_gen` | unknown |
| 0.51% | `python` | `subtype_dealloc` | memory |

## python_startup

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 7.99% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.27% | `python` | `type_new` | memory |
| 3.28% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.80% | `python` | `deduce_unreachable` | gc |
| 2.78% | `python` | `_PyCode_New` | memory |
| 2.75% | `python` | `visit_decref` | gc |
| 2.39% | `python` | `r_object` | import |
| 2.13% | `python` | `gc_collect_region.isra.0` | gc |
| 1.89% | `python` | `PyUnicode_FromKindAndData` | str |
| 1.88% | `python` | `visit_reachable` | gc |
| 1.67% | `ld-2.31.so` | `_dl_rtld_di_serinfo` | library |
| 1.56% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 1.42% | `python` | `siphash13` | str |
| 1.17% | `python` | `_Py_hashtable_get` | unknown |
| 1.04% | `python` | `unicode_decode_utf8` | str |
| 0.97% | `python` | `tupledealloc` | memory |
| 0.94% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.89% | `python` | `find_name_in_mro` | lookup |
| 0.85% | `python` | `dict_traverse` | gc |
| 0.85% | `[kernel.kallsyms]` | `native_irq_return_iret` | kernel |
| 0.83% | `python` | `type_ready` | dynamic |
| 0.81% | `python` | `PyDict_SetItem` | dict |
| 0.78% | `[kernel.kallsyms]` | `filemap_map_pages` | kernel |
| 0.70% | `python` | `dictresize` | dict |
| 0.66% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.64% | `[kernel.kallsyms]` | `sync_regs` | kernel |
| 0.63% | `python` | `insertdict` | dict |
| 0.62% | `python` | `unicode_dealloc` | memory |
| 0.58% | `python` | `PyDict_GetItemRef` | dict |
| 0.55% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.52% | `libc-2.31.so` | `wcsrtombs` | libc |
| 0.51% | `libc-2.31.so` | `__gconv_get_alias_db` | libc |

## python_startup_no_site

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 7.69% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.43% | `python` | `type_new` | memory |
| 3.34% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.76% | `python` | `visit_decref` | gc |
| 2.64% | `python` | `_PyCode_New` | memory |
| 2.58% | `python` | `deduce_unreachable` | gc |
| 2.36% | `ld-2.31.so` | `_dl_rtld_di_serinfo` | library |
| 2.31% | `python` | `gc_collect_region.isra.0` | gc |
| 2.24% | `python` | `r_object` | import |
| 1.84% | `python` | `visit_reachable` | gc |
| 1.66% | `python` | `PyUnicode_FromKindAndData` | str |
| 1.57% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 1.40% | `python` | `siphash13` | str |
| 1.35% | `python` | `unicode_decode_utf8` | str |
| 1.14% | `python` | `_Py_hashtable_get` | unknown |
| 1.02% | `[kernel.kallsyms]` | `native_irq_return_iret` | kernel |
| 0.96% | `[kernel.kallsyms]` | `filemap_map_pages` | kernel |
| 0.94% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.94% | `python` | `type_ready` | dynamic |
| 0.92% | `python` | `tupledealloc` | memory |
| 0.86% | `python` | `dict_traverse` | gc |
| 0.80% | `[kernel.kallsyms]` | `sync_regs` | kernel |
| 0.77% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.77% | `python` | `insertdict` | dict |
| 0.74% | `python` | `PyDict_SetItem` | dict |
| 0.73% | `python` | `find_name_in_mro` | lookup |
| 0.71% | `libc-2.31.so` | `wcsrtombs` | libc |
| 0.63% | `python` | `unicode_dealloc` | memory |
| 0.60% | `python` | `dictresize` | dict |
| 0.58% | `libc-2.31.so` | `__gconv_get_alias_db` | libc |
| 0.54% | `python` | `PyDict_GetItemRef` | dict |
| 0.54% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.52% | `[kernel.kallsyms]` | `zap_pte_range.isra.0` | kernel |
| 0.50% | `[kernel.kallsyms]` | `perf_iterate_ctx` | kernel |

## raytrace

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 47.75% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 11.17% | `[JIT]` | `jit` | jit |
| 5.83% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.64% | `python` | `subtype_dealloc` | memory |
| 2.00% | `python` | `PyType_GenericAlloc` | memory |
| 1.99% | `python` | `PyObject_GC_Del` | gc |
| 1.53% | `python` | `vectorcall_maybe.constprop.0` | unknown |
| 1.44% | `python` | `PyFloat_FromDouble` | float |
| 1.11% | `python` | `float_dealloc` | memory |
| 1.00% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.84% | `python` | `PyNumber_Subtract` | dynamic |
| 0.81% | `python` | `float_sub` | float |
| 0.76% | `python` | `float_mul` | float |
| 0.67% | `python` | `tupledealloc` | memory |
| 0.59% | `python` | `convert_to_double` | unknown |
| 0.56% | `python` | `long_dealloc` | memory |
| 0.52% | `python` | `type_new` | memory |
| 0.51% | `python` | `float_richcompare` | float |
| 0.50% | `python` | `_PyFloat_ExactDealloc` | memory |

## regex_compile

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 28.60% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 14.63% | `[JIT]` | `jit` | jit |
| 4.12% | `python` | `sre_ucs1_match` | library |
| 2.59% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.52% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 1.51% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.15% | `python` | `PyLong_FromLong` | int |
| 1.09% | `python` | `tupledealloc` | memory |
| 1.09% | `python` | `long_dealloc` | memory |
| 0.96% | `python` | `object_isinstance` | dynamic |
| 0.93% | `python` | `list_dealloc` | memory |
| 0.89% | `python` | `sre_ucs2_charset.isra.0` | library |
| 0.87% | `python` | `bytearray_ass_subscript` | miscobj |
| 0.77% | `python` | `type_new` | memory |
| 0.75% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.63% | `python` | `deduce_unreachable` | gc |
| 0.59% | `python` | `_PyObject_Malloc` | memory |
| 0.55% | `python` | `slot_mp_subscript` | unknown |
| 0.51% | `python` | `sre_search` | library |
| 0.50% | `python` | `visit_decref` | gc |
| 0.50% | `python` | `PyMem_Free` | memory |

## regex_dna

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 33.70% | `python` | `sre_ucs1_match` | library |
| 27.75% | `python` | `sre_ucs2_charset.isra.0` | library |
| 6.73% | `python` | `sre_search` | library |
| 4.35% | `[JIT]` | `jit` | jit |
| 3.13% | `libm-2.31.so` | `__fmod_finite` | library |
| 2.53% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 1.14% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.11% | `_bisect.cpython-313-x86_64-linux-gnu.so` | `_bisect_bisect_right` | library |
| 0.87% | `python` | `float_richcompare` | float |
| 0.84% | `python` | `pattern_subx` | library |
| 0.59% | `python` | `stringlib_bytes_join.lto_priv.1` | str |
| 0.56% | `python` | `PyFloat_FromDouble` | float |
| 0.54% | `python` | `type_new` | memory |

## regex_effbot

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 39.38% | `python` | `sre_ucs1_match` | library |
| 15.34% | `python` | `sre_ucs2_charset.isra.0` | library |
| 7.08% | `python` | `PyMem_Malloc` | memory |
| 5.49% | `python` | `sre_search` | library |
| 5.34% | `python` | `PyMem_Free` | memory |
| 4.39% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 1.83% | `python` | `sre_ucs1_count` | library |
| 0.80% | `python` | `type_new` | memory |
| 0.63% | `[JIT]` | `jit` | jit |
| 0.63% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.60% | `python` | `deduce_unreachable` | gc |
| 0.52% | `python` | `visit_decref` | gc |

## regex_v8

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 33.20% | `python` | `sre_ucs1_match` | library |
| 8.07% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.00% | `python` | `sre_ucs1_count` | library |
| 3.48% | `python` | `sre_search` | library |
| 3.41% | `python` | `PyCode_Addr2Line` | exceptions |
| 2.41% | `[JIT]` | `jit` | jit |
| 1.81% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.43% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.20% | `python` | `pattern_subx` | library |
| 1.06% | `python` | `state_init` | unknown |
| 1.03% | `python` | `type_new` | memory |
| 1.01% | `python` | `PyMem_Free` | memory |
| 0.92% | `python` | `sre_ucs1_match.cold` | library |
| 0.82% | `python` | `deduce_unreachable` | gc |
| 0.77% | `python` | `PyDict_GetItemRef` | dict |
| 0.66% | `python` | `visit_decref` | gc |
| 0.66% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.65% | `python` | `gc_collect_region.isra.0` | gc |
| 0.63% | `python` | `list_dealloc` | memory |
| 0.61% | `python` | `PyUnicode_Substring` | str |
| 0.59% | `python` | `PyLong_FromLong` | int |
| 0.58% | `python` | `PyMem_Malloc` | memory |
| 0.56% | `python` | `long_dealloc` | memory |
| 0.55% | `libc-2.31.so` | `malloc` | libc |
| 0.54% | `python` | `_PyUnicode_JoinArray` | str |
| 0.53% | `python` | `_PyObject_Malloc` | memory |
| 0.52% | `python` | `tupledealloc` | memory |
| 0.51% | `python` | `unicode_dealloc` | memory |

## richards

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 43.80% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 19.66% | `[JIT]` | `jit` | jit |
| 4.90% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 3.99% | `python` | `_PyObject_GetMethod` | dynamic |
| 2.98% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.56% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.24% | `python` | `PyObject_GetAttr` | dynamic |
| 1.15% | `python` | `long_dealloc` | memory |
| 0.91% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.80% | `python` | `PyObject_SetAttr` | dynamic |
| 0.74% | `python` | `type_new` | memory |
| 0.62% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.59% | `python` | `_PyLong_Add` | int |
| 0.53% | `python` | `deduce_unreachable` | gc |

## richards_super

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 39.91% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 15.41% | `[JIT]` | `jit` | jit |
| 4.48% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.98% | `python` | `_PyObject_GetMethod` | dynamic |
| 2.58% | `python` | `_PySuper_Lookup` | dynamic |
| 2.54% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.05% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.26% | `python` | `PyObject_SetAttr` | dynamic |
| 1.18% | `python` | `type_new` | memory |
| 1.07% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.00% | `python` | `PyObject_GetAttr` | dynamic |
| 0.88% | `python` | `long_dealloc` | memory |
| 0.82% | `python` | `deduce_unreachable` | gc |
| 0.70% | `python` | `gc_collect_region.isra.0` | gc |
| 0.67% | `python` | `visit_decref` | gc |
| 0.58% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.54% | `python` | `_PyLong_Add` | int |
| 0.52% | `python` | `visit_reachable` | gc |

## scimark

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.16% | `[JIT]` | `jit` | jit |
| 15.30% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.97% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 4.34% | `python` | `long_dealloc` | memory |
| 3.81% | `array.cpython-313-x86_64-linux-gnu.so` | `array_subscr` | library |
| 2.80% | `python` | `_PyLong_Add` | int |
| 2.70% | `python` | `PyFloat_FromDouble` | float |
| 2.37% | `python` | `PyObject_GetItem` | dynamic |
| 2.19% | `python` | `vgetargs1_impl` | calls |
| 2.12% | `python` | `slot_mp_subscript` | unknown |
| 1.92% | `python` | `PyLong_FromLong` | int |
| 1.78% | `python` | `PyType_GetModuleByDef` | dynamic |
| 1.78% | `python` | `convertitem` | unknown |
| 1.48% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.43% | `array.cpython-313-x86_64-linux-gnu.so` | `array_ass_subscr` | library |
| 1.31% | `python` | `float_dealloc` | memory |
| 1.19% | `python` | `object_isinstance` | dynamic |
| 1.15% | `python` | `_PyLong_Multiply` | int |
| 0.91% | `python` | `PyObject_Free` | dynamic |
| 0.83% | `array.cpython-313-x86_64-linux-gnu.so` | `d_setitem` | library |
| 0.80% | `python` | `PyIndex_Check` | unknown |
| 0.78% | `python` | `PyArg_Parse` | calls |
| 0.68% | `python` | `PyObject_SetItem` | dynamic |
| 0.57% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.54% | `python` | `_Py_Dealloc` | memory |
| 0.53% | `python` | `PyLong_AsDouble.part.0` | int |
| 0.51% | `python` | `tupledealloc` | memory |

## spectral_norm

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 28.97% | `[JIT]` | `jit` | jit |
| 10.41% | `python` | `_PyLong_Add` | int |
| 4.96% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.67% | `python` | `long_dealloc` | memory |
| 4.30% | `python` | `long_div` | int |
| 3.87% | `python` | `PyObject_Free` | dynamic |
| 3.58% | `python` | `enum_next` | miscobj |
| 3.39% | `python` | `_PyLong_Multiply` | int |
| 3.24% | `python` | `float_div` | float |
| 2.15% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.56% | `python` | `convert_to_double` | unknown |
| 1.35% | `python` | `PyNumber_TrueDivide` | dynamic |
| 1.00% | `python` | `float_mul` | float |
| 0.99% | `python` | `type_new` | memory |
| 0.81% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.81% | `python` | `float_dealloc` | memory |
| 0.80% | `python` | `deduce_unreachable` | gc |
| 0.78% | `python` | `PyNumber_FloorDivide` | dynamic |
| 0.69% | `python` | `PyNumber_Multiply` | dynamic |
| 0.64% | `python` | `visit_decref` | gc |
| 0.60% | `python` | `gc_collect_region.isra.0` | gc |
| 0.51% | `python` | `PyType_IsSubtype` | dynamic |
| 0.50% | `python` | `_PyCode_New` | memory |

## sqlglot

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 30.51% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.66% | `[JIT]` | `jit` | jit |
| 3.29% | `python` | `object_isinstance` | dynamic |
| 2.17% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.13% | `python` | `tupledealloc` | memory |
| 1.77% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.46% | `python` | `method_get` | dynamic |
| 1.44% | `python` | `type_new` | memory |
| 1.36% | `python` | `meth_dealloc` | memory |
| 1.08% | `python` | `_PyObject_LookupSpecial` | dynamic |
| 1.08% | `python` | `PyFunction_NewWithQualName` | memory |
| 1.03% | `python` | `dictiter_iternextitem` | dict |
| 1.02% | `python` | `deduce_unreachable` | gc |
| 0.92% | `python` | `PyObject_GetOptionalAttr` | dynamic |
| 0.91% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.87% | `python` | `PyObject_IsInstance` | dynamic |
| 0.86% | `python` | `visit_decref` | gc |
| 0.83% | `python` | `gc_collect_region.isra.0` | gc |
| 0.80% | `python` | `gen_dealloc` | memory |
| 0.79% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.76% | `python` | `list_dealloc` | memory |
| 0.75% | `python` | `make_gen` | unknown |
| 0.71% | `python` | `dict_items` | dict |
| 0.69% | `python` | `getset_get` | dynamic |
| 0.68% | `python` | `object_recursive_isinstance.part.0` | dynamic |
| 0.68% | `python` | `PyObject_GC_Del` | gc |
| 0.67% | `python` | `insert_to_emptydict` | dict |
| 0.66% | `python` | `dictiter_dealloc` | memory |
| 0.64% | `python` | `dictview_dealloc` | memory |
| 0.60% | `python` | `_PyCode_New` | memory |
| 0.59% | `python` | `siphash13` | str |
| 0.59% | `python` | `dictitems_iter` | unknown |
| 0.59% | `python` | `visit_reachable` | gc |
| 0.53% | `python` | `slot_tp_hash` | unknown |
| 0.52% | `python` | `func_dealloc` | memory |
| 0.51% | `python` | `_PyEvalFramePushAndInit` | interpreter |

## sqlglot_optimize

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 26.69% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.68% | `[JIT]` | `jit` | jit |
| 4.00% | `python` | `object_isinstance` | dynamic |
| 2.18% | `python` | `tupledealloc` | memory |
| 2.04% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.65% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.65% | `python` | `meth_dealloc` | memory |
| 1.45% | `python` | `type_new` | memory |
| 1.41% | `python` | `method_get` | dynamic |
| 1.27% | `python` | `_PyObject_LookupSpecial` | dynamic |
| 1.22% | `python` | `dictiter_iternextitem` | dict |
| 1.06% | `python` | `deduce_unreachable` | gc |
| 1.05% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.05% | `python` | `PyObject_IsInstance` | dynamic |
| 1.00% | `python` | `list_dealloc` | memory |
| 0.99% | `python` | `PyObject_GetOptionalAttr` | dynamic |
| 0.92% | `python` | `gc_collect_region.isra.0` | gc |
| 0.90% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.88% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.88% | `python` | `visit_decref` | gc |
| 0.73% | `python` | `getset_get` | dynamic |
| 0.70% | `python` | `object_recursive_isinstance.part.0` | dynamic |
| 0.70% | `python` | `dictiter_dealloc` | memory |
| 0.65% | `python` | `PyObject_GC_Del` | gc |
| 0.61% | `python` | `_PyCode_New` | memory |
| 0.59% | `python` | `dict_get` | dict |
| 0.56% | `python` | `list_iter` | list |
| 0.55% | `python` | `tuplehash` | tuple |
| 0.55% | `python` | `visit_reachable` | gc |
| 0.55% | `python` | `member_get` | unknown |
| 0.54% | `python` | `dict_dealloc` | memory |
| 0.53% | `python` | `find_name_in_mro` | lookup |
| 0.53% | `python` | `siphash13` | str |
| 0.53% | `python` | `PyMem_Calloc` | memory |
| 0.52% | `python` | `dict_items` | dict |
| 0.52% | `python` | `r_object` | import |
| 0.51% | `python` | `unicode_dealloc` | memory |

## sqlglot_parse

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 42.19% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.44% | `[JIT]` | `jit` | jit |
| 2.98% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.30% | `python` | `_Py_type_getattro` | lookup |
| 1.29% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.28% | `python` | `deduce_unreachable` | gc |
| 1.24% | `python` | `gc_collect_region.isra.0` | gc |
| 1.19% | `python` | `PyDict_Contains` | dict |
| 1.08% | `python` | `type_new` | memory |
| 0.93% | `python` | `visit_decref` | gc |
| 0.90% | `python` | `dict_get` | dict |
| 0.84% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.84% | `python` | `long_dealloc` | memory |
| 0.75% | `python` | `slot_tp_hash` | unknown |
| 0.75% | `python` | `_PyLong_Add` | int |
| 0.70% | `python` | `tupledealloc` | memory |
| 0.69% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.66% | `python` | `PyObject_RichCompare` | dynamic |
| 0.63% | `python` | `PyObject_GetAttr` | dynamic |
| 0.61% | `python` | `dict_dealloc` | memory |
| 0.60% | `python` | `object_isinstance` | dynamic |
| 0.57% | `python` | `find_name_in_mro` | lookup |
| 0.56% | `python` | `PyObject_SetAttr` | dynamic |
| 0.56% | `python` | `PyDict_SetItem` | dict |
| 0.53% | `python` | `visit_reachable` | gc |
| 0.52% | `python` | `unicode_dealloc` | memory |

## sqlglot_transpile

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 37.46% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.00% | `[JIT]` | `jit` | jit |
| 2.84% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.71% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.43% | `python` | `type_new` | memory |
| 1.40% | `python` | `deduce_unreachable` | gc |
| 1.16% | `python` | `gc_collect_region.isra.0` | gc |
| 1.11% | `python` | `dict_get` | dict |
| 1.03% | `python` | `_Py_type_getattro` | lookup |
| 1.01% | `python` | `visit_decref` | gc |
| 0.97% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.96% | `python` | `find_name_in_mro` | lookup |
| 0.90% | `python` | `object_isinstance` | dynamic |
| 0.89% | `python` | `PyDict_Contains` | dict |
| 0.81% | `python` | `tupledealloc` | memory |
| 0.70% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.69% | `python` | `unicode_dealloc` | memory |
| 0.68% | `python` | `dict_dealloc` | memory |
| 0.67% | `python` | `long_dealloc` | memory |
| 0.66% | `python` | `visit_reachable` | gc |
| 0.63% | `python` | `_PyCode_New` | memory |
| 0.60% | `python` | `PyObject_GetAttr` | dynamic |
| 0.59% | `python` | `slot_tp_hash` | unknown |
| 0.51% | `python` | `PyDict_SetItem` | dict |
| 0.51% | `python` | `_PyLong_Add` | int |

## sqlite_synth

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 11.62% | `libpthread-2.31.so` | `__pthread_mutex_lock` | library |
| 11.62% | `libpthread-2.31.so` | `pthread_mutex_unlock` | library |
| 5.54% | `python` | `PyEval_RestoreThread` | interpreter |
| 4.92% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.67% | `libsqlite3.so.0.8.6` | `sqlite3_reset` | library |
| 3.10% | `[JIT]` | `jit` | jit |
| 2.50% | `libm-2.31.so` | `f64xsubf128` | library |
| 1.39% | `libsqlite3.so.0.8.6` | `sqlite3_randomness` | library |
| 1.27% | `python` | `PyTuple_New` | memory |
| 1.25% | `python` | `PyEval_SaveThread` | interpreter |
| 1.24% | `python` | `long_dealloc` | memory |
| 1.09% | `python` | `PyObject_Str` | dynamic |
| 1.08% | `python` | `tupledealloc` | memory |
| 0.98% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.92% | `libpthread-2.31.so` | `pthread_cond_signal@@GLIBC_2.3.2` | library |
| 0.92% | `_sqlite3.cpython-313-x86_64-linux-gnu.so` | `_pysqlite_query_execute` | library |
| 0.90% | `libsqlite3.so.0.8.6` | `sqlite3_value_double` | library |
| 0.80% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.75% | `python` | `list_dealloc` | memory |
| 0.71% | `libsqlite3.so.0.8.6` | `sqlite3_value_int64` | library |
| 0.71% | `python` | `type_new` | memory |
| 0.70% | `python` | `PyFloat_AsDouble` | float |
| 0.68% | `libsqlite3.so.0.8.6` | `sqlite3_preupdate_old` | library |
| 0.67% | `libc-2.31.so` | `pthread_mutex_unlock` | libc |
| 0.66% | `python` | `unicode_dealloc` | memory |
| 0.65% | `libsqlite3.so.0.8.6` | `sqlite3_extended_errcode` | library |
| 0.65% | `python` | `PyList_New` | memory |
| 0.62% | `libsqlite3.so.0.8.6` | `sqlite3_wal_checkpoint` | library |
| 0.61% | `python` | `unicode_decode_utf8` | str |
| 0.57% | `python` | `PyFloat_FromDouble` | float |
| 0.57% | `libsqlite3.so.0.8.6` | `sqlite3_vtab_config` | library |
| 0.56% | `libc-2.31.so` | `pthread_mutex_lock` | libc |
| 0.56% | `libsqlite3.so.0.8.6` | `sqlite3_enable_shared_cache` | library |
| 0.52% | `python` | `deduce_unreachable` | gc |
| 0.51% | `python` | `_PyObject_Malloc` | memory |

## sympy

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 25.35% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.35% | `[JIT]` | `jit` | jit |
| 2.31% | `python` | `tupledealloc` | memory |
| 2.09% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.30% | `python` | `PyDict_GetItemRef` | dict |
| 1.26% | `python` | `deduce_unreachable` | gc |
| 1.13% | `python` | `type_new` | memory |
| 1.12% | `python` | `visit_decref` | gc |
| 1.12% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 1.08% | `python` | `_Py_type_getattro` | lookup |
| 1.08% | `python` | `gc_collect_region.isra.0` | gc |
| 1.00% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.99% | `python` | `PyDict_SetItem` | dict |
| 0.98% | `python` | `find_name_in_mro` | lookup |
| 0.79% | `python` | `visit_reachable` | gc |
| 0.76% | `python` | `object_isinstance` | dynamic |
| 0.75% | `python` | `dict_dealloc` | memory |
| 0.74% | `python` | `_Py_dict_lookup` | lookup |
| 0.74% | `python` | `method_get` | dynamic |
| 0.73% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.73% | `python` | `slot_tp_richcompare` | dynamic |
| 0.72% | `python` | `_PyCode_New` | memory |
| 0.72% | `python` | `meth_dealloc` | memory |
| 0.70% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.67% | `python` | `list_dealloc` | memory |
| 0.66% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.61% | `python` | `PyObject_GetAttr` | dynamic |
| 0.59% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.58% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.55% | `python` | `r_object` | import |
| 0.52% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.50% | `python` | `_PyObject_GetMethod` | dynamic |

## telco

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 11.61% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.93% | `[JIT]` | `jit` | jit |
| 3.85% | `python` | `PyType_GetModuleByDef` | dynamic |
| 3.71% | `python` | `PyObject_GC_Del` | gc |
| 3.20% | `python` | `_PyObject_GC_New` | gc |
| 2.21% | `python` | `meth_dealloc` | memory |
| 2.11% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_qaddsub` | library |
| 1.87% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.85% | `python` | `PyTuple_New` | memory |
| 1.82% | `python` | `method_get` | dynamic |
| 1.79% | `python` | `PyContextVar_Get` | unknown |
| 1.72% | `python` | `tupledealloc` | memory |
| 1.68% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_baseshiftr` | library |
| 1.64% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `nm_mpd_qadd` | library |
| 1.61% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `nm_mpd_qmul` | library |
| 1.60% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.55% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `convert_op` | library |
| 1.46% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_qmul` | library |
| 1.30% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_qfinalize` | library |
| 1.28% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_qshiftr` | library |
| 1.22% | `python` | `vgetargskeywords.constprop.0` | calls |
| 1.04% | `python` | `_io_BytesIO_read` | unknown |
| 0.99% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `dec_mpd_qquantize` | library |
| 0.99% | `python` | `_PyArg_UnpackKeywordsWithVararg` | calls |
| 0.93% | `python` | `vgetargs1_impl` | calls |
| 0.92% | `python` | `type_new` | memory |
| 0.91% | `python` | `method_vectorcall_VARARGS_KEYWORDS` | calls |
| 0.90% | `python` | `PyUnicode_New` | memory |
| 0.83% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `PyDecType_New` | library |
| 0.81% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_qquantize` | library |
| 0.80% | `python` | `PyDict_GetItemRef` | dict |
| 0.74% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `dec_dealloc` | library |
| 0.69% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `dec_addstatus` | library |
| 0.68% | `python` | `deduce_unreachable` | gc |
| 0.65% | `python` | `find_keyword` | unknown |
| 0.65% | `python` | `unicode_dealloc` | memory |
| 0.59% | `python` | `as_ucs4` | unknown |
| 0.57% | `python` | `PyObject_GetAttr` | dynamic |
| 0.56% | `python` | `visit_decref` | gc |
| 0.55% | `_struct.cpython-313-x86_64-linux-gnu.so` | `unpack` | library |
| 0.55% | `python` | `gc_collect_region.isra.0` | gc |

## thrift

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 22.06% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.31% | `python` | `object_new` | memory |
| 2.17% | `python` | `slot_tp_init` | unknown |
| 2.14% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::encodeValue` | library |
| 1.95% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.91% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.86% | `python` | `_PyFunction_Vectorcall` | calls |
| 1.85% | `python` | `PyObject_GC_Del` | gc |
| 1.85% | `python` | `PyDict_GetItemRef` | dict |
| 1.77% | `python` | `subtype_dealloc` | memory |
| 1.64% | `python` | `PyDict_SetItem` | dict |
| 1.62% | `python` | `insert_to_emptydict` | dict |
| 1.55% | `python` | `_PyStack_UnpackDict` | unknown |
| 1.42% | `python` | `tupledealloc` | memory |
| 1.37% | `python` | `dict_dealloc` | memory |
| 1.33% | `python` | `PyUnicode_FromFormatV` | str |
| 1.25% | `[JIT]` | `jit` | jit |
| 1.24% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.13% | `python` | `type_new` | memory |
| 1.12% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 1.07% | `python` | `unicode_decode_utf8` | str |
| 0.98% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.92% | `python` | `unicode_dealloc` | memory |
| 0.91% | `python` | `insertdict` | dict |
| 0.91% | `python` | `deduce_unreachable` | gc |
| 0.87% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.72% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::decodeValue` | library |
| 0.71% | `python` | `PyMem_Free` | memory |
| 0.71% | `python` | `list_dealloc` | memory |
| 0.66% | `python` | `gc_collect_region.isra.0` | gc |
| 0.62% | `python` | `visit_decref` | gc |
| 0.61% | `python` | `_PySuper_Lookup` | dynamic |
| 0.59% | `python` | `PyLong_AsLong` | int |
| 0.59% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readStruct` | library |
| 0.58% | `python` | `dict_merge` | dict |
| 0.58% | `python` | `_Py_type_getattro` | lookup |
| 0.55% | `python` | `dictresize` | dict |
| 0.55% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readBytes` | library |
| 0.55% | `python` | `PyObject_GetOptionalAttr` | dynamic |
| 0.53% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.53% | `python` | `_PyCode_New` | memory |
| 0.52% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.51% | `python` | `PyObject_GetAttr` | dynamic |
| 0.50% | `python` | `visit_reachable` | gc |

## tomli_loads

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.36% | `[JIT]` | `jit` | jit |
| 23.21% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.00% | `python` | `_PyLong_Add` | int |
| 4.85% | `python` | `_PySet_Contains` | unknown |
| 4.49% | `python` | `long_dealloc` | memory |
| 2.58% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.38% | `python` | `PyDict_GetItemRef` | dict |
| 2.17% | `python` | `PyDict_Contains` | dict |
| 2.12% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.09% | `python` | `_PyUnicode_Equal` | str |
| 1.30% | `python` | `_PyIncrementalNewlineDecoder_decode.cold` | memory |
| 1.04% | `python` | `tupledealloc` | memory |
| 1.01% | `python` | `set_contains_lock_held` | miscobj |
| 0.70% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.70% | `python` | `PyUnicode_New` | memory |
| 0.65% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.65% | `python` | `_PyIncrementalNewlineDecoder_decode` | memory |
| 0.61% | `python` | `_PyDict_LoadGlobal` | dict |
| 0.60% | `python` | `sre_ucs4_match` | library |
| 0.60% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.59% | `python` | `unicode_subscript` | str |
| 0.51% | `python` | `object_isinstance` | dynamic |

## tornado_http

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 26.46% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.10% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.33% | `[JIT]` | `jit` | jit |
| 1.91% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.69% | `python` | `type_new` | memory |
| 1.32% | `python` | `tupledealloc` | memory |
| 1.28% | `python` | `deduce_unreachable` | gc |
| 1.16% | `python` | `visit_decref` | gc |
| 1.03% | `python` | `gc_collect_region.isra.0` | gc |
| 0.83% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.80% | `python` | `_PyCode_New` | memory |
| 0.77% | `python` | `visit_reachable` | gc |
| 0.76% | `python` | `PyDict_GetItemRef` | dict |
| 0.69% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 0.62% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.62% | `python` | `r_object` | import |
| 0.60% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.54% | `python` | `find_name_in_mro` | lookup |
| 0.53% | `python` | `subtype_dealloc` | memory |
| 0.51% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.51% | `python` | `list_dealloc` | memory |
| 0.51% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.50% | `python` | `unicode_dealloc` | memory |
| 0.50% | `python` | `PyUnicode_FromKindAndData` | str |

## typing_runtime_protocols

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 29.30% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.48% | `[JIT]` | `jit` | jit |
| 3.29% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 3.12% | `python` | `tupledealloc` | memory |
| 2.64% | `python` | `_Py_dict_lookup` | lookup |
| 2.10% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.98% | `python` | `_Py_type_getattro` | lookup |
| 1.71% | `python` | `PyObject_GC_Del` | gc |
| 1.57% | `python` | `PyDict_Contains` | dict |
| 1.46% | `python` | `tuplehash` | tuple |
| 1.38% | `python` | `PyTraceBack_Here` | exceptions |
| 1.24% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.18% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.15% | `python` | `type_new` | memory |
| 1.05% | `python` | `_PyObject_GC_New` | gc |
| 1.04% | `python` | `frame_dealloc` | memory |
| 1.03% | `python` | `bounded_lru_cache_wrapper` | unknown |
| 0.98% | `python` | `_PyFrame_MakeAndSetFrameObject` | unknown |
| 0.95% | `python` | `PyObject_Vectorcall` | dynamic |
| 0.91% | `python` | `getset_get` | dynamic |
| 0.91% | `python` | `deduce_unreachable` | gc |
| 0.78% | `python` | `tuple_iter` | tuple |
| 0.74% | `python` | `PySet_Contains` | unknown |
| 0.73% | `python` | `tuplecontains` | tuple |
| 0.72% | `python` | `gc_collect_region.isra.0` | gc |
| 0.71% | `python` | `visit_decref` | gc |
| 0.67% | `python` | `wrap_descr_get` | unknown |
| 0.64% | `python` | `PyArg_UnpackTuple` | calls |
| 0.62% | `python` | `_PyDict_GetItem_KnownHash` | dict |
| 0.61% | `python` | `method_dealloc` | memory |
| 0.57% | `python` | `tb_dealloc` | memory |
| 0.56% | `python` | `_Py_type_getattro_impl` | dynamic |
| 0.53% | `python` | `weakref_richcompare` | unknown |
| 0.51% | `python` | `lru_cache_make_key` | unknown |

## unpack_sequence

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 75.96% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 1.13% | `python` | `gc_collect_main` | gc |
| 1.04% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.91% | `python` | `_PyObject_Malloc` | memory |
| 0.69% | `python` | `_PyObject_Free` | memory |
| 0.64% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.61% | `python` | `visit_decref` | gc |

## unpickle

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 14.40% | `python` | `unicode_decode_utf8` | str |
| 9.22% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `load` | library |
| 7.56% | `python` | `insertdict` | dict |
| 6.04% | `python` | `unicode_dealloc` | memory |
| 5.99% | `python` | `siphash13` | str |
| 4.47% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `load_counted_binunicode` | library |
| 3.78% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.74% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.42% | `python` | `dictresize` | dict |
| 2.00% | `python` | `dict_ass_sub` | dict |
| 1.64% | `python` | `dict_dealloc` | memory |
| 1.50% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Unpickler_dealloc` | library |
| 1.28% | `python` | `PyObject_SetItem` | dynamic |
| 1.17% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pdata_clear` | library |
| 1.09% | `python` | `_PyObject_Malloc` | memory |
| 0.99% | `python` | `PyMem_Realloc` | memory |
| 0.98% | `python` | `list_dealloc` | memory |
| 0.96% | `[JIT]` | `jit` | jit |
| 0.88% | `python` | `long_dealloc` | memory |
| 0.81% | `python` | `PyLong_FromLong` | int |
| 0.77% | `python` | `type_new` | memory |
| 0.76% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `do_setitems.isra.0` | library |
| 0.72% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pdata_push` | library |
| 0.69% | `python` | `PyMem_Free` | memory |
| 0.65% | `python` | `_PyObject_GC_New` | gc |
| 0.63% | `python` | `deduce_unreachable` | gc |
| 0.60% | `python` | `unicode_hash` | str |
| 0.57% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.51% | `python` | `gc_collect_region.isra.0` | gc |

## unpickle_list

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 15.76% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `load` | library |
| 13.71% | `python` | `list_dealloc` | memory |
| 5.48% | `python` | `PyList_New` | memory |
| 5.19% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pdata_push` | library |
| 5.05% | `python` | `PyList_SetSlice` | list |
| 5.02% | `python` | `PyMem_Calloc` | memory |
| 4.91% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.85% | `python` | `PyLong_FromLong` | int |
| 3.36% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `do_append.isra.0` | library |
| 3.35% | `python` | `_PyObject_Malloc` | memory |
| 1.93% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.61% | `python` | `list_resize` | list |
| 1.11% | `python` | `type_new` | memory |
| 0.92% | `[JIT]` | `jit` | jit |
| 0.82% | `python` | `deduce_unreachable` | gc |
| 0.70% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005ba4` | library |
| 0.69% | `python` | `visit_decref` | gc |
| 0.63% | `python` | `gc_collect_region.isra.0` | gc |
| 0.53% | `python` | `PyMem_Realloc` | memory |
| 0.52% | `python` | `_PyObject_GC_New` | gc |
| 0.50% | `python` | `visit_reachable` | gc |

## unpickle_pure_python

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 31.99% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 21.98% | `[JIT]` | `jit` | jit |
| 2.87% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.71% | `python` | `_io_BytesIO_read` | unknown |
| 2.38% | `python` | `PyObject_IsTrue` | dynamic |
| 2.13% | `python` | `PyDict_GetItemRef` | dict |
| 1.61% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.27% | `python` | `unicode_decode_utf8` | str |
| 1.14% | `python` | `tupledealloc` | memory |
| 0.98% | `python` | `unicode_new` | memory |
| 0.89% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.86% | `python` | `PyObject_Free` | dynamic |
| 0.82% | `python` | `bytes_subscript` | str |
| 0.80% | `python` | `type_new` | memory |
| 0.79% | `python` | `insertdict` | dict |
| 0.71% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.67% | `python` | `PyObject_Size` | dynamic |
| 0.63% | `python` | `deduce_unreachable` | gc |
| 0.61% | `python` | `PyObject_GetItem` | dynamic |
| 0.56% | `python` | `_PyDict_SetItem_Take2` | dict |
| 0.52% | `python` | `visit_decref` | gc |
| 0.52% | `python` | `gc_collect_region.isra.0` | gc |
| 0.52% | `python` | `PyObject_IsInstance` | dynamic |
| 0.52% | `python` | `unicode_dealloc` | memory |
| 0.51% | `python` | `siphash13` | str |

## xml_etree

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 17.35% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.59% | `[JIT]` | `jit` | jit |
| 3.07% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `doContent` | library |
| 3.07% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 2.32% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `PyExpat_XML_Parse` | library |
| 2.04% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.93% | `python` | `_io_TextIOWrapper_write` | unknown |
| 1.90% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `normal_contentTok` | library |
| 1.89% | `python` | `deduce_unreachable` | gc |
| 1.75% | `python` | `unicode_decode_utf8` | str |
| 1.63% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `hash` | library |
| 1.56% | `python` | `unicode_dealloc` | memory |
| 1.54% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `storeAtts` | library |
| 1.50% | `python` | `_PyObject_GC_New` | gc |
| 1.44% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `makeuniversal.isra.0` | library |
| 1.41% | `python` | `PyObject_GC_Del` | gc |
| 1.39% | `python` | `PyUnicode_Concat` | str |
| 1.37% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.33% | `python` | `visit_reachable` | gc |
| 1.31% | `python` | `visit_decref` | gc |
| 1.20% | `python` | `PyObject_VectorcallMethod` | dynamic |
| 1.10% | `python` | `tupledealloc` | memory |
| 1.04% | `python` | `object_isinstance` | dynamic |
| 0.99% | `python` | `list_dealloc` | memory |
| 0.96% | `python` | `gc_collect_region.isra.0` | gc |
| 0.96% | `python` | `PyBytes_FromStringAndSize` | str |
| 0.96% | `python` | `long_to_decimal_string_internal` | int |
| 0.94% | `python` | `_PyFunction_Vectorcall` | calls |
| 0.83% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `elementiter_next` | library |
| 0.82% | `python` | `PyUnicode_Format` | str |
| 0.76% | `python` | `PyObject_GetAttr` | dynamic |
| 0.74% | `python` | `PyUnicode_Contains` | str |
| 0.74% | `python` | `getset_get` | dynamic |
| 0.73% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `element_dealloc` | library |
| 0.71% | `python` | `PyDict_GetItemWithError` | dict |
| 0.71% | `python` | `vgetargs1_impl` | calls |
| 0.70% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `treebuilder_handle_start` | library |
| 0.66% | `python` | `siphash13` | str |
| 0.62% | `python` | `PyObject_Free` | dynamic |
| 0.61% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.60% | `python` | `type_new` | memory |
| 0.58% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `treebuilder_handle_end.isra.0` | library |
| 0.58% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `element_gc_traverse` | library |
| 0.54% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.51% | `python` | `list_vectorcall` | list |


## Categories

### interpreter

24.29% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 21.59% | python | _PyEval_EvalFrameDefault |
| 1.68% | python | _PyEval_FrameClearAndPop |
| 0.36% | python | _PyEvalFramePushAndInit |
| 0.11% | python | _PyFrame_ClearExceptCode |
| 0.10% | python | _PyEval_EvalFrameDefault.cold |
| 0.10% | python | PyEval_RestoreThread |
| 0.08% | python | _PyPegen_fill_token |
| 0.04% | python | intern_string_constants |
| 0.03% | python | PyEval_SaveThread |
| 0.03% | python | _PyPegen_update_memo |
| 0.02% | python | initialize_locals |
| 0.02% | python | _PyCode_Validate |
| 0.02% | python | _PyEval_SliceIndex |
| 0.01% | python | _PyPegen_is_memoized |
| 0.01% | python | _PyPegen_name_token |
| 0.01% | python | _PyCode_Quicken |
| 0.01% | python | advance |
| 0.01% | python | _PyPegen_expect_token |
| 0.01% | python | _PyEval_CheckExceptTypeValid |
| 0.01% | python | _PyPegen_Parser_Free |
| 0.01% | python | _PyThreadState_PopFrame |
| 0.01% | python | PyEval_GetFrame |
| 0.01% | python | _PyEval_Vector |

### memory

10.49% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.87% | python | type_new |
| 0.85% | python | tupledealloc |
| 0.83% | python | list_dealloc |
| 0.70% | python | long_dealloc |
| 0.56% | python | unicode_dealloc |
| 0.41% | python | _PyCode_New |
| 0.38% | python | dict_dealloc |
| 0.37% | python | _PyObject_Malloc |
| 0.36% | python | gen_dealloc |
| 0.32% | python | subtype_dealloc |
| 0.28% | python | meth_dealloc |
| 0.24% | python | PyMem_Free |
| 0.23% | python | PyList_New |
| 0.23% | python | PyFunction_NewWithQualName |
| 0.22% | python | object_new |
| 0.21% | python | PyMem_Malloc |
| 0.21% | python | _PyLong_New |
| 0.20% | python | PyType_GenericAlloc |
| 0.15% | python | PyMem_Calloc |
| 0.15% | python | PyUnicode_New |
| 0.15% | python | func_dealloc |
| 0.14% | python | _Py_Dealloc |
| 0.13% | python | _PyObject_Free |
| 0.13% | python | method_dealloc |
| 0.12% | python | PyTuple_New |
| 0.12% | python | set_dealloc |
| 0.12% | python | BaseException_new |
| 0.12% | python | code_dealloc |
| 0.11% | python | frame_dealloc |
| 0.10% | python | float_dealloc |
| 0.09% | python | slice_dealloc |
| 0.06% | python | listiter_dealloc |
| 0.06% | python | StopIteration_dealloc |
| 0.06% | python | allocate_from_new_pool |
| 0.05% | python | weakref_dealloc |
| 0.05% | python | PyType_GenericNew |
| 0.05% | python | context_tp_dealloc |
| 0.05% | python | BaseException_dealloc |
| 0.04% | python | tb_dealloc |
| 0.04% | python | dictiter_dealloc |
| 0.04% | python | list_new_prealloc |
| 0.04% | python | make_new_set |
| 0.04% | python | tp_new_wrapper |
| 0.04% | python | range_dealloc |
| 0.04% | python | cell_dealloc |
| 0.03% | python | PySlice_New |
| 0.03% | python | _PyObject_Malloc (inlined) |
| 0.03% | python | dictview_dealloc |
| 0.03% | python | slot_tp_new |
| 0.03% | python | object_dealloc |
| 0.03% | python | _Py_NewReference |
| 0.02% | python | PyMem_Realloc |
| 0.02% | python | _PyObject_Realloc |
| 0.02% | python | _PyFloat_ExactDealloc |
| 0.02% | python | match_dealloc |
| 0.02% | python | _PyIncrementalNewlineDecoder_decode.cold |
| 0.02% | python | async_gen_asend_dealloc |
| 0.02% | python | async_gen_asend_new |
| 0.02% | python | PyCMethod_New |
| 0.02% | python | tupleiter_dealloc |
| 0.02% | python | PyDict_New |
| 0.02% | python | unicode_new |
| 0.02% | python | async_gen_wrapped_val_dealloc |
| 0.02% | python | PyObject_CallFinalizerFromDealloc |
| 0.02% | python | _PyAsyncGenValueWrapperNew |
| 0.01% | python | tuple_alloc |
| 0.01% | python | structseq_dealloc |
| 0.01% | python | _PyIncrementalNewlineDecoder_decode |
| 0.01% | python | _PyUnicode_ExactDealloc |
| 0.01% | python | descr_dealloc |
| 0.01% | python | _PyTokenizer_translate_newlines.constprop.0 |
| 0.01% | python | _PyMem_RawMalloc |
| 0.01% | python | AttributeError_dealloc |
| 0.01% | python | _PyObject_New |
| 0.01% | python | pattern_new_match.isra.0 |
| 0.01% | python | PyDictProxy_New |
| 0.01% | python | reversed_new_impl |
| 0.01% | python | zip_new |
| 0.01% | python | PyUnicode_New.part.0 |

### library

10.24% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 1.69% | python | sre_ucs1_match |
| 1.34% | _pickle.cpython-313-x86_64-linux-gnu.so | save |
| 0.75% | libz.so.1.2.11 | crc32_combine64 |
| 0.70% | python | sre_ucs2_charset.isra.0 |
| 0.49% | _json.cpython-313-x86_64-linux-gnu.so | _parse_object_unicode |
| 0.30% | _pickle.cpython-313-x86_64-linux-gnu.so | load |
| 0.28% | libz.so.1.2.11 | inflateBackEnd |
| 0.28% | _pickle.cpython-313-x86_64-linux-gnu.so | _Pickler_Write |
| 0.24% | _pickle.cpython-313-x86_64-linux-gnu.so | memo_put.isra.0 |
| 0.21% | python | sre_search |
| 0.20% | libpthread-2.31.so | __pthread_mutex_lock |
| 0.19% | libpthread-2.31.so | pthread_mutex_unlock |
| 0.15% | libm-2.31.so | f64xsubf128 |
| 0.14% | python | sre_ucs1_count |
| 0.13% | ld-2.31.so | _dl_rtld_di_serinfo |
| 0.12% | python | _sre_SRE_Pattern_match |
| 0.10% | _json.cpython-313-x86_64-linux-gnu.so | encoder_encode_key_value |
| 0.09% | tracer.cpython-313-x86_64-linux-gnu.so | CTracer_trace |
| 0.08% | _pickle.cpython-313-x86_64-linux-gnu.so | _Pickler_write_bytes |
| 0.07% | libpython3.11.so.1.0 | _PyEval_EvalFrameDefault |
| 0.07% | _pickle.cpython-313-x86_64-linux-gnu.so | Pdata_push |
| 0.06% | libsqlite3.so.0.8.6 | sqlite3_reset |
| 0.05% | _pickle.cpython-313-x86_64-linux-gnu.so | Pickler_dealloc |
| 0.05% | _pickle.cpython-313-x86_64-linux-gnu.so | load_counted_binunicode |
| 0.05% | _asyncio.cpython-313-x86_64-linux-gnu.so | TaskObj_traverse |
| 0.05% | libmagic.so.1.0.0 | 0x000000000000f936 |
| 0.05% | array.cpython-313-x86_64-linux-gnu.so | array_subscr |
| 0.04% | libz.so.1.2.11 | inflateCodesUsed |
| 0.04% | _pickle.cpython-313-x86_64-linux-gnu.so | do_append.isra.0 |
| 0.04% | ld-2.31.so | _dl_catch_error |
| 0.04% | libm-2.31.so | __fmod_finite |
| 0.04% | pyexpat.cpython-313-x86_64-linux-gnu.so | doContent |
| 0.03% | _json.cpython-313-x86_64-linux-gnu.so | py_encode_basestring_ascii |
| 0.03% | _json.cpython-313-x86_64-linux-gnu.so | _match_number_unicode.isra.0 |
| 0.03% | libmagic.so.1.0.0 | 0x000000000000f932 |
| 0.03% | _pickle.cpython-313-x86_64-linux-gnu.so | memo_get.isra.0 |
| 0.03% | python | pattern_subx |
| 0.03% | pyexpat.cpython-313-x86_64-linux-gnu.so | PyExpat_XML_Parse |
| 0.03% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::encodeValue |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_qaddsub |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | Unpickler_dealloc |
| 0.02% | _asyncio.cpython-313-x86_64-linux-gnu.so | task_step_impl |
| 0.02% | pyexpat.cpython-313-x86_64-linux-gnu.so | normal_contentTok |
| 0.02% | libpthread-2.31.so | pthread_cond_signal@@GLIBC_2.3.2 |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_baseshiftr |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | nm_mpd_qadd |
| 0.02% | pyexpat.cpython-313-x86_64-linux-gnu.so | hash |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | nm_mpd_qmul |
| 0.02% | _heapq.cpython-313-x86_64-linux-gnu.so | _heapq_heappop |
| 0.02% | libz.so.1.2.11 | inflate |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | convert_op |
| 0.02% | pyexpat.cpython-313-x86_64-linux-gnu.so | storeAtts |
| 0.02% | array.cpython-313-x86_64-linux-gnu.so | array_ass_subscr |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005cd4 |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_qmul |
| 0.02% | _asyncio.cpython-313-x86_64-linux-gnu.so | TaskObj_clear |
| 0.02% | _elementtree.cpython-313-x86_64-linux-gnu.so | makeuniversal.isra.0 |
| 0.02% | libpython3.11.so.1.0 | _PyDict_GetItem_KnownHash |
| 0.02% | libsqlite3.so.0.8.6 | sqlite3_randomness |
| 0.02% | math.cpython-313-x86_64-linux-gnu.so | factorial_partial_product |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_qfinalize |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_qshiftr |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | Pdata_clear |
| 0.01% | _json.cpython-313-x86_64-linux-gnu.so | _parse_array_unicode |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | _asyncio_Future_add_done_callback |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | TaskStepMethWrapper_traverse |
| 0.01% | libpython3.11.so.1.0 | PyObject_Malloc |
| 0.01% | _bisect.cpython-313-x86_64-linux-gnu.so | _bisect_bisect_right |
| 0.01% | libpython3.11.so.1.0 | deduce_unreachable |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | dec_mpd_qquantize |
| 0.01% | python | sre_ucs1_match.cold |
| 0.01% | math.cpython-313-x86_64-linux-gnu.so | math_factorial |
| 0.01% | libpython3.11.so.1.0 | visit_decref |
| 0.01% | libpthread-2.31.so | sem_post@@GLIBC_2.2.5 |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_value_double |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | _asyncio_Task___init__ |
| 0.01% | _sqlite3.cpython-313-x86_64-linux-gnu.so | _pysqlite_query_execute |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | _pickle_loads |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | _pickle_dumps |
| 0.01% | libssl.so.1.1 | SSL_rstate_string |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005e54 |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | FutureObj_traverse |
| 0.01% | libpthread-2.31.so | sem_trywait@@GLIBC_2.2.5 |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | future_init |
| 0.01% | libpython3.11.so.1.0 | type_new |
| 0.01% | libpython3.11.so.1.0 | PyDict_SetDefault |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | PyDecType_New |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | elementiter_next |
| 0.01% | array.cpython-313-x86_64-linux-gnu.so | d_setitem |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_exec |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_qquantize |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | element_dealloc |
| 0.01% | _struct.cpython-313-x86_64-linux-gnu.so | unpack |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005ba4 |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | do_setitems.isra.0 |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | dec_dealloc |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005fc4 |
| 0.01% | libpython3.11.so.1.0 | visit_reachable |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_value_int64 |
| 0.01% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::decodeValue |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | treebuilder_handle_start |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | element_gc_traverse |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_extended_errcode |
| 0.01% | libpython3.11.so.1.0 | r_object |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | task_step |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | dec_addstatus |
| 0.01% | libpython3.11.so.1.0 | gc_collect_main |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_preupdate_old |
| 0.01% | math.cpython-313-x86_64-linux-gnu.so | math_sqrt |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_wal_checkpoint |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | call_soon |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_str_value |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | task_wakeup |
| 0.01% | libpython3.11.so.1.0 | PyObject_Free |
| 0.01% | python | sre_ucs4_match |
| 0.01% | python | _sre_SRE_Pattern_search |
| 0.01% | libm-2.31.so | pow |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_vtab_config |
| 0.01% | _json.cpython-313-x86_64-linux-gnu.so | encoder_listencode_obj |
| 0.01% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readStruct |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | treebuilder_handle_end.isra.0 |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_enable_shared_cache |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | FutureObj_clear |
| 0.01% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readBytes |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | future_schedule_callbacks |
| 0.01% | math.cpython-313-x86_64-linux-gnu.so | math_cos |
| 0.01% | _struct.cpython-313-x86_64-linux-gnu.so | s_pack |
| 0.01% | tracer.cpython-313-x86_64-linux-gnu.so | CTracer_set_pdata_stack |

### gc

9.68% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 1.75% | python | deduce_unreachable |
| 1.59% | python | visit_decref |
| 1.50% | python | visit_reachable |
| 1.43% | python | gc_collect_region.isra.0 |
| 0.71% | python | visit_add_to_container |
| 0.52% | python | PyObject_GC_Del |
| 0.32% | python | subtype_traverse |
| 0.31% | python | dict_traverse |
| 0.27% | python | _PyObject_GC_New |
| 0.24% | python | list_traverse |
| 0.21% | python | _PyGC_Collect |
| 0.12% | python | set_traverse |
| 0.11% | python | _PyObject_GC_NewVar |
| 0.10% | python | func_traverse |
| 0.10% | python | gc_collect_main |
| 0.09% | python | gen_traverse |
| 0.06% | python | PyObject_GC_UnTrack |
| 0.05% | python | type_traverse |
| 0.03% | python | meth_traverse |
| 0.02% | python | gc_traverse |
| 0.01% | python | PyObject_GC_Track |
| 0.01% | python | context_tp_traverse |
| 0.01% | python | frame_traverse |
| 0.01% | python | PyObject_IS_GC |
| 0.01% | python | _PyTrash_end |
| 0.01% | python | descr_traverse |
| 0.01% | python | _PyTrash_begin |
| 0.01% | python | module_traverse |
| 0.01% | python | executor_traverse |
| 0.01% | python | method_traverse |

### jit

8.42% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 8.42% | [JIT] | jit |

### dynamic

5.78% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.55% | python | PyObject_GenericGetAttr |
| 0.34% | python | _PyObject_MakeTpCall |
| 0.29% | python | _PyObject_GetMethod |
| 0.26% | python | object_isinstance |
| 0.25% | python | PyObject_Free |
| 0.21% | python | PyObject_GetAttr |
| 0.21% | python | method_get |
| 0.20% | python | PyObject_Str |
| 0.16% | python | PyObject_SetAttr |
| 0.16% | python | _PySuper_Lookup |
| 0.16% | python | PyNumber_AsSsize_t |
| 0.15% | python | PyObject_Vectorcall |
| 0.15% | python | PyObject_VectorcallMethod |
| 0.14% | python | PyObject_IsTrue |
| 0.14% | python | PyType_GetModuleByDef |
| 0.13% | python | type_ready |
| 0.11% | python | _PyObject_LookupSpecial |
| 0.11% | python | PyObject_GetItem |
| 0.11% | python | PyObject_GetOptionalAttr |
| 0.10% | python | PyObject_RichCompareBool |
| 0.09% | python | PyObject_RichCompare |
| 0.09% | python | getset_get |
| 0.08% | python | type_call |
| 0.08% | python | _PyObject_GenericGetAttrWithDict |
| 0.08% | python | PyObject_Hash |
| 0.08% | python | PyObject_IsInstance |
| 0.08% | python | PyObject_GetIter |
| 0.07% | python | slot_tp_richcompare |
| 0.06% | python | _Py_type_getattro_impl |
| 0.06% | python | _PyObject_Call |
| 0.05% | python | PyObject_CallOneArg |
| 0.05% | python | PyObject_SetAttrString |
| 0.05% | python | PyMapping_GetOptionalItem |
| 0.05% | python | PyObject_SetItem |
| 0.05% | python | PyType_IsSubtype |
| 0.05% | python | _PyObject_ClearFreeLists |
| 0.05% | python | PyNumber_Multiply |
| 0.04% | python | _PyObject_VectorcallTstate.lto_priv.5 |
| 0.03% | python | object_recursive_isinstance.part.0 |
| 0.03% | python | StopIteration_init |
| 0.03% | python | PyNumber_TrueDivide |
| 0.03% | python | PyNumber_Add |
| 0.03% | python | PyIter_Send |
| 0.03% | python | PySequence_Tuple |
| 0.03% | python | PyNumber_And |
| 0.02% | python | PyObject_Size |
| 0.02% | python | PyObject_ClearWeakRefs |
| 0.02% | python | object_richcompare |
| 0.02% | python | PyNumber_Subtract |
| 0.02% | python | PyIter_Next |
| 0.02% | python | PyNumber_Remainder |
| 0.01% | python | PyObject_VisitManagedDict |
| 0.01% | python | PySequence_Contains |
| 0.01% | python | PyObject_LengthHint |
| 0.01% | python | PyNumber_FloorDivide |
| 0.01% | python | delitem_common |
| 0.01% | python | object_get_class |
| 0.01% | python | PyObject_CallFunction |
| 0.01% | python | PyNumber_Rshift |
| 0.01% | python | PyNumber_InPlaceAdd |
| 0.01% | python | _PyNumber_Index |
| 0.01% | python | PyObject_ClearManagedDict |
| 0.01% | python | PyNumber_Negative |
| 0.01% | python | PyObject_GenericHash |
| 0.01% | python | object_vacall |
| 0.01% | python | PyObject_CallMethodObjArgs |
| 0.01% | python | object_init |
| 0.01% | python | PyObject_GetBuffer |
| 0.01% | python | PyNumber_Index |
| 0.01% | python | type_dealloc_common |
| 0.01% | python | PyObject_Call |
| 0.01% | python | _PyObject_LookupAttr |
| 0.01% | python | PyObject_SelfIter |
| 0.01% | python | PyNumber_Lshift |
| 0.01% | python | _PyObject_GenericSetAttrWithDict |
| 0.01% | python | _PyNumber_PowerNoMod |
| 0.01% | python | PyObject_DelItem |
| 0.01% | python | PyObject_Malloc |

### unknown

5.32% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.28% | python | make_gen |
| 0.23% | python | slot_tp_init |
| 0.18% | python | _Py_hashtable_get |
| 0.11% | python | clear_slots |
| 0.09% | python | func_descr_get |
| 0.09% | python | _PySet_Contains |
| 0.08% | python | _PyStack_UnpackDict |
| 0.08% | python | method_vectorcall |
| 0.08% | python | _PyFrame_MakeAndSetFrameObject |
| 0.07% | python | gen_iternext |
| 0.06% | python | slot_mp_subscript |
| 0.06% | python | memcpy@plt |
| 0.06% | python | memset@plt |
| 0.06% | python | call_instrumentation_vector |
| 0.05% | python | range_vectorcall |
| 0.05% | python | _list_extend |
| 0.05% | python | range_iter |
| 0.05% | python | convert_to_double |
| 0.05% | python | builtin_min |
| 0.05% | python | _io_BytesIO_read |
| 0.04% | python | _stringio_readline.cold |
| 0.04% | python | _PyBuildSlice_Consume2 |
| 0.04% | python | slot_tp_hash |
| 0.04% | python | PySys_Audit |
| 0.04% | python | path_converter |
| 0.04% | python | as_ucs4 |
| 0.04% | python | dictkeys_decref.constprop.0 |
| 0.04% | python | _Py_module_getattro |
| 0.03% | python | builtin_hasattr |
| 0.03% | python | _PyCfg_OptimizeCodeUnit.constprop.0 |
| 0.03% | python | PySet_Add |
| 0.03% | python | builtin_sum |
| 0.03% | python | member_get |
| 0.03% | [vdso] | __vdso_clock_gettime |
| 0.03% | python | gen_send_ex2 |
| 0.03% | python | gen_send_ex |
| 0.03% | python | vectorcall_maybe.constprop.0 |
| 0.03% | python | call_one_instrument |
| 0.03% | python | state_init |
| 0.03% | python | async_gen_asend_send |
| 0.03% | python | ucs4lib_find_max_char |
| 0.03% | python | cm_descr_get |
| 0.03% | python | dictitems_iter |
| 0.03% | python | _Py_VaBuildStack.constprop.0 |
| 0.02% | python | code_hash |
| 0.02% | python | convertitem |
| 0.02% | python | unsafe_tuple_compare |
| 0.02% | python | _io_TextIOWrapper_write |
| 0.02% | python | builtin_id |
| 0.02% | python | term_raw |
| 0.02% | python | _PyAssemble_MakeCodeObject |
| 0.02% | python | bounded_lru_cache_wrapper |
| 0.02% | python | _PyCoro_GetAwaitableIter |
| 0.02% | python | range_subscript |
| 0.02% | python | get_or_create_weakref |
| 0.02% | python | hashtable_unicode_hash |
| 0.02% | python | PyContextVar_Get |
| 0.02% | python | hashtable_unicode_compare |
| 0.02% | python | bitwise_xor_rule |
| 0.02% | python | slot_mp_ass_subscript |
| 0.02% | python | builtin___import__ |
| 0.02% | python | Py_XDECREF.lto_priv.1 |
| 0.02% | python | binary_op |
| 0.02% | python | binary_op1 |
| 0.02% | python | _PyModule_ClearDict |
| 0.02% | python | wrapperdescr_call |
| 0.02% | python | optimize_uops |
| 0.02% | python | _Py_slot_tp_getattr_hook |
| 0.02% | python | member_set |
| 0.02% | python | _PyCfg_OptimizedCfgToInstructionSequence |
| 0.02% | python | make_range_object |
| 0.02% | python | do_mktuple |
| 0.02% | python | memcmp@plt |
| 0.02% | python | _PyDictKeys_StringLookup |
| 0.02% | python | build_indices_generic |
| 0.02% | python | classmethod_get |
| 0.01% | python | _PyLexer_update_fstring_expr |
| 0.01% | python | ScandirIterator_iternext |
| 0.01% | python | _Py_module_getattro_impl.part.0 |
| 0.01% | python | async_gen_unwrap_value.isra.0 |
| 0.01% | python | os_listdir |
| 0.01% | python | sum_rule |
| 0.01% | python | shift_expr_rule |
| 0.01% | python | write_bytes |
| 0.01% | python | PySet_Contains |
| 0.01% | python | get_type_attr_as_size |
| 0.01% | python | _add_methods_to_object |
| 0.01% | python | Py_XDECREF.lto_priv.7 |
| 0.01% | python | _PyBytes_Resize |
| 0.01% | python | _PyGen_FetchStopIterationValue.cold |
| 0.01% | python | ins1 |
| 0.01% | python | clear_weakref_lock_held |
| 0.01% | python | PyTime_AsSecondsDouble |
| 0.01% | python | expression_rule |
| 0.01% | python | atom_rule |
| 0.01% | python | call_trace_func.isra.0 |
| 0.01% | python | PyIndex_Check |
| 0.01% | python | _PyThreadState_GetCurrent |
| 0.01% | python | context_run |
| 0.01% | python | slot_sq_contains |
| 0.01% | python | builtin_max |
| 0.01% | python | primary_raw |
| 0.01% | python | symtable_add_def_helper |
| 0.01% | python | va_build_value |
| 0.01% | python | _io_open |
| 0.01% | python | _PyType_FromMetaclass_impl |
| 0.01% | python | mro_implementation_unlocked |
| 0.01% | python | builtin_issubclass |
| 0.01% | python | lru_cache_make_key |
| 0.01% | python | data_stack_grow |
| 0.01% | python | _Py_bytes_lower |
| 0.01% | python | builtin_sorted |
| 0.01% | python | inversion_rule |
| 0.01% | python | slot_sq_item |
| 0.01% | python | _PyContext_Exit |
| 0.01% | python | PyThread_acquire_lock_timed |
| 0.01% | python | frozenset_vectorcall |
| 0.01% | python | builtin_hash |
| 0.01% | python | _Py_call_instrumentation_jump |
| 0.01% | python | astfold_expr |
| 0.01% | python | builtin_any |
| 0.01% | python | fill_time |
| 0.01% | python | _PyCode_GetCode |
| 0.01% | python | pthread_self@plt |
| 0.01% | python | lookup_maybe_method |
| 0.01% | python | weakref_richcompare |
| 0.01% | python | update_slots_callback |
| 0.01% | python | slot_tp_iter |
| 0.01% | python | _getbytevalue |
| 0.01% | python | _PyGen_SetStopIterationValue |
| 0.01% | python | assign_version_tag |
| 0.01% | python | wrap_descr_get |
| 0.01% | python | weakref_hash |
| 0.01% | python | map_next |
| 0.01% | python | bitwise_or_rule |
| 0.01% | python | symtable_visit_expr |
| 0.01% | python | unsafe_latin_compare |
| 0.01% | python | compiler_nameop |
| 0.01% | python | unsafe_long_compare |
| 0.01% | python | find_keyword |
| 0.01% | python | compiler_visit_expr1 |
| 0.01% | python | update_slot |
| 0.01% | python | pytime_divide |
| 0.01% | python | instr_sequence_to_cfg |
| 0.01% | python | _Py_dg_dtoa |
| 0.01% | python | 0x0000000000086720 |
| 0.01% | python | term_rule |
| 0.01% | python | os_fspath |
| 0.01% | python | ascii_upper_or_lower |
| 0.01% | python | uop_optimize.cold |
| 0.01% | python | sm_descr_get |
| 0.01% | python | zip_next |
| 0.01% | python | new_dict |
| 0.01% | python | _abc__abc_instancecheck |
| 0.01% | python | _PyGen_yf |
| 0.01% | python | PyThread_get_thread_ident_ex |
| 0.01% | python | make_executor_from_uops |
| 0.01% | python | pthread_mutex_unlock@plt |
| 0.01% | python | make_dict_from_instance_attributes |
| 0.01% | python | _io_FileIO___init__ |
| 0.01% | python | primary_rule |
| 0.01% | python | islice_next |
| 0.01% | python | analyze_block |
| 0.01% | python | _loop1_104_rule |
| 0.01% | python | binary_iop1 |
| 0.01% | python | super_getattro |
| 0.01% | python | subtype_clear |
| 0.01% | python | tok_nextc |
| 0.01% | python | ucs4lib_utf8_decode |
| 0.01% | python | builtin___build_class__ |
| 0.01% | python | simple_stmt_rule |

### kernel

4.93% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.62% | [kernel.kallsyms] | copy_user_enhanced_fast_string |
| 0.27% | [kernel.kallsyms] | clear_page_erms |
| 0.15% | [kernel.kallsyms] | native_irq_return_iret |
| 0.11% | [kernel.kallsyms] | sync_regs |
| 0.10% | [kernel.kallsyms] | __d_lookup_rcu |
| 0.09% | [kernel.kallsyms] | rmqueue |
| 0.08% | [kernel.kallsyms] | _raw_spin_lock |
| 0.08% | [kernel.kallsyms] | zap_pte_range.isra.0 |
| 0.07% | [kernel.kallsyms] | free_pcppages_bulk |
| 0.06% | [kernel.kallsyms] | memset_erms |
| 0.06% | [kernel.kallsyms] | __handle_mm_fault |
| 0.05% | [kernel.kallsyms] | filemap_map_pages |
| 0.05% | [kernel.kallsyms] | try_charge |
| 0.04% | [kernel.kallsyms] | smp_call_function_single |
| 0.04% | [kernel.kallsyms] | release_pages |
| 0.04% | [kernel.kallsyms] | get_mem_cgroup_from_mm |
| 0.04% | [kernel.kallsyms] | kmem_cache_alloc |
| 0.04% | [kernel.kallsyms] | __pagevec_lru_add_fn |
| 0.04% | [kernel.kallsyms] | link_path_walk.part.0 |
| 0.04% | [kernel.kallsyms] | perf_iterate_ctx |
| 0.04% | [kernel.kallsyms] | mem_cgroup_throttle_swaprate |
| 0.04% | [kernel.kallsyms] | syscall_return_via_sysret |
| 0.03% | [kernel.kallsyms] | mem_cgroup_try_charge |
| 0.03% | [kernel.kallsyms] | handle_mm_fault |
| 0.03% | [kernel.kallsyms] | __alloc_pages_nodemask |
| 0.03% | [kernel.kallsyms] | ext4_htree_store_dirent |
| 0.03% | [kernel.kallsyms] | kmem_cache_free |
| 0.03% | [kernel.kallsyms] | __ext4fs_dirhash |
| 0.03% | [kernel.kallsyms] | page_remove_rmap |
| 0.03% | [kernel.kallsyms] | memcg_kmem_get_cache |
| 0.03% | [kernel.kallsyms] | find_vma |
| 0.03% | [kernel.kallsyms] | entry_SYSCALL_64 |
| 0.02% | [kernel.kallsyms] | copy_page |
| 0.02% | [kernel.kallsyms] | filldir64 |
| 0.02% | [kernel.kallsyms] | perf_event_alloc |
| 0.02% | [kernel.kallsyms] | do_user_addr_fault |
| 0.02% | [kernel.kallsyms] | strncpy_from_user |
| 0.02% | [kernel.kallsyms] | find_get_entry |
| 0.02% | [kernel.kallsyms] | kfree |
| 0.02% | [kernel.kallsyms] | lookup_fast |
| 0.02% | [kernel.kallsyms] | do_syscall_64 |
| 0.02% | [kernel.kallsyms] | inode_permission |
| 0.02% | [kernel.kallsyms] | __virt_addr_valid |
| 0.02% | [kernel.kallsyms] | memcpy_erms |
| 0.02% | [kernel.kallsyms] | do_anonymous_page |
| 0.02% | [kernel.kallsyms] | unmapped_area_topdown |
| 0.02% | [kernel.kallsyms] | _raw_spin_lock_irqsave |
| 0.02% | [kernel.kallsyms] | native_flush_tlb_one_user |
| 0.02% | [kernel.kallsyms] | get_page_from_freelist |
| 0.02% | [kernel.kallsyms] | prep_new_page |
| 0.02% | [kernel.kallsyms] | rb_next |
| 0.02% | [kernel.kallsyms] | vmacache_find |
| 0.02% | [kernel.kallsyms] | __count_memcg_events |
| 0.02% | [kernel.kallsyms] | page_fault |
| 0.02% | [kernel.kallsyms] | generic_permission |
| 0.02% | [kernel.kallsyms] | rb_insert_color |
| 0.02% | [kernel.kallsyms] | walk_component |
| 0.02% | [kernel.kallsyms] | error_entry |
| 0.02% | [kernel.kallsyms] | __fget_light |
| 0.01% | [kernel.kallsyms] | __slab_free |
| 0.01% | [kernel.kallsyms] | ext4_getattr |
| 0.01% | [kernel.kallsyms] | __mod_memcg_state |
| 0.01% | [kernel.kallsyms] | str2hashbuf_signed |
| 0.01% | [kernel.kallsyms] | __mod_lruvec_state |
| 0.01% | [kernel.kallsyms] | _cond_resched |
| 0.01% | [kernel.kallsyms] | entry_SYSCALL_64_after_hwframe |
| 0.01% | [kernel.kallsyms] | psi_task_change |
| 0.01% | [kernel.kallsyms] | __vma_adjust |
| 0.01% | [kernel.kallsyms] | up_read |
| 0.01% | [kernel.kallsyms] | __perf_addr_filters_adjust |
| 0.01% | [kernel.kallsyms] | lru_cache_add_active_or_unevictable |
| 0.01% | [kernel.kallsyms] | free_unref_page_prepare.part.0 |
| 0.01% | [kernel.kallsyms] | __lru_cache_add |
| 0.01% | [kernel.kallsyms] | xas_load |
| 0.01% | [kernel.kallsyms] | security_inode_getattr |
| 0.01% | [kernel.kallsyms] | tcp_sendmsg_locked |
| 0.01% | [kernel.kallsyms] | page_add_file_rmap |
| 0.01% | [kernel.kallsyms] | down_read_trylock |
| 0.01% | [kernel.kallsyms] | perf_event_mmap |
| 0.01% | [kernel.kallsyms] | pagevec_lru_move_fn |
| 0.01% | [kernel.kallsyms] | __check_object_size |
| 0.01% | [kernel.kallsyms] | set_root |
| 0.01% | [kernel.kallsyms] | generic_file_buffered_read |
| 0.01% | [kernel.kallsyms] | __kmalloc |
| 0.01% | [kernel.kallsyms] | alloc_pages_vma |
| 0.01% | [kernel.kallsyms] | swapgs_restore_regs_and_return_to_usermode |
| 0.01% | [kernel.kallsyms] | fsnotify |
| 0.01% | [kernel.kallsyms] | __mod_node_page_state |
| 0.01% | [kernel.kallsyms] | rcu_all_qs |
| 0.01% | [kernel.kallsyms] | ___slab_alloc |
| 0.01% | [kernel.kallsyms] | __lock_text_start |
| 0.01% | [kernel.kallsyms] | memcg_kmem_put_cache |
| 0.01% | [kernel.kallsyms] | fpregs_assert_state_consistent |
| 0.01% | [kernel.kallsyms] | format_decode |
| 0.01% | [kernel.kallsyms] | free_pages_and_swap_cache |
| 0.01% | [kernel.kallsyms] | native_write_msr |
| 0.01% | [kernel.kallsyms] | show_cpuinfo |
| 0.01% | [kernel.kallsyms] | mem_cgroup_commit_charge |
| 0.01% | [kernel.kallsyms] | __mod_zone_page_state |
| 0.01% | [kernel.kallsyms] | free_unref_page_list |
| 0.01% | [kernel.kallsyms] | perf_iterate_sb |
| 0.01% | [kernel.kallsyms] | alloc_set_pte |
| 0.01% | [kernel.kallsyms] | update_curr |
| 0.01% | [kernel.kallsyms] | kmem_cache_alloc_trace |
| 0.01% | [kernel.kallsyms] | page_counter_cancel |
| 0.01% | [kernel.kallsyms] | __follow_mount_rcu.isra.0 |
| 0.01% | [kernel.kallsyms] | vsnprintf |
| 0.01% | [kernel.kallsyms] | mem_cgroup_from_task |
| 0.01% | [kernel.kallsyms] | __legitimize_mnt |
| 0.01% | [kernel.kallsyms] | __ext4_check_dir_entry |
| 0.01% | [kernel.kallsyms] | unlock_page |
| 0.01% | [kernel.kallsyms] | security_inode_permission |
| 0.01% | [kernel.kallsyms] | mmap_region |
| 0.01% | [kernel.kallsyms] | vma_interval_tree_insert |
| 0.01% | [kernel.kallsyms] | in_group_p |
| 0.01% | [kernel.kallsyms] | free_unref_page_commit |
| 0.01% | [kernel.kallsyms] | __vma_link_rb |
| 0.01% | [kernel.kallsyms] | update_cfs_group |
| 0.01% | [kernel.kallsyms] | up_write |
| 0.01% | [kernel.kallsyms] | memchr |
| 0.01% | [kernel.kallsyms] | mem_cgroup_try_charge_delay |
| 0.01% | [kernel.kallsyms] | xas_start |
| 0.01% | [kernel.kallsyms] | __update_load_avg_se |
| 0.01% | [kernel.kallsyms] | __check_heap_object |
| 0.01% | [kernel.kallsyms] | call_filldir |
| 0.01% | [kernel.kallsyms] | down_write |
| 0.01% | [kernel.kallsyms] | __free_pages_ok |
| 0.01% | [kernel.kallsyms] | kthread_blkcg |
| 0.01% | [kernel.kallsyms] | native_sched_clock |
| 0.01% | [kernel.kallsyms] | mutex_lock |
| 0.01% | [kernel.kallsyms] | __alloc_file |
| 0.01% | [kernel.kallsyms] | page_counter_try_charge |
| 0.01% | [kernel.kallsyms] | string_nocheck |
| 0.01% | [kernel.kallsyms] | update_load_avg |
| 0.01% | [kernel.kallsyms] | skb_release_data |
| 0.01% | [kernel.kallsyms] | __fput |
| 0.01% | [kernel.kallsyms] | __tcp_transmit_skb |
| 0.01% | [kernel.kallsyms] | do_dentry_open |
| 0.01% | [kernel.kallsyms] | vfs_getattr_nosec |

### dict

3.69% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.62% | python | PyDict_GetItemRef |
| 0.47% | python | dict_setdefault_ref_lock_held |
| 0.42% | python | insertdict |
| 0.34% | python | PyDict_SetItem |
| 0.29% | python | dict_get |
| 0.23% | python | dictresize |
| 0.20% | python | PyDict_Next |
| 0.20% | python | insert_to_emptydict |
| 0.16% | python | PyDict_Contains |
| 0.11% | python | _PyDict_LoadGlobal |
| 0.10% | python | dict_subscript |
| 0.07% | python | dictiter_iternextitem |
| 0.06% | python | dict_merge |
| 0.04% | python | PyDict_GetItemWithError |
| 0.04% | python | _PyDict_SetItem_Take2 |
| 0.04% | python | _PyDict_GetItem_KnownHash |
| 0.04% | python | dict_items |
| 0.03% | python | dict_ass_sub |
| 0.03% | python | PyDict_Copy |
| 0.02% | python | _PyDict_FromItems |
| 0.02% | python | PyDict_DelItem |
| 0.02% | python | _PyDict_Next |
| 0.02% | python | dict_getitem |
| 0.01% | python | dictiter_iternextkey |
| 0.01% | python | dictiter_iternextvalue |
| 0.01% | python | free_keys_object |
| 0.01% | python | PyDict_SetItemString |

### libc

3.64% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 2.30% | libc-2.31.so | __nss_database_lookup |
| 0.50% | libc-2.31.so | pthread_attr_setschedparam |
| 0.30% | libcrypto.so.1.1 | CRYPTO_secure_actual_size |
| 0.13% | libc-2.31.so | malloc |
| 0.04% | libc-2.31.so | free |
| 0.03% | libc-2.31.so | __gconv_get_alias_db |
| 0.02% | libc-2.31.so | wcsrtombs |
| 0.02% | libc-2.31.so | pthread_self |
| 0.02% | libc-2.31.so | pthread_mutex_lock |
| 0.02% | libc-2.31.so | __errno_location |
| 0.02% | libc-2.31.so | clock_gettime |
| 0.02% | libc-2.31.so | __libc_realloc |
| 0.01% | libc-2.31.so | pthread_mutex_unlock |
| 0.01% | libc-2.31.so | _dl_addr |
| 0.01% | libc-2.31.so | pthread_cond_signal |
| 0.01% | libc-2.31.so | __xstat |
| 0.01% | libc-2.31.so | __wcsncasecmp_l |
| 0.01% | libc-2.31.so | psiginfo |

### int

3.49% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.71% | python | k_mul |
| 0.48% | python | _PyLong_Add |
| 0.38% | python | x_divrem |
| 0.29% | python | PyLong_FromLong |
| 0.23% | python | long_hash |
| 0.20% | python | x_add |
| 0.14% | python | _PyLong_Subtract |
| 0.09% | python | long_bitwise |
| 0.09% | python | x_sub |
| 0.09% | python | PyLong_AsLongAndOverflow |
| 0.08% | python | long_richcompare |
| 0.08% | python | PyLong_FromString |
| 0.07% | python | _PyLong_Multiply |
| 0.06% | python | long_div |
| 0.06% | python | long_and |
| 0.06% | python | long_rshift |
| 0.06% | python | long_to_decimal_string |
| 0.04% | python | long_mod |
| 0.03% | python | long_mul |
| 0.03% | python | PyLong_FromUnsignedLongLong |
| 0.03% | python | PyLong_FromSsize_t |
| 0.02% | python | long_lshift |
| 0.02% | python | long_to_decimal_string_internal |
| 0.02% | python | _PyLong_FromBytes |
| 0.01% | python | PyLong_FromUnsignedLong |
| 0.01% | python | PyLong_AsLong |
| 0.01% | python | _PyLong_GCD |
| 0.01% | python | PyLong_AsSsize_t |
| 0.01% | python | long_xor |
| 0.01% | python | _PyLong_Lshift |
| 0.01% | python | PyLong_AsDouble.part.0 |
| 0.01% | python | long_vectorcall |
| 0.01% | python | PyLong_FromUnicodeObject |
| 0.01% | python | long_add |

### str

3.23% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.50% | python | siphash13 |
| 0.43% | python | unicode_decode_utf8 |
| 0.26% | python | PyUnicode_FromKindAndData |
| 0.25% | python | PyUnicode_Substring |
| 0.19% | python | _PyUnicode_JoinArray |
| 0.14% | python | PyBytes_FromStringAndSize |
| 0.11% | python | unicode_replace |
| 0.09% | python | _PyUnicodeWriter_PrepareInternal |
| 0.08% | python | PyUnicode_Format |
| 0.07% | python | _PyUnicodeWriter_WriteStr |
| 0.06% | python | PyUnicode_Concat |
| 0.06% | python | PyUnicode_FromFormatV |
| 0.06% | python | _PyUnicode_InternInPlace |
| 0.05% | python | unicode_subscript |
| 0.05% | python | PyUnicode_RichCompare |
| 0.05% | python | PyUnicode_FSConverter |
| 0.04% | python | bytes_subscript |
| 0.04% | python | unicode_hash |
| 0.04% | python | PyUnicode_Contains |
| 0.04% | python | _PyUnicode_FromUCS4 |
| 0.04% | python | _PyUnicode_Equal |
| 0.03% | python | unicode_encode |
| 0.03% | python | bytes_concat |
| 0.03% | python | PyUnicode_AsUTF8AndSize |
| 0.03% | python | unicode_encode_utf8 |
| 0.02% | python | stringlib_bytes_join.lto_priv.1 |
| 0.02% | python | resize_compact |
| 0.02% | python | _PyUnicode_FromASCII |
| 0.02% | python | unicode_startswith |
| 0.02% | python | unicode_split |
| 0.02% | python | PyUnicode_FromWideChar |
| 0.01% | python | unicode_join |
| 0.01% | python | unicode_repr |
| 0.01% | python | PyBytes_Repr |
| 0.01% | python | PyUnicode_DecodeFSDefault |
| 0.01% | python | _PyUnicodeWriter_Finish |
| 0.01% | python | replace |
| 0.01% | python | _PyUnicodeWriter_Init |
| 0.01% | python | bytes_decode |
| 0.01% | python | bytes_richcompare |
| 0.01% | python | unicode_rstrip |
| 0.01% | python | _PyUnicode_IsAlpha |
| 0.01% | python | unicode_splitlines |
| 0.01% | python | split |
| 0.01% | python | PyUnicode_InternInPlace |
| 0.01% | python | unicode_rfind |
| 0.01% | python | unicode_strip |
| 0.01% | python | _PyUnicode_FromUCS1.part.0 |
| 0.01% | python | PyUnicode_RPartition |
| 0.01% | python | _PyUnicode_TranslateCharmap |
| 0.01% | python | unicode_find |

### list

1.18% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.23% | python | list_subscript |
| 0.17% | python | list_ass_slice_lock_held |
| 0.16% | python | list_iter |
| 0.12% | python | list_resize |
| 0.06% | python | PyList_SetSlice |
| 0.06% | python | list_contains |
| 0.04% | python | list_sort_impl |
| 0.04% | python | PyList_Append |
| 0.04% | python | list_ass_subscript |
| 0.04% | python | list_append |
| 0.03% | python | list_vectorcall |
| 0.03% | python | list_concat |
| 0.03% | python | listiter_next |
| 0.02% | python | _PyList_FromArraySteal |
| 0.02% | python | list_pop |
| 0.01% | python | PyList_Size |
| 0.01% | python | _PyList_AppendTakeRefListResize |
| 0.01% | python | list_clear_impl.constprop.0 |
| 0.01% | python | list_richcompare |
| 0.01% | python | list_length |

### lookup

1.16% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.29% | python | unicodekeys_lookup_unicode |
| 0.28% | python | find_name_in_mro |
| 0.24% | python | _Py_type_getattro |
| 0.24% | python | _Py_dict_lookup |
| 0.06% | python | _PyType_Lookup |
| 0.03% | python | builtin_getattr |
| 0.02% | python | update_one_slot |

### tuple

1.10% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.49% | python | tuplehash |
| 0.20% | python | _PyTuple_FromArraySteal |
| 0.12% | python | tupletraverse |
| 0.07% | python | tuple_iter |
| 0.06% | python | tuplerichcompare |
| 0.05% | python | PyTuple_Pack |
| 0.03% | python | tuplecontains |
| 0.03% | python | _PyTuple_FromArray |
| 0.01% | python | tuplesubscript |
| 0.01% | python | tupleiter_next |
| 0.01% | python | _PyTuple_Resize |
| 0.01% | python | PyTuple_Size |

### miscobj

0.99% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.10% | python | set_lookkey |
| 0.09% | python | set_issubset_impl |
| 0.09% | python | setiter_iternext |
| 0.07% | python | set_vectorcall |
| 0.06% | python | _PyBuildSlice_ConsumeRefs |
| 0.06% | python | enum_next |
| 0.06% | python | set_difference |
| 0.06% | python | PySlice_Unpack |
| 0.05% | python | set_contains_lock_held |
| 0.04% | python | set_add |
| 0.03% | python | set_table_resize |
| 0.03% | python | deque_append_lock_held |
| 0.02% | python | set_add_entry |
| 0.02% | python | dequeiter_next_lock_held.isra.0 |
| 0.02% | python | bytearray_ass_subscript |
| 0.02% | python | PySlice_AdjustIndices |
| 0.01% | python | set_merge_lock_held.part.0 |
| 0.01% | python | deque_append_impl |
| 0.01% | python | deque_popleft_impl |
| 0.01% | python | set_intersection |
| 0.01% | python | PyBuffer_Release |
| 0.01% | python | deque_clear |
| 0.01% | python | PyBool_FromLong |
| 0.01% | python | _PySlice_GetLongIndices |

### calls

0.86% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.33% | python | _PyFunction_Vectorcall |
| 0.08% | python | vgetargs1_impl |
| 0.07% | python | vgetargskeywords.constprop.0 |
| 0.06% | python | vectorcall_method |
| 0.05% | python | _PyArg_UnpackKeywords |
| 0.03% | python | method_vectorcall_VARARGS_KEYWORDS |
| 0.02% | python | PyArg_UnpackTuple |
| 0.02% | python | cfunction_vectorcall_NOARGS |
| 0.02% | python | cfunction_vectorcall_FASTCALL_KEYWORDS |
| 0.02% | python | cfunction_vectorcall_O |
| 0.02% | python | method_vectorcall_FASTCALL_KEYWORDS_METHOD |
| 0.02% | python | _Py_CheckFunctionResult |
| 0.02% | python | method_vectorcall_NOARGS |
| 0.01% | python | cfunction_call |
| 0.01% | python | method_vectorcall_VARARGS |
| 0.01% | python | _PyArg_UnpackKeywordsWithVararg |
| 0.01% | python | PyArg_ParseTupleAndKeywords |
| 0.01% | python | method_vectorcall_FASTCALL |
| 0.01% | python | PyArg_Parse |
| 0.01% | python | method_vectorcall_O |
| 0.01% | python | cfunction_vectorcall_FASTCALL_KEYWORDS_METHOD |
| 0.01% | python | PyArg_ParseTuple |

### exceptions

0.43% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.13% | python | _PyErr_SetObject |
| 0.07% | python | PyTraceBack_Here |
| 0.07% | python | PyCode_Addr2Line |
| 0.03% | python | PyErr_GivenExceptionMatches |
| 0.03% | python | PyErr_ExceptionMatches |
| 0.02% | python | BaseException_init |
| 0.02% | python | PyErr_Occurred |
| 0.01% | python | PyErr_Format |
| 0.01% | python | AttributeError_init |

### float

0.40% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.16% | python | PyFloat_FromDouble |
| 0.08% | python | float_div |
| 0.03% | python | float_richcompare |
| 0.03% | python | float_mul |
| 0.03% | python | PyFloat_AsDouble |
| 0.02% | python | float_sub |
| 0.02% | python | float_pow |
| 0.01% | python | float_add |

### import

0.39% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.35% | python | r_object |
| 0.02% | python | PyImport_ImportModuleLevelObject |

### compiler

0.13% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.08% | python | uop_optimize |
| 0.05% | python | _PyJIT_Compile |

### gil

0.00% total

| percentage | object | symbol |
| ---: | :--- | :--- |
