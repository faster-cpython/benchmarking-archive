# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: darwin-arm64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 162 ms: 1.18x faster                                                           |
| chameleon      | 6.26 ms                                                | 4.62 ms: 1.35x faster                                                          |
| docutils       | 1.73 sec                                               | 1.48 sec: 1.17x faster                                                         |
| html5lib       | 42.4 ms                                                | 32.1 ms: 1.32x faster                                                          |
| tornado_http   | 86.7 ms                                                | 78.4 ms: 1.11x faster                                                          |
| Geometric mean | (ref)                                                  | 1.22x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 205 ms: 1.90x faster                                                           |
| async_tree_memoization  | 474 ms                                                 | 273 ms: 1.73x faster                                                           |
| async_tree_io           | 980 ms                                                 | 576 ms: 1.70x faster                                                           |
| async_tree_cpu_io_mixed | 649 ms                                                 | 467 ms: 1.39x faster                                                           |
| Geometric mean          | (ref)                                                  | 1.67x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 65.7 ms: 1.41x faster                                                          |
| float          | 69.0 ms                                                | 52.2 ms: 1.32x faster                                                          |
| Geometric mean | (ref)                                                  | 1.23x faster                                                                   |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 70.9 ms: 1.34x faster                                                          |
| regex_dna      | 174 ms                                                 | 150 ms: 1.17x faster                                                           |
| regex_v8       | 17.1 ms                                                | 17.5 ms: 1.02x slower                                                          |
| regex_effbot   | 2.46 ms                                                | 2.59 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 188 us: 1.49x faster                                                           |
| unpickle_pure_python | 194 us                                                 | 145 us: 1.34x faster                                                           |
| json_dumps           | 8.11 ms                                                | 6.22 ms: 1.30x faster                                                          |
| xml_etree_process    | 46.5 ms                                                | 38.4 ms: 1.21x faster                                                          |
| tomli_loads          | 1.71 sec                                               | 1.51 sec: 1.13x faster                                                         |
| xml_etree_parse      | 108 ms                                                 | 99.2 ms: 1.09x faster                                                          |
| xml_etree_iterparse  | 72.1 ms                                                | 68.5 ms: 1.05x faster                                                          |
| xml_etree_generate   | 53.5 ms                                                | 55.1 ms: 1.03x slower                                                          |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                          |
| pickle               | 6.97 us                                                | 7.39 us: 1.06x slower                                                          |
| unpickle             | 8.80 us                                                | 9.32 us: 1.06x slower                                                          |
| pickle_list          | 2.74 us                                                | 2.95 us: 1.08x slower                                                          |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                          |
| pickle_dict          | 17.0 us                                                | 18.3 us: 1.08x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 11.9 ms: 1.10x slower                                                          |
| python_startup_no_site | 7.91 ms                                                | 9.15 ms: 1.16x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 7.32 ms: 1.35x faster                                                          |
| django_template | 26.4 ms                                                | 20.6 ms: 1.28x faster                                                          |
| genshi_text     | 17.3 ms                                                | 14.6 ms: 1.19x faster                                                          |
| genshi_xml      | 33.8 ms                                                | 31.5 ms: 1.07x faster                                                          |
| Geometric mean  | (ref)                                                  | 1.22x faster                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.5 us: 4.65x faster                                                          |
| deltablue                | 4.91 ms                                                | 2.28 ms: 2.15x faster                                                          |
| raytrace                 | 301 ms                                                 | 157 ms: 1.92x faster                                                           |
| async_tree_none          | 388 ms                                                 | 205 ms: 1.90x faster                                                           |
| chaos                    | 65.8 ms                                                | 36.9 ms: 1.78x faster                                                          |
| logging_silent           | 117 ns                                                 | 66.4 ns: 1.77x faster                                                          |
| async_tree_memoization   | 474 ms                                                 | 273 ms: 1.73x faster                                                           |
| async_tree_io            | 980 ms                                                 | 576 ms: 1.70x faster                                                           |
| richards_super           | 57.8 ms                                                | 35.8 ms: 1.62x faster                                                          |
| pylint                   | 277 ms                                                 | 171 ms: 1.62x faster                                                           |
| sqlglot_parse            | 1.24 ms                                                | 772 us: 1.61x faster                                                           |
| mypy2                    | 607 ms                                                 | 385 ms: 1.58x faster                                                           |
| sqlglot_transpile        | 1.44 ms                                                | 932 us: 1.55x faster                                                           |
| asyncio_tcp              | 659 ms                                                 | 430 ms: 1.53x faster                                                           |
| crypto_pyaes             | 71.8 ms                                                | 47.4 ms: 1.52x faster                                                          |
| comprehensions           | 16.9 us                                                | 11.2 us: 1.51x faster                                                          |
| richards                 | 48.7 ms                                                | 32.4 ms: 1.50x faster                                                          |
| pickle_pure_python       | 281 us                                                 | 188 us: 1.49x faster                                                           |
| scimark_lu               | 103 ms                                                 | 69.6 ms: 1.48x faster                                                          |
| go                       | 151 ms                                                 | 102 ms: 1.47x faster                                                           |
| scimark_monte_carlo      | 65.6 ms                                                | 44.8 ms: 1.46x faster                                                          |
| hexiom                   | 6.19 ms                                                | 4.27 ms: 1.45x faster                                                          |
| deepcopy_memo            | 34.7 us                                                | 24.3 us: 1.43x faster                                                          |
| nbody                    | 93.0 ms                                                | 65.7 ms: 1.41x faster                                                          |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 467 ms: 1.39x faster                                                           |
| logging_format           | 4.83 us                                                | 3.48 us: 1.39x faster                                                          |
| logging_simple           | 4.45 us                                                | 3.21 us: 1.39x faster                                                          |
| chameleon                | 6.26 ms                                                | 4.62 ms: 1.35x faster                                                          |
| mako                     | 9.87 ms                                                | 7.32 ms: 1.35x faster                                                          |
| regex_compile            | 95.3 ms                                                | 70.9 ms: 1.34x faster                                                          |
| unpickle_pure_python     | 194 us                                                 | 145 us: 1.34x faster                                                           |
| pycparser                | 877 ms                                                 | 654 ms: 1.34x faster                                                           |
| spectral_norm            | 94.8 ms                                                | 71.1 ms: 1.33x faster                                                          |
| html5lib                 | 42.4 ms                                                | 32.1 ms: 1.32x faster                                                          |
| float                    | 69.0 ms                                                | 52.2 ms: 1.32x faster                                                          |
| pprint_pformat           | 1.30 sec                                               | 989 ms: 1.32x faster                                                           |
| pprint_safe_repr         | 641 ms                                                 | 487 ms: 1.32x faster                                                           |
| json_dumps               | 8.11 ms                                                | 6.22 ms: 1.30x faster                                                          |
| pyflate                  | 427 ms                                                 | 330 ms: 1.29x faster                                                           |
| thrift                   | 572 us                                                 | 444 us: 1.29x faster                                                           |
| sympy_sum                | 92.2 ms                                                | 71.7 ms: 1.29x faster                                                          |
| scimark_sor              | 128 ms                                                 | 100 ms: 1.28x faster                                                           |
| django_template          | 26.4 ms                                                | 20.6 ms: 1.28x faster                                                          |
| deepcopy                 | 272 us                                                 | 215 us: 1.27x faster                                                           |
| dulwich_log              | 35.3 ms                                                | 28.1 ms: 1.26x faster                                                          |
| sympy_integrate          | 13.1 ms                                                | 10.5 ms: 1.25x faster                                                          |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.31 sec: 1.22x faster                                                         |
| sympy_str                | 165 ms                                                 | 136 ms: 1.22x faster                                                           |
| deepcopy_reduce          | 2.33 us                                                | 1.91 us: 1.22x faster                                                          |
| xml_etree_process        | 46.5 ms                                                | 38.4 ms: 1.21x faster                                                          |
| generators               | 32.3 ms                                                | 27.2 ms: 1.19x faster                                                          |
| coroutines               | 20.7 ms                                                | 17.4 ms: 1.19x faster                                                          |
| genshi_text              | 17.3 ms                                                | 14.6 ms: 1.19x faster                                                          |
| 2to3                     | 192 ms                                                 | 162 ms: 1.18x faster                                                           |
| fannkuch                 | 303 ms                                                 | 257 ms: 1.18x faster                                                           |
| docutils                 | 1.73 sec                                               | 1.48 sec: 1.17x faster                                                         |
| regex_dna                | 174 ms                                                 | 150 ms: 1.17x faster                                                           |
| sympy_expand             | 269 ms                                                 | 231 ms: 1.16x faster                                                           |
| dask                     | 253 ms                                                 | 219 ms: 1.16x faster                                                           |
| nqueens                  | 63.8 ms                                                | 55.2 ms: 1.16x faster                                                          |
| gunicorn                 | 1.30 ms                                                | 1.13 ms: 1.15x faster                                                          |
| scimark_fft              | 224 ms                                                 | 195 ms: 1.15x faster                                                           |
| sqlglot_optimize         | 36.8 ms                                                | 32.1 ms: 1.14x faster                                                          |
| aiohttp                  | 1.22 ms                                                | 1.07 ms: 1.14x faster                                                          |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.02 ms: 1.13x faster                                                          |
| tomli_loads              | 1.71 sec                                               | 1.51 sec: 1.13x faster                                                         |
| bench_thread_pool        | 527 us                                                 | 473 us: 1.12x faster                                                           |
| sqlglot_normalize        | 190 ms                                                 | 172 ms: 1.11x faster                                                           |
| tornado_http             | 86.7 ms                                                | 78.4 ms: 1.11x faster                                                          |
| meteor_contest           | 77.7 ms                                                | 71.4 ms: 1.09x faster                                                          |
| xml_etree_parse          | 108 ms                                                 | 99.2 ms: 1.09x faster                                                          |
| genshi_xml               | 33.8 ms                                                | 31.5 ms: 1.07x faster                                                          |
| mdp                      | 1.63 sec                                               | 1.54 sec: 1.06x faster                                                         |
| json                     | 3.08 ms                                                | 2.92 ms: 1.05x faster                                                          |
| xml_etree_iterparse      | 72.1 ms                                                | 68.5 ms: 1.05x faster                                                          |
| pathlib                  | 24.5 ms                                                | 23.7 ms: 1.03x faster                                                          |
| regex_v8                 | 17.1 ms                                                | 17.5 ms: 1.02x slower                                                          |
| xml_etree_generate       | 53.5 ms                                                | 55.1 ms: 1.03x slower                                                          |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                          |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                                          |
| create_gc_cycles         | 860 us                                                 | 897 us: 1.04x slower                                                           |
| regex_effbot             | 2.46 ms                                                | 2.59 ms: 1.05x slower                                                          |
| pickle                   | 6.97 us                                                | 7.39 us: 1.06x slower                                                          |
| unpickle                 | 8.80 us                                                | 9.32 us: 1.06x slower                                                          |
| sqlite_synth             | 1.46 us                                                | 1.56 us: 1.07x slower                                                          |
| pickle_list              | 2.74 us                                                | 2.95 us: 1.08x slower                                                          |
| unpickle_list            | 2.69 us                                                | 2.90 us: 1.08x slower                                                          |
| pickle_dict              | 17.0 us                                                | 18.3 us: 1.08x slower                                                          |
| python_startup           | 10.9 ms                                                | 11.9 ms: 1.10x slower                                                          |
| coverage                 | 41.5 ms                                                | 46.6 ms: 1.12x slower                                                          |
| bench_mp_pool            | 37.4 ms                                                | 43.0 ms: 1.15x slower                                                          |
| python_startup_no_site   | 7.91 ms                                                | 9.15 ms: 1.16x slower                                                          |
| async_generators         | 231 ms                                                 | 290 ms: 1.25x slower                                                           |
| telco                    | 3.49 ms                                                | 4.63 ms: 1.33x slower                                                          |
| Geometric mean           | (ref)                                                  | 1.24x faster                                                                   |

Benchmark hidden because not significant (2): asyncio_websockets, pidigits
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.15x