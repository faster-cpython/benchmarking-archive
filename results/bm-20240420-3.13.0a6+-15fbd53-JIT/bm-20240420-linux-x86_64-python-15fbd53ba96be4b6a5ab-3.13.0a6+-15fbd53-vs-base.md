# Results vs. base

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 268 ms                                                                                                            | 277 ms: 1.03x slower                                                                                                  |
| chameleon      | 7.04 ms                                                                                                           | 7.09 ms: 1.01x slower                                                                                                 |
| docutils       | 2.80 sec                                                                                                          | 2.89 sec: 1.03x slower                                                                                                |
| html5lib       | 67.3 ms                                                                                                           | 66.5 ms: 1.01x faster                                                                                                 |
| tornado_http   | 94.2 ms                                                                                                           | 94.9 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 78.8 ms                                                                                                           | 76.6 ms: 1.03x faster                                                                                                 |
| pidigits       | 193 ms                                                                                                            | 189 ms: 1.02x faster                                                                                                  |
| nbody          | 88.7 ms                                                                                                           | 94.3 ms: 1.06x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 3.74 ms                                                                                                           | 3.68 ms: 1.02x faster                                                                                                 |
| regex_v8       | 24.6 ms                                                                                                           | 25.2 ms: 1.02x slower                                                                                                 |
| regex_dna      | 221 ms                                                                                                            | 228 ms: 1.03x slower                                                                                                  |
| regex_compile  | 135 ms                                                                                                            | 140 ms: 1.04x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 2.18 sec                                                                                                          | 2.07 sec: 1.05x faster                                                                                                |
| xml_etree_parse      | 157 ms                                                                                                            | 152 ms: 1.04x faster                                                                                                  |
| pickle_list          | 5.16 us                                                                                                           | 5.00 us: 1.03x faster                                                                                                 |
| xml_etree_iterparse  | 108 ms                                                                                                            | 104 ms: 1.03x faster                                                                                                  |
| unpickle_list        | 5.46 us                                                                                                           | 5.32 us: 1.03x faster                                                                                                 |
| pickle_dict          | 35.6 us                                                                                                           | 35.1 us: 1.02x faster                                                                                                 |
| xml_etree_process    | 60.6 ms                                                                                                           | 59.8 ms: 1.01x faster                                                                                                 |
| json_dumps           | 10.6 ms                                                                                                           | 10.5 ms: 1.00x faster                                                                                                 |
| xml_etree_generate   | 87.1 ms                                                                                                           | 86.7 ms: 1.00x faster                                                                                                 |
| json_loads           | 27.6 us                                                                                                           | 27.7 us: 1.00x slower                                                                                                 |
| pickle_pure_python   | 302 us                                                                                                            | 304 us: 1.01x slower                                                                                                  |
| pickle               | 11.6 us                                                                                                           | 11.7 us: 1.01x slower                                                                                                 |
| unpickle             | 15.2 us                                                                                                           | 16.2 us: 1.06x slower                                                                                                 |
| unpickle_pure_python | 213 us                                                                                                            | 233 us: 1.09x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                                                           | 11.0 ms: 1.05x slower                                                                                                 |
| python_startup_no_site | 7.08 ms                                                                                                           | 7.57 ms: 1.07x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.06x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 52.9 ms                                                                                                           | 53.8 ms: 1.02x slower                                                                                                 |
| django_template | 35.0 ms                                                                                                           | 36.7 ms: 1.05x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark                | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards                 | 47.0 ms                                                                                                           | 42.6 ms: 1.10x faster                                                                                                 |
| scimark_fft              | 374 ms                                                                                                            | 339 ms: 1.10x faster                                                                                                  |
| scimark_sparse_mat_mult  | 5.23 ms                                                                                                           | 4.78 ms: 1.09x faster                                                                                                 |
| richards_super           | 53.0 ms                                                                                                           | 48.8 ms: 1.09x faster                                                                                                 |
| gc_traversal             | 3.78 ms                                                                                                           | 3.57 ms: 1.06x faster                                                                                                 |
| tomli_loads              | 2.18 sec                                                                                                          | 2.07 sec: 1.05x faster                                                                                                |
| typing_runtime_protocols | 117 us                                                                                                            | 113 us: 1.04x faster                                                                                                  |
| xml_etree_parse          | 157 ms                                                                                                            | 152 ms: 1.04x faster                                                                                                  |
| pickle_list              | 5.16 us                                                                                                           | 5.00 us: 1.03x faster                                                                                                 |
| xml_etree_iterparse      | 108 ms                                                                                                            | 104 ms: 1.03x faster                                                                                                  |
| float                    | 78.8 ms                                                                                                           | 76.6 ms: 1.03x faster                                                                                                 |
| unpickle_list            | 5.46 us                                                                                                           | 5.32 us: 1.03x faster                                                                                                 |
| logging_simple           | 5.95 us                                                                                                           | 5.82 us: 1.02x faster                                                                                                 |
| telco                    | 8.74 ms                                                                                                           | 8.56 ms: 1.02x faster                                                                                                 |
| pidigits                 | 193 ms                                                                                                            | 189 ms: 1.02x faster                                                                                                  |
| deepcopy_reduce          | 3.25 us                                                                                                           | 3.19 us: 1.02x faster                                                                                                 |
| regex_effbot             | 3.74 ms                                                                                                           | 3.68 ms: 1.02x faster                                                                                                 |
| logging_format           | 6.57 us                                                                                                           | 6.45 us: 1.02x faster                                                                                                 |
| sqlite_synth             | 2.97 us                                                                                                           | 2.93 us: 1.02x faster                                                                                                 |
| pickle_dict              | 35.6 us                                                                                                           | 35.1 us: 1.02x faster                                                                                                 |
| pyflate                  | 483 ms                                                                                                            | 476 ms: 1.02x faster                                                                                                  |
| fannkuch                 | 393 ms                                                                                                            | 388 ms: 1.01x faster                                                                                                  |
| xml_etree_process        | 60.6 ms                                                                                                           | 59.8 ms: 1.01x faster                                                                                                 |
| crypto_pyaes             | 75.4 ms                                                                                                           | 74.4 ms: 1.01x faster                                                                                                 |
| html5lib                 | 67.3 ms                                                                                                           | 66.5 ms: 1.01x faster                                                                                                 |
| json_dumps               | 10.6 ms                                                                                                           | 10.5 ms: 1.00x faster                                                                                                 |
| xml_etree_generate       | 87.1 ms                                                                                                           | 86.7 ms: 1.00x faster                                                                                                 |
| json_loads               | 27.6 us                                                                                                           | 27.7 us: 1.00x slower                                                                                                 |
| generators               | 29.9 ms                                                                                                           | 30.0 ms: 1.00x slower                                                                                                 |
| deepcopy                 | 358 us                                                                                                            | 359 us: 1.00x slower                                                                                                  |
| scimark_monte_carlo      | 68.7 ms                                                                                                           | 69.1 ms: 1.01x slower                                                                                                 |
| pickle_pure_python       | 302 us                                                                                                            | 304 us: 1.01x slower                                                                                                  |
| asyncio_tcp_ssl          | 1.84 sec                                                                                                          | 1.85 sec: 1.01x slower                                                                                                |
| asyncio_websockets       | 564 ms                                                                                                            | 567 ms: 1.01x slower                                                                                                  |
| chameleon                | 7.04 ms                                                                                                           | 7.09 ms: 1.01x slower                                                                                                 |
| meteor_contest           | 110 ms                                                                                                            | 111 ms: 1.01x slower                                                                                                  |
| tornado_http             | 94.2 ms                                                                                                           | 94.9 ms: 1.01x slower                                                                                                 |
| asyncio_tcp              | 505 ms                                                                                                            | 509 ms: 1.01x slower                                                                                                  |
| pickle                   | 11.6 us                                                                                                           | 11.7 us: 1.01x slower                                                                                                 |
| create_gc_cycles         | 1.74 ms                                                                                                           | 1.76 ms: 1.01x slower                                                                                                 |
| dask                     | 367 ms                                                                                                            | 372 ms: 1.01x slower                                                                                                  |
| scimark_sor              | 129 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                  |
| sqlglot_parse            | 1.29 ms                                                                                                           | 1.31 ms: 1.02x slower                                                                                                 |
| genshi_xml               | 52.9 ms                                                                                                           | 53.8 ms: 1.02x slower                                                                                                 |
| sqlglot_transpile        | 1.60 ms                                                                                                           | 1.62 ms: 1.02x slower                                                                                                 |
| pprint_safe_repr         | 740 ms                                                                                                            | 753 ms: 1.02x slower                                                                                                  |
| pprint_pformat           | 1.51 sec                                                                                                          | 1.54 sec: 1.02x slower                                                                                                |
| gunicorn                 | 1.27 ms                                                                                                           | 1.29 ms: 1.02x slower                                                                                                 |
| pycparser                | 1.15 sec                                                                                                          | 1.17 sec: 1.02x slower                                                                                                |
| aiohttp                  | 1.17 ms                                                                                                           | 1.20 ms: 1.02x slower                                                                                                 |
| regex_v8                 | 24.6 ms                                                                                                           | 25.2 ms: 1.02x slower                                                                                                 |
| bench_thread_pool        | 830 us                                                                                                            | 852 us: 1.03x slower                                                                                                  |
| sqlglot_normalize        | 109 ms                                                                                                            | 112 ms: 1.03x slower                                                                                                  |
| deepcopy_memo            | 37.4 us                                                                                                           | 38.5 us: 1.03x slower                                                                                                 |
| docutils                 | 2.80 sec                                                                                                          | 2.89 sec: 1.03x slower                                                                                                |
| chaos                    | 60.6 ms                                                                                                           | 62.3 ms: 1.03x slower                                                                                                 |
| regex_dna                | 221 ms                                                                                                            | 228 ms: 1.03x slower                                                                                                  |
| raytrace                 | 262 ms                                                                                                            | 270 ms: 1.03x slower                                                                                                  |
| 2to3                     | 268 ms                                                                                                            | 277 ms: 1.03x slower                                                                                                  |
| regex_compile            | 135 ms                                                                                                            | 140 ms: 1.04x slower                                                                                                  |
| async_generators         | 442 ms                                                                                                            | 458 ms: 1.04x slower                                                                                                  |
| sqlglot_optimize         | 54.7 ms                                                                                                           | 56.9 ms: 1.04x slower                                                                                                 |
| dulwich_log              | 66.0 ms                                                                                                           | 68.7 ms: 1.04x slower                                                                                                 |
| mdp                      | 2.73 sec                                                                                                          | 2.84 sec: 1.04x slower                                                                                                |
| logging_silent           | 100 ns                                                                                                            | 104 ns: 1.04x slower                                                                                                  |
| sympy_expand             | 469 ms                                                                                                            | 490 ms: 1.04x slower                                                                                                  |
| python_startup           | 10.5 ms                                                                                                           | 11.0 ms: 1.05x slower                                                                                                 |
| sympy_str                | 279 ms                                                                                                            | 292 ms: 1.05x slower                                                                                                  |
| django_template          | 35.0 ms                                                                                                           | 36.7 ms: 1.05x slower                                                                                                 |
| sympy_sum                | 157 ms                                                                                                            | 166 ms: 1.06x slower                                                                                                  |
| go                       | 145 ms                                                                                                            | 153 ms: 1.06x slower                                                                                                  |
| unpickle                 | 15.2 us                                                                                                           | 16.2 us: 1.06x slower                                                                                                 |
| nbody                    | 88.7 ms                                                                                                           | 94.3 ms: 1.06x slower                                                                                                 |
| mypy2                    | 735 ms                                                                                                            | 782 ms: 1.06x slower                                                                                                  |
| python_startup_no_site   | 7.08 ms                                                                                                           | 7.57 ms: 1.07x slower                                                                                                 |
| sympy_integrate          | 20.3 ms                                                                                                           | 21.8 ms: 1.07x slower                                                                                                 |
| comprehensions           | 16.6 us                                                                                                           | 17.9 us: 1.08x slower                                                                                                 |
| unpickle_pure_python     | 213 us                                                                                                            | 233 us: 1.09x slower                                                                                                  |
| hexiom                   | 6.23 ms                                                                                                           | 6.80 ms: 1.09x slower                                                                                                 |
| deltablue                | 3.24 ms                                                                                                           | 3.61 ms: 1.11x slower                                                                                                 |
| nqueens                  | 79.9 ms                                                                                                           | 89.2 ms: 1.12x slower                                                                                                 |
| scimark_lu               | 114 ms                                                                                                            | 133 ms: 1.16x slower                                                                                                  |
| Geometric mean           | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (19): async_tree_cpu_io_mixed_tg, thrift, json, async_tree_cpu_io_mixed, spectral_norm, coverage, async_tree_io, pathlib, mako, genshi_text, coroutines, async_tree_memoization, async_tree_none_tg, bench_mp_pool, async_tree_memoization_tg, djangocms, async_tree_io_tg, async_tree_none, pylint

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x