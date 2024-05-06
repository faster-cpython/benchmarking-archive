# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: c179c0e
- commit date: 2024-04-17
- overall geometric mean: 1.09x faster
- HPT reliability: 96.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 179 ms: 1.07x faster                                   |
| chameleon      | 6.26 ms                                                | 4.81 ms: 1.30x faster                                  |
| docutils       | 1.73 sec                                               | 1.61 sec: 1.08x faster                                 |
| html5lib       | 42.4 ms                                                | 33.0 ms: 1.28x faster                                  |
| Geometric mean | (ref)                                                  | 1.15x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 216 ms: 1.80x faster                                   |
| async_tree_io           | 980 ms                                                 | 586 ms: 1.67x faster                                   |
| async_tree_memoization  | 474 ms                                                 | 284 ms: 1.66x faster                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 476 ms: 1.36x faster                                   |
| Geometric mean          | (ref)                                                  | 1.62x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 282 ms                                                 | 284 ms: 1.01x slower                                   |
| nbody          | 93.0 ms                                                | 97.8 ms: 1.05x slower                                  |
| float          | 69.0 ms                                                | 75.1 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                   |
| regex_v8       | 17.1 ms                                                | 17.8 ms: 1.04x slower                                  |
| regex_effbot   | 2.46 ms                                                | 2.59 ms: 1.05x slower                                  |
| regex_compile  | 95.3 ms                                                | 102 ms: 1.07x slower                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 186 us: 1.51x faster                                   |
| json_dumps           | 8.11 ms                                                | 6.27 ms: 1.29x faster                                  |
| xml_etree_process    | 46.5 ms                                                | 40.7 ms: 1.14x faster                                  |
| xml_etree_parse      | 108 ms                                                 | 106 ms: 1.01x faster                                   |
| json_loads           | 16.4 us                                                | 16.9 us: 1.03x slower                                  |
| unpickle_pure_python | 194 us                                                 | 202 us: 1.04x slower                                   |
| unpickle             | 8.80 us                                                | 9.29 us: 1.06x slower                                  |
| tomli_loads          | 1.71 sec                                               | 1.83 sec: 1.07x slower                                 |
| pickle_dict          | 17.0 us                                                | 18.2 us: 1.07x slower                                  |
| pickle               | 6.97 us                                                | 7.51 us: 1.08x slower                                  |
| unpickle_list        | 2.69 us                                                | 2.92 us: 1.08x slower                                  |
| pickle_list          | 2.74 us                                                | 3.01 us: 1.10x slower                                  |
| xml_etree_generate   | 53.5 ms                                                | 59.4 ms: 1.11x slower                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 80.9 ms: 1.12x slower                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 12.1 ms: 1.11x slower                                  |
| python_startup_no_site | 7.91 ms                                                | 9.25 ms: 1.17x slower                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 26.4 ms                                                | 23.2 ms: 1.14x faster                                  |
| genshi_text     | 17.3 ms                                                | 15.4 ms: 1.13x faster                                  |
| genshi_xml      | 33.8 ms                                                | 33.6 ms: 1.01x faster                                  |
| mako            | 9.87 ms                                                | 10.5 ms: 1.07x slower                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 73.5 us: 4.39x faster                                  |
| async_tree_none          | 388 ms                                                 | 216 ms: 1.80x faster                                   |
| logging_silent           | 117 ns                                                 | 66.6 ns: 1.76x faster                                  |
| async_tree_io            | 980 ms                                                 | 586 ms: 1.67x faster                                   |
| async_tree_memoization   | 474 ms                                                 | 284 ms: 1.66x faster                                   |
| deltablue                | 4.91 ms                                                | 3.03 ms: 1.62x faster                                  |
| asyncio_tcp              | 659 ms                                                 | 415 ms: 1.59x faster                                   |
| raytrace                 | 301 ms                                                 | 192 ms: 1.57x faster                                   |
| pickle_pure_python       | 281 us                                                 | 186 us: 1.51x faster                                   |
| pylint                   | 277 ms                                                 | 185 ms: 1.50x faster                                   |
| mypy2                    | 607 ms                                                 | 418 ms: 1.45x faster                                   |
| sqlglot_parse            | 1.24 ms                                                | 868 us: 1.43x faster                                   |
| sqlglot_transpile        | 1.44 ms                                                | 1.04 ms: 1.39x faster                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 476 ms: 1.36x faster                                   |
| logging_format           | 4.83 us                                                | 3.57 us: 1.35x faster                                  |
| logging_simple           | 4.45 us                                                | 3.29 us: 1.35x faster                                  |
| richards_super           | 57.8 ms                                                | 43.6 ms: 1.33x faster                                  |
| chameleon                | 6.26 ms                                                | 4.81 ms: 1.30x faster                                  |
| json_dumps               | 8.11 ms                                                | 6.27 ms: 1.29x faster                                  |
| html5lib                 | 42.4 ms                                                | 33.0 ms: 1.28x faster                                  |
| thrift                   | 572 us                                                 | 446 us: 1.28x faster                                   |
| chaos                    | 65.8 ms                                                | 51.8 ms: 1.27x faster                                  |
| pycparser                | 877 ms                                                 | 693 ms: 1.26x faster                                   |
| coroutines               | 20.7 ms                                                | 17.0 ms: 1.21x faster                                  |
| deepcopy                 | 272 us                                                 | 224 us: 1.21x faster                                   |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.21x faster                                 |
| richards                 | 48.7 ms                                                | 40.2 ms: 1.21x faster                                  |
| deepcopy_memo            | 34.7 us                                                | 28.7 us: 1.21x faster                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.93 us: 1.20x faster                                  |
| dulwich_log              | 35.3 ms                                                | 29.5 ms: 1.20x faster                                  |
| generators               | 32.3 ms                                                | 27.2 ms: 1.19x faster                                  |
| go                       | 151 ms                                                 | 129 ms: 1.17x faster                                   |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                   |
| crypto_pyaes             | 71.8 ms                                                | 62.8 ms: 1.14x faster                                  |
| xml_etree_process        | 46.5 ms                                                | 40.7 ms: 1.14x faster                                  |
| django_template          | 26.4 ms                                                | 23.2 ms: 1.14x faster                                  |
| genshi_text              | 17.3 ms                                                | 15.4 ms: 1.13x faster                                  |
| dask                     | 253 ms                                                 | 224 ms: 1.13x faster                                   |
| scimark_sor              | 128 ms                                                 | 117 ms: 1.09x faster                                   |
| sympy_sum                | 92.2 ms                                                | 84.7 ms: 1.09x faster                                  |
| gunicorn                 | 1.30 ms                                                | 1.20 ms: 1.08x faster                                  |
| docutils                 | 1.73 sec                                               | 1.61 sec: 1.08x faster                                 |
| 2to3                     | 192 ms                                                 | 179 ms: 1.07x faster                                   |
| sympy_expand             | 269 ms                                                 | 251 ms: 1.07x faster                                   |
| aiohttp                  | 1.22 ms                                                | 1.15 ms: 1.06x faster                                  |
| sympy_integrate          | 13.1 ms                                                | 12.4 ms: 1.06x faster                                  |
| json                     | 3.08 ms                                                | 2.94 ms: 1.05x faster                                  |
| sympy_str                | 165 ms                                                 | 159 ms: 1.04x faster                                   |
| bench_thread_pool        | 527 us                                                 | 517 us: 1.02x faster                                   |
| xml_etree_parse          | 108 ms                                                 | 106 ms: 1.01x faster                                   |
| sqlglot_normalize        | 190 ms                                                 | 188 ms: 1.01x faster                                   |
| genshi_xml               | 33.8 ms                                                | 33.6 ms: 1.01x faster                                  |
| pidigits                 | 282 ms                                                 | 284 ms: 1.01x slower                                   |
| pprint_safe_repr         | 641 ms                                                 | 645 ms: 1.01x slower                                   |
| create_gc_cycles         | 860 us                                                 | 870 us: 1.01x slower                                   |
| pprint_pformat           | 1.30 sec                                               | 1.33 sec: 1.02x slower                                 |
| mdp                      | 1.63 sec                                               | 1.67 sec: 1.02x slower                                 |
| json_loads               | 16.4 us                                                | 16.9 us: 1.03x slower                                  |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                  |
| unpickle_pure_python     | 194 us                                                 | 202 us: 1.04x slower                                   |
| regex_v8                 | 17.1 ms                                                | 17.8 ms: 1.04x slower                                  |
| nbody                    | 93.0 ms                                                | 97.8 ms: 1.05x slower                                  |
| regex_effbot             | 2.46 ms                                                | 2.59 ms: 1.05x slower                                  |
| unpickle                 | 8.80 us                                                | 9.29 us: 1.06x slower                                  |
| mako                     | 9.87 ms                                                | 10.5 ms: 1.07x slower                                  |
| tomli_loads              | 1.71 sec                                               | 1.83 sec: 1.07x slower                                 |
| regex_compile            | 95.3 ms                                                | 102 ms: 1.07x slower                                   |
| pickle_dict              | 17.0 us                                                | 18.2 us: 1.07x slower                                  |
| pickle                   | 6.97 us                                                | 7.51 us: 1.08x slower                                  |
| scimark_lu               | 103 ms                                                 | 111 ms: 1.08x slower                                   |
| unpickle_list            | 2.69 us                                                | 2.92 us: 1.08x slower                                  |
| float                    | 69.0 ms                                                | 75.1 ms: 1.09x slower                                  |
| scimark_monte_carlo      | 65.6 ms                                                | 71.6 ms: 1.09x slower                                  |
| meteor_contest           | 77.7 ms                                                | 84.9 ms: 1.09x slower                                  |
| pickle_list              | 2.74 us                                                | 3.01 us: 1.10x slower                                  |
| pyflate                  | 427 ms                                                 | 472 ms: 1.11x slower                                   |
| python_startup           | 10.9 ms                                                | 12.1 ms: 1.11x slower                                  |
| xml_etree_generate       | 53.5 ms                                                | 59.4 ms: 1.11x slower                                  |
| xml_etree_iterparse      | 72.1 ms                                                | 80.9 ms: 1.12x slower                                  |
| coverage                 | 41.5 ms                                                | 46.6 ms: 1.12x slower                                  |
| hexiom                   | 6.19 ms                                                | 7.01 ms: 1.13x slower                                  |
| comprehensions           | 16.9 us                                                | 19.3 us: 1.14x slower                                  |
| sqlite_synth             | 1.46 us                                                | 1.67 us: 1.14x slower                                  |
| bench_mp_pool            | 37.4 ms                                                | 43.7 ms: 1.17x slower                                  |
| python_startup_no_site   | 7.91 ms                                                | 9.25 ms: 1.17x slower                                  |
| scimark_fft              | 224 ms                                                 | 275 ms: 1.22x slower                                   |
| spectral_norm            | 94.8 ms                                                | 116 ms: 1.23x slower                                   |
| nqueens                  | 63.8 ms                                                | 80.0 ms: 1.26x slower                                  |
| fannkuch                 | 303 ms                                                 | 381 ms: 1.26x slower                                   |
| async_generators         | 231 ms                                                 | 306 ms: 1.32x slower                                   |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 4.60 ms: 1.34x slower                                  |
| telco                    | 3.49 ms                                                | 4.94 ms: 1.42x slower                                  |
| Geometric mean           | (ref)                                                  | 1.09x faster                                           |

Benchmark hidden because not significant (4): tornado_http, pathlib, asyncio_websockets, sqlglot_optimize
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240417-3.13.0a6+-c179c0e-PYTHON_UOPS/bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 96.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x