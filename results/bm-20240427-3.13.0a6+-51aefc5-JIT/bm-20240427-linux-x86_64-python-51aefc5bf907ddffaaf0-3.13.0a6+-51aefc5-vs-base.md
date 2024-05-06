# Results vs. base

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.02x slower
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 271 ms                                                                                                            | 282 ms: 1.04x slower                                                                                                  |
| chameleon      | 7.29 ms                                                                                                           | 7.03 ms: 1.04x faster                                                                                                 |
| docutils       | 2.82 sec                                                                                                          | 2.96 sec: 1.05x slower                                                                                                |
| tornado_http   | 94.4 ms                                                                                                           | 96.6 ms: 1.02x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io  | 908 ms                                                                                                            | 947 ms: 1.04x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                                                                           | 76.9 ms: 1.03x faster                                                                                                 |
| pidigits       | 194 ms                                                                                                            | 189 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 227 ms                                                                                                            | 218 ms: 1.04x faster                                                                                                  |
| regex_v8       | 24.9 ms                                                                                                           | 24.3 ms: 1.02x faster                                                                                                 |
| regex_effbot   | 3.67 ms                                                                                                           | 3.64 ms: 1.01x faster                                                                                                 |
| regex_compile  | 136 ms                                                                                                            | 143 ms: 1.05x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                                                                          | 2.04 sec: 1.08x faster                                                                                                |
| xml_etree_parse      | 160 ms                                                                                                            | 152 ms: 1.06x faster                                                                                                  |
| pickle_dict          | 35.8 us                                                                                                           | 34.7 us: 1.03x faster                                                                                                 |
| xml_etree_iterparse  | 107 ms                                                                                                            | 104 ms: 1.03x faster                                                                                                  |
| pickle               | 12.0 us                                                                                                           | 11.7 us: 1.03x faster                                                                                                 |
| json_dumps           | 10.7 ms                                                                                                           | 10.5 ms: 1.01x faster                                                                                                 |
| json_loads           | 27.6 us                                                                                                           | 27.3 us: 1.01x faster                                                                                                 |
| unpickle             | 15.3 us                                                                                                           | 15.2 us: 1.01x faster                                                                                                 |
| unpickle_list        | 5.32 us                                                                                                           | 5.36 us: 1.01x slower                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                            | 311 us: 1.02x slower                                                                                                  |
| pickle_list          | 5.02 us                                                                                                           | 5.11 us: 1.02x slower                                                                                                 |
| unpickle_pure_python | 219 us                                                                                                            | 235 us: 1.07x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                                                           | 11.0 ms: 1.05x slower                                                                                                 |
| python_startup_no_site | 7.11 ms                                                                                                           | 7.61 ms: 1.07x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.06x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                                                                           | 10.7 ms: 1.03x faster                                                                                                 |
| django_template | 34.9 ms                                                                                                           | 37.0 ms: 1.06x slower                                                                                                 |
| genshi_text     | 24.8 ms                                                                                                           | 26.5 ms: 1.07x slower                                                                                                 |
| genshi_xml      | 54.0 ms                                                                                                           | 57.9 ms: 1.07x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.04x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                | results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json | results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards                 | 48.0 ms                                                                                                           | 43.2 ms: 1.11x faster                                                                                                 |
| richards_super           | 54.3 ms                                                                                                           | 49.0 ms: 1.11x faster                                                                                                 |
| tomli_loads              | 2.20 sec                                                                                                          | 2.04 sec: 1.08x faster                                                                                                |
| scimark_fft              | 369 ms                                                                                                            | 344 ms: 1.07x faster                                                                                                  |
| xml_etree_parse          | 160 ms                                                                                                            | 152 ms: 1.06x faster                                                                                                  |
| scimark_sparse_mat_mult  | 5.20 ms                                                                                                           | 4.94 ms: 1.05x faster                                                                                                 |
| fannkuch                 | 401 ms                                                                                                            | 383 ms: 1.05x faster                                                                                                  |
| pyflate                  | 484 ms                                                                                                            | 463 ms: 1.04x faster                                                                                                  |
| regex_dna                | 227 ms                                                                                                            | 218 ms: 1.04x faster                                                                                                  |
| chameleon                | 7.29 ms                                                                                                           | 7.03 ms: 1.04x faster                                                                                                 |
| mako                     | 11.0 ms                                                                                                           | 10.7 ms: 1.03x faster                                                                                                 |
| pickle_dict              | 35.8 us                                                                                                           | 34.7 us: 1.03x faster                                                                                                 |
| xml_etree_iterparse      | 107 ms                                                                                                            | 104 ms: 1.03x faster                                                                                                  |
| float                    | 78.9 ms                                                                                                           | 76.9 ms: 1.03x faster                                                                                                 |
| pickle                   | 12.0 us                                                                                                           | 11.7 us: 1.03x faster                                                                                                 |
| pprint_safe_repr         | 759 ms                                                                                                            | 740 ms: 1.03x faster                                                                                                  |
| pidigits                 | 194 ms                                                                                                            | 189 ms: 1.02x faster                                                                                                  |
| sqlite_synth             | 2.92 us                                                                                                           | 2.85 us: 1.02x faster                                                                                                 |
| regex_v8                 | 24.9 ms                                                                                                           | 24.3 ms: 1.02x faster                                                                                                 |
| pprint_pformat           | 1.55 sec                                                                                                          | 1.53 sec: 1.01x faster                                                                                                |
| json_dumps               | 10.7 ms                                                                                                           | 10.5 ms: 1.01x faster                                                                                                 |
| json                     | 5.16 ms                                                                                                           | 5.10 ms: 1.01x faster                                                                                                 |
| coroutines               | 23.0 ms                                                                                                           | 22.8 ms: 1.01x faster                                                                                                 |
| regex_effbot             | 3.67 ms                                                                                                           | 3.64 ms: 1.01x faster                                                                                                 |
| json_loads               | 27.6 us                                                                                                           | 27.3 us: 1.01x faster                                                                                                 |
| crypto_pyaes             | 74.8 ms                                                                                                           | 74.3 ms: 1.01x faster                                                                                                 |
| unpickle                 | 15.3 us                                                                                                           | 15.2 us: 1.01x faster                                                                                                 |
| meteor_contest           | 112 ms                                                                                                            | 111 ms: 1.00x faster                                                                                                  |
| unpickle_list            | 5.32 us                                                                                                           | 5.36 us: 1.01x slower                                                                                                 |
| asyncio_tcp_ssl          | 1.84 sec                                                                                                          | 1.86 sec: 1.01x slower                                                                                                |
| thrift                   | 810 us                                                                                                            | 821 us: 1.01x slower                                                                                                  |
| create_gc_cycles         | 1.76 ms                                                                                                           | 1.78 ms: 1.02x slower                                                                                                 |
| pickle_pure_python       | 306 us                                                                                                            | 311 us: 1.02x slower                                                                                                  |
| pickle_list              | 5.02 us                                                                                                           | 5.11 us: 1.02x slower                                                                                                 |
| dask                     | 370 ms                                                                                                            | 376 ms: 1.02x slower                                                                                                  |
| deepcopy                 | 361 us                                                                                                            | 369 us: 1.02x slower                                                                                                  |
| tornado_http             | 94.4 ms                                                                                                           | 96.6 ms: 1.02x slower                                                                                                 |
| djangocms                | 31.7 us                                                                                                           | 32.5 us: 1.02x slower                                                                                                 |
| asyncio_tcp              | 509 ms                                                                                                            | 522 ms: 1.03x slower                                                                                                  |
| generators               | 29.6 ms                                                                                                           | 30.4 ms: 1.03x slower                                                                                                 |
| logging_format           | 6.41 us                                                                                                           | 6.63 us: 1.04x slower                                                                                                 |
| logging_simple           | 5.77 us                                                                                                           | 5.97 us: 1.04x slower                                                                                                 |
| gunicorn                 | 1.26 ms                                                                                                           | 1.31 ms: 1.04x slower                                                                                                 |
| sqlglot_normalize        | 111 ms                                                                                                            | 115 ms: 1.04x slower                                                                                                  |
| sqlglot_parse            | 1.28 ms                                                                                                           | 1.33 ms: 1.04x slower                                                                                                 |
| 2to3                     | 271 ms                                                                                                            | 282 ms: 1.04x slower                                                                                                  |
| bench_thread_pool        | 835 us                                                                                                            | 870 us: 1.04x slower                                                                                                  |
| async_tree_io            | 908 ms                                                                                                            | 947 ms: 1.04x slower                                                                                                  |
| sqlglot_transpile        | 1.59 ms                                                                                                           | 1.66 ms: 1.04x slower                                                                                                 |
| typing_runtime_protocols | 167 us                                                                                                            | 175 us: 1.04x slower                                                                                                  |
| python_startup           | 10.5 ms                                                                                                           | 11.0 ms: 1.05x slower                                                                                                 |
| async_generators         | 444 ms                                                                                                            | 465 ms: 1.05x slower                                                                                                  |
| docutils                 | 2.82 sec                                                                                                          | 2.96 sec: 1.05x slower                                                                                                |
| regex_compile            | 136 ms                                                                                                            | 143 ms: 1.05x slower                                                                                                  |
| aiohttp                  | 1.17 ms                                                                                                           | 1.22 ms: 1.05x slower                                                                                                 |
| chaos                    | 60.5 ms                                                                                                           | 63.7 ms: 1.05x slower                                                                                                 |
| sqlglot_optimize         | 55.3 ms                                                                                                           | 58.3 ms: 1.05x slower                                                                                                 |
| dulwich_log              | 65.8 ms                                                                                                           | 69.6 ms: 1.06x slower                                                                                                 |
| raytrace                 | 263 ms                                                                                                            | 279 ms: 1.06x slower                                                                                                  |
| django_template          | 34.9 ms                                                                                                           | 37.0 ms: 1.06x slower                                                                                                 |
| sympy_str                | 280 ms                                                                                                            | 299 ms: 1.06x slower                                                                                                  |
| sympy_expand             | 472 ms                                                                                                            | 502 ms: 1.07x slower                                                                                                  |
| gc_traversal             | 3.77 ms                                                                                                           | 4.02 ms: 1.07x slower                                                                                                 |
| genshi_text              | 24.8 ms                                                                                                           | 26.5 ms: 1.07x slower                                                                                                 |
| python_startup_no_site   | 7.11 ms                                                                                                           | 7.61 ms: 1.07x slower                                                                                                 |
| unpickle_pure_python     | 219 us                                                                                                            | 235 us: 1.07x slower                                                                                                  |
| genshi_xml               | 54.0 ms                                                                                                           | 57.9 ms: 1.07x slower                                                                                                 |
| pylint                   | 319 ms                                                                                                            | 346 ms: 1.08x slower                                                                                                  |
| comprehensions           | 16.8 us                                                                                                           | 18.3 us: 1.09x slower                                                                                                 |
| sympy_sum                | 156 ms                                                                                                            | 170 ms: 1.09x slower                                                                                                  |
| go                       | 143 ms                                                                                                            | 156 ms: 1.10x slower                                                                                                  |
| mypy2                    | 737 ms                                                                                                            | 813 ms: 1.10x slower                                                                                                  |
| sympy_integrate          | 20.3 ms                                                                                                           | 22.6 ms: 1.11x slower                                                                                                 |
| scimark_sor              | 126 ms                                                                                                            | 140 ms: 1.11x slower                                                                                                  |
| hexiom                   | 6.37 ms                                                                                                           | 7.16 ms: 1.12x slower                                                                                                 |
| nqueens                  | 80.6 ms                                                                                                           | 92.1 ms: 1.14x slower                                                                                                 |
| scimark_lu               | 118 ms                                                                                                            | 136 ms: 1.15x slower                                                                                                  |
| deltablue                | 3.23 ms                                                                                                           | 3.85 ms: 1.19x slower                                                                                                 |
| Geometric mean           | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (23): coverage, scimark_monte_carlo, telco, xml_etree_process, async_tree_cpu_io_mixed, xml_etree_generate, mdp, asyncio_websockets, async_tree_memoization_tg, pathlib, html5lib, nbody, deepcopy_reduce, async_tree_cpu_io_mixed_tg, bench_mp_pool, deepcopy_memo, spectral_norm, async_tree_none_tg, logging_silent, async_tree_io_tg, async_tree_memoization, pycparser, async_tree_none

# HPT report

- Reliability score: 99.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x