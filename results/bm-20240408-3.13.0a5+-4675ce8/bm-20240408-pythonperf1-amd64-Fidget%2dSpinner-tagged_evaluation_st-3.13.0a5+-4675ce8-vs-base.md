# Results vs. base

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-amd64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                                      | 220 ms: 1.03x slower                                                                  |
| chameleon      | 5.01 ms                                                                     | 5.55 ms: 1.11x slower                                                                 |
| docutils       | 1.64 sec                                                                    | 1.70 sec: 1.04x slower                                                                |
| html5lib       | 36.7 ms                                                                     | 38.0 ms: 1.04x slower                                                                 |
| Geometric mean | (ref)                                                                       | 1.04x slower                                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 394 ms                                                                      | 403 ms: 1.02x slower                                                                  |
| Geometric mean          | (ref)                                                                       | 1.02x slower                                                                          |

Benchmark hidden because not significant (7): async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                      | 147 ms: 1.00x slower                                                                  |
| nbody          | 74.1 ms                                                                     | 76.0 ms: 1.03x slower                                                                 |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                                     | 1.57 ms: 1.01x faster                                                                 |
| regex_dna      | 120 ms                                                                      | 119 ms: 1.01x faster                                                                  |
| regex_compile  | 81.2 ms                                                                     | 82.6 ms: 1.02x slower                                                                 |
| Geometric mean | (ref)                                                                       | 1.02x slower                                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| pickle               | 7.52 us                                                                     | 7.35 us: 1.02x faster                                                                 |
| unpickle             | 8.63 us                                                                     | 8.48 us: 1.02x faster                                                                 |
| pickle_dict          | 18.9 us                                                                     | 18.9 us: 1.00x faster                                                                 |
| unpickle_pure_python | 138 us                                                                      | 139 us: 1.01x slower                                                                  |
| unpickle_list        | 2.80 us                                                                     | 2.85 us: 1.02x slower                                                                 |
| pickle_list          | 2.93 us                                                                     | 3.00 us: 1.02x slower                                                                 |
| xml_etree_generate   | 55.7 ms                                                                     | 59.0 ms: 1.06x slower                                                                 |
| json_dumps           | 5.72 ms                                                                     | 6.07 ms: 1.06x slower                                                                 |
| xml_etree_process    | 38.1 ms                                                                     | 41.7 ms: 1.09x slower                                                                 |
| pickle_pure_python   | 185 us                                                                      | 206 us: 1.11x slower                                                                  |
| Geometric mean       | (ref)                                                                       | 1.02x slower                                                                          |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, tomli_loads, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| python_startup | 19.9 ms                                                                     | 20.1 ms: 1.01x slower                                                                 |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| genshi_text    | 16.7 ms                                                                     | 17.9 ms: 1.07x slower                                                                 |
| Geometric mean | (ref)                                                                       | 1.03x slower                                                                          |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| richards                 | 30.5 ms                                                                     | 27.5 ms: 1.11x faster                                                                 |
| richards_super           | 34.1 ms                                                                     | 30.9 ms: 1.10x faster                                                                 |
| go                       | 92.1 ms                                                                     | 88.0 ms: 1.05x faster                                                                 |
| logging_silent           | 58.0 ns                                                                     | 55.7 ns: 1.04x faster                                                                 |
| spectral_norm            | 65.2 ms                                                                     | 63.3 ms: 1.03x faster                                                                 |
| deltablue                | 2.11 ms                                                                     | 2.05 ms: 1.03x faster                                                                 |
| scimark_monte_carlo      | 42.9 ms                                                                     | 41.9 ms: 1.02x faster                                                                 |
| pickle                   | 7.52 us                                                                     | 7.35 us: 1.02x faster                                                                 |
| unpickle                 | 8.63 us                                                                     | 8.48 us: 1.02x faster                                                                 |
| scimark_fft              | 186 ms                                                                      | 183 ms: 1.02x faster                                                                  |
| scimark_sparse_mat_mult  | 2.71 ms                                                                     | 2.68 ms: 1.01x faster                                                                 |
| scimark_lu               | 60.1 ms                                                                     | 59.6 ms: 1.01x faster                                                                 |
| regex_effbot             | 1.58 ms                                                                     | 1.57 ms: 1.01x faster                                                                 |
| regex_dna                | 120 ms                                                                      | 119 ms: 1.01x faster                                                                  |
| scimark_sor              | 80.1 ms                                                                     | 79.5 ms: 1.01x faster                                                                 |
| deepcopy_memo            | 23.1 us                                                                     | 22.9 us: 1.01x faster                                                                 |
| hexiom                   | 4.09 ms                                                                     | 4.07 ms: 1.01x faster                                                                 |
| gc_traversal             | 1.54 ms                                                                     | 1.53 ms: 1.01x faster                                                                 |
| pickle_dict              | 18.9 us                                                                     | 18.9 us: 1.00x faster                                                                 |
| pidigits                 | 147 ms                                                                      | 147 ms: 1.00x slower                                                                  |
| unpickle_pure_python     | 138 us                                                                      | 139 us: 1.01x slower                                                                  |
| aiohttp                  | 892 us                                                                      | 901 us: 1.01x slower                                                                  |
| pyflate                  | 296 ms                                                                      | 299 ms: 1.01x slower                                                                  |
| typing_runtime_protocols | 75.0 us                                                                     | 75.9 us: 1.01x slower                                                                 |
| python_startup           | 19.9 ms                                                                     | 20.1 ms: 1.01x slower                                                                 |
| async_generators         | 234 ms                                                                      | 238 ms: 1.02x slower                                                                  |
| regex_compile            | 81.2 ms                                                                     | 82.6 ms: 1.02x slower                                                                 |
| unpickle_list            | 2.80 us                                                                     | 2.85 us: 1.02x slower                                                                 |
| mypy2                    | 427 ms                                                                      | 435 ms: 1.02x slower                                                                  |
| raytrace                 | 171 ms                                                                      | 174 ms: 1.02x slower                                                                  |
| async_tree_cpu_io_mixed  | 394 ms                                                                      | 403 ms: 1.02x slower                                                                  |
| pickle_list              | 2.93 us                                                                     | 3.00 us: 1.02x slower                                                                 |
| sympy_integrate          | 12.6 ms                                                                     | 12.9 ms: 1.02x slower                                                                 |
| logging_simple           | 6.09 us                                                                     | 6.24 us: 1.02x slower                                                                 |
| nbody                    | 74.1 ms                                                                     | 76.0 ms: 1.03x slower                                                                 |
| 2to3                     | 214 ms                                                                      | 220 ms: 1.03x slower                                                                  |
| logging_format           | 6.47 us                                                                     | 6.67 us: 1.03x slower                                                                 |
| deepcopy                 | 228 us                                                                      | 235 us: 1.03x slower                                                                  |
| sqlglot_parse            | 785 us                                                                      | 811 us: 1.03x slower                                                                  |
| pylint                   | 187 ms                                                                      | 193 ms: 1.03x slower                                                                  |
| sqlglot_transpile        | 994 us                                                                      | 1.03 ms: 1.03x slower                                                                 |
| sympy_expand             | 277 ms                                                                      | 287 ms: 1.03x slower                                                                  |
| meteor_contest           | 73.9 ms                                                                     | 76.5 ms: 1.04x slower                                                                 |
| html5lib                 | 36.7 ms                                                                     | 38.0 ms: 1.04x slower                                                                 |
| sympy_str                | 164 ms                                                                      | 170 ms: 1.04x slower                                                                  |
| docutils                 | 1.64 sec                                                                    | 1.70 sec: 1.04x slower                                                                |
| sqlglot_optimize         | 34.5 ms                                                                     | 35.9 ms: 1.04x slower                                                                 |
| dulwich_log              | 41.0 ms                                                                     | 42.6 ms: 1.04x slower                                                                 |
| coverage                 | 45.8 ms                                                                     | 47.7 ms: 1.04x slower                                                                 |
| crypto_pyaes             | 47.1 ms                                                                     | 49.1 ms: 1.04x slower                                                                 |
| sympy_sum                | 85.2 ms                                                                     | 88.8 ms: 1.04x slower                                                                 |
| json                     | 2.88 ms                                                                     | 3.02 ms: 1.05x slower                                                                 |
| sqlglot_normalize        | 182 ms                                                                      | 191 ms: 1.05x slower                                                                  |
| chaos                    | 40.1 ms                                                                     | 42.1 ms: 1.05x slower                                                                 |
| mdp                      | 1.40 sec                                                                    | 1.47 sec: 1.05x slower                                                                |
| sqlite_synth             | 1.62 us                                                                     | 1.71 us: 1.05x slower                                                                 |
| xml_etree_generate       | 55.7 ms                                                                     | 59.0 ms: 1.06x slower                                                                 |
| json_dumps               | 5.72 ms                                                                     | 6.07 ms: 1.06x slower                                                                 |
| deepcopy_reduce          | 2.05 us                                                                     | 2.18 us: 1.07x slower                                                                 |
| genshi_text              | 16.7 ms                                                                     | 17.9 ms: 1.07x slower                                                                 |
| comprehensions           | 11.4 us                                                                     | 12.2 us: 1.07x slower                                                                 |
| thrift                   | 8.18 ms                                                                     | 8.77 ms: 1.07x slower                                                                 |
| telco                    | 4.98 ms                                                                     | 5.40 ms: 1.08x slower                                                                 |
| pprint_safe_repr         | 498 ms                                                                      | 544 ms: 1.09x slower                                                                  |
| nqueens                  | 60.5 ms                                                                     | 66.3 ms: 1.09x slower                                                                 |
| xml_etree_process        | 38.1 ms                                                                     | 41.7 ms: 1.09x slower                                                                 |
| pprint_pformat           | 1.01 sec                                                                    | 1.11 sec: 1.10x slower                                                                |
| chameleon                | 5.01 ms                                                                     | 5.55 ms: 1.11x slower                                                                 |
| generators               | 21.1 ms                                                                     | 23.4 ms: 1.11x slower                                                                 |
| pickle_pure_python       | 185 us                                                                      | 206 us: 1.11x slower                                                                  |
| coroutines               | 13.5 ms                                                                     | 15.2 ms: 1.12x slower                                                                 |
| fannkuch                 | 265 ms                                                                      | 297 ms: 1.12x slower                                                                  |
| Geometric mean           | (ref)                                                                       | 1.02x slower                                                                          |

Benchmark hidden because not significant (24): asyncio_tcp_ssl, asyncio_tcp, async_tree_io, mako, xml_etree_parse, create_gc_cycles, xml_etree_iterparse, bench_thread_pool, tomli_loads, bench_mp_pool, float, pathlib, tornado_http, json_loads, python_startup_no_site, async_tree_io_tg, pycparser, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, genshi_xml, async_tree_none_tg, regex_v8

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown