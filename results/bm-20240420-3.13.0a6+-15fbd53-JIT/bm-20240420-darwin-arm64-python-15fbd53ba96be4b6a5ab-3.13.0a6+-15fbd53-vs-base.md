# Results vs. base

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 92.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 161 ms                                                                                                            | 168 ms: 1.05x slower                                                                                                  |
| chameleon      | 4.49 ms                                                                                                           | 4.47 ms: 1.00x faster                                                                                                 |
| docutils       | 1.45 sec                                                                                                          | 1.49 sec: 1.03x slower                                                                                                |
| html5lib       | 31.9 ms                                                                                                           | 31.1 ms: 1.03x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io                    | 566 ms                                                                                                            | 557 ms: 1.02x faster                                                                                                  |
| async_tree_eager_tg              | 43.4 ms                                                                                                           | 42.9 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 336 ms                                                                                                            | 334 ms: 1.01x faster                                                                                                  |
| async_tree_eager                 | 63.0 ms                                                                                                           | 64.0 ms: 1.02x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (12): async_tree_eager_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_eager_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_eager_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 50.8 ms                                                                                                           | 48.6 ms: 1.05x faster                                                                                                 |
| nbody          | 65.2 ms                                                                                                           | 70.1 ms: 1.07x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.63 ms                                                                                                           | 2.57 ms: 1.02x faster                                                                                                 |
| regex_compile  | 69.4 ms                                                                                                           | 83.3 ms: 1.20x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 1.50 sec                                                                                                          | 1.26 sec: 1.19x faster                                                                                                |
| unpickle_pure_python | 143 us                                                                                                            | 135 us: 1.05x faster                                                                                                  |
| xml_etree_generate   | 54.9 ms                                                                                                           | 52.8 ms: 1.04x faster                                                                                                 |
| xml_etree_process    | 37.9 ms                                                                                                           | 36.7 ms: 1.03x faster                                                                                                 |
| pickle_pure_python   | 183 us                                                                                                            | 180 us: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 68.8 ms                                                                                                           | 67.7 ms: 1.02x faster                                                                                                 |
| xml_etree_parse      | 99.0 ms                                                                                                           | 97.8 ms: 1.01x faster                                                                                                 |
| unpickle_list        | 2.90 us                                                                                                           | 2.93 us: 1.01x slower                                                                                                 |
| json_dumps           | 6.26 ms                                                                                                           | 6.35 ms: 1.01x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (5): unpickle, pickle_dict, pickle, json_loads, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 11.9 ms                                                                                                           | 13.3 ms: 1.12x slower                                                                                                 |
| python_startup_no_site | 9.12 ms                                                                                                           | 10.5 ms: 1.15x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.13x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 7.14 ms                                                                                                           | 6.87 ms: 1.04x faster                                                                                                 |
| genshi_xml      | 31.7 ms                                                                                                           | 30.8 ms: 1.03x faster                                                                                                 |
| genshi_text     | 14.7 ms                                                                                                           | 14.6 ms: 1.01x faster                                                                                                 |
| django_template | 20.1 ms                                                                                                           | 20.4 ms: 1.02x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.01x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                        | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads                      | 1.50 sec                                                                                                          | 1.26 sec: 1.19x faster                                                                                                |
| generators                       | 28.9 ms                                                                                                           | 26.4 ms: 1.09x faster                                                                                                 |
| richards                         | 31.2 ms                                                                                                           | 29.5 ms: 1.06x faster                                                                                                 |
| unpickle_pure_python             | 143 us                                                                                                            | 135 us: 1.05x faster                                                                                                  |
| richards_super                   | 34.3 ms                                                                                                           | 32.8 ms: 1.05x faster                                                                                                 |
| float                            | 50.8 ms                                                                                                           | 48.6 ms: 1.05x faster                                                                                                 |
| mako                             | 7.14 ms                                                                                                           | 6.87 ms: 1.04x faster                                                                                                 |
| xml_etree_generate               | 54.9 ms                                                                                                           | 52.8 ms: 1.04x faster                                                                                                 |
| scimark_monte_carlo              | 44.5 ms                                                                                                           | 43.0 ms: 1.03x faster                                                                                                 |
| xml_etree_process                | 37.9 ms                                                                                                           | 36.7 ms: 1.03x faster                                                                                                 |
| deepcopy_reduce                  | 1.90 us                                                                                                           | 1.84 us: 1.03x faster                                                                                                 |
| genshi_xml                       | 31.7 ms                                                                                                           | 30.8 ms: 1.03x faster                                                                                                 |
| logging_simple                   | 3.15 us                                                                                                           | 3.07 us: 1.03x faster                                                                                                 |
| pyflate                          | 322 ms                                                                                                            | 314 ms: 1.03x faster                                                                                                  |
| html5lib                         | 31.9 ms                                                                                                           | 31.1 ms: 1.03x faster                                                                                                 |
| regex_effbot                     | 2.63 ms                                                                                                           | 2.57 ms: 1.02x faster                                                                                                 |
| logging_format                   | 3.42 us                                                                                                           | 3.34 us: 1.02x faster                                                                                                 |
| logging_silent                   | 64.8 ns                                                                                                           | 63.5 ns: 1.02x faster                                                                                                 |
| deepcopy                         | 216 us                                                                                                            | 212 us: 1.02x faster                                                                                                  |
| pathlib                          | 24.0 ms                                                                                                           | 23.5 ms: 1.02x faster                                                                                                 |
| pickle_pure_python               | 183 us                                                                                                            | 180 us: 1.02x faster                                                                                                  |
| thrift                           | 444 us                                                                                                            | 437 us: 1.02x faster                                                                                                  |
| async_tree_io                    | 566 ms                                                                                                            | 557 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse              | 68.8 ms                                                                                                           | 67.7 ms: 1.02x faster                                                                                                 |
| coverage                         | 47.1 ms                                                                                                           | 46.4 ms: 1.02x faster                                                                                                 |
| json                             | 2.96 ms                                                                                                           | 2.91 ms: 1.02x faster                                                                                                 |
| telco                            | 4.65 ms                                                                                                           | 4.58 ms: 1.01x faster                                                                                                 |
| xml_etree_parse                  | 99.0 ms                                                                                                           | 97.8 ms: 1.01x faster                                                                                                 |
| async_tree_eager_tg              | 43.4 ms                                                                                                           | 42.9 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 336 ms                                                                                                            | 334 ms: 1.01x faster                                                                                                  |
| genshi_text                      | 14.7 ms                                                                                                           | 14.6 ms: 1.01x faster                                                                                                 |
| crypto_pyaes                     | 46.5 ms                                                                                                           | 46.2 ms: 1.01x faster                                                                                                 |
| chameleon                        | 4.49 ms                                                                                                           | 4.47 ms: 1.00x faster                                                                                                 |
| asyncio_websockets               | 408 ms                                                                                                            | 409 ms: 1.00x slower                                                                                                  |
| gc_traversal                     | 2.44 ms                                                                                                           | 2.45 ms: 1.00x slower                                                                                                 |
| coroutines                       | 17.2 ms                                                                                                           | 17.2 ms: 1.00x slower                                                                                                 |
| deepcopy_memo                    | 23.9 us                                                                                                           | 24.1 us: 1.01x slower                                                                                                 |
| pycparser                        | 640 ms                                                                                                            | 645 ms: 1.01x slower                                                                                                  |
| sqlite_synth                     | 1.56 us                                                                                                           | 1.57 us: 1.01x slower                                                                                                 |
| unpickle_list                    | 2.90 us                                                                                                           | 2.93 us: 1.01x slower                                                                                                 |
| sqlglot_parse                    | 749 us                                                                                                            | 758 us: 1.01x slower                                                                                                  |
| json_dumps                       | 6.26 ms                                                                                                           | 6.35 ms: 1.01x slower                                                                                                 |
| pprint_safe_repr                 | 479 ms                                                                                                            | 486 ms: 1.01x slower                                                                                                  |
| async_tree_eager                 | 63.0 ms                                                                                                           | 64.0 ms: 1.02x slower                                                                                                 |
| meteor_contest                   | 71.8 ms                                                                                                           | 73.1 ms: 1.02x slower                                                                                                 |
| django_template                  | 20.1 ms                                                                                                           | 20.4 ms: 1.02x slower                                                                                                 |
| mdp                              | 1.54 sec                                                                                                          | 1.57 sec: 1.02x slower                                                                                                |
| sympy_expand                     | 229 ms                                                                                                            | 234 ms: 1.02x slower                                                                                                  |
| sqlglot_normalize                | 169 ms                                                                                                            | 173 ms: 1.02x slower                                                                                                  |
| sqlglot_transpile                | 908 us                                                                                                            | 929 us: 1.02x slower                                                                                                  |
| pprint_pformat                   | 972 ms                                                                                                            | 995 ms: 1.02x slower                                                                                                  |
| dulwich_log                      | 27.7 ms                                                                                                           | 28.4 ms: 1.03x slower                                                                                                 |
| docutils                         | 1.45 sec                                                                                                          | 1.49 sec: 1.03x slower                                                                                                |
| scimark_fft                      | 195 ms                                                                                                            | 201 ms: 1.03x slower                                                                                                  |
| bench_thread_pool                | 472 us                                                                                                            | 487 us: 1.03x slower                                                                                                  |
| async_generators                 | 286 ms                                                                                                            | 296 ms: 1.03x slower                                                                                                  |
| scimark_sparse_mat_mult          | 3.02 ms                                                                                                           | 3.12 ms: 1.03x slower                                                                                                 |
| spectral_norm                    | 71.0 ms                                                                                                           | 73.7 ms: 1.04x slower                                                                                                 |
| sympy_str                        | 134 ms                                                                                                            | 139 ms: 1.04x slower                                                                                                  |
| chaos                            | 36.3 ms                                                                                                           | 37.9 ms: 1.04x slower                                                                                                 |
| aiohttp                          | 1.07 ms                                                                                                           | 1.12 ms: 1.05x slower                                                                                                 |
| 2to3                             | 161 ms                                                                                                            | 168 ms: 1.05x slower                                                                                                  |
| sqlglot_optimize                 | 31.5 ms                                                                                                           | 33.1 ms: 1.05x slower                                                                                                 |
| nqueens                          | 56.3 ms                                                                                                           | 59.3 ms: 1.05x slower                                                                                                 |
| go                               | 100 ms                                                                                                            | 106 ms: 1.06x slower                                                                                                  |
| scimark_sor                      | 99.4 ms                                                                                                           | 105 ms: 1.06x slower                                                                                                  |
| mypy2                            | 380 ms                                                                                                            | 402 ms: 1.06x slower                                                                                                  |
| sympy_sum                        | 70.6 ms                                                                                                           | 74.8 ms: 1.06x slower                                                                                                 |
| raytrace                         | 153 ms                                                                                                            | 163 ms: 1.06x slower                                                                                                  |
| bench_mp_pool                    | 43.1 ms                                                                                                           | 46.2 ms: 1.07x slower                                                                                                 |
| sympy_integrate                  | 10.4 ms                                                                                                           | 11.2 ms: 1.07x slower                                                                                                 |
| nbody                            | 65.2 ms                                                                                                           | 70.1 ms: 1.07x slower                                                                                                 |
| gunicorn                         | 1.10 ms                                                                                                           | 1.19 ms: 1.08x slower                                                                                                 |
| hexiom                           | 4.24 ms                                                                                                           | 4.71 ms: 1.11x slower                                                                                                 |
| comprehensions                   | 10.6 us                                                                                                           | 11.8 us: 1.12x slower                                                                                                 |
| python_startup                   | 11.9 ms                                                                                                           | 13.3 ms: 1.12x slower                                                                                                 |
| deltablue                        | 2.18 ms                                                                                                           | 2.47 ms: 1.14x slower                                                                                                 |
| python_startup_no_site           | 9.12 ms                                                                                                           | 10.5 ms: 1.15x slower                                                                                                 |
| scimark_lu                       | 68.9 ms                                                                                                           | 81.6 ms: 1.18x slower                                                                                                 |
| regex_compile                    | 69.4 ms                                                                                                           | 83.3 ms: 1.20x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (28): async_tree_eager_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_eager_cpu_io_mixed, unpickle, pickle_dict, async_tree_cpu_io_mixed_tg, pickle, json_loads, fannkuch, pidigits, async_tree_eager_memoization, regex_dna, async_tree_memoization_tg, regex_v8, create_gc_cycles, pickle_list, asyncio_tcp_ssl, typing_runtime_protocols, asyncio_tcp, dask, tornado_http, pylint

# HPT report

- Reliability score: 92.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x