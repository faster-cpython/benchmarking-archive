# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.12x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 178 ms: 1.08x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.83 ms: 1.30x faster                                                  |
| docutils       | 1.73 sec                                               | 1.62 sec: 1.07x faster                                                 |
| html5lib       | 42.4 ms                                                | 35.0 ms: 1.21x faster                                                  |
| Geometric mean | (ref)                                                  | 1.14x faster                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization  | 474 ms                                                 | 276 ms: 1.71x faster                                                   |
| async_tree_io           | 980 ms                                                 | 584 ms: 1.68x faster                                                   |
| async_tree_none         | 388 ms                                                 | 236 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 471 ms: 1.38x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.60x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 86.7 ms: 1.07x faster                                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| float          | 69.0 ms                                                | 69.4 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                                   |
| regex_compile  | 95.3 ms                                                | 92.7 ms: 1.03x faster                                                  |
| regex_v8       | 17.1 ms                                                | 17.2 ms: 1.00x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.56 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 189 us: 1.49x faster                                                   |
| json_dumps           | 8.11 ms                                                | 6.28 ms: 1.29x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 39.2 ms: 1.19x faster                                                  |
| unpickle_pure_python | 194 us                                                 | 188 us: 1.04x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.69 sec: 1.01x faster                                                 |
| xml_etree_parse      | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                  |
| unpickle             | 8.80 us                                                | 9.13 us: 1.04x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| pickle               | 6.97 us                                                | 7.52 us: 1.08x slower                                                  |
| pickle_list          | 2.74 us                                                | 3.01 us: 1.10x slower                                                  |
| xml_etree_generate   | 53.5 ms                                                | 58.9 ms: 1.10x slower                                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 79.5 ms: 1.10x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 12.0 ms: 1.10x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 10.3 ms: 1.30x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 26.4 ms                                                | 22.6 ms: 1.17x faster                                                  |
| genshi_text     | 17.3 ms                                                | 15.4 ms: 1.12x faster                                                  |
| mako            | 9.87 ms                                                | 9.32 ms: 1.06x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 33.1 ms: 1.02x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.09x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 72.6 us: 4.45x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.63 ms: 1.87x faster                                                  |
| pylint                   | 277 ms                                                 | 159 ms: 1.74x faster                                                   |
| logging_silent           | 117 ns                                                 | 67.9 ns: 1.73x faster                                                  |
| async_tree_memoization   | 474 ms                                                 | 276 ms: 1.71x faster                                                   |
| async_tree_io            | 980 ms                                                 | 584 ms: 1.68x faster                                                   |
| async_tree_none          | 388 ms                                                 | 236 ms: 1.65x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 436 ms: 1.51x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 189 us: 1.49x faster                                                   |
| sqlglot_parse            | 1.24 ms                                                | 843 us: 1.48x faster                                                   |
| mypy2                    | 607 ms                                                 | 417 ms: 1.46x faster                                                   |
| sqlglot_transpile        | 1.44 ms                                                | 1.01 ms: 1.43x faster                                                  |
| raytrace                 | 301 ms                                                 | 215 ms: 1.40x faster                                                   |
| richards_super           | 57.8 ms                                                | 41.8 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 471 ms: 1.38x faster                                                   |
| chaos                    | 65.8 ms                                                | 48.0 ms: 1.37x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.39 us: 1.31x faster                                                  |
| logging_format           | 4.83 us                                                | 3.68 us: 1.31x faster                                                  |
| chameleon                | 6.26 ms                                                | 4.83 ms: 1.30x faster                                                  |
| json_dumps               | 8.11 ms                                                | 6.28 ms: 1.29x faster                                                  |
| thrift                   | 572 us                                                 | 447 us: 1.28x faster                                                   |
| go                       | 151 ms                                                 | 118 ms: 1.28x faster                                                   |
| richards                 | 48.7 ms                                                | 38.1 ms: 1.28x faster                                                  |
| crypto_pyaes             | 71.8 ms                                                | 56.7 ms: 1.27x faster                                                  |
| pycparser                | 877 ms                                                 | 705 ms: 1.24x faster                                                   |
| deepcopy_memo            | 34.7 us                                                | 28.0 us: 1.24x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.31 sec: 1.23x faster                                                 |
| deepcopy                 | 272 us                                                 | 222 us: 1.22x faster                                                   |
| coroutines               | 20.7 ms                                                | 17.0 ms: 1.22x faster                                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.92 us: 1.22x faster                                                  |
| html5lib                 | 42.4 ms                                                | 35.0 ms: 1.21x faster                                                  |
| xml_etree_process        | 46.5 ms                                                | 39.2 ms: 1.19x faster                                                  |
| django_template          | 26.4 ms                                                | 22.6 ms: 1.17x faster                                                  |
| dulwich_log              | 35.3 ms                                                | 30.4 ms: 1.16x faster                                                  |
| generators               | 32.3 ms                                                | 28.0 ms: 1.16x faster                                                  |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                                   |
| aiohttp                  | 1.22 ms                                                | 1.08 ms: 1.14x faster                                                  |
| dask                     | 253 ms                                                 | 223 ms: 1.14x faster                                                   |
| genshi_text              | 17.3 ms                                                | 15.4 ms: 1.12x faster                                                  |
| sympy_sum                | 92.2 ms                                                | 82.3 ms: 1.12x faster                                                  |
| gunicorn                 | 1.30 ms                                                | 1.18 ms: 1.11x faster                                                  |
| pprint_safe_repr         | 641 ms                                                 | 580 ms: 1.10x faster                                                   |
| pprint_pformat           | 1.30 sec                                               | 1.18 sec: 1.10x faster                                                 |
| scimark_sor              | 128 ms                                                 | 117 ms: 1.10x faster                                                   |
| sympy_integrate          | 13.1 ms                                                | 12.0 ms: 1.09x faster                                                  |
| unpack_sequence          | 39.0 ns                                                | 35.8 ns: 1.09x faster                                                  |
| sympy_expand             | 269 ms                                                 | 247 ms: 1.09x faster                                                   |
| sympy_str                | 165 ms                                                 | 153 ms: 1.08x faster                                                   |
| 2to3                     | 192 ms                                                 | 178 ms: 1.08x faster                                                   |
| nbody                    | 93.0 ms                                                | 86.7 ms: 1.07x faster                                                  |
| docutils                 | 1.73 sec                                               | 1.62 sec: 1.07x faster                                                 |
| mako                     | 9.87 ms                                                | 9.32 ms: 1.06x faster                                                  |
| unpickle_pure_python     | 194 us                                                 | 188 us: 1.04x faster                                                   |
| json                     | 3.08 ms                                                | 2.98 ms: 1.03x faster                                                  |
| sqlglot_optimize         | 36.8 ms                                                | 35.7 ms: 1.03x faster                                                  |
| regex_compile            | 95.3 ms                                                | 92.7 ms: 1.03x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 186 ms: 1.02x faster                                                   |
| genshi_xml               | 33.8 ms                                                | 33.1 ms: 1.02x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 517 us: 1.02x faster                                                   |
| create_gc_cycles         | 860 us                                                 | 845 us: 1.02x faster                                                   |
| tomli_loads              | 1.71 sec                                               | 1.69 sec: 1.01x faster                                                 |
| xml_etree_parse          | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                                   |
| regex_v8                 | 17.1 ms                                                | 17.2 ms: 1.00x slower                                                  |
| mdp                      | 1.63 sec                                               | 1.64 sec: 1.00x slower                                                 |
| pidigits                 | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| float                    | 69.0 ms                                                | 69.4 ms: 1.01x slower                                                  |
| scimark_lu               | 103 ms                                                 | 104 ms: 1.01x slower                                                   |
| pyflate                  | 427 ms                                                 | 434 ms: 1.02x slower                                                   |
| hexiom                   | 6.19 ms                                                | 6.31 ms: 1.02x slower                                                  |
| comprehensions           | 16.9 us                                                | 17.4 us: 1.03x slower                                                  |
| pathlib                  | 24.5 ms                                                | 25.1 ms: 1.03x slower                                                  |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.13 us: 1.04x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.56 ms: 1.04x slower                                                  |
| meteor_contest           | 77.7 ms                                                | 81.1 ms: 1.04x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| spectral_norm            | 94.8 ms                                                | 102 ms: 1.07x slower                                                   |
| pickle                   | 6.97 us                                                | 7.52 us: 1.08x slower                                                  |
| pickle_list              | 2.74 us                                                | 3.01 us: 1.10x slower                                                  |
| xml_etree_generate       | 53.5 ms                                                | 58.9 ms: 1.10x slower                                                  |
| python_startup           | 10.9 ms                                                | 12.0 ms: 1.10x slower                                                  |
| xml_etree_iterparse      | 72.1 ms                                                | 79.5 ms: 1.10x slower                                                  |
| scimark_fft              | 224 ms                                                 | 249 ms: 1.11x slower                                                   |
| coverage                 | 41.5 ms                                                | 46.7 ms: 1.13x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.65 us: 1.13x slower                                                  |
| unpickle_list            | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| fannkuch                 | 303 ms                                                 | 347 ms: 1.15x slower                                                   |
| nqueens                  | 63.8 ms                                                | 74.1 ms: 1.16x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 43.8 ms: 1.17x slower                                                  |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 4.19 ms: 1.22x slower                                                  |
| python_startup_no_site   | 7.91 ms                                                | 10.3 ms: 1.30x slower                                                  |
| async_generators         | 231 ms                                                 | 303 ms: 1.31x slower                                                   |
| telco                    | 3.49 ms                                                | 4.80 ms: 1.38x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (2): tornado_http, scimark_monte_carlo
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (12) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x