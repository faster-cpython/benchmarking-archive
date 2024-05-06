# Results vs. base

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 165 ms                                                                                                            | 173 ms: 1.05x slower                                                                                                  |
| chameleon      | 4.60 ms                                                                                                           | 4.46 ms: 1.03x faster                                                                                                 |
| docutils       | 1.48 sec                                                                                                          | 1.55 sec: 1.05x slower                                                                                                |
| html5lib       | 34.0 ms                                                                                                           | 33.6 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg                 | 575 ms                                                                                                            | 556 ms: 1.03x faster                                                                                                  |
| async_tree_eager_tg              | 45.1 ms                                                                                                           | 44.7 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 336 ms                                                                                                            | 335 ms: 1.00x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 353 ms                                                                                                            | 355 ms: 1.00x slower                                                                                                  |
| async_tree_cpu_io_mixed          | 456 ms                                                                                                            | 462 ms: 1.01x slower                                                                                                  |
| async_tree_io                    | 558 ms                                                                                                            | 566 ms: 1.01x slower                                                                                                  |
| async_tree_eager                 | 64.2 ms                                                                                                           | 65.6 ms: 1.02x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (9): async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_none_tg, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 51.9 ms                                                                                                           | 49.2 ms: 1.05x faster                                                                                                 |
| nbody          | 66.1 ms                                                                                                           | 70.3 ms: 1.06x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 152 ms                                                                                                            | 152 ms: 1.00x slower                                                                                                  |
| regex_v8       | 17.0 ms                                                                                                           | 17.1 ms: 1.01x slower                                                                                                 |
| regex_compile  | 69.7 ms                                                                                                           | 81.0 ms: 1.16x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 1.49 sec                                                                                                          | 1.30 sec: 1.15x faster                                                                                                |
| unpickle_pure_python | 150 us                                                                                                            | 143 us: 1.05x faster                                                                                                  |
| xml_etree_process    | 37.8 ms                                                                                                           | 36.8 ms: 1.03x faster                                                                                                 |
| xml_etree_parse      | 109 ms                                                                                                            | 107 ms: 1.02x faster                                                                                                  |
| xml_etree_generate   | 55.2 ms                                                                                                           | 54.4 ms: 1.01x faster                                                                                                 |
| pickle_list          | 3.00 us                                                                                                           | 2.96 us: 1.01x faster                                                                                                 |
| unpickle             | 9.27 us                                                                                                           | 9.14 us: 1.01x faster                                                                                                 |
| pickle_pure_python   | 185 us                                                                                                            | 183 us: 1.01x faster                                                                                                  |
| json_loads           | 17.1 us                                                                                                           | 17.0 us: 1.01x faster                                                                                                 |
| xml_etree_iterparse  | 72.8 ms                                                                                                           | 72.3 ms: 1.01x faster                                                                                                 |
| pickle               | 7.48 us                                                                                                           | 7.44 us: 1.01x faster                                                                                                 |
| pickle_dict          | 18.1 us                                                                                                           | 18.0 us: 1.00x faster                                                                                                 |
| json_dumps           | 6.25 ms                                                                                                           | 6.37 ms: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 11.9 ms                                                                                                           | 13.4 ms: 1.12x slower                                                                                                 |
| python_startup_no_site | 10.2 ms                                                                                                           | 11.6 ms: 1.13x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.13x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml     | 31.5 ms                                                                                                           | 31.4 ms: 1.01x faster                                                                                                 |
| genshi_text    | 14.6 ms                                                                                                           | 14.9 ms: 1.02x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                        | results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json | results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads                      | 1.49 sec                                                                                                          | 1.30 sec: 1.15x faster                                                                                                |
| float                            | 51.9 ms                                                                                                           | 49.2 ms: 1.05x faster                                                                                                 |
| generators                       | 27.7 ms                                                                                                           | 26.4 ms: 1.05x faster                                                                                                 |
| unpickle_pure_python             | 150 us                                                                                                            | 143 us: 1.05x faster                                                                                                  |
| async_tree_io_tg                 | 575 ms                                                                                                            | 556 ms: 1.03x faster                                                                                                  |
| chameleon                        | 4.60 ms                                                                                                           | 4.46 ms: 1.03x faster                                                                                                 |
| xml_etree_process                | 37.8 ms                                                                                                           | 36.8 ms: 1.03x faster                                                                                                 |
| deepcopy_reduce                  | 1.91 us                                                                                                           | 1.87 us: 1.02x faster                                                                                                 |
| coroutines                       | 17.0 ms                                                                                                           | 16.7 ms: 1.02x faster                                                                                                 |
| xml_etree_parse                  | 109 ms                                                                                                            | 107 ms: 1.02x faster                                                                                                  |
| typing_runtime_protocols         | 70.8 us                                                                                                           | 69.6 us: 1.02x faster                                                                                                 |
| xml_etree_generate               | 55.2 ms                                                                                                           | 54.4 ms: 1.01x faster                                                                                                 |
| logging_simple                   | 3.34 us                                                                                                           | 3.29 us: 1.01x faster                                                                                                 |
| pickle_list                      | 3.00 us                                                                                                           | 2.96 us: 1.01x faster                                                                                                 |
| unpickle                         | 9.27 us                                                                                                           | 9.14 us: 1.01x faster                                                                                                 |
| deepcopy                         | 215 us                                                                                                            | 212 us: 1.01x faster                                                                                                  |
| html5lib                         | 34.0 ms                                                                                                           | 33.6 ms: 1.01x faster                                                                                                 |
| logging_format                   | 3.62 us                                                                                                           | 3.58 us: 1.01x faster                                                                                                 |
| pickle_pure_python               | 185 us                                                                                                            | 183 us: 1.01x faster                                                                                                  |
| json_loads                       | 17.1 us                                                                                                           | 17.0 us: 1.01x faster                                                                                                 |
| thrift                           | 442 us                                                                                                            | 437 us: 1.01x faster                                                                                                  |
| async_tree_eager_tg              | 45.1 ms                                                                                                           | 44.7 ms: 1.01x faster                                                                                                 |
| fannkuch                         | 263 ms                                                                                                            | 261 ms: 1.01x faster                                                                                                  |
| scimark_monte_carlo              | 44.6 ms                                                                                                           | 44.2 ms: 1.01x faster                                                                                                 |
| telco                            | 4.54 ms                                                                                                           | 4.51 ms: 1.01x faster                                                                                                 |
| xml_etree_iterparse              | 72.8 ms                                                                                                           | 72.3 ms: 1.01x faster                                                                                                 |
| genshi_xml                       | 31.5 ms                                                                                                           | 31.4 ms: 1.01x faster                                                                                                 |
| pickle                           | 7.48 us                                                                                                           | 7.44 us: 1.01x faster                                                                                                 |
| crypto_pyaes                     | 47.2 ms                                                                                                           | 47.0 ms: 1.00x faster                                                                                                 |
| pickle_dict                      | 18.1 us                                                                                                           | 18.0 us: 1.00x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 336 ms                                                                                                            | 335 ms: 1.00x faster                                                                                                  |
| logging_silent                   | 65.9 ns                                                                                                           | 65.7 ns: 1.00x faster                                                                                                 |
| pprint_safe_repr                 | 486 ms                                                                                                            | 487 ms: 1.00x slower                                                                                                  |
| regex_dna                        | 152 ms                                                                                                            | 152 ms: 1.00x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 353 ms                                                                                                            | 355 ms: 1.00x slower                                                                                                  |
| regex_v8                         | 17.0 ms                                                                                                           | 17.1 ms: 1.01x slower                                                                                                 |
| richards                         | 31.3 ms                                                                                                           | 31.5 ms: 1.01x slower                                                                                                 |
| pyflate                          | 329 ms                                                                                                            | 332 ms: 1.01x slower                                                                                                  |
| pprint_pformat                   | 989 ms                                                                                                            | 1.00 sec: 1.01x slower                                                                                                |
| async_tree_cpu_io_mixed          | 456 ms                                                                                                            | 462 ms: 1.01x slower                                                                                                  |
| sqlglot_parse                    | 756 us                                                                                                            | 765 us: 1.01x slower                                                                                                  |
| deepcopy_memo                    | 23.9 us                                                                                                           | 24.3 us: 1.01x slower                                                                                                 |
| sqlite_synth                     | 1.57 us                                                                                                           | 1.59 us: 1.01x slower                                                                                                 |
| async_tree_io                    | 558 ms                                                                                                            | 566 ms: 1.01x slower                                                                                                  |
| sqlglot_normalize                | 172 ms                                                                                                            | 175 ms: 1.02x slower                                                                                                  |
| create_gc_cycles                 | 835 us                                                                                                            | 849 us: 1.02x slower                                                                                                  |
| pycparser                        | 660 ms                                                                                                            | 671 ms: 1.02x slower                                                                                                  |
| sqlglot_transpile                | 918 us                                                                                                            | 935 us: 1.02x slower                                                                                                  |
| genshi_text                      | 14.6 ms                                                                                                           | 14.9 ms: 1.02x slower                                                                                                 |
| json_dumps                       | 6.25 ms                                                                                                           | 6.37 ms: 1.02x slower                                                                                                 |
| async_tree_eager                 | 64.2 ms                                                                                                           | 65.6 ms: 1.02x slower                                                                                                 |
| scimark_fft                      | 195 ms                                                                                                            | 200 ms: 1.02x slower                                                                                                  |
| deltablue                        | 2.30 ms                                                                                                           | 2.36 ms: 1.03x slower                                                                                                 |
| mdp                              | 1.53 sec                                                                                                          | 1.57 sec: 1.03x slower                                                                                                |
| scimark_sparse_mat_mult          | 3.05 ms                                                                                                           | 3.13 ms: 1.03x slower                                                                                                 |
| spectral_norm                    | 71.3 ms                                                                                                           | 73.7 ms: 1.03x slower                                                                                                 |
| bench_thread_pool                | 476 us                                                                                                            | 494 us: 1.04x slower                                                                                                  |
| meteor_contest                   | 71.3 ms                                                                                                           | 74.1 ms: 1.04x slower                                                                                                 |
| dulwich_log                      | 28.9 ms                                                                                                           | 30.0 ms: 1.04x slower                                                                                                 |
| go                               | 101 ms                                                                                                            | 105 ms: 1.04x slower                                                                                                  |
| sqlglot_optimize                 | 32.1 ms                                                                                                           | 33.6 ms: 1.05x slower                                                                                                 |
| docutils                         | 1.48 sec                                                                                                          | 1.55 sec: 1.05x slower                                                                                                |
| async_generators                 | 286 ms                                                                                                            | 300 ms: 1.05x slower                                                                                                  |
| 2to3                             | 165 ms                                                                                                            | 173 ms: 1.05x slower                                                                                                  |
| pylint                           | 149 ms                                                                                                            | 156 ms: 1.05x slower                                                                                                  |
| chaos                            | 36.5 ms                                                                                                           | 38.5 ms: 1.06x slower                                                                                                 |
| sympy_str                        | 132 ms                                                                                                            | 140 ms: 1.06x slower                                                                                                  |
| nbody                            | 66.1 ms                                                                                                           | 70.3 ms: 1.06x slower                                                                                                 |
| gc_traversal                     | 2.43 ms                                                                                                           | 2.59 ms: 1.06x slower                                                                                                 |
| scimark_sor                      | 101 ms                                                                                                            | 107 ms: 1.07x slower                                                                                                  |
| mypy2                            | 385 ms                                                                                                            | 413 ms: 1.07x slower                                                                                                  |
| nqueens                          | 56.2 ms                                                                                                           | 60.5 ms: 1.08x slower                                                                                                 |
| bench_mp_pool                    | 42.9 ms                                                                                                           | 46.4 ms: 1.08x slower                                                                                                 |
| sympy_sum                        | 70.0 ms                                                                                                           | 75.9 ms: 1.08x slower                                                                                                 |
| gunicorn                         | 1.10 ms                                                                                                           | 1.20 ms: 1.09x slower                                                                                                 |
| sympy_integrate                  | 10.4 ms                                                                                                           | 11.3 ms: 1.09x slower                                                                                                 |
| python_startup                   | 11.9 ms                                                                                                           | 13.4 ms: 1.12x slower                                                                                                 |
| python_startup_no_site           | 10.2 ms                                                                                                           | 11.6 ms: 1.13x slower                                                                                                 |
| raytrace                         | 157 ms                                                                                                            | 180 ms: 1.15x slower                                                                                                  |
| hexiom                           | 4.27 ms                                                                                                           | 4.96 ms: 1.16x slower                                                                                                 |
| regex_compile                    | 69.7 ms                                                                                                           | 81.0 ms: 1.16x slower                                                                                                 |
| comprehensions                   | 10.2 us                                                                                                           | 12.0 us: 1.17x slower                                                                                                 |
| scimark_lu                       | 68.9 ms                                                                                                           | 81.6 ms: 1.18x slower                                                                                                 |
| unpack_sequence                  | 26.9 ns                                                                                                           | 116 ns: 4.29x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.03x slower                                                                                                          |

Benchmark hidden because not significant (25): sympy_expand, asyncio_tcp, coverage, async_tree_eager_memoization_tg, pidigits, richards_super, asyncio_websockets, mako, async_tree_eager_io, async_tree_none_tg, django_template, async_tree_eager_io_tg, unpickle_list, json, async_tree_eager_memoization, async_tree_memoization_tg, pathlib, dask, regex_effbot, async_tree_memoization, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, aiohttp, async_tree_none, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x