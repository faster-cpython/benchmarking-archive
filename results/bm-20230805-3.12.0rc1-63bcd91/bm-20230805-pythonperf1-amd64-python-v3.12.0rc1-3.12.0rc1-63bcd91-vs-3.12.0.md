
# Results vs. 3.12.0

- fork: python
- ref: v3.12.0rc1
- machine: windows-amd64
- commit hash: 63bcd91
- commit date: 2023-08-05
- overall geometric mean: 1.02x faster \*
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 211 ms: 1.03x faster                                              |
| docutils       | 1.66 sec                                                    | 1.60 sec: 1.04x faster                                            |
| tornado_http   | 89.5 ms                                                     | 87.2 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                       | 1.03x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io           | 731 ms                                                      | 701 ms: 1.04x faster                                              |
| async_tree_cpu_io_mixed | 489 ms                                                      | 471 ms: 1.04x faster                                              |
| async_tree_memoization  | 339 ms                                                      | 331 ms: 1.02x faster                                              |
| async_tree_none         | 291 ms                                                      | 286 ms: 1.02x faster                                              |
| Geometric mean          | (ref)                                                       | 1.03x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 53.8 ms: 1.06x faster                                             |
| nbody          | 71.9 ms                                                     | 68.7 ms: 1.05x faster                                             |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                              |
| Geometric mean | (ref)                                                       | 1.05x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 121 ms: 1.04x faster                                              |
| regex_v8       | 14.2 ms                                                     | 13.8 ms: 1.03x faster                                             |
| regex_compile  | 87.5 ms                                                     | 85.8 ms: 1.02x faster                                             |
| regex_effbot   | 1.62 ms                                                     | 1.61 ms: 1.00x faster                                             |
| Geometric mean | (ref)                                                       | 1.03x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle               | 7.43 us                                                     | 6.98 us: 1.07x faster                                             |
| xml_etree_iterparse  | 65.2 ms                                                     | 63.1 ms: 1.03x faster                                             |
| json_loads           | 13.9 us                                                     | 13.5 us: 1.03x faster                                             |
| pickle_pure_python   | 195 us                                                      | 191 us: 1.02x faster                                              |
| xml_etree_parse      | 93.0 ms                                                     | 91.3 ms: 1.02x faster                                             |
| json_dumps           | 5.70 ms                                                     | 5.59 ms: 1.02x faster                                             |
| tomli_loads          | 1.37 sec                                                    | 1.35 sec: 1.02x faster                                            |
| xml_etree_generate   | 55.8 ms                                                     | 55.1 ms: 1.01x faster                                             |
| pickle_dict          | 18.4 us                                                     | 18.3 us: 1.01x faster                                             |
| unpickle_pure_python | 133 us                                                      | 133 us: 1.00x faster                                              |
| unpickle_list        | 2.75 us                                                     | 2.79 us: 1.02x slower                                             |
| pickle_list          | 2.83 us                                                     | 2.87 us: 1.02x slower                                             |
| unpickle             | 8.18 us                                                     | 8.38 us: 1.02x slower                                             |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                      |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup | 19.5 ms                                                     | 18.7 ms: 1.04x faster                                             |
| Geometric mean | (ref)                                                       | 1.02x faster                                                      |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|-----------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 6.82 ms: 1.04x faster                                             |

All benchmarks:
===============

| Benchmark                | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20230805-pythonperf1-amd64-python-v3.12.0rc1-3.12.0rc1-63bcd91 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------:|
| asyncio_tcp_ssl          | 2.10 sec                                                    | 1.90 sec: 1.10x faster                                            |
| richards_super           | 32.1 ms                                                     | 29.5 ms: 1.09x faster                                             |
| richards                 | 28.4 ms                                                     | 26.1 ms: 1.09x faster                                             |
| unpack_sequence          | 37.5 ns                                                     | 35.1 ns: 1.07x faster                                             |
| pickle                   | 7.43 us                                                     | 6.98 us: 1.07x faster                                             |
| scimark_fft              | 184 ms                                                      | 174 ms: 1.06x faster                                              |
| go                       | 91.6 ms                                                     | 86.3 ms: 1.06x faster                                             |
| float                    | 56.8 ms                                                     | 53.8 ms: 1.06x faster                                             |
| scimark_monte_carlo      | 43.7 ms                                                     | 41.5 ms: 1.05x faster                                             |
| create_gc_cycles         | 752 us                                                      | 717 us: 1.05x faster                                              |
| fannkuch                 | 247 ms                                                      | 236 ms: 1.05x faster                                              |
| json                     | 3.05 ms                                                     | 2.91 ms: 1.05x faster                                             |
| nbody                    | 71.9 ms                                                     | 68.7 ms: 1.05x faster                                             |
| async_generators         | 239 ms                                                      | 229 ms: 1.05x faster                                              |
| async_tree_io            | 731 ms                                                      | 701 ms: 1.04x faster                                              |
| raytrace                 | 192 ms                                                      | 184 ms: 1.04x faster                                              |
| bench_mp_pool            | 69.2 ms                                                     | 66.3 ms: 1.04x faster                                             |
| dulwich_log              | 44.3 ms                                                     | 42.5 ms: 1.04x faster                                             |
| pycparser                | 699 ms                                                      | 670 ms: 1.04x faster                                              |
| regex_dna                | 126 ms                                                      | 121 ms: 1.04x faster                                              |
| sqlglot_normalize        | 187 ms                                                      | 180 ms: 1.04x faster                                              |
| async_tree_cpu_io_mixed  | 489 ms                                                      | 471 ms: 1.04x faster                                              |
| spectral_norm            | 66.9 ms                                                     | 64.4 ms: 1.04x faster                                             |
| mako                     | 7.09 ms                                                     | 6.82 ms: 1.04x faster                                             |
| deepcopy                 | 238 us                                                      | 229 us: 1.04x faster                                              |
| python_startup           | 19.5 ms                                                     | 18.7 ms: 1.04x faster                                             |
| telco                    | 4.13 ms                                                     | 3.98 ms: 1.04x faster                                             |
| asyncio_tcp              | 487 ms                                                      | 470 ms: 1.04x faster                                              |
| docutils                 | 1.66 sec                                                    | 1.60 sec: 1.04x faster                                            |
| pidigits                 | 152 ms                                                      | 147 ms: 1.04x faster                                              |
| deepcopy_memo            | 23.7 us                                                     | 22.9 us: 1.04x faster                                             |
| aiohttp                  | 884 us                                                      | 854 us: 1.04x faster                                              |
| scimark_sparse_mat_mult  | 2.56 ms                                                     | 2.47 ms: 1.04x faster                                             |
| 2to3                     | 218 ms                                                      | 211 ms: 1.03x faster                                              |
| regex_v8                 | 14.2 ms                                                     | 13.8 ms: 1.03x faster                                             |
| gc_traversal             | 1.52 ms                                                     | 1.47 ms: 1.03x faster                                             |
| crypto_pyaes             | 48.5 ms                                                     | 46.9 ms: 1.03x faster                                             |
| xml_etree_iterparse      | 65.2 ms                                                     | 63.1 ms: 1.03x faster                                             |
| json_loads               | 13.9 us                                                     | 13.5 us: 1.03x faster                                             |
| hexiom                   | 4.10 ms                                                     | 3.98 ms: 1.03x faster                                             |
| sqlglot_optimize         | 34.5 ms                                                     | 33.5 ms: 1.03x faster                                             |
| scimark_lu               | 58.9 ms                                                     | 57.1 ms: 1.03x faster                                             |
| pathlib                  | 80.5 ms                                                     | 78.1 ms: 1.03x faster                                             |
| tornado_http             | 89.5 ms                                                     | 87.2 ms: 1.03x faster                                             |
| async_tree_memoization   | 339 ms                                                      | 331 ms: 1.02x faster                                              |
| pickle_pure_python       | 195 us                                                      | 191 us: 1.02x faster                                              |
| pprint_pformat           | 1.05 sec                                                    | 1.02 sec: 1.02x faster                                            |
| meteor_contest           | 74.6 ms                                                     | 73.1 ms: 1.02x faster                                             |
| regex_compile            | 87.5 ms                                                     | 85.8 ms: 1.02x faster                                             |
| nqueens                  | 62.8 ms                                                     | 61.6 ms: 1.02x faster                                             |
| async_tree_none          | 291 ms                                                      | 286 ms: 1.02x faster                                              |
| typing_runtime_protocols | 95.1 us                                                     | 93.3 us: 1.02x faster                                             |
| xml_etree_parse          | 93.0 ms                                                     | 91.3 ms: 1.02x faster                                             |
| json_dumps               | 5.70 ms                                                     | 5.59 ms: 1.02x faster                                             |
| coroutines               | 14.3 ms                                                     | 14.0 ms: 1.02x faster                                             |
| pprint_safe_repr         | 513 ms                                                      | 504 ms: 1.02x faster                                              |
| tomli_loads              | 1.37 sec                                                    | 1.35 sec: 1.02x faster                                            |
| sqlite_synth             | 1.76 us                                                     | 1.73 us: 1.02x faster                                             |
| deltablue                | 2.16 ms                                                     | 2.13 ms: 1.01x faster                                             |
| xml_etree_generate       | 55.8 ms                                                     | 55.1 ms: 1.01x faster                                             |
| chaos                    | 43.3 ms                                                     | 42.8 ms: 1.01x faster                                             |
| pyflate                  | 295 ms                                                      | 292 ms: 1.01x faster                                              |
| sqlglot_transpile        | 1.02 ms                                                     | 1.01 ms: 1.01x faster                                             |
| logging_silent           | 60.5 ns                                                     | 60.0 ns: 1.01x faster                                             |
| pickle_dict              | 18.4 us                                                     | 18.3 us: 1.01x faster                                             |
| deepcopy_reduce          | 2.09 us                                                     | 2.08 us: 1.01x faster                                             |
| sqlglot_parse            | 804 us                                                      | 800 us: 1.00x faster                                              |
| regex_effbot             | 1.62 ms                                                     | 1.61 ms: 1.00x faster                                             |
| unpickle_pure_python     | 133 us                                                      | 133 us: 1.00x faster                                              |
| logging_format           | 6.72 us                                                     | 6.77 us: 1.01x slower                                             |
| unpickle_list            | 2.75 us                                                     | 2.79 us: 1.02x slower                                             |
| logging_simple           | 6.28 us                                                     | 6.37 us: 1.02x slower                                             |
| pickle_list              | 2.83 us                                                     | 2.87 us: 1.02x slower                                             |
| unpickle                 | 8.18 us                                                     | 8.38 us: 1.02x slower                                             |
| mdp                      | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                            |
| coverage                 | 40.8 ms                                                     | 52.1 ms: 1.28x slower                                             |
| dask                     | 263 ms                                                      | 361 ms: 1.38x slower                                              |
| Geometric mean           | (ref)                                                       | 1.02x faster                                                      |

Benchmark hidden because not significant (6): python_startup_no_site, bench_thread_pool, xml_etree_process, scimark_sor, generators, comprehensions
Ignored benchmarks (13) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, chameleon, django_template, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sympy_expand, sympy_integrate, sympy_str, sympy_sum


# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x


# Memory

- memory change: unknown