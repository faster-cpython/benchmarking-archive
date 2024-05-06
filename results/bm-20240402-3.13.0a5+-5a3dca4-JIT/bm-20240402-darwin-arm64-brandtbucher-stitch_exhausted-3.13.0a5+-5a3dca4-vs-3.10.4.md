# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 176 ms: 1.09x faster                                                     |
| chameleon      | 6.26 ms                                                | 4.47 ms: 1.40x faster                                                    |
| docutils       | 1.73 sec                                               | 1.58 sec: 1.09x faster                                                   |
| html5lib       | 42.4 ms                                                | 33.8 ms: 1.25x faster                                                    |
| Geometric mean | (ref)                                                  | 1.17x faster                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization  | 474 ms                                                 | 266 ms: 1.78x faster                                                     |
| async_tree_io           | 980 ms                                                 | 569 ms: 1.72x faster                                                     |
| async_tree_none         | 388 ms                                                 | 228 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed | 649 ms                                                 | 466 ms: 1.39x faster                                                     |
| Geometric mean          | (ref)                                                  | 1.64x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.2 ms: 1.40x faster                                                    |
| nbody          | 93.0 ms                                                | 70.0 ms: 1.33x faster                                                    |
| Geometric mean | (ref)                                                  | 1.23x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                                     |
| regex_compile  | 95.3 ms                                                | 87.2 ms: 1.09x faster                                                    |
| regex_effbot   | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.54x faster                                                     |
| unpickle_pure_python | 194 us                                                 | 143 us: 1.36x faster                                                     |
| tomli_loads          | 1.71 sec                                               | 1.29 sec: 1.33x faster                                                   |
| json_dumps           | 8.11 ms                                                | 6.28 ms: 1.29x faster                                                    |
| xml_etree_process    | 46.5 ms                                                | 36.5 ms: 1.27x faster                                                    |
| xml_etree_parse      | 108 ms                                                 | 98.3 ms: 1.10x faster                                                    |
| xml_etree_iterparse  | 72.1 ms                                                | 68.5 ms: 1.05x faster                                                    |
| xml_etree_generate   | 53.5 ms                                                | 54.1 ms: 1.01x slower                                                    |
| json_loads           | 16.4 us                                                | 17.1 us: 1.04x slower                                                    |
| unpickle             | 8.80 us                                                | 9.17 us: 1.04x slower                                                    |
| pickle_dict          | 17.0 us                                                | 18.0 us: 1.06x slower                                                    |
| pickle               | 6.97 us                                                | 7.47 us: 1.07x slower                                                    |
| pickle_list          | 2.74 us                                                | 2.98 us: 1.09x slower                                                    |
| unpickle_list        | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.4 ms: 1.23x slower                                                    |
| python_startup_no_site | 7.91 ms                                                | 11.6 ms: 1.47x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.96 ms: 1.42x faster                                                    |
| django_template | 26.4 ms                                                | 21.3 ms: 1.24x faster                                                    |
| genshi_text     | 17.3 ms                                                | 14.7 ms: 1.18x faster                                                    |
| genshi_xml      | 33.8 ms                                                | 32.7 ms: 1.04x faster                                                    |
| Geometric mean  | (ref)                                                  | 1.21x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.9 us: 4.62x faster                                                    |
| deltablue                | 4.91 ms                                                | 2.37 ms: 2.08x faster                                                    |
| logging_silent           | 117 ns                                                 | 65.7 ns: 1.78x faster                                                    |
| async_tree_memoization   | 474 ms                                                 | 266 ms: 1.78x faster                                                     |
| pylint                   | 277 ms                                                 | 159 ms: 1.74x faster                                                     |
| async_tree_io            | 980 ms                                                 | 569 ms: 1.72x faster                                                     |
| async_tree_none          | 388 ms                                                 | 228 ms: 1.70x faster                                                     |
| chaos                    | 65.8 ms                                                | 39.4 ms: 1.67x faster                                                    |
| richards_super           | 57.8 ms                                                | 34.8 ms: 1.66x faster                                                    |
| raytrace                 | 301 ms                                                 | 181 ms: 1.66x faster                                                     |
| sqlglot_parse            | 1.24 ms                                                | 769 us: 1.62x faster                                                     |
| richards                 | 48.7 ms                                                | 31.2 ms: 1.56x faster                                                    |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.54x faster                                                     |
| sqlglot_transpile        | 1.44 ms                                                | 944 us: 1.53x faster                                                     |
| crypto_pyaes             | 71.8 ms                                                | 47.5 ms: 1.51x faster                                                    |
| asyncio_tcp              | 659 ms                                                 | 449 ms: 1.47x faster                                                     |
| scimark_monte_carlo      | 65.6 ms                                                | 45.9 ms: 1.43x faster                                                    |
| deepcopy_memo            | 34.7 us                                                | 24.3 us: 1.43x faster                                                    |
| mypy2                    | 607 ms                                                 | 426 ms: 1.43x faster                                                     |
| mako                     | 9.87 ms                                                | 6.96 ms: 1.42x faster                                                    |
| go                       | 151 ms                                                 | 107 ms: 1.40x faster                                                     |
| float                    | 69.0 ms                                                | 49.2 ms: 1.40x faster                                                    |
| chameleon                | 6.26 ms                                                | 4.47 ms: 1.40x faster                                                    |
| comprehensions           | 16.9 us                                                | 12.1 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 466 ms: 1.39x faster                                                     |
| unpickle_pure_python     | 194 us                                                 | 143 us: 1.36x faster                                                     |
| logging_simple           | 4.45 us                                                | 3.29 us: 1.35x faster                                                    |
| logging_format           | 4.83 us                                                | 3.59 us: 1.34x faster                                                    |
| nbody                    | 93.0 ms                                                | 70.0 ms: 1.33x faster                                                    |
| tomli_loads              | 1.71 sec                                               | 1.29 sec: 1.33x faster                                                   |
| pycparser                | 877 ms                                                 | 667 ms: 1.31x faster                                                     |
| thrift                   | 572 us                                                 | 437 us: 1.31x faster                                                     |
| json_dumps               | 8.11 ms                                                | 6.28 ms: 1.29x faster                                                    |
| spectral_norm            | 94.8 ms                                                | 73.8 ms: 1.29x faster                                                    |
| pyflate                  | 427 ms                                                 | 335 ms: 1.28x faster                                                     |
| xml_etree_process        | 46.5 ms                                                | 36.5 ms: 1.27x faster                                                    |
| deepcopy                 | 272 us                                                 | 215 us: 1.26x faster                                                     |
| scimark_lu               | 103 ms                                                 | 81.5 ms: 1.26x faster                                                    |
| html5lib                 | 42.4 ms                                                | 33.8 ms: 1.25x faster                                                    |
| deepcopy_reduce          | 2.33 us                                                | 1.87 us: 1.25x faster                                                    |
| django_template          | 26.4 ms                                                | 21.3 ms: 1.24x faster                                                    |
| coroutines               | 20.7 ms                                                | 16.7 ms: 1.24x faster                                                    |
| generators               | 32.3 ms                                                | 26.2 ms: 1.23x faster                                                    |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.30 sec: 1.23x faster                                                   |
| pprint_pformat           | 1.30 sec                                               | 1.07 sec: 1.22x faster                                                   |
| pprint_safe_repr         | 641 ms                                                 | 527 ms: 1.22x faster                                                     |
| scimark_sor              | 128 ms                                                 | 108 ms: 1.19x faster                                                     |
| sympy_sum                | 92.2 ms                                                | 77.9 ms: 1.18x faster                                                    |
| genshi_text              | 17.3 ms                                                | 14.7 ms: 1.18x faster                                                    |
| fannkuch                 | 303 ms                                                 | 258 ms: 1.17x faster                                                     |
| hexiom                   | 6.19 ms                                                | 5.28 ms: 1.17x faster                                                    |
| dulwich_log              | 35.3 ms                                                | 30.2 ms: 1.17x faster                                                    |
| sympy_str                | 165 ms                                                 | 143 ms: 1.16x faster                                                     |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                                     |
| sympy_integrate          | 13.1 ms                                                | 11.7 ms: 1.13x faster                                                    |
| scimark_fft              | 224 ms                                                 | 200 ms: 1.12x faster                                                     |
| dask                     | 253 ms                                                 | 226 ms: 1.12x faster                                                     |
| sympy_expand             | 269 ms                                                 | 241 ms: 1.12x faster                                                     |
| xml_etree_parse          | 108 ms                                                 | 98.3 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.13 ms: 1.10x faster                                                    |
| docutils                 | 1.73 sec                                               | 1.58 sec: 1.09x faster                                                   |
| regex_compile            | 95.3 ms                                                | 87.2 ms: 1.09x faster                                                    |
| 2to3                     | 192 ms                                                 | 176 ms: 1.09x faster                                                     |
| gunicorn                 | 1.30 ms                                                | 1.21 ms: 1.08x faster                                                    |
| aiohttp                  | 1.22 ms                                                | 1.14 ms: 1.07x faster                                                    |
| sqlglot_optimize         | 36.8 ms                                                | 34.4 ms: 1.07x faster                                                    |
| sqlglot_normalize        | 190 ms                                                 | 178 ms: 1.07x faster                                                     |
| xml_etree_iterparse      | 72.1 ms                                                | 68.5 ms: 1.05x faster                                                    |
| bench_thread_pool        | 527 us                                                 | 501 us: 1.05x faster                                                     |
| json                     | 3.08 ms                                                | 2.95 ms: 1.05x faster                                                    |
| meteor_contest           | 77.7 ms                                                | 74.4 ms: 1.04x faster                                                    |
| nqueens                  | 63.8 ms                                                | 61.6 ms: 1.04x faster                                                    |
| genshi_xml               | 33.8 ms                                                | 32.7 ms: 1.04x faster                                                    |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                                   |
| create_gc_cycles         | 860 us                                                 | 847 us: 1.01x faster                                                     |
| xml_etree_generate       | 53.5 ms                                                | 54.1 ms: 1.01x slower                                                    |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                                    |
| json_loads               | 16.4 us                                                | 17.1 us: 1.04x slower                                                    |
| unpickle                 | 8.80 us                                                | 9.17 us: 1.04x slower                                                    |
| pickle_dict              | 17.0 us                                                | 18.0 us: 1.06x slower                                                    |
| regex_effbot             | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                    |
| pickle                   | 6.97 us                                                | 7.47 us: 1.07x slower                                                    |
| sqlite_synth             | 1.46 us                                                | 1.58 us: 1.08x slower                                                    |
| pickle_list              | 2.74 us                                                | 2.98 us: 1.09x slower                                                    |
| coverage                 | 41.5 ms                                                | 46.4 ms: 1.12x slower                                                    |
| unpickle_list            | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| python_startup           | 10.9 ms                                                | 13.4 ms: 1.23x slower                                                    |
| bench_mp_pool            | 37.4 ms                                                | 47.0 ms: 1.26x slower                                                    |
| telco                    | 3.49 ms                                                | 4.48 ms: 1.29x slower                                                    |
| async_generators         | 231 ms                                                 | 301 ms: 1.30x slower                                                     |
| python_startup_no_site   | 7.91 ms                                                | 11.6 ms: 1.47x slower                                                    |
| unpack_sequence          | 39.0 ns                                                | 116 ns: 2.97x slower                                                     |
| Geometric mean           | (ref)                                                  | 1.19x faster                                                             |

Benchmark hidden because not significant (5): tornado_http, asyncio_websockets, regex_v8, pidigits, pathlib
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (12) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.43x