# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 221 ms: 1.01x slower                                                        |
| chameleon      | 4.98 ms                                                     | 4.74 ms: 1.05x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.70 sec: 1.02x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 83.9 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 214 ms: 1.33x faster                                                        |
| async_tree_none            | 291 ms                                                      | 221 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.31x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                        |
| async_tree_io              | 731 ms                                                      | 584 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 618 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 392 ms: 1.25x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.29x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 58.1 ms: 1.24x faster                                                       |
| float          | 56.8 ms                                                     | 47.1 ms: 1.21x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.16x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| regex_compile  | 87.5 ms                                                     | 86.4 ms: 1.01x faster                                                       |
| regex_effbot   | 1.62 ms                                                     | 1.61 ms: 1.01x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.9 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.20 sec: 1.14x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 174 us: 1.12x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 52.7 ms: 1.06x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 127 us: 1.05x faster                                                        |
| xml_etree_process    | 37.7 ms                                                     | 36.4 ms: 1.04x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 90.9 ms: 1.02x faster                                                       |
| pickle               | 7.43 us                                                     | 7.26 us: 1.02x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.60 ms: 1.02x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.5 us: 1.00x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.94 us: 1.04x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.89 us: 1.05x slower                                                       |
| unpickle             | 8.18 us                                                     | 9.30 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.9 ms: 1.12x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 19.7 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.64 ms: 1.26x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.38x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 70.8 us: 1.34x faster                                                       |
| async_tree_none_tg         | 285 ms                                                      | 214 ms: 1.33x faster                                                        |
| async_tree_none            | 291 ms                                                      | 221 ms: 1.32x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.60 sec: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.31x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.8 us: 1.30x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 52.2 ms: 1.28x faster                                                       |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                        |
| mako                       | 7.09 ms                                                     | 5.64 ms: 1.26x faster                                                       |
| async_tree_io              | 731 ms                                                      | 584 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 618 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 392 ms: 1.25x faster                                                        |
| nbody                      | 71.9 ms                                                     | 58.1 ms: 1.24x faster                                                       |
| float                      | 56.8 ms                                                     | 47.1 ms: 1.21x faster                                                       |
| raytrace                   | 192 ms                                                      | 163 ms: 1.18x faster                                                        |
| generators                 | 22.5 ms                                                     | 19.5 ms: 1.16x faster                                                       |
| chaos                      | 43.3 ms                                                     | 37.9 ms: 1.14x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 53.0 ns: 1.14x faster                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.20 sec: 1.14x faster                                                      |
| mypy2                      | 509 ms                                                      | 448 ms: 1.14x faster                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.26 ms: 1.13x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.0 us: 1.13x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 174 us: 1.12x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.57 us: 1.12x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.0 ms: 1.12x faster                                                       |
| scimark_fft                | 184 ms                                                      | 166 ms: 1.11x faster                                                        |
| crypto_pyaes               | 48.5 ms                                                     | 44.0 ms: 1.10x faster                                                       |
| pyflate                    | 295 ms                                                      | 268 ms: 1.10x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.09x faster                                                       |
| deepcopy                   | 238 us                                                      | 220 us: 1.08x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.83 us: 1.08x faster                                                       |
| fannkuch                   | 247 ms                                                      | 230 ms: 1.07x faster                                                        |
| logging_format             | 6.72 us                                                     | 6.26 us: 1.07x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 976 ms: 1.07x faster                                                        |
| dulwich_log                | 44.3 ms                                                     | 41.4 ms: 1.07x faster                                                       |
| pprint_safe_repr           | 513 ms                                                      | 480 ms: 1.07x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 1.96 us: 1.07x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 83.9 ms: 1.07x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 52.7 ms: 1.06x faster                                                       |
| richards                   | 28.4 ms                                                     | 26.8 ms: 1.06x faster                                                       |
| json                       | 3.05 ms                                                     | 2.90 ms: 1.05x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.74 ms: 1.05x faster                                                       |
| richards_super             | 32.1 ms                                                     | 30.6 ms: 1.05x faster                                                       |
| sympy_str                  | 175 ms                                                      | 167 ms: 1.05x faster                                                        |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 127 us: 1.05x faster                                                        |
| bench_thread_pool          | 857 us                                                      | 818 us: 1.05x faster                                                        |
| sqlglot_parse              | 804 us                                                      | 772 us: 1.04x faster                                                        |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 88.2 ms: 1.04x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 180 ms: 1.04x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 36.4 ms: 1.04x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 60.9 ms: 1.03x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 992 us: 1.03x faster                                                        |
| asyncio_tcp                | 487 ms                                                      | 473 ms: 1.03x faster                                                        |
| pathlib                    | 80.5 ms                                                     | 78.1 ms: 1.03x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 90.9 ms: 1.02x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.26 us: 1.02x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 73.1 ms: 1.02x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.60 ms: 1.02x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 86.4 ms: 1.01x faster                                                       |
| async_generators           | 239 ms                                                      | 237 ms: 1.01x faster                                                        |
| deltablue                  | 2.16 ms                                                     | 2.14 ms: 1.01x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.61 ms: 1.01x faster                                                       |
| sympy_expand               | 284 ms                                                      | 282 ms: 1.00x faster                                                        |
| pickle_dict                | 18.4 us                                                     | 18.5 us: 1.00x slower                                                       |
| 2to3                       | 218 ms                                                      | 221 ms: 1.01x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.70 sec: 1.02x slower                                                      |
| aiohttp                    | 884 us                                                      | 907 us: 1.03x slower                                                        |
| sympy_integrate            | 13.0 ms                                                     | 13.3 ms: 1.03x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.94 us: 1.04x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.9 ms: 1.05x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.89 us: 1.05x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 83.5 ms: 1.06x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.47 ms: 1.09x slower                                                       |
| coverage                   | 40.8 ms                                                     | 45.1 ms: 1.10x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.53 sec: 1.12x slower                                                      |
| python_startup             | 19.5 ms                                                     | 21.9 ms: 1.12x slower                                                       |
| unpickle                   | 8.18 us                                                     | 9.30 us: 1.14x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.84 ms: 1.17x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 909 us: 1.21x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 19.7 ms: 1.21x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 75.0 ms: 1.27x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (4): bench_mp_pool, go, json_loads, pycparser
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown