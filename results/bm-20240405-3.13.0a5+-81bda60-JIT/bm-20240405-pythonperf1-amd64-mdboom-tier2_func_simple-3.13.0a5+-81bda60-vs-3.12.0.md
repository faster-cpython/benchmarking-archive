# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-amd64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| chameleon      | 4.98 ms                                                     | 4.70 ms: 1.06x faster                                                    |
| docutils       | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                   |
| tornado_http   | 89.5 ms                                                     | 84.2 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                       | 1.03x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 262 ms: 1.40x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 214 ms: 1.33x faster                                                     |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 389 ms: 1.29x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 612 ms: 1.26x faster                                                     |
| async_tree_io              | 731 ms                                                      | 588 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 393 ms: 1.24x faster                                                     |
| async_tree_memoization     | 339 ms                                                      | 274 ms: 1.24x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 56.9 ms: 1.26x faster                                                    |
| float          | 56.8 ms                                                     | 46.5 ms: 1.22x faster                                                    |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                       | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 118 ms: 1.07x faster                                                     |
| regex_effbot   | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                    |
| regex_v8       | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                    |
| regex_compile  | 87.5 ms                                                     | 87.0 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                       | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.18 sec: 1.16x faster                                                   |
| pickle_pure_python   | 195 us                                                      | 174 us: 1.12x faster                                                     |
| xml_etree_generate   | 55.8 ms                                                     | 52.8 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 65.2 ms                                                     | 62.6 ms: 1.04x faster                                                    |
| pickle               | 7.43 us                                                     | 7.16 us: 1.04x faster                                                    |
| json_dumps           | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                    |
| xml_etree_process    | 37.7 ms                                                     | 36.5 ms: 1.03x faster                                                    |
| unpickle_pure_python | 133 us                                                      | 129 us: 1.03x faster                                                     |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                    |
| pickle_list          | 2.83 us                                                     | 2.93 us: 1.04x slower                                                    |
| unpickle             | 8.18 us                                                     | 9.17 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                             |

Benchmark hidden because not significant (3): unpickle_list, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.6 ms: 1.11x slower                                                    |
| python_startup_no_site | 16.2 ms                                                     | 19.5 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-----------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.68 ms: 1.25x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 262 ms: 1.40x faster                                                     |
| typing_runtime_protocols   | 95.1 us                                                     | 70.7 us: 1.35x faster                                                    |
| async_tree_none_tg         | 285 ms                                                      | 214 ms: 1.33x faster                                                     |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.58 sec: 1.33x faster                                                   |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                     |
| spectral_norm              | 66.9 ms                                                     | 51.4 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 389 ms: 1.29x faster                                                     |
| comprehensions             | 14.1 us                                                     | 11.0 us: 1.28x faster                                                    |
| nbody                      | 71.9 ms                                                     | 56.9 ms: 1.26x faster                                                    |
| async_tree_io_tg           | 771 ms                                                      | 612 ms: 1.26x faster                                                     |
| mako                       | 7.09 ms                                                     | 5.68 ms: 1.25x faster                                                    |
| async_tree_io              | 731 ms                                                      | 588 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 393 ms: 1.24x faster                                                     |
| async_tree_memoization     | 339 ms                                                      | 274 ms: 1.24x faster                                                     |
| float                      | 56.8 ms                                                     | 46.5 ms: 1.22x faster                                                    |
| raytrace                   | 192 ms                                                      | 161 ms: 1.19x faster                                                     |
| tomli_loads                | 1.37 sec                                                    | 1.18 sec: 1.16x faster                                                   |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.23 ms: 1.15x faster                                                    |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.2 ms: 1.15x faster                                                    |
| logging_silent             | 60.5 ns                                                     | 52.9 ns: 1.14x faster                                                    |
| generators                 | 22.5 ms                                                     | 19.8 ms: 1.14x faster                                                    |
| mypy2                      | 509 ms                                                      | 449 ms: 1.13x faster                                                     |
| chaos                      | 43.3 ms                                                     | 38.3 ms: 1.13x faster                                                    |
| deepcopy_memo              | 23.7 us                                                     | 21.0 us: 1.13x faster                                                    |
| sqlite_synth               | 1.76 us                                                     | 1.57 us: 1.12x faster                                                    |
| pickle_pure_python         | 195 us                                                      | 174 us: 1.12x faster                                                     |
| scimark_fft                | 184 ms                                                      | 167 ms: 1.10x faster                                                     |
| logging_simple             | 6.28 us                                                     | 5.70 us: 1.10x faster                                                    |
| crypto_pyaes               | 48.5 ms                                                     | 44.1 ms: 1.10x faster                                                    |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.10x faster                                                    |
| logging_format             | 6.72 us                                                     | 6.15 us: 1.09x faster                                                    |
| pprint_pformat             | 1.05 sec                                                    | 958 ms: 1.09x faster                                                     |
| pyflate                    | 295 ms                                                      | 272 ms: 1.08x faster                                                     |
| deepcopy                   | 238 us                                                      | 220 us: 1.08x faster                                                     |
| fannkuch                   | 247 ms                                                      | 228 ms: 1.08x faster                                                     |
| dulwich_log                | 44.3 ms                                                     | 41.0 ms: 1.08x faster                                                    |
| pprint_safe_repr           | 513 ms                                                      | 479 ms: 1.07x faster                                                     |
| regex_dna                  | 126 ms                                                      | 118 ms: 1.07x faster                                                     |
| json                       | 3.05 ms                                                     | 2.87 ms: 1.06x faster                                                    |
| tornado_http               | 89.5 ms                                                     | 84.2 ms: 1.06x faster                                                    |
| bench_thread_pool          | 857 us                                                      | 806 us: 1.06x faster                                                     |
| chameleon                  | 4.98 ms                                                     | 4.70 ms: 1.06x faster                                                    |
| deepcopy_reduce            | 2.09 us                                                     | 1.98 us: 1.06x faster                                                    |
| xml_etree_generate         | 55.8 ms                                                     | 52.8 ms: 1.06x faster                                                    |
| sympy_str                  | 175 ms                                                      | 167 ms: 1.05x faster                                                     |
| nqueens                    | 62.8 ms                                                     | 60.1 ms: 1.05x faster                                                    |
| xml_etree_iterparse        | 65.2 ms                                                     | 62.6 ms: 1.04x faster                                                    |
| regex_effbot               | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                    |
| pickle                     | 7.43 us                                                     | 7.16 us: 1.04x faster                                                    |
| sqlglot_normalize          | 187 ms                                                      | 180 ms: 1.04x faster                                                     |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                     |
| asyncio_tcp                | 487 ms                                                      | 470 ms: 1.04x faster                                                     |
| meteor_contest             | 74.6 ms                                                     | 72.1 ms: 1.03x faster                                                    |
| json_dumps                 | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                    |
| xml_etree_process          | 37.7 ms                                                     | 36.5 ms: 1.03x faster                                                    |
| pathlib                    | 80.5 ms                                                     | 78.0 ms: 1.03x faster                                                    |
| richards_super             | 32.1 ms                                                     | 31.1 ms: 1.03x faster                                                    |
| unpickle_pure_python       | 133 us                                                      | 129 us: 1.03x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 781 us: 1.03x faster                                                     |
| async_generators           | 239 ms                                                      | 233 ms: 1.03x faster                                                     |
| sympy_sum                  | 91.5 ms                                                     | 89.2 ms: 1.03x faster                                                    |
| richards                   | 28.4 ms                                                     | 27.7 ms: 1.03x faster                                                    |
| sqlglot_transpile          | 1.02 ms                                                     | 998 us: 1.02x faster                                                     |
| bench_mp_pool              | 69.2 ms                                                     | 67.7 ms: 1.02x faster                                                    |
| regex_v8                   | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                    |
| regex_compile              | 87.5 ms                                                     | 87.0 ms: 1.01x faster                                                    |
| sympy_expand               | 284 ms                                                      | 283 ms: 1.00x faster                                                     |
| go                         | 91.6 ms                                                     | 92.1 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 34.8 ms: 1.01x slower                                                    |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                    |
| docutils                   | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                   |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                    |
| sympy_integrate            | 13.0 ms                                                     | 13.3 ms: 1.03x slower                                                    |
| aiohttp                    | 884 us                                                      | 911 us: 1.03x slower                                                     |
| pickle_list                | 2.83 us                                                     | 2.93 us: 1.04x slower                                                    |
| scimark_sor                | 78.8 ms                                                     | 82.8 ms: 1.05x slower                                                    |
| mdp                        | 1.37 sec                                                    | 1.46 sec: 1.07x slower                                                   |
| hexiom                     | 4.10 ms                                                     | 4.42 ms: 1.08x slower                                                    |
| python_startup             | 19.5 ms                                                     | 21.6 ms: 1.11x slower                                                    |
| unpickle                   | 8.18 us                                                     | 9.17 us: 1.12x slower                                                    |
| telco                      | 4.13 ms                                                     | 4.75 ms: 1.15x slower                                                    |
| coverage                   | 40.8 ms                                                     | 47.5 ms: 1.16x slower                                                    |
| create_gc_cycles           | 752 us                                                      | 898 us: 1.19x slower                                                     |
| python_startup_no_site     | 16.2 ms                                                     | 19.5 ms: 1.20x slower                                                    |
| scimark_lu                 | 58.9 ms                                                     | 71.4 ms: 1.21x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                             |

Benchmark hidden because not significant (6): pycparser, unpickle_list, xml_etree_parse, deltablue, json_loads, 2to3
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown