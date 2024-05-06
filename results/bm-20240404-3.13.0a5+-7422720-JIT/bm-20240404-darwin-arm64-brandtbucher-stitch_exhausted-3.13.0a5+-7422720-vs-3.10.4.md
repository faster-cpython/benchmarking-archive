# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 173 ms: 1.10x faster                                                     |
| chameleon      | 6.26 ms                                                | 4.46 ms: 1.40x faster                                                    |
| docutils       | 1.73 sec                                               | 1.58 sec: 1.10x faster                                                   |
| html5lib       | 42.4 ms                                                | 31.2 ms: 1.36x faster                                                    |
| Geometric mean | (ref)                                                  | 1.20x faster                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 204 ms: 1.91x faster                                                     |
| async_tree_memoization  | 474 ms                                                 | 262 ms: 1.81x faster                                                     |
| async_tree_io           | 980 ms                                                 | 568 ms: 1.73x faster                                                     |
| async_tree_cpu_io_mixed | 649 ms                                                 | 464 ms: 1.40x faster                                                     |
| Geometric mean          | (ref)                                                  | 1.70x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.5 ms: 1.39x faster                                                    |
| nbody          | 93.0 ms                                                | 70.3 ms: 1.32x faster                                                    |
| Geometric mean | (ref)                                                  | 1.23x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 145 ms: 1.20x faster                                                     |
| regex_compile  | 95.3 ms                                                | 86.1 ms: 1.11x faster                                                    |
| regex_v8       | 17.1 ms                                                | 17.2 ms: 1.00x slower                                                    |
| regex_effbot   | 2.46 ms                                                | 2.56 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.53x faster                                                     |
| unpickle_pure_python | 194 us                                                 | 140 us: 1.39x faster                                                     |
| tomli_loads          | 1.71 sec                                               | 1.29 sec: 1.32x faster                                                   |
| xml_etree_process    | 46.5 ms                                                | 36.5 ms: 1.28x faster                                                    |
| json_dumps           | 8.11 ms                                                | 6.37 ms: 1.27x faster                                                    |
| xml_etree_parse      | 108 ms                                                 | 106 ms: 1.01x faster                                                     |
| xml_etree_generate   | 53.5 ms                                                | 54.3 ms: 1.02x slower                                                    |
| json_loads           | 16.4 us                                                | 17.1 us: 1.04x slower                                                    |
| unpickle             | 8.80 us                                                | 9.27 us: 1.05x slower                                                    |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                    |
| pickle               | 6.97 us                                                | 7.49 us: 1.07x slower                                                    |
| pickle_list          | 2.74 us                                                | 3.00 us: 1.10x slower                                                    |
| unpickle_list        | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.5 ms: 1.24x slower                                                    |
| python_startup_no_site | 7.91 ms                                                | 11.7 ms: 1.48x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 9.87 ms                                                | 6.92 ms: 1.43x faster                                                    |
| genshi_text    | 17.3 ms                                                | 14.7 ms: 1.18x faster                                                    |
| genshi_xml     | 33.8 ms                                                | 33.2 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                  | 1.20x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 70.3 us: 4.60x faster                                                    |
| deltablue                | 4.91 ms                                                | 2.48 ms: 1.98x faster                                                    |
| async_tree_none          | 388 ms                                                 | 204 ms: 1.91x faster                                                     |
| logging_silent           | 117 ns                                                 | 63.8 ns: 1.84x faster                                                    |
| raytrace                 | 301 ms                                                 | 165 ms: 1.83x faster                                                     |
| async_tree_memoization   | 474 ms                                                 | 262 ms: 1.81x faster                                                     |
| richards_super           | 57.8 ms                                                | 32.7 ms: 1.77x faster                                                    |
| pylint                   | 277 ms                                                 | 157 ms: 1.76x faster                                                     |
| async_tree_io            | 980 ms                                                 | 568 ms: 1.73x faster                                                     |
| chaos                    | 65.8 ms                                                | 38.9 ms: 1.69x faster                                                    |
| richards                 | 48.7 ms                                                | 29.1 ms: 1.67x faster                                                    |
| sqlglot_parse            | 1.24 ms                                                | 772 us: 1.61x faster                                                     |
| asyncio_tcp              | 659 ms                                                 | 419 ms: 1.57x faster                                                     |
| crypto_pyaes             | 71.8 ms                                                | 46.9 ms: 1.53x faster                                                    |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.53x faster                                                     |
| sqlglot_transpile        | 1.44 ms                                                | 948 us: 1.52x faster                                                     |
| scimark_monte_carlo      | 65.6 ms                                                | 44.3 ms: 1.48x faster                                                    |
| go                       | 151 ms                                                 | 105 ms: 1.44x faster                                                     |
| deepcopy_memo            | 34.7 us                                                | 24.2 us: 1.44x faster                                                    |
| mako                     | 9.87 ms                                                | 6.92 ms: 1.43x faster                                                    |
| mypy2                    | 607 ms                                                 | 427 ms: 1.42x faster                                                     |
| chameleon                | 6.26 ms                                                | 4.46 ms: 1.40x faster                                                    |
| logging_simple           | 4.45 us                                                | 3.17 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 464 ms: 1.40x faster                                                     |
| logging_format           | 4.83 us                                                | 3.46 us: 1.39x faster                                                    |
| float                    | 69.0 ms                                                | 49.5 ms: 1.39x faster                                                    |
| comprehensions           | 16.9 us                                                | 12.2 us: 1.39x faster                                                    |
| unpickle_pure_python     | 194 us                                                 | 140 us: 1.39x faster                                                     |
| html5lib                 | 42.4 ms                                                | 31.2 ms: 1.36x faster                                                    |
| pyflate                  | 427 ms                                                 | 319 ms: 1.34x faster                                                     |
| pycparser                | 877 ms                                                 | 655 ms: 1.34x faster                                                     |
| nbody                    | 93.0 ms                                                | 70.3 ms: 1.32x faster                                                    |
| tomli_loads              | 1.71 sec                                               | 1.29 sec: 1.32x faster                                                   |
| deepcopy                 | 272 us                                                 | 211 us: 1.29x faster                                                     |
| spectral_norm            | 94.8 ms                                                | 73.5 ms: 1.29x faster                                                    |
| thrift                   | 572 us                                                 | 448 us: 1.28x faster                                                     |
| xml_etree_process        | 46.5 ms                                                | 36.5 ms: 1.28x faster                                                    |
| json_dumps               | 8.11 ms                                                | 6.37 ms: 1.27x faster                                                    |
| scimark_lu               | 103 ms                                                 | 81.3 ms: 1.26x faster                                                    |
| pprint_safe_repr         | 641 ms                                                 | 507 ms: 1.26x faster                                                     |
| pprint_pformat           | 1.30 sec                                               | 1.04 sec: 1.26x faster                                                   |
| deepcopy_reduce          | 2.33 us                                                | 1.86 us: 1.25x faster                                                    |
| generators               | 32.3 ms                                                | 26.1 ms: 1.24x faster                                                    |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.31 sec: 1.22x faster                                                   |
| dulwich_log              | 35.3 ms                                                | 29.0 ms: 1.22x faster                                                    |
| coroutines               | 20.7 ms                                                | 17.0 ms: 1.22x faster                                                    |
| scimark_sor              | 128 ms                                                 | 106 ms: 1.21x faster                                                     |
| hexiom                   | 6.19 ms                                                | 5.15 ms: 1.20x faster                                                    |
| regex_dna                | 174 ms                                                 | 145 ms: 1.20x faster                                                     |
| sympy_sum                | 92.2 ms                                                | 77.7 ms: 1.19x faster                                                    |
| genshi_text              | 17.3 ms                                                | 14.7 ms: 1.18x faster                                                    |
| fannkuch                 | 303 ms                                                 | 261 ms: 1.16x faster                                                     |
| sympy_str                | 165 ms                                                 | 144 ms: 1.15x faster                                                     |
| dask                     | 253 ms                                                 | 222 ms: 1.14x faster                                                     |
| scimark_fft              | 224 ms                                                 | 201 ms: 1.12x faster                                                     |
| sympy_integrate          | 13.1 ms                                                | 11.8 ms: 1.12x faster                                                    |
| sympy_expand             | 269 ms                                                 | 241 ms: 1.12x faster                                                     |
| regex_compile            | 95.3 ms                                                | 86.1 ms: 1.11x faster                                                    |
| 2to3                     | 192 ms                                                 | 173 ms: 1.10x faster                                                     |
| docutils                 | 1.73 sec                                               | 1.58 sec: 1.10x faster                                                   |
| gunicorn                 | 1.30 ms                                                | 1.19 ms: 1.09x faster                                                    |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.13 ms: 1.09x faster                                                    |
| sqlglot_optimize         | 36.8 ms                                                | 34.2 ms: 1.08x faster                                                    |
| aiohttp                  | 1.22 ms                                                | 1.14 ms: 1.07x faster                                                    |
| sqlglot_normalize        | 190 ms                                                 | 178 ms: 1.07x faster                                                     |
| bench_thread_pool        | 527 us                                                 | 495 us: 1.07x faster                                                     |
| json                     | 3.08 ms                                                | 2.94 ms: 1.05x faster                                                    |
| meteor_contest           | 77.7 ms                                                | 74.3 ms: 1.05x faster                                                    |
| nqueens                  | 63.8 ms                                                | 62.0 ms: 1.03x faster                                                    |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                                   |
| genshi_xml               | 33.8 ms                                                | 33.2 ms: 1.02x faster                                                    |
| xml_etree_parse          | 108 ms                                                 | 106 ms: 1.01x faster                                                     |
| regex_v8                 | 17.1 ms                                                | 17.2 ms: 1.00x slower                                                    |
| xml_etree_generate       | 53.5 ms                                                | 54.3 ms: 1.02x slower                                                    |
| pathlib                  | 24.5 ms                                                | 25.3 ms: 1.03x slower                                                    |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                                    |
| json_loads               | 16.4 us                                                | 17.1 us: 1.04x slower                                                    |
| create_gc_cycles         | 860 us                                                 | 893 us: 1.04x slower                                                     |
| regex_effbot             | 2.46 ms                                                | 2.56 ms: 1.04x slower                                                    |
| unpickle                 | 8.80 us                                                | 9.27 us: 1.05x slower                                                    |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                    |
| pickle                   | 6.97 us                                                | 7.49 us: 1.07x slower                                                    |
| sqlite_synth             | 1.46 us                                                | 1.58 us: 1.08x slower                                                    |
| pickle_list              | 2.74 us                                                | 3.00 us: 1.10x slower                                                    |
| coverage                 | 41.5 ms                                                | 46.5 ms: 1.12x slower                                                    |
| unpickle_list            | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| python_startup           | 10.9 ms                                                | 13.5 ms: 1.24x slower                                                    |
| bench_mp_pool            | 37.4 ms                                                | 46.4 ms: 1.24x slower                                                    |
| async_generators         | 231 ms                                                 | 300 ms: 1.30x slower                                                     |
| telco                    | 3.49 ms                                                | 4.57 ms: 1.31x slower                                                    |
| python_startup_no_site   | 7.91 ms                                                | 11.7 ms: 1.48x slower                                                    |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                             |

Benchmark hidden because not significant (4): tornado_http, asyncio_websockets, pidigits, xml_etree_iterparse
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.40x