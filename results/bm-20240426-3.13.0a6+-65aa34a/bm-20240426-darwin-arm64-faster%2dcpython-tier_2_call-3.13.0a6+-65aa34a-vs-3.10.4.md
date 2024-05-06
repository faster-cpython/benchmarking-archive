# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: darwin-arm64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 161 ms: 1.19x faster                                                    |
| chameleon      | 6.26 ms                                                | 4.45 ms: 1.41x faster                                                   |
| docutils       | 1.73 sec                                               | 1.45 sec: 1.19x faster                                                  |
| html5lib       | 42.4 ms                                                | 31.7 ms: 1.34x faster                                                   |
| tornado_http   | 86.7 ms                                                | 74.1 ms: 1.17x faster                                                   |
| Geometric mean | (ref)                                                  | 1.26x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 202 ms: 1.92x faster                                                    |
| async_tree_memoization  | 474 ms                                                 | 268 ms: 1.76x faster                                                    |
| async_tree_io           | 980 ms                                                 | 568 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed | 649 ms                                                 | 463 ms: 1.40x faster                                                    |
| Geometric mean          | (ref)                                                  | 1.69x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 51.1 ms: 1.35x faster                                                   |
| nbody          | 93.0 ms                                                | 69.9 ms: 1.33x faster                                                   |
| pidigits       | 282 ms                                                 | 282 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                  | 1.22x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 69.1 ms: 1.38x faster                                                   |
| regex_dna      | 174 ms                                                 | 153 ms: 1.14x faster                                                    |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                   |
| regex_effbot   | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 180 us: 1.56x faster                                                    |
| unpickle_pure_python | 194 us                                                 | 141 us: 1.38x faster                                                    |
| json_dumps           | 8.11 ms                                                | 6.19 ms: 1.31x faster                                                   |
| xml_etree_process    | 46.5 ms                                                | 37.8 ms: 1.23x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.51 sec: 1.13x faster                                                  |
| xml_etree_parse      | 108 ms                                                 | 104 ms: 1.04x faster                                                    |
| xml_etree_generate   | 53.5 ms                                                | 54.5 ms: 1.02x slower                                                   |
| json_loads           | 16.4 us                                                | 16.9 us: 1.03x slower                                                   |
| unpickle             | 8.80 us                                                | 9.28 us: 1.06x slower                                                   |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                   |
| pickle               | 6.97 us                                                | 7.48 us: 1.07x slower                                                   |
| pickle_list          | 2.74 us                                                | 2.96 us: 1.08x slower                                                   |
| unpickle_list        | 2.69 us                                                | 2.98 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.0 ms: 1.19x slower                                                   |
| python_startup_no_site | 7.91 ms                                                | 10.2 ms: 1.29x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 7.12 ms: 1.39x faster                                                   |
| django_template | 26.4 ms                                                | 20.1 ms: 1.32x faster                                                   |
| genshi_text     | 17.3 ms                                                | 14.5 ms: 1.19x faster                                                   |
| genshi_xml      | 33.8 ms                                                | 31.5 ms: 1.07x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.24x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 93.1 us: 3.47x faster                                                   |
| deltablue                | 4.91 ms                                                | 2.19 ms: 2.24x faster                                                   |
| raytrace                 | 301 ms                                                 | 155 ms: 1.95x faster                                                    |
| async_tree_none          | 388 ms                                                 | 202 ms: 1.92x faster                                                    |
| logging_silent           | 117 ns                                                 | 62.3 ns: 1.88x faster                                                   |
| chaos                    | 65.8 ms                                                | 36.4 ms: 1.81x faster                                                   |
| async_tree_memoization   | 474 ms                                                 | 268 ms: 1.76x faster                                                    |
| async_tree_io            | 980 ms                                                 | 568 ms: 1.72x faster                                                    |
| sqlglot_parse            | 1.24 ms                                                | 747 us: 1.66x faster                                                    |
| richards_super           | 57.8 ms                                                | 34.8 ms: 1.66x faster                                                   |
| comprehensions           | 16.9 us                                                | 10.5 us: 1.61x faster                                                   |
| pylint                   | 277 ms                                                 | 172 ms: 1.61x faster                                                    |
| asyncio_tcp              | 659 ms                                                 | 411 ms: 1.60x faster                                                    |
| sqlglot_transpile        | 1.44 ms                                                | 906 us: 1.59x faster                                                    |
| pickle_pure_python       | 281 us                                                 | 180 us: 1.56x faster                                                    |
| crypto_pyaes             | 71.8 ms                                                | 46.7 ms: 1.54x faster                                                   |
| richards                 | 48.7 ms                                                | 31.8 ms: 1.53x faster                                                   |
| scimark_lu               | 103 ms                                                 | 68.4 ms: 1.50x faster                                                   |
| deepcopy_memo            | 34.7 us                                                | 23.2 us: 1.49x faster                                                   |
| go                       | 151 ms                                                 | 101 ms: 1.49x faster                                                    |
| scimark_monte_carlo      | 65.6 ms                                                | 44.3 ms: 1.48x faster                                                   |
| hexiom                   | 6.19 ms                                                | 4.22 ms: 1.47x faster                                                   |
| chameleon                | 6.26 ms                                                | 4.45 ms: 1.41x faster                                                   |
| logging_simple           | 4.45 us                                                | 3.17 us: 1.40x faster                                                   |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 463 ms: 1.40x faster                                                    |
| logging_format           | 4.83 us                                                | 3.46 us: 1.40x faster                                                   |
| mako                     | 9.87 ms                                                | 7.12 ms: 1.39x faster                                                   |
| regex_compile            | 95.3 ms                                                | 69.1 ms: 1.38x faster                                                   |
| unpickle_pure_python     | 194 us                                                 | 141 us: 1.38x faster                                                    |
| pycparser                | 877 ms                                                 | 637 ms: 1.38x faster                                                    |
| pprint_safe_repr         | 641 ms                                                 | 470 ms: 1.36x faster                                                    |
| pprint_pformat           | 1.30 sec                                               | 958 ms: 1.36x faster                                                    |
| float                    | 69.0 ms                                                | 51.1 ms: 1.35x faster                                                   |
| html5lib                 | 42.4 ms                                                | 31.7 ms: 1.34x faster                                                   |
| nbody                    | 93.0 ms                                                | 69.9 ms: 1.33x faster                                                   |
| pyflate                  | 427 ms                                                 | 323 ms: 1.32x faster                                                    |
| django_template          | 26.4 ms                                                | 20.1 ms: 1.32x faster                                                   |
| spectral_norm            | 94.8 ms                                                | 72.1 ms: 1.32x faster                                                   |
| mypy2                    | 607 ms                                                 | 462 ms: 1.32x faster                                                    |
| json_dumps               | 8.11 ms                                                | 6.19 ms: 1.31x faster                                                   |
| sympy_sum                | 92.2 ms                                                | 70.7 ms: 1.30x faster                                                   |
| scimark_sor              | 128 ms                                                 | 98.5 ms: 1.30x faster                                                   |
| deepcopy                 | 272 us                                                 | 209 us: 1.30x faster                                                    |
| dulwich_log              | 35.3 ms                                                | 27.6 ms: 1.28x faster                                                   |
| thrift                   | 572 us                                                 | 448 us: 1.28x faster                                                    |
| sympy_integrate          | 13.1 ms                                                | 10.4 ms: 1.26x faster                                                   |
| deepcopy_reduce          | 2.33 us                                                | 1.89 us: 1.24x faster                                                   |
| coroutines               | 20.7 ms                                                | 16.8 ms: 1.24x faster                                                   |
| sympy_str                | 165 ms                                                 | 134 ms: 1.23x faster                                                    |
| xml_etree_process        | 46.5 ms                                                | 37.8 ms: 1.23x faster                                                   |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.22x faster                                                  |
| docutils                 | 1.73 sec                                               | 1.45 sec: 1.19x faster                                                  |
| genshi_text              | 17.3 ms                                                | 14.5 ms: 1.19x faster                                                   |
| 2to3                     | 192 ms                                                 | 161 ms: 1.19x faster                                                    |
| fannkuch                 | 303 ms                                                 | 256 ms: 1.18x faster                                                    |
| gunicorn                 | 1.30 ms                                                | 1.11 ms: 1.18x faster                                                   |
| tornado_http             | 86.7 ms                                                | 74.1 ms: 1.17x faster                                                   |
| sqlglot_optimize         | 36.8 ms                                                | 31.6 ms: 1.17x faster                                                   |
| sympy_expand             | 269 ms                                                 | 231 ms: 1.17x faster                                                    |
| aiohttp                  | 1.22 ms                                                | 1.06 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 2.97 ms: 1.15x faster                                                   |
| scimark_fft              | 224 ms                                                 | 195 ms: 1.15x faster                                                    |
| dask                     | 253 ms                                                 | 222 ms: 1.14x faster                                                    |
| nqueens                  | 63.8 ms                                                | 55.9 ms: 1.14x faster                                                   |
| regex_dna                | 174 ms                                                 | 153 ms: 1.14x faster                                                    |
| tomli_loads              | 1.71 sec                                               | 1.51 sec: 1.13x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 169 ms: 1.13x faster                                                    |
| bench_thread_pool        | 527 us                                                 | 471 us: 1.12x faster                                                    |
| generators               | 32.3 ms                                                | 28.9 ms: 1.12x faster                                                   |
| meteor_contest           | 77.7 ms                                                | 71.3 ms: 1.09x faster                                                   |
| genshi_xml               | 33.8 ms                                                | 31.5 ms: 1.07x faster                                                   |
| mdp                      | 1.63 sec                                               | 1.53 sec: 1.07x faster                                                  |
| json                     | 3.08 ms                                                | 2.93 ms: 1.05x faster                                                   |
| xml_etree_parse          | 108 ms                                                 | 104 ms: 1.04x faster                                                    |
| pathlib                  | 24.5 ms                                                | 24.0 ms: 1.02x faster                                                   |
| pidigits                 | 282 ms                                                 | 282 ms: 1.00x faster                                                    |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                   |
| xml_etree_generate       | 53.5 ms                                                | 54.5 ms: 1.02x slower                                                   |
| json_loads               | 16.4 us                                                | 16.9 us: 1.03x slower                                                   |
| gc_traversal             | 2.36 ms                                                | 2.44 ms: 1.03x slower                                                   |
| create_gc_cycles         | 860 us                                                 | 895 us: 1.04x slower                                                    |
| unpickle                 | 8.80 us                                                | 9.28 us: 1.06x slower                                                   |
| sqlite_synth             | 1.46 us                                                | 1.55 us: 1.06x slower                                                   |
| regex_effbot             | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                   |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                   |
| pickle                   | 6.97 us                                                | 7.48 us: 1.07x slower                                                   |
| pickle_list              | 2.74 us                                                | 2.96 us: 1.08x slower                                                   |
| unpickle_list            | 2.69 us                                                | 2.98 us: 1.11x slower                                                   |
| coverage                 | 41.5 ms                                                | 46.2 ms: 1.11x slower                                                   |
| bench_mp_pool            | 37.4 ms                                                | 43.5 ms: 1.16x slower                                                   |
| python_startup           | 10.9 ms                                                | 13.0 ms: 1.19x slower                                                   |
| async_generators         | 231 ms                                                 | 285 ms: 1.23x slower                                                    |
| telco                    | 3.49 ms                                                | 4.46 ms: 1.28x slower                                                   |
| python_startup_no_site   | 7.91 ms                                                | 10.2 ms: 1.29x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.25x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, xml_etree_iterparse
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.15x