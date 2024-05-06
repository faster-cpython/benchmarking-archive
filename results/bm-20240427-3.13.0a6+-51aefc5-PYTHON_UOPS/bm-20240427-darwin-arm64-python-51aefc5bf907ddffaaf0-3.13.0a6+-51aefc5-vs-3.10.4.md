# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.12x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 180 ms: 1.07x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.76 ms: 1.31x faster                                                  |
| docutils       | 1.73 sec                                               | 1.60 sec: 1.08x faster                                                 |
| html5lib       | 42.4 ms                                                | 32.2 ms: 1.32x faster                                                  |
| tornado_http   | 86.7 ms                                                | 78.6 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 212 ms: 1.84x faster                                                   |
| async_tree_io           | 980 ms                                                 | 579 ms: 1.69x faster                                                   |
| async_tree_memoization  | 474 ms                                                 | 280 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 473 ms: 1.37x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.64x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 84.1 ms: 1.11x faster                                                  |
| float          | 69.0 ms                                                | 65.0 ms: 1.06x faster                                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| regex_v8       | 17.1 ms                                                | 17.7 ms: 1.03x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.57 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 188 us: 1.49x faster                                                   |
| json_dumps           | 8.11 ms                                                | 6.31 ms: 1.28x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 40.0 ms: 1.16x faster                                                  |
| unpickle_pure_python | 194 us                                                 | 182 us: 1.07x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.64 sec: 1.04x faster                                                 |
| xml_etree_parse      | 108 ms                                                 | 106 ms: 1.02x faster                                                   |
| json_loads           | 16.4 us                                                | 16.9 us: 1.03x slower                                                  |
| unpickle             | 8.80 us                                                | 9.26 us: 1.05x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 77.4 ms: 1.07x slower                                                  |
| pickle               | 6.97 us                                                | 7.49 us: 1.07x slower                                                  |
| pickle_list          | 2.74 us                                                | 2.96 us: 1.08x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| xml_etree_generate   | 53.5 ms                                                | 58.2 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.6 ms: 1.26x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 10.9 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 26.4 ms                                                | 23.1 ms: 1.14x faster                                                  |
| mako            | 9.87 ms                                                | 9.31 ms: 1.06x faster                                                  |
| genshi_text     | 17.3 ms                                                | 16.7 ms: 1.04x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 34.6 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 111 us: 2.92x faster                                                   |
| async_tree_none          | 388 ms                                                 | 212 ms: 1.84x faster                                                   |
| logging_silent           | 117 ns                                                 | 66.6 ns: 1.76x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.86 ms: 1.72x faster                                                  |
| async_tree_io            | 980 ms                                                 | 579 ms: 1.69x faster                                                   |
| async_tree_memoization   | 474 ms                                                 | 280 ms: 1.69x faster                                                   |
| raytrace                 | 301 ms                                                 | 183 ms: 1.65x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 418 ms: 1.58x faster                                                   |
| sqlglot_parse            | 1.24 ms                                                | 832 us: 1.49x faster                                                   |
| pylint                   | 277 ms                                                 | 185 ms: 1.49x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 188 us: 1.49x faster                                                   |
| richards_super           | 57.8 ms                                                | 39.0 ms: 1.48x faster                                                  |
| sqlglot_transpile        | 1.44 ms                                                | 1.01 ms: 1.43x faster                                                  |
| chaos                    | 65.8 ms                                                | 47.8 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 473 ms: 1.37x faster                                                   |
| richards                 | 48.7 ms                                                | 35.5 ms: 1.37x faster                                                  |
| logging_format           | 4.83 us                                                | 3.60 us: 1.34x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.32 us: 1.34x faster                                                  |
| html5lib                 | 42.4 ms                                                | 32.2 ms: 1.32x faster                                                  |
| chameleon                | 6.26 ms                                                | 4.76 ms: 1.31x faster                                                  |
| pycparser                | 877 ms                                                 | 678 ms: 1.29x faster                                                   |
| json_dumps               | 8.11 ms                                                | 6.31 ms: 1.28x faster                                                  |
| crypto_pyaes             | 71.8 ms                                                | 56.4 ms: 1.27x faster                                                  |
| thrift                   | 572 us                                                 | 449 us: 1.27x faster                                                   |
| go                       | 151 ms                                                 | 119 ms: 1.27x faster                                                   |
| deepcopy_memo            | 34.7 us                                                | 27.7 us: 1.25x faster                                                  |
| coroutines               | 20.7 ms                                                | 16.6 ms: 1.25x faster                                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.91 us: 1.22x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.21x faster                                                 |
| deepcopy                 | 272 us                                                 | 225 us: 1.21x faster                                                   |
| mypy2                    | 607 ms                                                 | 502 ms: 1.21x faster                                                   |
| dulwich_log              | 35.3 ms                                                | 29.3 ms: 1.21x faster                                                  |
| generators               | 32.3 ms                                                | 27.1 ms: 1.19x faster                                                  |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| xml_etree_process        | 46.5 ms                                                | 40.0 ms: 1.16x faster                                                  |
| scimark_sor              | 128 ms                                                 | 111 ms: 1.15x faster                                                   |
| django_template          | 26.4 ms                                                | 23.1 ms: 1.14x faster                                                  |
| sympy_sum                | 92.2 ms                                                | 82.3 ms: 1.12x faster                                                  |
| dask                     | 253 ms                                                 | 227 ms: 1.12x faster                                                   |
| sympy_integrate          | 13.1 ms                                                | 11.9 ms: 1.11x faster                                                  |
| nbody                    | 93.0 ms                                                | 84.1 ms: 1.11x faster                                                  |
| tornado_http             | 86.7 ms                                                | 78.6 ms: 1.10x faster                                                  |
| sympy_expand             | 269 ms                                                 | 245 ms: 1.10x faster                                                   |
| aiohttp                  | 1.22 ms                                                | 1.11 ms: 1.10x faster                                                  |
| gunicorn                 | 1.30 ms                                                | 1.20 ms: 1.08x faster                                                  |
| docutils                 | 1.73 sec                                               | 1.60 sec: 1.08x faster                                                 |
| pprint_safe_repr         | 641 ms                                                 | 593 ms: 1.08x faster                                                   |
| pprint_pformat           | 1.30 sec                                               | 1.21 sec: 1.08x faster                                                 |
| sympy_str                | 165 ms                                                 | 154 ms: 1.07x faster                                                   |
| unpickle_pure_python     | 194 us                                                 | 182 us: 1.07x faster                                                   |
| 2to3                     | 192 ms                                                 | 180 ms: 1.07x faster                                                   |
| float                    | 69.0 ms                                                | 65.0 ms: 1.06x faster                                                  |
| mako                     | 9.87 ms                                                | 9.31 ms: 1.06x faster                                                  |
| json                     | 3.08 ms                                                | 2.94 ms: 1.05x faster                                                  |
| genshi_text              | 17.3 ms                                                | 16.7 ms: 1.04x faster                                                  |
| tomli_loads              | 1.71 sec                                               | 1.64 sec: 1.04x faster                                                 |
| pyflate                  | 427 ms                                                 | 411 ms: 1.04x faster                                                   |
| scimark_monte_carlo      | 65.6 ms                                                | 63.6 ms: 1.03x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 516 us: 1.02x faster                                                   |
| xml_etree_parse          | 108 ms                                                 | 106 ms: 1.02x faster                                                   |
| sqlglot_optimize         | 36.8 ms                                                | 36.2 ms: 1.02x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 189 ms: 1.01x faster                                                   |
| pidigits                 | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| spectral_norm            | 94.8 ms                                                | 95.2 ms: 1.00x slower                                                  |
| genshi_xml               | 33.8 ms                                                | 34.6 ms: 1.02x slower                                                  |
| json_loads               | 16.4 us                                                | 16.9 us: 1.03x slower                                                  |
| regex_v8                 | 17.1 ms                                                | 17.7 ms: 1.03x slower                                                  |
| mdp                      | 1.63 sec                                               | 1.68 sec: 1.03x slower                                                 |
| meteor_contest           | 77.7 ms                                                | 80.5 ms: 1.04x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.57 ms: 1.05x slower                                                  |
| scimark_fft              | 224 ms                                                 | 236 ms: 1.05x slower                                                   |
| unpickle                 | 8.80 us                                                | 9.26 us: 1.05x slower                                                  |
| create_gc_cycles         | 860 us                                                 | 905 us: 1.05x slower                                                   |
| comprehensions           | 16.9 us                                                | 17.9 us: 1.06x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| xml_etree_iterparse      | 72.1 ms                                                | 77.4 ms: 1.07x slower                                                  |
| fannkuch                 | 303 ms                                                 | 325 ms: 1.07x slower                                                   |
| pickle                   | 6.97 us                                                | 7.49 us: 1.07x slower                                                  |
| pickle_list              | 2.74 us                                                | 2.96 us: 1.08x slower                                                  |
| coverage                 | 41.5 ms                                                | 44.8 ms: 1.08x slower                                                  |
| unpickle_list            | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| xml_etree_generate       | 53.5 ms                                                | 58.2 ms: 1.09x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.62 us: 1.11x slower                                                  |
| nqueens                  | 63.8 ms                                                | 72.1 ms: 1.13x slower                                                  |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.92 ms: 1.14x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 44.9 ms: 1.20x slower                                                  |
| python_startup           | 10.9 ms                                                | 13.6 ms: 1.26x slower                                                  |
| async_generators         | 231 ms                                                 | 296 ms: 1.28x slower                                                   |
| telco                    | 3.49 ms                                                | 4.64 ms: 1.33x slower                                                  |
| python_startup_no_site   | 7.91 ms                                                | 10.9 ms: 1.37x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (5): pathlib, asyncio_websockets, regex_compile, hexiom, scimark_lu
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.16x