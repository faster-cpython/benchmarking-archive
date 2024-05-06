# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 281 ms: 1.24x faster                                              |
| chameleon      | 9.68 ms                                                | 7.19 ms: 1.35x faster                                             |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                            |
| html5lib       | 88.9 ms                                                | 66.8 ms: 1.33x faster                                             |
| tornado_http   | 136 ms                                                 | 97.1 ms: 1.40x faster                                             |
| Geometric mean | (ref)                                                  | 1.29x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                              |
| async_tree_none         | 728 ms                                                 | 391 ms: 1.86x faster                                              |
| async_tree_io           | 1.77 sec                                               | 957 ms: 1.85x faster                                              |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 601 ms: 1.69x faster                                              |
| Geometric mean          | (ref)                                                  | 1.82x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.6 ms: 1.69x faster                                             |
| float          | 117 ms                                                 | 77.1 ms: 1.52x faster                                             |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                  | 1.37x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 146 ms: 1.29x faster                                              |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                             |
| regex_dna      | 227 ms                                                 | 230 ms: 1.02x slower                                              |
| regex_effbot   | 3.63 ms                                                | 3.84 ms: 1.06x slower                                             |
| Geometric mean | (ref)                                                  | 1.07x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 308 us: 1.57x faster                                              |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                            |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                             |
| unpickle_pure_python | 331 us                                                 | 245 us: 1.35x faster                                              |
| xml_etree_process    | 79.1 ms                                                | 61.7 ms: 1.28x faster                                             |
| xml_etree_generate   | 99.4 ms                                                | 89.7 ms: 1.11x faster                                             |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                             |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                              |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                              |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                             |
| unpickle_list        | 5.20 us                                                | 5.38 us: 1.03x slower                                             |
| unpickle             | 14.4 us                                                | 15.7 us: 1.09x slower                                             |
| pickle               | 10.7 us                                                | 12.0 us: 1.12x slower                                             |
| pickle_dict          | 29.6 us                                                | 34.6 us: 1.17x slower                                             |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                             |
| python_startup_no_site | 5.93 ms                                                | 9.49 ms: 1.60x slower                                             |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.53x faster                                             |
| django_template | 48.2 ms                                                | 36.5 ms: 1.32x faster                                             |
| genshi_text     | 31.8 ms                                                | 25.4 ms: 1.25x faster                                             |
| genshi_xml      | 66.0 ms                                                | 56.4 ms: 1.17x faster                                             |
| Geometric mean  | (ref)                                                  | 1.31x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.66x faster                                              |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                             |
| deltablue                | 7.91 ms                                                | 3.93 ms: 2.01x faster                                             |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                              |
| async_tree_none          | 728 ms                                                 | 391 ms: 1.86x faster                                              |
| async_tree_io            | 1.77 sec                                               | 957 ms: 1.85x faster                                              |
| asyncio_tcp              | 922 ms                                                 | 511 ms: 1.80x faster                                              |
| richards_super           | 94.7 ms                                                | 53.9 ms: 1.76x faster                                             |
| logging_silent           | 190 ns                                                 | 108 ns: 1.76x faster                                              |
| chaos                    | 115 ms                                                 | 65.8 ms: 1.75x faster                                             |
| crypto_pyaes             | 128 ms                                                 | 74.6 ms: 1.71x faster                                             |
| raytrace                 | 507 ms                                                 | 297 ms: 1.71x faster                                              |
| nbody                    | 154 ms                                                 | 90.6 ms: 1.69x faster                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 601 ms: 1.69x faster                                              |
| richards                 | 79.3 ms                                                | 47.3 ms: 1.68x faster                                             |
| scimark_monte_carlo      | 118 ms                                                 | 71.2 ms: 1.66x faster                                             |
| scimark_sor              | 220 ms                                                 | 133 ms: 1.65x faster                                              |
| pylint                   | 551 ms                                                 | 338 ms: 1.63x faster                                              |
| sqlglot_parse            | 2.17 ms                                                | 1.35 ms: 1.61x faster                                             |
| pickle_pure_python       | 484 us                                                 | 308 us: 1.57x faster                                              |
| comprehensions           | 28.8 us                                                | 18.3 us: 1.57x faster                                             |
| go                       | 240 ms                                                 | 153 ms: 1.57x faster                                              |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.56x faster                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                             |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                             |
| float                    | 117 ms                                                 | 77.1 ms: 1.52x faster                                             |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                            |
| deepcopy_memo            | 58.5 us                                                | 39.7 us: 1.47x faster                                             |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.47x faster                                              |
| pyflate                  | 716 ms                                                 | 492 ms: 1.45x faster                                              |
| hexiom                   | 10.4 ms                                                | 7.15 ms: 1.45x faster                                             |
| tornado_http             | 136 ms                                                 | 97.1 ms: 1.40x faster                                             |
| logging_simple           | 8.30 us                                                | 5.98 us: 1.39x faster                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                            |
| logging_format           | 9.09 us                                                | 6.61 us: 1.38x faster                                             |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                            |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                             |
| scimark_fft              | 466 ms                                                 | 346 ms: 1.35x faster                                              |
| chameleon                | 9.68 ms                                                | 7.19 ms: 1.35x faster                                             |
| unpickle_pure_python     | 331 us                                                 | 245 us: 1.35x faster                                              |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                              |
| pprint_safe_repr         | 1.02 sec                                               | 759 ms: 1.34x faster                                              |
| html5lib                 | 88.9 ms                                                | 66.8 ms: 1.33x faster                                             |
| deepcopy                 | 479 us                                                 | 361 us: 1.33x faster                                              |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.32x faster                                              |
| thrift                   | 1.07 ms                                                | 810 us: 1.32x faster                                              |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                             |
| django_template          | 48.2 ms                                                | 36.5 ms: 1.32x faster                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.96 ms: 1.30x faster                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                             |
| regex_compile            | 188 ms                                                 | 146 ms: 1.29x faster                                              |
| xml_etree_process        | 79.1 ms                                                | 61.7 ms: 1.28x faster                                             |
| pycparser                | 1.58 sec                                               | 1.23 sec: 1.28x faster                                            |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.25x faster                                              |
| genshi_text              | 31.8 ms                                                | 25.4 ms: 1.25x faster                                             |
| 2to3                     | 348 ms                                                 | 281 ms: 1.24x faster                                              |
| djangocms                | 38.4 us                                                | 32.0 us: 1.20x faster                                             |
| sqlglot_optimize         | 69.2 ms                                                | 58.0 ms: 1.19x faster                                             |
| dulwich_log              | 84.3 ms                                                | 70.7 ms: 1.19x faster                                             |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                             |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.18x faster                                              |
| sympy_str                | 346 ms                                                 | 292 ms: 1.18x faster                                              |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                             |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                             |
| genshi_xml               | 66.0 ms                                                | 56.4 ms: 1.17x faster                                             |
| nqueens                  | 106 ms                                                 | 90.7 ms: 1.17x faster                                             |
| dask                     | 441 ms                                                 | 378 ms: 1.17x faster                                              |
| bench_thread_pool        | 986 us                                                 | 856 us: 1.15x faster                                              |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                            |
| sympy_expand             | 566 ms                                                 | 498 ms: 1.14x faster                                              |
| mypy2                    | 894 ms                                                 | 791 ms: 1.13x faster                                              |
| xml_etree_generate       | 99.4 ms                                                | 89.7 ms: 1.11x faster                                             |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                             |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                             |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.07x faster                                              |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                              |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                             |
| mdp                      | 2.85 sec                                               | 2.67 sec: 1.07x faster                                            |
| json                     | 5.69 ms                                                | 5.36 ms: 1.06x faster                                             |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                             |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                              |
| pickle_list              | 5.08 us                                                | 4.93 us: 1.03x faster                                             |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                              |
| regex_dna                | 227 ms                                                 | 230 ms: 1.02x slower                                              |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                              |
| unpickle_list            | 5.20 us                                                | 5.38 us: 1.03x slower                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.69 ms: 1.04x slower                                             |
| gc_traversal             | 3.62 ms                                                | 3.78 ms: 1.04x slower                                             |
| async_generators         | 444 ms                                                 | 466 ms: 1.05x slower                                              |
| regex_effbot             | 3.63 ms                                                | 3.84 ms: 1.06x slower                                             |
| unpickle                 | 14.4 us                                                | 15.7 us: 1.09x slower                                             |
| pickle                   | 10.7 us                                                | 12.0 us: 1.12x slower                                             |
| pickle_dict              | 29.6 us                                                | 34.6 us: 1.17x slower                                             |
| telco                    | 7.27 ms                                                | 8.71 ms: 1.20x slower                                             |
| coverage                 | 79.4 ms                                                | 99.8 ms: 1.26x slower                                             |
| unpack_sequence          | 60.0 ns                                                | 86.2 ns: 1.44x slower                                             |
| python_startup_no_site   | 5.93 ms                                                | 9.49 ms: 1.60x slower                                             |
| Geometric mean           | (ref)                                                  | 1.29x faster                                                      |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-7bb5618-JIT/bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x