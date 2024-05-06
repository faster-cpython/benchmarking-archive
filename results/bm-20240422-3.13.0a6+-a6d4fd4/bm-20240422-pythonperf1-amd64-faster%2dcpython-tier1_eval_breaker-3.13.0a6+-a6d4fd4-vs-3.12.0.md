# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-amd64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 213 ms: 1.03x faster                                                                |
| docutils       | 1.66 sec                                                    | 1.65 sec: 1.01x faster                                                              |
| tornado_http   | 89.5 ms                                                     | 81.8 ms: 1.09x faster                                                               |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                        |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 271 ms: 1.35x faster                                                                |
| async_tree_none            | 291 ms                                                      | 224 ms: 1.30x faster                                                                |
| async_tree_none_tg         | 285 ms                                                      | 220 ms: 1.30x faster                                                                |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 387 ms: 1.30x faster                                                                |
| async_tree_io_tg           | 771 ms                                                      | 619 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 394 ms: 1.24x faster                                                                |
| async_tree_memoization     | 339 ms                                                      | 274 ms: 1.24x faster                                                                |
| async_tree_io              | 731 ms                                                      | 597 ms: 1.22x faster                                                                |
| Geometric mean             | (ref)                                                       | 1.27x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 51.7 ms: 1.10x faster                                                               |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                                |
| nbody          | 71.9 ms                                                     | 69.8 ms: 1.03x faster                                                               |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 80.5 ms: 1.09x faster                                                               |
| regex_dna      | 126 ms                                                      | 121 ms: 1.04x faster                                                                |
| regex_v8       | 14.2 ms                                                     | 16.1 ms: 1.13x slower                                                               |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                        |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|---------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pickle_pure_python  | 195 us                                                      | 184 us: 1.06x faster                                                                |
| xml_etree_parse     | 93.0 ms                                                     | 90.2 ms: 1.03x faster                                                               |
| pickle              | 7.43 us                                                     | 7.24 us: 1.03x faster                                                               |
| xml_etree_iterparse | 65.2 ms                                                     | 63.9 ms: 1.02x faster                                                               |
| xml_etree_generate  | 55.8 ms                                                     | 55.0 ms: 1.02x faster                                                               |
| json_loads          | 13.9 us                                                     | 13.8 us: 1.01x faster                                                               |
| json_dumps          | 5.70 ms                                                     | 5.66 ms: 1.01x faster                                                               |
| xml_etree_process   | 37.7 ms                                                     | 37.9 ms: 1.01x slower                                                               |
| tomli_loads         | 1.37 sec                                                    | 1.40 sec: 1.02x slower                                                              |
| pickle_dict         | 18.4 us                                                     | 18.8 us: 1.02x slower                                                               |
| pickle_list         | 2.83 us                                                     | 2.92 us: 1.03x slower                                                               |
| unpickle            | 8.18 us                                                     | 8.49 us: 1.04x slower                                                               |
| Geometric mean      | (ref)                                                       | 1.00x faster                                                                        |

Benchmark hidden because not significant (2): unpickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup | 19.5 ms                                                     | 19.8 ms: 1.02x slower                                                               |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                        |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.56 ms: 1.08x faster                                                               |
| django_template | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                               |
| Geometric mean  | (ref)                                                       | 1.05x faster                                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 271 ms: 1.35x faster                                                                |
| async_tree_none            | 291 ms                                                      | 224 ms: 1.30x faster                                                                |
| async_tree_none_tg         | 285 ms                                                      | 220 ms: 1.30x faster                                                                |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 387 ms: 1.30x faster                                                                |
| typing_runtime_protocols   | 95.1 us                                                     | 74.8 us: 1.27x faster                                                               |
| comprehensions             | 14.1 us                                                     | 11.2 us: 1.26x faster                                                               |
| async_tree_io_tg           | 771 ms                                                      | 619 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 394 ms: 1.24x faster                                                                |
| async_tree_memoization     | 339 ms                                                      | 274 ms: 1.24x faster                                                                |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.70 sec: 1.23x faster                                                              |
| async_tree_io              | 731 ms                                                      | 597 ms: 1.22x faster                                                                |
| raytrace                   | 192 ms                                                      | 160 ms: 1.20x faster                                                                |
| mypy2                      | 509 ms                                                      | 424 ms: 1.20x faster                                                                |
| chaos                      | 43.3 ms                                                     | 39.0 ms: 1.11x faster                                                               |
| float                      | 56.8 ms                                                     | 51.7 ms: 1.10x faster                                                               |
| dulwich_log                | 44.3 ms                                                     | 40.5 ms: 1.09x faster                                                               |
| tornado_http               | 89.5 ms                                                     | 81.8 ms: 1.09x faster                                                               |
| regex_compile              | 87.5 ms                                                     | 80.5 ms: 1.09x faster                                                               |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                               |
| bench_mp_pool              | 69.2 ms                                                     | 64.0 ms: 1.08x faster                                                               |
| mako                       | 7.09 ms                                                     | 6.56 ms: 1.08x faster                                                               |
| deltablue                  | 2.16 ms                                                     | 2.00 ms: 1.08x faster                                                               |
| sympy_sum                  | 91.5 ms                                                     | 85.0 ms: 1.08x faster                                                               |
| generators                 | 22.5 ms                                                     | 21.0 ms: 1.07x faster                                                               |
| logging_silent             | 60.5 ns                                                     | 56.4 ns: 1.07x faster                                                               |
| deepcopy                   | 238 us                                                      | 223 us: 1.07x faster                                                                |
| go                         | 91.6 ms                                                     | 86.1 ms: 1.06x faster                                                               |
| sympy_str                  | 175 ms                                                      | 165 ms: 1.06x faster                                                                |
| richards                   | 28.4 ms                                                     | 26.7 ms: 1.06x faster                                                               |
| sqlite_synth               | 1.76 us                                                     | 1.66 us: 1.06x faster                                                               |
| json                       | 3.05 ms                                                     | 2.87 ms: 1.06x faster                                                               |
| pickle_pure_python         | 195 us                                                      | 184 us: 1.06x faster                                                                |
| pprint_pformat             | 1.05 sec                                                    | 986 ms: 1.06x faster                                                                |
| sqlglot_parse              | 804 us                                                      | 760 us: 1.06x faster                                                                |
| bench_thread_pool          | 857 us                                                      | 810 us: 1.06x faster                                                                |
| logging_format             | 6.72 us                                                     | 6.35 us: 1.06x faster                                                               |
| logging_simple             | 6.28 us                                                     | 5.94 us: 1.06x faster                                                               |
| pprint_safe_repr           | 513 ms                                                      | 486 ms: 1.06x faster                                                                |
| sqlglot_transpile          | 1.02 ms                                                     | 968 us: 1.06x faster                                                                |
| sqlglot_normalize          | 187 ms                                                      | 177 ms: 1.05x faster                                                                |
| richards_super             | 32.1 ms                                                     | 30.5 ms: 1.05x faster                                                               |
| pathlib                    | 80.5 ms                                                     | 76.5 ms: 1.05x faster                                                               |
| hexiom                     | 4.10 ms                                                     | 3.90 ms: 1.05x faster                                                               |
| crypto_pyaes               | 48.5 ms                                                     | 46.2 ms: 1.05x faster                                                               |
| nqueens                    | 62.8 ms                                                     | 60.0 ms: 1.05x faster                                                               |
| spectral_norm              | 66.9 ms                                                     | 64.1 ms: 1.04x faster                                                               |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.04x faster                                                                |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                                |
| xml_etree_parse            | 93.0 ms                                                     | 90.2 ms: 1.03x faster                                                               |
| nbody                      | 71.9 ms                                                     | 69.8 ms: 1.03x faster                                                               |
| deepcopy_memo              | 23.7 us                                                     | 23.0 us: 1.03x faster                                                               |
| deepcopy_reduce            | 2.09 us                                                     | 2.04 us: 1.03x faster                                                               |
| pickle                     | 7.43 us                                                     | 7.24 us: 1.03x faster                                                               |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                               |
| mdp                        | 1.37 sec                                                    | 1.34 sec: 1.03x faster                                                              |
| 2to3                       | 218 ms                                                      | 213 ms: 1.03x faster                                                                |
| sqlglot_optimize           | 34.5 ms                                                     | 33.8 ms: 1.02x faster                                                               |
| xml_etree_iterparse        | 65.2 ms                                                     | 63.9 ms: 1.02x faster                                                               |
| django_template            | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                               |
| scimark_lu                 | 58.9 ms                                                     | 57.9 ms: 1.02x faster                                                               |
| scimark_sor                | 78.8 ms                                                     | 77.5 ms: 1.02x faster                                                               |
| xml_etree_generate         | 55.8 ms                                                     | 55.0 ms: 1.02x faster                                                               |
| sympy_expand               | 284 ms                                                      | 281 ms: 1.01x faster                                                                |
| json_loads                 | 13.9 us                                                     | 13.8 us: 1.01x faster                                                               |
| docutils                   | 1.66 sec                                                    | 1.65 sec: 1.01x faster                                                              |
| json_dumps                 | 5.70 ms                                                     | 5.66 ms: 1.01x faster                                                               |
| meteor_contest             | 74.6 ms                                                     | 74.3 ms: 1.00x faster                                                               |
| xml_etree_process          | 37.7 ms                                                     | 37.9 ms: 1.01x slower                                                               |
| scimark_monte_carlo        | 43.7 ms                                                     | 44.1 ms: 1.01x slower                                                               |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                               |
| python_startup             | 19.5 ms                                                     | 19.8 ms: 1.02x slower                                                               |
| tomli_loads                | 1.37 sec                                                    | 1.40 sec: 1.02x slower                                                              |
| pickle_dict                | 18.4 us                                                     | 18.8 us: 1.02x slower                                                               |
| scimark_fft                | 184 ms                                                      | 189 ms: 1.02x slower                                                                |
| pickle_list                | 2.83 us                                                     | 2.92 us: 1.03x slower                                                               |
| unpickle                   | 8.18 us                                                     | 8.49 us: 1.04x slower                                                               |
| fannkuch                   | 247 ms                                                      | 259 ms: 1.05x slower                                                                |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.72 ms: 1.06x slower                                                               |
| regex_v8                   | 14.2 ms                                                     | 16.1 ms: 1.13x slower                                                               |
| coverage                   | 40.8 ms                                                     | 48.1 ms: 1.18x slower                                                               |
| create_gc_cycles           | 752 us                                                      | 888 us: 1.18x slower                                                                |
| telco                      | 4.13 ms                                                     | 5.18 ms: 1.25x slower                                                               |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                                        |

Benchmark hidden because not significant (10): asyncio_tcp, pycparser, regex_effbot, chameleon, aiohttp, unpickle_pure_python, pyflate, python_startup_no_site, async_generators, unpickle_list
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown