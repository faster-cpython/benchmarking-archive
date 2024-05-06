# Results vs. 3.10.4

- fork: python
- ref: v3.12.3
- machine: darwin-arm64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 168 ms: 1.14x faster                                   |
| chameleon      | 6.26 ms                                                | 4.65 ms: 1.35x faster                                  |
| docutils       | 1.73 sec                                               | 1.49 sec: 1.16x faster                                 |
| html5lib       | 42.4 ms                                                | 32.5 ms: 1.30x faster                                  |
| tornado_http   | 86.7 ms                                                | 75.9 ms: 1.14x faster                                  |
| Geometric mean | (ref)                                                  | 1.22x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_memoization  | 474 ms                                                 | 315 ms: 1.50x faster                                   |
| async_tree_io           | 980 ms                                                 | 671 ms: 1.46x faster                                   |
| async_tree_none         | 388 ms                                                 | 269 ms: 1.44x faster                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 526 ms: 1.23x faster                                   |
| Geometric mean          | (ref)                                                  | 1.41x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 67.4 ms: 1.38x faster                                  |
| float          | 69.0 ms                                                | 55.6 ms: 1.24x faster                                  |
| Geometric mean | (ref)                                                  | 1.20x faster                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 77.6 ms: 1.23x faster                                  |
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                   |
| regex_v8       | 17.1 ms                                                | 16.7 ms: 1.03x faster                                  |
| regex_effbot   | 2.46 ms                                                | 2.68 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 201 us: 1.39x faster                                   |
| unpickle_pure_python | 194 us                                                 | 149 us: 1.31x faster                                   |
| json_dumps           | 8.11 ms                                                | 6.26 ms: 1.29x faster                                  |
| tomli_loads          | 1.71 sec                                               | 1.39 sec: 1.23x faster                                 |
| xml_etree_process    | 46.5 ms                                                | 39.8 ms: 1.17x faster                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 74.8 ms: 1.04x slower                                  |
| xml_etree_generate   | 53.5 ms                                                | 56.2 ms: 1.05x slower                                  |
| pickle               | 6.97 us                                                | 7.35 us: 1.05x slower                                  |
| json_loads           | 16.4 us                                                | 17.4 us: 1.06x slower                                  |
| pickle_list          | 2.74 us                                                | 2.89 us: 1.06x slower                                  |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                  |
| unpickle             | 8.80 us                                                | 9.38 us: 1.07x slower                                  |
| unpickle_list        | 2.69 us                                                | 3.08 us: 1.14x slower                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 11.2 ms: 1.03x slower                                  |
| python_startup_no_site | 7.91 ms                                                | 8.97 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 9.87 ms                                                | 7.60 ms: 1.30x faster                                  |
| django_template | 26.4 ms                                                | 22.4 ms: 1.18x faster                                  |
| genshi_text     | 17.3 ms                                                | 15.4 ms: 1.13x faster                                  |
| genshi_xml      | 33.8 ms                                                | 31.7 ms: 1.07x faster                                  |
| Geometric mean  | (ref)                                                  | 1.17x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 73.5 us: 4.40x faster                                  |
| deltablue                | 4.91 ms                                                | 2.67 ms: 1.84x faster                                  |
| asyncio_tcp              | 659 ms                                                 | 408 ms: 1.62x faster                                   |
| richards_super           | 57.8 ms                                                | 36.1 ms: 1.60x faster                                  |
| pylint                   | 277 ms                                                 | 175 ms: 1.58x faster                                   |
| chaos                    | 65.8 ms                                                | 42.8 ms: 1.54x faster                                  |
| richards                 | 48.7 ms                                                | 32.0 ms: 1.52x faster                                  |
| async_tree_memoization   | 474 ms                                                 | 315 ms: 1.50x faster                                   |
| logging_silent           | 117 ns                                                 | 78.7 ns: 1.49x faster                                  |
| go                       | 151 ms                                                 | 102 ms: 1.48x faster                                   |
| sqlglot_parse            | 1.24 ms                                                | 851 us: 1.46x faster                                   |
| async_tree_io            | 980 ms                                                 | 671 ms: 1.46x faster                                   |
| scimark_sor              | 128 ms                                                 | 88.2 ms: 1.45x faster                                  |
| comprehensions           | 16.9 us                                                | 11.7 us: 1.45x faster                                  |
| async_tree_none          | 388 ms                                                 | 269 ms: 1.44x faster                                   |
| scimark_monte_carlo      | 65.6 ms                                                | 45.6 ms: 1.44x faster                                  |
| raytrace                 | 301 ms                                                 | 211 ms: 1.43x faster                                   |
| sqlglot_transpile        | 1.44 ms                                                | 1.02 ms: 1.41x faster                                  |
| pickle_pure_python       | 281 us                                                 | 201 us: 1.39x faster                                   |
| crypto_pyaes             | 71.8 ms                                                | 51.9 ms: 1.38x faster                                  |
| nbody                    | 93.0 ms                                                | 67.4 ms: 1.38x faster                                  |
| scimark_lu               | 103 ms                                                 | 75.0 ms: 1.37x faster                                  |
| hexiom                   | 6.19 ms                                                | 4.55 ms: 1.36x faster                                  |
| chameleon                | 6.26 ms                                                | 4.65 ms: 1.35x faster                                  |
| pyflate                  | 427 ms                                                 | 318 ms: 1.34x faster                                   |
| mypy2                    | 607 ms                                                 | 457 ms: 1.33x faster                                   |
| sqlalchemy_imperative    | 8.86 ms                                                | 6.71 ms: 1.32x faster                                  |
| unpickle_pure_python     | 194 us                                                 | 149 us: 1.31x faster                                   |
| html5lib                 | 42.4 ms                                                | 32.5 ms: 1.30x faster                                  |
| mako                     | 9.87 ms                                                | 7.60 ms: 1.30x faster                                  |
| json_dumps               | 8.11 ms                                                | 6.26 ms: 1.29x faster                                  |
| pycparser                | 877 ms                                                 | 681 ms: 1.29x faster                                   |
| pprint_pformat           | 1.30 sec                                               | 1.01 sec: 1.29x faster                                 |
| pprint_safe_repr         | 641 ms                                                 | 502 ms: 1.28x faster                                   |
| deepcopy_memo            | 34.7 us                                                | 27.5 us: 1.26x faster                                  |
| spectral_norm            | 94.8 ms                                                | 76.2 ms: 1.24x faster                                  |
| sympy_sum                | 92.2 ms                                                | 74.2 ms: 1.24x faster                                  |
| float                    | 69.0 ms                                                | 55.6 ms: 1.24x faster                                  |
| create_gc_cycles         | 860 us                                                 | 695 us: 1.24x faster                                   |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 526 ms: 1.23x faster                                   |
| gunicorn                 | 1.30 ms                                                | 1.06 ms: 1.23x faster                                  |
| tomli_loads              | 1.71 sec                                               | 1.39 sec: 1.23x faster                                 |
| regex_compile            | 95.3 ms                                                | 77.6 ms: 1.23x faster                                  |
| aiohttp                  | 1.22 ms                                                | 1.01 ms: 1.21x faster                                  |
| fannkuch                 | 303 ms                                                 | 250 ms: 1.21x faster                                   |
| logging_format           | 4.83 us                                                | 4.00 us: 1.21x faster                                  |
| dulwich_log              | 35.3 ms                                                | 29.3 ms: 1.21x faster                                  |
| sympy_integrate          | 13.1 ms                                                | 10.9 ms: 1.20x faster                                  |
| logging_simple           | 4.45 us                                                | 3.71 us: 1.20x faster                                  |
| thrift                   | 572 us                                                 | 479 us: 1.20x faster                                   |
| django_template          | 26.4 ms                                                | 22.4 ms: 1.18x faster                                  |
| deepcopy                 | 272 us                                                 | 230 us: 1.18x faster                                   |
| sqlalchemy_declarative   | 73.3 ms                                                | 62.5 ms: 1.17x faster                                  |
| sympy_str                | 165 ms                                                 | 141 ms: 1.17x faster                                   |
| xml_etree_process        | 46.5 ms                                                | 39.8 ms: 1.17x faster                                  |
| docutils                 | 1.73 sec                                               | 1.49 sec: 1.16x faster                                 |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                   |
| deepcopy_reduce          | 2.33 us                                                | 2.03 us: 1.15x faster                                  |
| tornado_http             | 86.7 ms                                                | 75.9 ms: 1.14x faster                                  |
| dask                     | 253 ms                                                 | 222 ms: 1.14x faster                                   |
| 2to3                     | 192 ms                                                 | 168 ms: 1.14x faster                                   |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.41 sec: 1.14x faster                                 |
| scimark_fft              | 224 ms                                                 | 198 ms: 1.13x faster                                   |
| genshi_text              | 17.3 ms                                                | 15.4 ms: 1.13x faster                                  |
| sympy_expand             | 269 ms                                                 | 241 ms: 1.12x faster                                   |
| coroutines               | 20.7 ms                                                | 18.8 ms: 1.10x faster                                  |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.15 ms: 1.09x faster                                  |
| sqlglot_optimize         | 36.8 ms                                                | 34.1 ms: 1.08x faster                                  |
| genshi_xml               | 33.8 ms                                                | 31.7 ms: 1.07x faster                                  |
| meteor_contest           | 77.7 ms                                                | 73.1 ms: 1.06x faster                                  |
| coverage                 | 41.5 ms                                                | 39.1 ms: 1.06x faster                                  |
| bench_thread_pool        | 527 us                                                 | 498 us: 1.06x faster                                   |
| generators               | 32.3 ms                                                | 30.5 ms: 1.06x faster                                  |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                 |
| regex_v8                 | 17.1 ms                                                | 16.7 ms: 1.03x faster                                  |
| sqlglot_normalize        | 190 ms                                                 | 186 ms: 1.02x faster                                   |
| json                     | 3.08 ms                                                | 3.06 ms: 1.01x faster                                  |
| nqueens                  | 63.8 ms                                                | 63.2 ms: 1.01x faster                                  |
| gc_traversal             | 2.36 ms                                                | 2.40 ms: 1.01x slower                                  |
| pathlib                  | 24.5 ms                                                | 25.3 ms: 1.03x slower                                  |
| python_startup           | 10.9 ms                                                | 11.2 ms: 1.03x slower                                  |
| xml_etree_iterparse      | 72.1 ms                                                | 74.8 ms: 1.04x slower                                  |
| xml_etree_generate       | 53.5 ms                                                | 56.2 ms: 1.05x slower                                  |
| pickle                   | 6.97 us                                                | 7.35 us: 1.05x slower                                  |
| json_loads               | 16.4 us                                                | 17.4 us: 1.06x slower                                  |
| pickle_list              | 2.74 us                                                | 2.89 us: 1.06x slower                                  |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                  |
| unpickle                 | 8.80 us                                                | 9.38 us: 1.07x slower                                  |
| telco                    | 3.49 ms                                                | 3.76 ms: 1.08x slower                                  |
| sqlite_synth             | 1.46 us                                                | 1.58 us: 1.08x slower                                  |
| regex_effbot             | 2.46 ms                                                | 2.68 ms: 1.09x slower                                  |
| python_startup_no_site   | 7.91 ms                                                | 8.97 ms: 1.13x slower                                  |
| unpickle_list            | 2.69 us                                                | 3.08 us: 1.14x slower                                  |
| bench_mp_pool            | 37.4 ms                                                | 44.0 ms: 1.18x slower                                  |
| async_generators         | 231 ms                                                 | 301 ms: 1.30x slower                                   |
| Geometric mean           | (ref)                                                  | 1.20x faster                                           |

Benchmark hidden because not significant (3): xml_etree_parse, asyncio_websockets, pidigits
Ignored benchmarks (2) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, unpack_sequence
Ignored benchmarks (12) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.07x