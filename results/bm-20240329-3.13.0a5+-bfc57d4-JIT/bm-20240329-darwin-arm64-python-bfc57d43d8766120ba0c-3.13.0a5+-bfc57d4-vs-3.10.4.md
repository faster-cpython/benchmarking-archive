# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 173 ms: 1.11x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.46 ms: 1.40x faster                                                  |
| docutils       | 1.73 sec                                               | 1.55 sec: 1.11x faster                                                 |
| html5lib       | 42.4 ms                                                | 33.6 ms: 1.26x faster                                                  |
| Geometric mean | (ref)                                                  | 1.19x faster                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization  | 474 ms                                                 | 264 ms: 1.79x faster                                                   |
| async_tree_io           | 980 ms                                                 | 566 ms: 1.73x faster                                                   |
| async_tree_none         | 388 ms                                                 | 226 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 462 ms: 1.41x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.65x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.2 ms: 1.40x faster                                                  |
| nbody          | 93.0 ms                                                | 70.3 ms: 1.32x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 81.0 ms: 1.18x faster                                                  |
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                                   |
| regex_v8       | 17.1 ms                                                | 17.1 ms: 1.00x faster                                                  |
| regex_effbot   | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.54x faster                                                   |
| unpickle_pure_python | 194 us                                                 | 143 us: 1.36x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.30 sec: 1.32x faster                                                 |
| json_dumps           | 8.11 ms                                                | 6.37 ms: 1.27x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 36.8 ms: 1.26x faster                                                  |
| xml_etree_parse      | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| xml_etree_generate   | 53.5 ms                                                | 54.4 ms: 1.02x slower                                                  |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                  |
| unpickle             | 8.80 us                                                | 9.14 us: 1.04x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.0 us: 1.06x slower                                                  |
| pickle               | 6.97 us                                                | 7.44 us: 1.07x slower                                                  |
| pickle_list          | 2.74 us                                                | 2.96 us: 1.08x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.4 ms: 1.23x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 11.6 ms: 1.46x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.95 ms: 1.42x faster                                                  |
| django_template | 26.4 ms                                                | 20.7 ms: 1.27x faster                                                  |
| genshi_text     | 17.3 ms                                                | 14.9 ms: 1.16x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 31.4 ms: 1.08x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.23x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.6 us: 4.64x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.36 ms: 2.08x faster                                                  |
| async_tree_memoization   | 474 ms                                                 | 264 ms: 1.79x faster                                                   |
| logging_silent           | 117 ns                                                 | 65.7 ns: 1.78x faster                                                  |
| pylint                   | 277 ms                                                 | 156 ms: 1.77x faster                                                   |
| async_tree_io            | 980 ms                                                 | 566 ms: 1.73x faster                                                   |
| async_tree_none          | 388 ms                                                 | 226 ms: 1.72x faster                                                   |
| chaos                    | 65.8 ms                                                | 38.5 ms: 1.71x faster                                                  |
| raytrace                 | 301 ms                                                 | 180 ms: 1.68x faster                                                   |
| richards_super           | 57.8 ms                                                | 34.9 ms: 1.66x faster                                                  |
| sqlglot_parse            | 1.24 ms                                                | 765 us: 1.62x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 406 ms: 1.62x faster                                                   |
| richards                 | 48.7 ms                                                | 31.5 ms: 1.54x faster                                                  |
| sqlglot_transpile        | 1.44 ms                                                | 935 us: 1.54x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.54x faster                                                   |
| crypto_pyaes             | 71.8 ms                                                | 47.0 ms: 1.53x faster                                                  |
| scimark_monte_carlo      | 65.6 ms                                                | 44.2 ms: 1.48x faster                                                  |
| mypy2                    | 607 ms                                                 | 413 ms: 1.47x faster                                                   |
| go                       | 151 ms                                                 | 105 ms: 1.44x faster                                                   |
| deepcopy_memo            | 34.7 us                                                | 24.3 us: 1.43x faster                                                  |
| mako                     | 9.87 ms                                                | 6.95 ms: 1.42x faster                                                  |
| comprehensions           | 16.9 us                                                | 12.0 us: 1.41x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 462 ms: 1.41x faster                                                   |
| chameleon                | 6.26 ms                                                | 4.46 ms: 1.40x faster                                                  |
| float                    | 69.0 ms                                                | 49.2 ms: 1.40x faster                                                  |
| unpickle_pure_python     | 194 us                                                 | 143 us: 1.36x faster                                                   |
| logging_format           | 4.83 us                                                | 3.58 us: 1.35x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.29 us: 1.35x faster                                                  |
| nbody                    | 93.0 ms                                                | 70.3 ms: 1.32x faster                                                  |
| tomli_loads              | 1.71 sec                                               | 1.30 sec: 1.32x faster                                                 |
| pprint_safe_repr         | 641 ms                                                 | 487 ms: 1.32x faster                                                   |
| thrift                   | 572 us                                                 | 437 us: 1.31x faster                                                   |
| pycparser                | 877 ms                                                 | 671 ms: 1.31x faster                                                   |
| pprint_pformat           | 1.30 sec                                               | 1.00 sec: 1.30x faster                                                 |
| pyflate                  | 427 ms                                                 | 332 ms: 1.29x faster                                                   |
| spectral_norm            | 94.8 ms                                                | 73.7 ms: 1.29x faster                                                  |
| deepcopy                 | 272 us                                                 | 212 us: 1.28x faster                                                   |
| django_template          | 26.4 ms                                                | 20.7 ms: 1.27x faster                                                  |
| json_dumps               | 8.11 ms                                                | 6.37 ms: 1.27x faster                                                  |
| xml_etree_process        | 46.5 ms                                                | 36.8 ms: 1.26x faster                                                  |
| html5lib                 | 42.4 ms                                                | 33.6 ms: 1.26x faster                                                  |
| scimark_lu               | 103 ms                                                 | 81.6 ms: 1.26x faster                                                  |
| hexiom                   | 6.19 ms                                                | 4.96 ms: 1.25x faster                                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.87 us: 1.25x faster                                                  |
| coroutines               | 20.7 ms                                                | 16.7 ms: 1.24x faster                                                  |
| generators               | 32.3 ms                                                | 26.4 ms: 1.23x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.31 sec: 1.22x faster                                                 |
| sympy_sum                | 92.2 ms                                                | 75.9 ms: 1.22x faster                                                  |
| scimark_sor              | 128 ms                                                 | 107 ms: 1.19x faster                                                   |
| sympy_str                | 165 ms                                                 | 140 ms: 1.18x faster                                                   |
| dulwich_log              | 35.3 ms                                                | 30.0 ms: 1.18x faster                                                  |
| regex_compile            | 95.3 ms                                                | 81.0 ms: 1.18x faster                                                  |
| genshi_text              | 17.3 ms                                                | 14.9 ms: 1.16x faster                                                  |
| fannkuch                 | 303 ms                                                 | 261 ms: 1.16x faster                                                   |
| sympy_integrate          | 13.1 ms                                                | 11.3 ms: 1.16x faster                                                  |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                                   |
| dask                     | 253 ms                                                 | 221 ms: 1.14x faster                                                   |
| sympy_expand             | 269 ms                                                 | 236 ms: 1.14x faster                                                   |
| scimark_fft              | 224 ms                                                 | 200 ms: 1.12x faster                                                   |
| aiohttp                  | 1.22 ms                                                | 1.09 ms: 1.12x faster                                                  |
| docutils                 | 1.73 sec                                               | 1.55 sec: 1.11x faster                                                 |
| 2to3                     | 192 ms                                                 | 173 ms: 1.11x faster                                                   |
| sqlglot_optimize         | 36.8 ms                                                | 33.6 ms: 1.10x faster                                                  |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.13 ms: 1.09x faster                                                  |
| gunicorn                 | 1.30 ms                                                | 1.20 ms: 1.09x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 175 ms: 1.09x faster                                                   |
| genshi_xml               | 33.8 ms                                                | 31.4 ms: 1.08x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 494 us: 1.07x faster                                                   |
| nqueens                  | 63.8 ms                                                | 60.5 ms: 1.05x faster                                                  |
| meteor_contest           | 77.7 ms                                                | 74.1 ms: 1.05x faster                                                  |
| mdp                      | 1.63 sec                                               | 1.57 sec: 1.04x faster                                                 |
| json                     | 3.08 ms                                                | 2.98 ms: 1.03x faster                                                  |
| create_gc_cycles         | 860 us                                                 | 849 us: 1.01x faster                                                   |
| xml_etree_parse          | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| regex_v8                 | 17.1 ms                                                | 17.1 ms: 1.00x faster                                                  |
| pathlib                  | 24.5 ms                                                | 24.9 ms: 1.02x slower                                                  |
| xml_etree_generate       | 53.5 ms                                                | 54.4 ms: 1.02x slower                                                  |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.14 us: 1.04x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.0 us: 1.06x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                  |
| pickle                   | 6.97 us                                                | 7.44 us: 1.07x slower                                                  |
| pickle_list              | 2.74 us                                                | 2.96 us: 1.08x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.59 us: 1.09x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.59 ms: 1.10x slower                                                  |
| coverage                 | 41.5 ms                                                | 46.7 ms: 1.12x slower                                                  |
| unpickle_list            | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| python_startup           | 10.9 ms                                                | 13.4 ms: 1.23x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 46.4 ms: 1.24x slower                                                  |
| telco                    | 3.49 ms                                                | 4.51 ms: 1.29x slower                                                  |
| async_generators         | 231 ms                                                 | 300 ms: 1.30x slower                                                   |
| python_startup_no_site   | 7.91 ms                                                | 11.6 ms: 1.46x slower                                                  |
| unpack_sequence          | 39.0 ns                                                | 116 ns: 2.96x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.20x faster                                                           |

Benchmark hidden because not significant (4): tornado_http, asyncio_websockets, pidigits, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (12) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.40x