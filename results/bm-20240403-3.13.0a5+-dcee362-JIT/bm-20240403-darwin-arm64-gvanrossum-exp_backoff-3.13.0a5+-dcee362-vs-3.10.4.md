# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: darwin-arm64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 171 ms: 1.12x faster                                              |
| chameleon      | 6.26 ms                                                | 4.47 ms: 1.40x faster                                             |
| docutils       | 1.73 sec                                               | 1.55 sec: 1.12x faster                                            |
| html5lib       | 42.4 ms                                                | 32.9 ms: 1.29x faster                                             |
| Geometric mean | (ref)                                                  | 1.19x faster                                                      |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 202 ms: 1.92x faster                                              |
| async_tree_memoization  | 474 ms                                                 | 260 ms: 1.82x faster                                              |
| async_tree_io           | 980 ms                                                 | 564 ms: 1.74x faster                                              |
| async_tree_cpu_io_mixed | 649 ms                                                 | 464 ms: 1.40x faster                                              |
| Geometric mean          | (ref)                                                  | 1.71x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.2 ms: 1.40x faster                                             |
| nbody          | 93.0 ms                                                | 70.7 ms: 1.31x faster                                             |
| Geometric mean | (ref)                                                  | 1.23x faster                                                      |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                              |
| regex_compile  | 95.3 ms                                                | 86.4 ms: 1.10x faster                                             |
| regex_effbot   | 2.46 ms                                                | 2.63 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                      |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 182 us: 1.54x faster                                              |
| unpickle_pure_python | 194 us                                                 | 139 us: 1.40x faster                                              |
| tomli_loads          | 1.71 sec                                               | 1.28 sec: 1.34x faster                                            |
| json_dumps           | 8.11 ms                                                | 6.33 ms: 1.28x faster                                             |
| xml_etree_process    | 46.5 ms                                                | 37.3 ms: 1.25x faster                                             |
| xml_etree_parse      | 108 ms                                                 | 106 ms: 1.02x faster                                              |
| xml_etree_generate   | 53.5 ms                                                | 54.3 ms: 1.01x slower                                             |
| json_loads           | 16.4 us                                                | 16.9 us: 1.03x slower                                             |
| unpickle             | 8.80 us                                                | 9.28 us: 1.05x slower                                             |
| pickle_dict          | 17.0 us                                                | 18.2 us: 1.07x slower                                             |
| pickle               | 6.97 us                                                | 7.50 us: 1.08x slower                                             |
| pickle_list          | 2.74 us                                                | 2.96 us: 1.08x slower                                             |
| unpickle_list        | 2.69 us                                                | 3.00 us: 1.11x slower                                             |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                      |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.3 ms: 1.22x slower                                             |
| python_startup_no_site | 7.91 ms                                                | 11.6 ms: 1.46x slower                                             |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 9.87 ms                                                | 6.97 ms: 1.42x faster                                             |
| genshi_text    | 17.3 ms                                                | 14.6 ms: 1.18x faster                                             |
| genshi_xml     | 33.8 ms                                                | 31.7 ms: 1.07x faster                                             |
| Geometric mean | (ref)                                                  | 1.21x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.2 us: 4.67x faster                                             |
| deltablue                | 4.91 ms                                                | 2.48 ms: 1.98x faster                                             |
| async_tree_none          | 388 ms                                                 | 202 ms: 1.92x faster                                              |
| raytrace                 | 301 ms                                                 | 163 ms: 1.85x faster                                              |
| logging_silent           | 117 ns                                                 | 63.7 ns: 1.84x faster                                             |
| async_tree_memoization   | 474 ms                                                 | 260 ms: 1.82x faster                                              |
| pylint                   | 277 ms                                                 | 154 ms: 1.79x faster                                              |
| async_tree_io            | 980 ms                                                 | 564 ms: 1.74x faster                                              |
| richards_super           | 57.8 ms                                                | 33.3 ms: 1.74x faster                                             |
| chaos                    | 65.8 ms                                                | 38.2 ms: 1.72x faster                                             |
| asyncio_tcp              | 659 ms                                                 | 390 ms: 1.69x faster                                              |
| richards                 | 48.7 ms                                                | 29.7 ms: 1.64x faster                                             |
| sqlglot_parse            | 1.24 ms                                                | 776 us: 1.60x faster                                              |
| crypto_pyaes             | 71.8 ms                                                | 46.3 ms: 1.55x faster                                             |
| pickle_pure_python       | 281 us                                                 | 182 us: 1.54x faster                                              |
| sqlglot_transpile        | 1.44 ms                                                | 943 us: 1.53x faster                                              |
| scimark_monte_carlo      | 65.6 ms                                                | 43.0 ms: 1.52x faster                                             |
| mypy2                    | 607 ms                                                 | 409 ms: 1.49x faster                                              |
| deepcopy_memo            | 34.7 us                                                | 24.2 us: 1.44x faster                                             |
| comprehensions           | 16.9 us                                                | 11.9 us: 1.42x faster                                             |
| mako                     | 9.87 ms                                                | 6.97 ms: 1.42x faster                                             |
| logging_simple           | 4.45 us                                                | 3.15 us: 1.41x faster                                             |
| go                       | 151 ms                                                 | 107 ms: 1.41x faster                                              |
| logging_format           | 4.83 us                                                | 3.44 us: 1.41x faster                                             |
| float                    | 69.0 ms                                                | 49.2 ms: 1.40x faster                                             |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 464 ms: 1.40x faster                                              |
| chameleon                | 6.26 ms                                                | 4.47 ms: 1.40x faster                                             |
| unpickle_pure_python     | 194 us                                                 | 139 us: 1.40x faster                                              |
| pycparser                | 877 ms                                                 | 652 ms: 1.34x faster                                              |
| pyflate                  | 427 ms                                                 | 317 ms: 1.34x faster                                              |
| tomli_loads              | 1.71 sec                                               | 1.28 sec: 1.34x faster                                            |
| nbody                    | 93.0 ms                                                | 70.7 ms: 1.31x faster                                             |
| pprint_pformat           | 1.30 sec                                               | 1.01 sec: 1.29x faster                                            |
| thrift                   | 572 us                                                 | 444 us: 1.29x faster                                              |
| html5lib                 | 42.4 ms                                                | 32.9 ms: 1.29x faster                                             |
| deepcopy                 | 272 us                                                 | 211 us: 1.29x faster                                              |
| spectral_norm            | 94.8 ms                                                | 73.7 ms: 1.29x faster                                             |
| hexiom                   | 6.19 ms                                                | 4.82 ms: 1.29x faster                                             |
| pprint_safe_repr         | 641 ms                                                 | 499 ms: 1.28x faster                                              |
| json_dumps               | 8.11 ms                                                | 6.33 ms: 1.28x faster                                             |
| scimark_lu               | 103 ms                                                 | 81.7 ms: 1.26x faster                                             |
| xml_etree_process        | 46.5 ms                                                | 37.3 ms: 1.25x faster                                             |
| deepcopy_reduce          | 2.33 us                                                | 1.87 us: 1.24x faster                                             |
| coroutines               | 20.7 ms                                                | 16.8 ms: 1.23x faster                                             |
| generators               | 32.3 ms                                                | 26.3 ms: 1.23x faster                                             |
| dulwich_log              | 35.3 ms                                                | 29.0 ms: 1.22x faster                                             |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.21x faster                                            |
| scimark_sor              | 128 ms                                                 | 106 ms: 1.21x faster                                              |
| sympy_sum                | 92.2 ms                                                | 76.6 ms: 1.20x faster                                             |
| genshi_text              | 17.3 ms                                                | 14.6 ms: 1.18x faster                                             |
| sympy_integrate          | 13.1 ms                                                | 11.3 ms: 1.16x faster                                             |
| fannkuch                 | 303 ms                                                 | 263 ms: 1.15x faster                                              |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                              |
| dask                     | 253 ms                                                 | 222 ms: 1.14x faster                                              |
| sympy_str                | 165 ms                                                 | 145 ms: 1.14x faster                                              |
| sympy_expand             | 269 ms                                                 | 237 ms: 1.13x faster                                              |
| scimark_fft              | 224 ms                                                 | 200 ms: 1.12x faster                                              |
| 2to3                     | 192 ms                                                 | 171 ms: 1.12x faster                                              |
| docutils                 | 1.73 sec                                               | 1.55 sec: 1.12x faster                                            |
| regex_compile            | 95.3 ms                                                | 86.4 ms: 1.10x faster                                             |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.12 ms: 1.10x faster                                             |
| gunicorn                 | 1.30 ms                                                | 1.19 ms: 1.10x faster                                             |
| sqlglot_optimize         | 36.8 ms                                                | 33.7 ms: 1.09x faster                                             |
| aiohttp                  | 1.22 ms                                                | 1.12 ms: 1.09x faster                                             |
| sqlglot_normalize        | 190 ms                                                 | 176 ms: 1.08x faster                                              |
| bench_thread_pool        | 527 us                                                 | 489 us: 1.08x faster                                              |
| genshi_xml               | 33.8 ms                                                | 31.7 ms: 1.07x faster                                             |
| nqueens                  | 63.8 ms                                                | 60.6 ms: 1.05x faster                                             |
| meteor_contest           | 77.7 ms                                                | 74.2 ms: 1.05x faster                                             |
| json                     | 3.08 ms                                                | 2.94 ms: 1.05x faster                                             |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                            |
| xml_etree_parse          | 108 ms                                                 | 106 ms: 1.02x faster                                              |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                              |
| xml_etree_generate       | 53.5 ms                                                | 54.3 ms: 1.01x slower                                             |
| json_loads               | 16.4 us                                                | 16.9 us: 1.03x slower                                             |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                             |
| create_gc_cycles         | 860 us                                                 | 894 us: 1.04x slower                                              |
| unpickle                 | 8.80 us                                                | 9.28 us: 1.05x slower                                             |
| regex_effbot             | 2.46 ms                                                | 2.63 ms: 1.07x slower                                             |
| pickle_dict              | 17.0 us                                                | 18.2 us: 1.07x slower                                             |
| pickle                   | 6.97 us                                                | 7.50 us: 1.08x slower                                             |
| pickle_list              | 2.74 us                                                | 2.96 us: 1.08x slower                                             |
| sqlite_synth             | 1.46 us                                                | 1.58 us: 1.08x slower                                             |
| unpickle_list            | 2.69 us                                                | 3.00 us: 1.11x slower                                             |
| coverage                 | 41.5 ms                                                | 46.3 ms: 1.12x slower                                             |
| python_startup           | 10.9 ms                                                | 13.3 ms: 1.22x slower                                             |
| bench_mp_pool            | 37.4 ms                                                | 46.1 ms: 1.23x slower                                             |
| async_generators         | 231 ms                                                 | 297 ms: 1.28x slower                                              |
| telco                    | 3.49 ms                                                | 4.54 ms: 1.30x slower                                             |
| python_startup_no_site   | 7.91 ms                                                | 11.6 ms: 1.46x slower                                             |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                      |

Benchmark hidden because not significant (5): tornado_http, pidigits, regex_v8, xml_etree_iterparse, pathlib
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240403-3.13.0a5+-dcee362-JIT/bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.39x