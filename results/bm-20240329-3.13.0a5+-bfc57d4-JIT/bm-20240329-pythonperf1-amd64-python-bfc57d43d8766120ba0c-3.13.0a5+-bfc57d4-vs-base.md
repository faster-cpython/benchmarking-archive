# Results vs. base

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.00x faster
- HPT reliability: 97.27%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                                      | 223 ms: 1.02x slower                                                        |
| chameleon      | 4.78 ms                                                                     | 4.64 ms: 1.03x faster                                                       |
| docutils       | 1.69 sec                                                                    | 1.68 sec: 1.01x faster                                                      |
| tornado_http   | 84.8 ms                                                                     | 84.0 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg        | 613 ms                                                                      | 600 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed | 376 ms                                                                      | 372 ms: 1.01x faster                                                        |
| Geometric mean          | (ref)                                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (6): async_tree_io, async_tree_none, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 84.6 ms                                                                     | 83.3 ms: 1.02x faster                                                       |
| regex_effbot   | 1.57 ms                                                                     | 1.60 ms: 1.02x slower                                                       |
| regex_dna      | 116 ms                                                                      | 121 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                       | 1.03x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 2.80 us                                                                     | 2.67 us: 1.05x faster                                                       |
| unpickle             | 8.72 us                                                                     | 8.53 us: 1.02x faster                                                       |
| json_dumps           | 5.61 ms                                                                     | 5.51 ms: 1.02x faster                                                       |
| tomli_loads          | 1.21 sec                                                                    | 1.19 sec: 1.01x faster                                                      |
| pickle_dict          | 18.6 us                                                                     | 18.4 us: 1.01x faster                                                       |
| pickle               | 7.32 us                                                                     | 7.27 us: 1.01x faster                                                       |
| xml_etree_parse      | 91.6 ms                                                                     | 92.4 ms: 1.01x slower                                                       |
| json_loads           | 13.8 us                                                                     | 14.0 us: 1.01x slower                                                       |
| unpickle_pure_python | 128 us                                                                      | 130 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 61.2 ms                                                                     | 62.3 ms: 1.02x slower                                                       |
| pickle_list          | 2.88 us                                                                     | 2.96 us: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 20.2 ms                                                                     | 20.4 ms: 1.01x slower                                                       |
| Geometric mean         | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 5.84 ms                                                                     | 5.61 ms: 1.04x faster                                                       |
| django_template | 22.8 ms                                                                     | 22.5 ms: 1.01x faster                                                       |
| genshi_text     | 15.1 ms                                                                     | 15.4 ms: 1.02x slower                                                       |
| genshi_xml      | 34.2 ms                                                                     | 36.3 ms: 1.06x slower                                                       |
| Geometric mean  | (ref)                                                                       | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence          | 46.5 ns                                                                     | 44.0 ns: 1.06x faster                                                       |
| unpickle_list            | 2.80 us                                                                     | 2.67 us: 1.05x faster                                                       |
| mako                     | 5.84 ms                                                                     | 5.61 ms: 1.04x faster                                                       |
| generators               | 20.1 ms                                                                     | 19.5 ms: 1.03x faster                                                       |
| chameleon                | 4.78 ms                                                                     | 4.64 ms: 1.03x faster                                                       |
| scimark_lu               | 70.9 ms                                                                     | 69.1 ms: 1.03x faster                                                       |
| deltablue                | 2.06 ms                                                                     | 2.01 ms: 1.03x faster                                                       |
| unpickle                 | 8.72 us                                                                     | 8.53 us: 1.02x faster                                                       |
| async_tree_io_tg         | 613 ms                                                                      | 600 ms: 1.02x faster                                                        |
| scimark_fft              | 171 ms                                                                      | 167 ms: 1.02x faster                                                        |
| json_dumps               | 5.61 ms                                                                     | 5.51 ms: 1.02x faster                                                       |
| logging_silent           | 53.6 ns                                                                     | 52.7 ns: 1.02x faster                                                       |
| regex_compile            | 84.6 ms                                                                     | 83.3 ms: 1.02x faster                                                       |
| thrift                   | 9.06 ms                                                                     | 8.91 ms: 1.02x faster                                                       |
| sympy_str                | 168 ms                                                                      | 165 ms: 1.01x faster                                                        |
| sqlglot_transpile        | 1000 us                                                                     | 986 us: 1.01x faster                                                        |
| django_template          | 22.8 ms                                                                     | 22.5 ms: 1.01x faster                                                       |
| pprint_pformat           | 985 ms                                                                      | 972 ms: 1.01x faster                                                        |
| tomli_loads              | 1.21 sec                                                                    | 1.19 sec: 1.01x faster                                                      |
| deepcopy_memo            | 21.9 us                                                                     | 21.6 us: 1.01x faster                                                       |
| logging_format           | 6.37 us                                                                     | 6.29 us: 1.01x faster                                                       |
| raytrace                 | 180 ms                                                                      | 178 ms: 1.01x faster                                                        |
| sympy_sum                | 87.7 ms                                                                     | 86.8 ms: 1.01x faster                                                       |
| sympy_expand             | 287 ms                                                                      | 284 ms: 1.01x faster                                                        |
| pickle_dict              | 18.6 us                                                                     | 18.4 us: 1.01x faster                                                       |
| async_tree_cpu_io_mixed  | 376 ms                                                                      | 372 ms: 1.01x faster                                                        |
| sympy_integrate          | 13.3 ms                                                                     | 13.2 ms: 1.01x faster                                                       |
| scimark_sor              | 81.3 ms                                                                     | 80.5 ms: 1.01x faster                                                       |
| docutils                 | 1.69 sec                                                                    | 1.68 sec: 1.01x faster                                                      |
| mypy2                    | 452 ms                                                                      | 448 ms: 1.01x faster                                                        |
| typing_runtime_protocols | 70.1 us                                                                     | 69.4 us: 1.01x faster                                                       |
| tornado_http             | 84.8 ms                                                                     | 84.0 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult  | 2.26 ms                                                                     | 2.24 ms: 1.01x faster                                                       |
| logging_simple           | 5.96 us                                                                     | 5.91 us: 1.01x faster                                                       |
| sqlglot_parse            | 778 us                                                                      | 772 us: 1.01x faster                                                        |
| coverage                 | 47.4 ms                                                                     | 47.0 ms: 1.01x faster                                                       |
| dulwich_log              | 40.9 ms                                                                     | 40.6 ms: 1.01x faster                                                       |
| scimark_monte_carlo      | 39.7 ms                                                                     | 39.4 ms: 1.01x faster                                                       |
| gc_traversal             | 1.55 ms                                                                     | 1.54 ms: 1.01x faster                                                       |
| pickle                   | 7.32 us                                                                     | 7.27 us: 1.01x faster                                                       |
| go                       | 93.5 ms                                                                     | 93.0 ms: 1.01x faster                                                       |
| deepcopy_reduce          | 1.93 us                                                                     | 1.92 us: 1.01x faster                                                       |
| chaos                    | 39.1 ms                                                                     | 38.9 ms: 1.00x faster                                                       |
| sqlite_synth             | 1.58 us                                                                     | 1.58 us: 1.00x slower                                                       |
| python_startup_no_site   | 20.2 ms                                                                     | 20.4 ms: 1.01x slower                                                       |
| hexiom                   | 4.57 ms                                                                     | 4.61 ms: 1.01x slower                                                       |
| xml_etree_parse          | 91.6 ms                                                                     | 92.4 ms: 1.01x slower                                                       |
| telco                    | 4.69 ms                                                                     | 4.74 ms: 1.01x slower                                                       |
| json_loads               | 13.8 us                                                                     | 14.0 us: 1.01x slower                                                       |
| unpickle_pure_python     | 128 us                                                                      | 130 us: 1.01x slower                                                        |
| nqueens                  | 60.9 ms                                                                     | 61.9 ms: 1.02x slower                                                       |
| crypto_pyaes             | 43.9 ms                                                                     | 44.6 ms: 1.02x slower                                                       |
| xml_etree_iterparse      | 61.2 ms                                                                     | 62.3 ms: 1.02x slower                                                       |
| genshi_text              | 15.1 ms                                                                     | 15.4 ms: 1.02x slower                                                       |
| 2to3                     | 218 ms                                                                      | 223 ms: 1.02x slower                                                        |
| coroutines               | 12.9 ms                                                                     | 13.2 ms: 1.02x slower                                                       |
| pylint                   | 190 ms                                                                      | 194 ms: 1.02x slower                                                        |
| regex_effbot             | 1.57 ms                                                                     | 1.60 ms: 1.02x slower                                                       |
| pickle_list              | 2.88 us                                                                     | 2.96 us: 1.03x slower                                                       |
| richards                 | 28.2 ms                                                                     | 29.1 ms: 1.03x slower                                                       |
| richards_super           | 31.6 ms                                                                     | 32.7 ms: 1.03x slower                                                       |
| comprehensions           | 10.9 us                                                                     | 11.3 us: 1.04x slower                                                       |
| regex_dna                | 116 ms                                                                      | 121 ms: 1.04x slower                                                        |
| bench_mp_pool            | 67.4 ms                                                                     | 70.8 ms: 1.05x slower                                                       |
| genshi_xml               | 34.2 ms                                                                     | 36.3 ms: 1.06x slower                                                       |
| Geometric mean           | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (33): json, pycparser, bench_thread_pool, async_tree_io, async_tree_none, async_tree_memoization_tg, async_tree_memoization, pprint_safe_repr, async_tree_none_tg, aiohttp, async_tree_cpu_io_mixed_tg, float, create_gc_cycles, python_startup, sqlglot_normalize, pathlib, pidigits, nbody, mdp, pickle_pure_python, meteor_contest, fannkuch, deepcopy, sqlglot_optimize, xml_etree_process, xml_etree_generate, async_generators, html5lib, asyncio_tcp, spectral_norm, pyflate, asyncio_tcp_ssl, regex_v8

# HPT report

- Reliability score: 97.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown