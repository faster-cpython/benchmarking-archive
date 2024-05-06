# Results vs. base

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 161 ms                                                                                                            | 172 ms: 1.07x slower                                                                                                          |
| chameleon      | 4.49 ms                                                                                                           | 4.68 ms: 1.04x slower                                                                                                         |
| docutils       | 1.45 sec                                                                                                          | 1.57 sec: 1.08x slower                                                                                                        |
| html5lib       | 31.9 ms                                                                                                           | 32.2 ms: 1.01x slower                                                                                                         |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed | 365 ms                                                                                                            | 368 ms: 1.01x slower                                                                                                          |
| async_tree_io                 | 566 ms                                                                                                            | 576 ms: 1.02x slower                                                                                                          |
| async_tree_none_tg            | 197 ms                                                                                                            | 204 ms: 1.03x slower                                                                                                          |
| async_tree_eager_tg           | 43.4 ms                                                                                                           | 45.4 ms: 1.05x slower                                                                                                         |
| async_tree_none               | 202 ms                                                                                                            | 212 ms: 1.05x slower                                                                                                          |
| async_tree_eager              | 63.0 ms                                                                                                           | 68.6 ms: 1.09x slower                                                                                                         |
| Geometric mean                | (ref)                                                                                                             | 1.03x slower                                                                                                                  |

Benchmark hidden because not significant (10): async_tree_eager_cpu_io_mixed_tg, async_tree_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| float          | 50.8 ms                                                                                                           | 64.7 ms: 1.27x slower                                                                                                         |
| nbody          | 65.2 ms                                                                                                           | 83.4 ms: 1.28x slower                                                                                                         |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 149 ms                                                                                                            | 149 ms: 1.00x faster                                                                                                          |
| regex_v8       | 17.4 ms                                                                                                           | 17.6 ms: 1.01x slower                                                                                                         |
| regex_compile  | 69.4 ms                                                                                                           | 92.8 ms: 1.34x slower                                                                                                         |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                                  |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 17.1 us                                                                                                           | 17.0 us: 1.01x faster                                                                                                         |
| pickle_dict          | 18.2 us                                                                                                           | 18.1 us: 1.00x faster                                                                                                         |
| unpickle_list        | 2.90 us                                                                                                           | 2.91 us: 1.00x slower                                                                                                         |
| pickle               | 7.44 us                                                                                                           | 7.47 us: 1.00x slower                                                                                                         |
| pickle_pure_python   | 183 us                                                                                                            | 184 us: 1.01x slower                                                                                                          |
| json_dumps           | 6.26 ms                                                                                                           | 6.39 ms: 1.02x slower                                                                                                         |
| xml_etree_process    | 37.9 ms                                                                                                           | 39.1 ms: 1.03x slower                                                                                                         |
| xml_etree_generate   | 54.9 ms                                                                                                           | 56.8 ms: 1.03x slower                                                                                                         |
| xml_etree_iterparse  | 68.8 ms                                                                                                           | 73.0 ms: 1.06x slower                                                                                                         |
| tomli_loads          | 1.50 sec                                                                                                          | 1.66 sec: 1.11x slower                                                                                                        |
| unpickle_pure_python | 143 us                                                                                                            | 181 us: 1.27x slower                                                                                                          |
| Geometric mean       | (ref)                                                                                                             | 1.04x slower                                                                                                                  |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 9.12 ms                                                                                                           | 9.19 ms: 1.01x slower                                                                                                         |
| python_startup         | 11.9 ms                                                                                                           | 12.0 ms: 1.01x slower                                                                                                         |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 31.7 ms                                                                                                           | 32.0 ms: 1.01x slower                                                                                                         |
| genshi_text     | 14.7 ms                                                                                                           | 15.0 ms: 1.02x slower                                                                                                         |
| django_template | 20.1 ms                                                                                                           | 22.3 ms: 1.11x slower                                                                                                         |
| mako            | 7.14 ms                                                                                                           | 9.33 ms: 1.31x slower                                                                                                         |
| Geometric mean  | (ref)                                                                                                             | 1.11x slower                                                                                                                  |

All benchmarks:
===============

| Benchmark                     | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| generators                    | 28.9 ms                                                                                                           | 26.0 ms: 1.11x faster                                                                                                         |
| coroutines                    | 17.2 ms                                                                                                           | 16.8 ms: 1.03x faster                                                                                                         |
| coverage                      | 47.1 ms                                                                                                           | 46.2 ms: 1.02x faster                                                                                                         |
| json                          | 2.96 ms                                                                                                           | 2.93 ms: 1.01x faster                                                                                                         |
| json_loads                    | 17.1 us                                                                                                           | 17.0 us: 1.01x faster                                                                                                         |
| pickle_dict                   | 18.2 us                                                                                                           | 18.1 us: 1.00x faster                                                                                                         |
| thrift                        | 444 us                                                                                                            | 443 us: 1.00x faster                                                                                                          |
| regex_dna                     | 149 ms                                                                                                            | 149 ms: 1.00x faster                                                                                                          |
| gc_traversal                  | 2.44 ms                                                                                                           | 2.45 ms: 1.00x slower                                                                                                         |
| unpickle_list                 | 2.90 us                                                                                                           | 2.91 us: 1.00x slower                                                                                                         |
| pickle                        | 7.44 us                                                                                                           | 7.47 us: 1.00x slower                                                                                                         |
| pickle_pure_python            | 183 us                                                                                                            | 184 us: 1.01x slower                                                                                                          |
| create_gc_cycles              | 872 us                                                                                                            | 877 us: 1.01x slower                                                                                                          |
| async_tree_eager_cpu_io_mixed | 365 ms                                                                                                            | 368 ms: 1.01x slower                                                                                                          |
| python_startup_no_site        | 9.12 ms                                                                                                           | 9.19 ms: 1.01x slower                                                                                                         |
| python_startup                | 11.9 ms                                                                                                           | 12.0 ms: 1.01x slower                                                                                                         |
| genshi_xml                    | 31.7 ms                                                                                                           | 32.0 ms: 1.01x slower                                                                                                         |
| html5lib                      | 31.9 ms                                                                                                           | 32.2 ms: 1.01x slower                                                                                                         |
| regex_v8                      | 17.4 ms                                                                                                           | 17.6 ms: 1.01x slower                                                                                                         |
| logging_silent                | 64.8 ns                                                                                                           | 65.6 ns: 1.01x slower                                                                                                         |
| logging_format                | 3.42 us                                                                                                           | 3.47 us: 1.01x slower                                                                                                         |
| dask                          | 219 ms                                                                                                            | 222 ms: 1.01x slower                                                                                                          |
| telco                         | 4.65 ms                                                                                                           | 4.72 ms: 1.01x slower                                                                                                         |
| async_tree_io                 | 566 ms                                                                                                            | 576 ms: 1.02x slower                                                                                                          |
| deepcopy                      | 216 us                                                                                                            | 219 us: 1.02x slower                                                                                                          |
| logging_simple                | 3.15 us                                                                                                           | 3.21 us: 1.02x slower                                                                                                         |
| json_dumps                    | 6.26 ms                                                                                                           | 6.39 ms: 1.02x slower                                                                                                         |
| genshi_text                   | 14.7 ms                                                                                                           | 15.0 ms: 1.02x slower                                                                                                         |
| async_generators              | 286 ms                                                                                                            | 294 ms: 1.03x slower                                                                                                          |
| xml_etree_process             | 37.9 ms                                                                                                           | 39.1 ms: 1.03x slower                                                                                                         |
| xml_etree_generate            | 54.9 ms                                                                                                           | 56.8 ms: 1.03x slower                                                                                                         |
| async_tree_none_tg            | 197 ms                                                                                                            | 204 ms: 1.03x slower                                                                                                          |
| chameleon                     | 4.49 ms                                                                                                           | 4.68 ms: 1.04x slower                                                                                                         |
| dulwich_log                   | 27.7 ms                                                                                                           | 28.9 ms: 1.04x slower                                                                                                         |
| async_tree_eager_tg           | 43.4 ms                                                                                                           | 45.4 ms: 1.05x slower                                                                                                         |
| sqlite_synth                  | 1.56 us                                                                                                           | 1.63 us: 1.05x slower                                                                                                         |
| async_tree_none               | 202 ms                                                                                                            | 212 ms: 1.05x slower                                                                                                          |
| typing_runtime_protocols      | 68.0 us                                                                                                           | 71.2 us: 1.05x slower                                                                                                         |
| mdp                           | 1.54 sec                                                                                                          | 1.61 sec: 1.05x slower                                                                                                        |
| pycparser                     | 640 ms                                                                                                            | 672 ms: 1.05x slower                                                                                                          |
| xml_etree_iterparse           | 68.8 ms                                                                                                           | 73.0 ms: 1.06x slower                                                                                                         |
| sympy_expand                  | 229 ms                                                                                                            | 244 ms: 1.06x slower                                                                                                          |
| bench_thread_pool             | 472 us                                                                                                            | 503 us: 1.07x slower                                                                                                          |
| sqlglot_normalize             | 169 ms                                                                                                            | 181 ms: 1.07x slower                                                                                                          |
| aiohttp                       | 1.07 ms                                                                                                           | 1.15 ms: 1.07x slower                                                                                                         |
| 2to3                          | 161 ms                                                                                                            | 172 ms: 1.07x slower                                                                                                          |
| mypy2                         | 380 ms                                                                                                            | 408 ms: 1.07x slower                                                                                                          |
| docutils                      | 1.45 sec                                                                                                          | 1.57 sec: 1.08x slower                                                                                                        |
| gunicorn                      | 1.10 ms                                                                                                           | 1.19 ms: 1.09x slower                                                                                                         |
| async_tree_eager              | 63.0 ms                                                                                                           | 68.6 ms: 1.09x slower                                                                                                         |
| meteor_contest                | 71.8 ms                                                                                                           | 78.9 ms: 1.10x slower                                                                                                         |
| sqlglot_transpile             | 908 us                                                                                                            | 1.00 ms: 1.10x slower                                                                                                         |
| tomli_loads                   | 1.50 sec                                                                                                          | 1.66 sec: 1.11x slower                                                                                                        |
| django_template               | 20.1 ms                                                                                                           | 22.3 ms: 1.11x slower                                                                                                         |
| sqlglot_parse                 | 749 us                                                                                                            | 833 us: 1.11x slower                                                                                                          |
| sqlglot_optimize              | 31.5 ms                                                                                                           | 35.2 ms: 1.11x slower                                                                                                         |
| scimark_sor                   | 99.4 ms                                                                                                           | 112 ms: 1.13x slower                                                                                                          |
| sympy_integrate               | 10.4 ms                                                                                                           | 11.8 ms: 1.13x slower                                                                                                         |
| sympy_str                     | 134 ms                                                                                                            | 151 ms: 1.13x slower                                                                                                          |
| richards                      | 31.2 ms                                                                                                           | 35.4 ms: 1.14x slower                                                                                                         |
| richards_super                | 34.3 ms                                                                                                           | 39.0 ms: 1.14x slower                                                                                                         |
| deepcopy_memo                 | 23.9 us                                                                                                           | 27.3 us: 1.14x slower                                                                                                         |
| sympy_sum                     | 70.6 ms                                                                                                           | 81.0 ms: 1.15x slower                                                                                                         |
| go                            | 100 ms                                                                                                            | 119 ms: 1.18x slower                                                                                                          |
| raytrace                      | 153 ms                                                                                                            | 181 ms: 1.19x slower                                                                                                          |
| crypto_pyaes                  | 46.5 ms                                                                                                           | 56.6 ms: 1.22x slower                                                                                                         |
| pprint_safe_repr              | 479 ms                                                                                                            | 587 ms: 1.23x slower                                                                                                          |
| pprint_pformat                | 972 ms                                                                                                            | 1.20 sec: 1.24x slower                                                                                                        |
| nqueens                       | 56.3 ms                                                                                                           | 69.9 ms: 1.24x slower                                                                                                         |
| scimark_fft                   | 195 ms                                                                                                            | 246 ms: 1.26x slower                                                                                                          |
| unpickle_pure_python          | 143 us                                                                                                            | 181 us: 1.27x slower                                                                                                          |
| float                         | 50.8 ms                                                                                                           | 64.7 ms: 1.27x slower                                                                                                         |
| nbody                         | 65.2 ms                                                                                                           | 83.4 ms: 1.28x slower                                                                                                         |
| deltablue                     | 2.18 ms                                                                                                           | 2.81 ms: 1.29x slower                                                                                                         |
| pyflate                       | 322 ms                                                                                                            | 418 ms: 1.30x slower                                                                                                          |
| mako                          | 7.14 ms                                                                                                           | 9.33 ms: 1.31x slower                                                                                                         |
| fannkuch                      | 258 ms                                                                                                            | 341 ms: 1.32x slower                                                                                                          |
| scimark_sparse_mat_mult       | 3.02 ms                                                                                                           | 4.00 ms: 1.33x slower                                                                                                         |
| chaos                         | 36.3 ms                                                                                                           | 48.4 ms: 1.33x slower                                                                                                         |
| regex_compile                 | 69.4 ms                                                                                                           | 92.8 ms: 1.34x slower                                                                                                         |
| hexiom                        | 4.24 ms                                                                                                           | 5.96 ms: 1.41x slower                                                                                                         |
| spectral_norm                 | 71.0 ms                                                                                                           | 100 ms: 1.41x slower                                                                                                          |
| scimark_monte_carlo           | 44.5 ms                                                                                                           | 64.3 ms: 1.45x slower                                                                                                         |
| scimark_lu                    | 68.9 ms                                                                                                           | 101 ms: 1.47x slower                                                                                                          |
| comprehensions                | 10.6 us                                                                                                           | 16.5 us: 1.56x slower                                                                                                         |
| Geometric mean                | (ref)                                                                                                             | 1.09x slower                                                                                                                  |

Benchmark hidden because not significant (23): asyncio_tcp, regex_effbot, deepcopy_reduce, xml_etree_parse, unpickle, async_tree_eager_cpu_io_mixed_tg, pidigits, asyncio_websockets, pickle_list, asyncio_tcp_ssl, pathlib, async_tree_cpu_io_mixed_tg, bench_mp_pool, async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_memoization, tornado_http, pylint

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.01x