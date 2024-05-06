# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: 07e95c4
- commit date: 2024-04-23
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 275 ms: 1.27x faster                                                 |
| chameleon      | 9.68 ms                                                | 6.93 ms: 1.40x faster                                                |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                               |
| html5lib       | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                |
| tornado_http   | 136 ms                                                 | 96.3 ms: 1.42x faster                                                |
| Geometric mean | (ref)                                                  | 1.30x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.05x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 925 ms: 1.91x faster                                                 |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                                 |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 82.2 ms: 1.87x faster                                                |
| float          | 117 ms                                                 | 73.4 ms: 1.59x faster                                                |
| pidigits       | 191 ms                                                 | 197 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.43x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                 |
| regex_v8       | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                 |
| regex_effbot   | 3.63 ms                                                | 3.57 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                  | 1.13x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.96 sec: 1.60x faster                                               |
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                 |
| unpickle_pure_python | 331 us                                                 | 227 us: 1.46x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 60.1 ms: 1.32x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 87.1 ms: 1.14x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 102 ms: 1.14x faster                                                 |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                |
| xml_etree_parse      | 168 ms                                                 | 150 ms: 1.12x faster                                                 |
| pickle_list          | 5.08 us                                                | 4.75 us: 1.07x faster                                                |
| unpickle_list        | 5.20 us                                                | 5.05 us: 1.03x faster                                                |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                |
| pickle               | 10.7 us                                                | 11.9 us: 1.11x slower                                                |
| pickle_dict          | 29.6 us                                                | 33.5 us: 1.13x slower                                                |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 7.57 ms: 1.28x slower                                                |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 9.96 ms: 1.64x faster                                                |
| django_template | 48.2 ms                                                | 36.2 ms: 1.33x faster                                                |
| genshi_text     | 31.8 ms                                                | 24.7 ms: 1.29x faster                                                |
| genshi_xml      | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.78x faster                                                 |
| generators               | 80.1 ms                                                | 30.4 ms: 2.63x faster                                                |
| deltablue                | 7.91 ms                                                | 3.69 ms: 2.14x faster                                                |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.05x faster                                                 |
| richards_super           | 94.7 ms                                                | 48.8 ms: 1.94x faster                                                |
| async_tree_io            | 1.77 sec                                               | 925 ms: 1.91x faster                                                 |
| chaos                    | 115 ms                                                 | 60.9 ms: 1.90x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                                 |
| raytrace                 | 507 ms                                                 | 271 ms: 1.87x faster                                                 |
| nbody                    | 154 ms                                                 | 82.2 ms: 1.87x faster                                                |
| richards                 | 79.3 ms                                                | 42.5 ms: 1.87x faster                                                |
| crypto_pyaes             | 128 ms                                                 | 68.6 ms: 1.86x faster                                                |
| scimark_monte_carlo      | 118 ms                                                 | 63.9 ms: 1.85x faster                                                |
| logging_silent           | 190 ns                                                 | 104 ns: 1.83x faster                                                 |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                                 |
| spectral_norm            | 170 ms                                                 | 98.9 ms: 1.72x faster                                                |
| comprehensions           | 28.8 us                                                | 17.0 us: 1.69x faster                                                |
| scimark_sor              | 220 ms                                                 | 130 ms: 1.69x faster                                                 |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                 |
| pylint                   | 551 ms                                                 | 335 ms: 1.64x faster                                                 |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                                |
| mako                     | 16.3 ms                                                | 9.96 ms: 1.64x faster                                                |
| pyflate                  | 716 ms                                                 | 442 ms: 1.62x faster                                                 |
| tomli_loads              | 3.14 sec                                               | 1.96 sec: 1.60x faster                                               |
| hexiom                   | 10.4 ms                                                | 6.50 ms: 1.60x faster                                                |
| float                    | 117 ms                                                 | 73.4 ms: 1.59x faster                                                |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                 |
| sqlglot_transpile        | 2.57 ms                                                | 1.64 ms: 1.57x faster                                                |
| go                       | 240 ms                                                 | 153 ms: 1.57x faster                                                 |
| coroutines               | 35.1 ms                                                | 22.9 ms: 1.53x faster                                                |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                |
| fannkuch                 | 532 ms                                                 | 353 ms: 1.51x faster                                                 |
| scimark_fft              | 466 ms                                                 | 316 ms: 1.47x faster                                                 |
| unpickle_pure_python     | 331 us                                                 | 227 us: 1.46x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.52 ms: 1.43x faster                                                |
| logging_simple           | 8.30 us                                                | 5.86 us: 1.42x faster                                                |
| tornado_http             | 136 ms                                                 | 96.3 ms: 1.42x faster                                                |
| chameleon                | 9.68 ms                                                | 6.93 ms: 1.40x faster                                                |
| scimark_lu               | 176 ms                                                 | 126 ms: 1.40x faster                                                 |
| logging_format           | 9.09 us                                                | 6.52 us: 1.39x faster                                                |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                               |
| pprint_safe_repr         | 1.02 sec                                               | 745 ms: 1.37x faster                                                 |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.36x faster                                               |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                 |
| deepcopy                 | 479 us                                                 | 358 us: 1.34x faster                                                 |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.34x faster                                               |
| django_template          | 48.2 ms                                                | 36.2 ms: 1.33x faster                                                |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 60.1 ms: 1.32x faster                                                |
| html5lib                 | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                |
| deepcopy_reduce          | 4.17 us                                                | 3.18 us: 1.31x faster                                                |
| thrift                   | 1.07 ms                                                | 822 us: 1.30x faster                                                 |
| genshi_text              | 31.8 ms                                                | 24.7 ms: 1.29x faster                                                |
| 2to3                     | 348 ms                                                 | 275 ms: 1.27x faster                                                 |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                 |
| nqueens                  | 106 ms                                                 | 86.4 ms: 1.22x faster                                                |
| dulwich_log              | 84.3 ms                                                | 69.1 ms: 1.22x faster                                                |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 57.4 ms: 1.21x faster                                                |
| genshi_xml               | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.18x faster                                                 |
| sympy_str                | 346 ms                                                 | 294 ms: 1.18x faster                                                 |
| sympy_integrate          | 25.8 ms                                                | 22.0 ms: 1.17x faster                                                |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.17x faster                                                |
| dask                     | 441 ms                                                 | 378 ms: 1.17x faster                                                 |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                |
| bench_thread_pool        | 986 us                                                 | 861 us: 1.15x faster                                                 |
| sympy_expand             | 566 ms                                                 | 495 ms: 1.14x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 87.1 ms: 1.14x faster                                                |
| regex_v8                 | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                               |
| xml_etree_iterparse      | 115 ms                                                 | 102 ms: 1.14x faster                                                 |
| mypy2                    | 894 ms                                                 | 790 ms: 1.13x faster                                                 |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 150 ms: 1.12x faster                                                 |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                                |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                 |
| pickle_list              | 5.08 us                                                | 4.75 us: 1.07x faster                                                |
| sqlite_synth             | 3.02 us                                                | 2.84 us: 1.06x faster                                                |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                 |
| mdp                      | 2.85 sec                                               | 2.76 sec: 1.03x faster                                               |
| unpickle_list            | 5.20 us                                                | 5.05 us: 1.03x faster                                                |
| regex_effbot             | 3.63 ms                                                | 3.57 ms: 1.02x faster                                                |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                 |
| pidigits                 | 191 ms                                                 | 197 ms: 1.03x slower                                                 |
| gc_traversal             | 3.62 ms                                                | 3.79 ms: 1.05x slower                                                |
| async_generators         | 444 ms                                                 | 469 ms: 1.06x slower                                                 |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                |
| pickle                   | 10.7 us                                                | 11.9 us: 1.11x slower                                                |
| pickle_dict              | 29.6 us                                                | 33.5 us: 1.13x slower                                                |
| telco                    | 7.27 ms                                                | 8.69 ms: 1.20x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 7.57 ms: 1.28x slower                                                |
| coverage                 | 79.4 ms                                                | 104 ms: 1.31x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                         |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-07e95c4-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.25x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.19x