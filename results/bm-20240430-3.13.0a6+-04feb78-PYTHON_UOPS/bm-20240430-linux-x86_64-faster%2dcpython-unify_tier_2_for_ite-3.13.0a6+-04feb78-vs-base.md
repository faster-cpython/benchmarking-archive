# Results vs. base

- fork: faster-cpython
- ref: unify_tier_2_for_ite
- machine: linux-x86_64
- commit hash: 04feb78
- commit date: 2024-04-30
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 334 ms                                                                 | 321 ms: 1.04x faster                                                             |
| chameleon      | 8.59 ms                                                                | 7.94 ms: 1.08x faster                                                            |
| docutils       | 3.25 sec                                                               | 3.19 sec: 1.02x faster                                                           |
| html5lib       | 80.6 ms                                                                | 76.3 ms: 1.06x faster                                                            |
| tornado_http   | 105 ms                                                                 | 104 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none           | 389 ms                                                                 | 373 ms: 1.04x faster                                                             |
| async_tree_memoization    | 520 ms                                                                 | 499 ms: 1.04x faster                                                             |
| async_tree_io             | 998 ms                                                                 | 964 ms: 1.04x faster                                                             |
| async_tree_none_tg        | 362 ms                                                                 | 350 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed   | 652 ms                                                                 | 633 ms: 1.03x faster                                                             |
| async_tree_memoization_tg | 471 ms                                                                 | 457 ms: 1.03x faster                                                             |
| Geometric mean            | (ref)                                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (2): async_tree_io_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 93.6 ms                                                                | 91.9 ms: 1.02x faster                                                            |
| pidigits       | 192 ms                                                                 | 213 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 198 ms                                                                 | 181 ms: 1.09x faster                                                             |
| regex_v8       | 25.6 ms                                                                | 25.0 ms: 1.03x faster                                                            |
| regex_dna      | 222 ms                                                                 | 221 ms: 1.00x faster                                                             |
| regex_effbot   | 3.61 ms                                                                | 3.68 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 324 us                                                                 | 286 us: 1.13x faster                                                             |
| tomli_loads          | 2.71 sec                                                               | 2.54 sec: 1.07x faster                                                           |
| pickle_dict          | 35.6 us                                                                | 35.2 us: 1.01x faster                                                            |
| pickle_list          | 5.01 us                                                                | 5.02 us: 1.00x slower                                                            |
| xml_etree_generate   | 96.0 ms                                                                | 96.3 ms: 1.00x slower                                                            |
| json_loads           | 27.5 us                                                                | 27.7 us: 1.00x slower                                                            |
| pickle               | 12.1 us                                                                | 12.1 us: 1.00x slower                                                            |
| xml_etree_process    | 67.0 ms                                                                | 67.5 ms: 1.01x slower                                                            |
| pickle_pure_python   | 317 us                                                                 | 321 us: 1.01x slower                                                             |
| unpickle_list        | 5.15 us                                                                | 5.28 us: 1.02x slower                                                            |
| unpickle             | 15.5 us                                                                | 16.5 us: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_iterparse, json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.14 ms                                                                | 7.17 ms: 1.01x slower                                                            |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 38.2 ms                                                                | 31.2 ms: 1.22x faster                                                            |
| genshi_xml      | 79.2 ms                                                                | 70.8 ms: 1.12x faster                                                            |
| django_template | 44.7 ms                                                                | 40.7 ms: 1.10x faster                                                            |
| mako            | 13.9 ms                                                                | 14.0 ms: 1.00x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                                     |

All benchmarks:
===============

| Benchmark                 | bm-20240430-linux-x86_64-python-11cbf77f9799e86603bc-3.13.0a6+-11cbf77 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| spectral_norm             | 196 ms                                                                 | 137 ms: 1.43x faster                                                             |
| nqueens                   | 140 ms                                                                 | 109 ms: 1.29x faster                                                             |
| pprint_pformat            | 2.49 sec                                                               | 2.00 sec: 1.25x faster                                                           |
| pprint_safe_repr          | 1.20 sec                                                               | 965 ms: 1.24x faster                                                             |
| genshi_text               | 38.2 ms                                                                | 31.2 ms: 1.22x faster                                                            |
| typing_runtime_protocols  | 218 us                                                                 | 190 us: 1.15x faster                                                             |
| unpickle_pure_python      | 324 us                                                                 | 286 us: 1.13x faster                                                             |
| genshi_xml                | 79.2 ms                                                                | 70.8 ms: 1.12x faster                                                            |
| django_template           | 44.7 ms                                                                | 40.7 ms: 1.10x faster                                                            |
| deepcopy_memo             | 49.8 us                                                                | 45.5 us: 1.09x faster                                                            |
| raytrace                  | 365 ms                                                                 | 334 ms: 1.09x faster                                                             |
| regex_compile             | 198 ms                                                                 | 181 ms: 1.09x faster                                                             |
| logging_format            | 7.73 us                                                                | 7.09 us: 1.09x faster                                                            |
| logging_simple            | 7.01 us                                                                | 6.44 us: 1.09x faster                                                            |
| deltablue                 | 4.65 ms                                                                | 4.29 ms: 1.08x faster                                                            |
| sqlglot_optimize          | 70.5 ms                                                                | 65.0 ms: 1.08x faster                                                            |
| comprehensions            | 26.7 us                                                                | 24.6 us: 1.08x faster                                                            |
| chameleon                 | 8.59 ms                                                                | 7.94 ms: 1.08x faster                                                            |
| sqlglot_normalize         | 139 ms                                                                 | 129 ms: 1.08x faster                                                             |
| chaos                     | 84.5 ms                                                                | 78.6 ms: 1.08x faster                                                            |
| scimark_monte_carlo       | 95.9 ms                                                                | 89.5 ms: 1.07x faster                                                            |
| tomli_loads               | 2.71 sec                                                               | 2.54 sec: 1.07x faster                                                           |
| go                        | 216 ms                                                                 | 203 ms: 1.06x faster                                                             |
| sqlglot_parse             | 1.58 ms                                                                | 1.49 ms: 1.06x faster                                                            |
| html5lib                  | 80.6 ms                                                                | 76.3 ms: 1.06x faster                                                            |
| pyflate                   | 628 ms                                                                 | 595 ms: 1.05x faster                                                             |
| bench_thread_pool         | 961 us                                                                 | 912 us: 1.05x faster                                                             |
| hexiom                    | 10.3 ms                                                                | 9.77 ms: 1.05x faster                                                            |
| meteor_contest            | 128 ms                                                                 | 122 ms: 1.05x faster                                                             |
| sqlglot_transpile         | 1.91 ms                                                                | 1.82 ms: 1.05x faster                                                            |
| mdp                       | 2.95 sec                                                               | 2.82 sec: 1.05x faster                                                           |
| richards_super            | 69.6 ms                                                                | 66.5 ms: 1.05x faster                                                            |
| async_tree_none           | 389 ms                                                                 | 373 ms: 1.04x faster                                                             |
| async_tree_memoization    | 520 ms                                                                 | 499 ms: 1.04x faster                                                             |
| pycparser                 | 1.33 sec                                                               | 1.28 sec: 1.04x faster                                                           |
| sympy_integrate           | 25.2 ms                                                                | 24.2 ms: 1.04x faster                                                            |
| 2to3                      | 334 ms                                                                 | 321 ms: 1.04x faster                                                             |
| telco                     | 9.67 ms                                                                | 9.32 ms: 1.04x faster                                                            |
| crypto_pyaes              | 92.9 ms                                                                | 89.6 ms: 1.04x faster                                                            |
| pathlib                   | 18.8 ms                                                                | 18.2 ms: 1.04x faster                                                            |
| async_tree_io             | 998 ms                                                                 | 964 ms: 1.04x faster                                                             |
| deepcopy                  | 403 us                                                                 | 389 us: 1.04x faster                                                             |
| async_tree_none_tg        | 362 ms                                                                 | 350 ms: 1.03x faster                                                             |
| sympy_str                 | 343 ms                                                                 | 332 ms: 1.03x faster                                                             |
| scimark_sparse_mat_mult   | 6.16 ms                                                                | 5.97 ms: 1.03x faster                                                            |
| richards                  | 61.6 ms                                                                | 59.7 ms: 1.03x faster                                                            |
| sympy_expand              | 579 ms                                                                 | 561 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed   | 652 ms                                                                 | 633 ms: 1.03x faster                                                             |
| async_tree_memoization_tg | 471 ms                                                                 | 457 ms: 1.03x faster                                                             |
| dulwich_log               | 77.1 ms                                                                | 75.1 ms: 1.03x faster                                                            |
| regex_v8                  | 25.6 ms                                                                | 25.0 ms: 1.03x faster                                                            |
| thrift                    | 851 us                                                                 | 831 us: 1.02x faster                                                             |
| mypy2                     | 861 ms                                                                 | 842 ms: 1.02x faster                                                             |
| asyncio_tcp               | 539 ms                                                                 | 528 ms: 1.02x faster                                                             |
| docutils                  | 3.25 sec                                                               | 3.19 sec: 1.02x faster                                                           |
| float                     | 93.6 ms                                                                | 91.9 ms: 1.02x faster                                                            |
| sympy_sum                 | 182 ms                                                                 | 179 ms: 1.02x faster                                                             |
| scimark_fft               | 453 ms                                                                 | 445 ms: 1.02x faster                                                             |
| fannkuch                  | 489 ms                                                                 | 481 ms: 1.02x faster                                                             |
| generators                | 31.7 ms                                                                | 31.2 ms: 1.02x faster                                                            |
| dask                      | 391 ms                                                                 | 386 ms: 1.01x faster                                                             |
| aiohttp                   | 1.27 ms                                                                | 1.26 ms: 1.01x faster                                                            |
| pickle_dict               | 35.6 us                                                                | 35.2 us: 1.01x faster                                                            |
| async_generators          | 482 ms                                                                 | 476 ms: 1.01x faster                                                             |
| tornado_http              | 105 ms                                                                 | 104 ms: 1.01x faster                                                             |
| json                      | 5.21 ms                                                                | 5.16 ms: 1.01x faster                                                            |
| scimark_sor               | 161 ms                                                                 | 159 ms: 1.01x faster                                                             |
| sqlite_synth              | 3.05 us                                                                | 3.03 us: 1.01x faster                                                            |
| asyncio_tcp_ssl           | 1.88 sec                                                               | 1.87 sec: 1.01x faster                                                           |
| regex_dna                 | 222 ms                                                                 | 221 ms: 1.00x faster                                                             |
| mako                      | 13.9 ms                                                                | 14.0 ms: 1.00x slower                                                            |
| pickle_list               | 5.01 us                                                                | 5.02 us: 1.00x slower                                                            |
| xml_etree_generate        | 96.0 ms                                                                | 96.3 ms: 1.00x slower                                                            |
| create_gc_cycles          | 1.77 ms                                                                | 1.78 ms: 1.00x slower                                                            |
| json_loads                | 27.5 us                                                                | 27.7 us: 1.00x slower                                                            |
| pickle                    | 12.1 us                                                                | 12.1 us: 1.00x slower                                                            |
| python_startup_no_site    | 7.14 ms                                                                | 7.17 ms: 1.01x slower                                                            |
| python_startup            | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| scimark_lu                | 167 ms                                                                 | 168 ms: 1.01x slower                                                             |
| xml_etree_process         | 67.0 ms                                                                | 67.5 ms: 1.01x slower                                                            |
| pickle_pure_python        | 317 us                                                                 | 321 us: 1.01x slower                                                             |
| coroutines                | 24.0 ms                                                                | 24.3 ms: 1.01x slower                                                            |
| logging_silent            | 106 ns                                                                 | 108 ns: 1.02x slower                                                             |
| regex_effbot              | 3.61 ms                                                                | 3.68 ms: 1.02x slower                                                            |
| coverage                  | 91.8 ms                                                                | 93.6 ms: 1.02x slower                                                            |
| unpickle_list             | 5.15 us                                                                | 5.28 us: 1.02x slower                                                            |
| unpickle                  | 15.5 us                                                                | 16.5 us: 1.06x slower                                                            |
| pidigits                  | 192 ms                                                                 | 213 ms: 1.11x slower                                                             |
| gc_traversal              | 3.65 ms                                                                | 4.06 ms: 1.11x slower                                                            |
| Geometric mean            | (ref)                                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (12): async_tree_io_tg, pylint, async_tree_cpu_io_mixed_tg, gunicorn, xml_etree_iterparse, bench_mp_pool, json_dumps, deepcopy_reduce, asyncio_websockets, nbody, xml_etree_parse, djangocms

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x