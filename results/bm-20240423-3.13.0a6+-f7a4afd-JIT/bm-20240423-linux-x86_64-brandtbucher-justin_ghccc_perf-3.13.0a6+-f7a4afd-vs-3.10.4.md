# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_perf
- machine: linux-x86_64
- commit hash: f7a4afd
- commit date: 2024-04-23
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 275 ms: 1.27x faster                                                      |
| chameleon      | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                     |
| docutils       | 3.30 sec                                               | 2.91 sec: 1.13x faster                                                    |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                     |
| tornado_http   | 136 ms                                                 | 95.7 ms: 1.43x faster                                                     |
| Geometric mean | (ref)                                                  | 1.30x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 360 ms: 2.02x faster                                                      |
| async_tree_memoization  | 870 ms                                                 | 458 ms: 1.90x faster                                                      |
| async_tree_io           | 1.77 sec                                               | 932 ms: 1.90x faster                                                      |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 618 ms: 1.64x faster                                                      |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 82.4 ms: 1.86x faster                                                     |
| float          | 117 ms                                                 | 74.9 ms: 1.56x faster                                                     |
| pidigits       | 191 ms                                                 | 192 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                  | 1.43x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.34x faster                                                      |
| regex_v8       | 27.8 ms                                                | 24.6 ms: 1.13x faster                                                     |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                      |
| regex_effbot   | 3.63 ms                                                | 3.80 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                  | 1.10x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.96 sec: 1.60x faster                                                    |
| pickle_pure_python   | 484 us                                                 | 307 us: 1.58x faster                                                      |
| unpickle_pure_python | 331 us                                                 | 227 us: 1.46x faster                                                      |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                     |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                     |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                     |
| xml_etree_iterparse  | 115 ms                                                 | 103 ms: 1.13x faster                                                      |
| xml_etree_parse      | 168 ms                                                 | 150 ms: 1.12x faster                                                      |
| json_loads           | 31.2 us                                                | 28.3 us: 1.10x faster                                                     |
| pickle_list          | 5.08 us                                                | 5.17 us: 1.02x slower                                                     |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                     |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                     |
| pickle_dict          | 29.6 us                                                | 34.4 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                              |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                     |
| python_startup_no_site | 5.93 ms                                                | 7.60 ms: 1.28x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.1 ms: 1.62x faster                                                     |
| django_template | 48.2 ms                                                | 36.7 ms: 1.31x faster                                                     |
| genshi_text     | 31.8 ms                                                | 24.6 ms: 1.29x faster                                                     |
| genshi_xml      | 66.0 ms                                                | 54.5 ms: 1.21x faster                                                     |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 112 us: 4.87x faster                                                      |
| generators               | 80.1 ms                                                | 29.8 ms: 2.68x faster                                                     |
| deltablue                | 7.91 ms                                                | 3.68 ms: 2.15x faster                                                     |
| async_tree_none          | 728 ms                                                 | 360 ms: 2.02x faster                                                      |
| richards_super           | 94.7 ms                                                | 48.9 ms: 1.94x faster                                                     |
| chaos                    | 115 ms                                                 | 60.7 ms: 1.90x faster                                                     |
| async_tree_memoization   | 870 ms                                                 | 458 ms: 1.90x faster                                                      |
| async_tree_io            | 1.77 sec                                               | 932 ms: 1.90x faster                                                      |
| logging_silent           | 190 ns                                                 | 101 ns: 1.87x faster                                                      |
| richards                 | 79.3 ms                                                | 42.3 ms: 1.87x faster                                                     |
| raytrace                 | 507 ms                                                 | 272 ms: 1.86x faster                                                      |
| nbody                    | 154 ms                                                 | 82.4 ms: 1.86x faster                                                     |
| scimark_monte_carlo      | 118 ms                                                 | 64.2 ms: 1.84x faster                                                     |
| crypto_pyaes             | 128 ms                                                 | 69.6 ms: 1.84x faster                                                     |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                                      |
| spectral_norm            | 170 ms                                                 | 97.8 ms: 1.74x faster                                                     |
| scimark_sor              | 220 ms                                                 | 128 ms: 1.72x faster                                                      |
| comprehensions           | 28.8 us                                                | 17.1 us: 1.68x faster                                                     |
| pylint                   | 551 ms                                                 | 335 ms: 1.65x faster                                                      |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 618 ms: 1.64x faster                                                      |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                                     |
| mako                     | 16.3 ms                                                | 10.1 ms: 1.62x faster                                                     |
| pyflate                  | 716 ms                                                 | 444 ms: 1.61x faster                                                      |
| tomli_loads              | 3.14 sec                                               | 1.96 sec: 1.60x faster                                                    |
| hexiom                   | 10.4 ms                                                | 6.58 ms: 1.58x faster                                                     |
| coroutines               | 35.1 ms                                                | 22.2 ms: 1.58x faster                                                     |
| pickle_pure_python       | 484 us                                                 | 307 us: 1.58x faster                                                      |
| sqlglot_transpile        | 2.57 ms                                                | 1.64 ms: 1.57x faster                                                     |
| float                    | 117 ms                                                 | 74.9 ms: 1.56x faster                                                     |
| go                       | 240 ms                                                 | 154 ms: 1.56x faster                                                      |
| deepcopy_memo            | 58.5 us                                                | 38.8 us: 1.51x faster                                                     |
| scimark_fft              | 466 ms                                                 | 315 ms: 1.48x faster                                                      |
| fannkuch                 | 532 ms                                                 | 364 ms: 1.46x faster                                                      |
| unpickle_pure_python     | 331 us                                                 | 227 us: 1.46x faster                                                      |
| tornado_http             | 136 ms                                                 | 95.7 ms: 1.43x faster                                                     |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.62 ms: 1.40x faster                                                     |
| logging_simple           | 8.30 us                                                | 5.94 us: 1.40x faster                                                     |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.40x faster                                                    |
| logging_format           | 9.09 us                                                | 6.56 us: 1.38x faster                                                     |
| chameleon                | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                     |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                    |
| scimark_lu               | 176 ms                                                 | 128 ms: 1.37x faster                                                      |
| pprint_safe_repr         | 1.02 sec                                               | 741 ms: 1.37x faster                                                      |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.35x faster                                                    |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                     |
| regex_compile            | 188 ms                                                 | 140 ms: 1.34x faster                                                      |
| deepcopy                 | 479 us                                                 | 360 us: 1.33x faster                                                      |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                     |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                     |
| django_template          | 48.2 ms                                                | 36.7 ms: 1.31x faster                                                     |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                     |
| genshi_text              | 31.8 ms                                                | 24.6 ms: 1.29x faster                                                     |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                     |
| thrift                   | 1.07 ms                                                | 830 us: 1.29x faster                                                      |
| 2to3                     | 348 ms                                                 | 275 ms: 1.27x faster                                                      |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                                      |
| dulwich_log              | 84.3 ms                                                | 68.9 ms: 1.22x faster                                                     |
| genshi_xml               | 66.0 ms                                                | 54.5 ms: 1.21x faster                                                     |
| sqlglot_optimize         | 69.2 ms                                                | 57.3 ms: 1.21x faster                                                     |
| nqueens                  | 106 ms                                                 | 87.9 ms: 1.20x faster                                                     |
| djangocms                | 38.4 us                                                | 32.1 us: 1.20x faster                                                     |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                     |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.18x faster                                                      |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                                     |
| dask                     | 441 ms                                                 | 374 ms: 1.18x faster                                                      |
| sympy_str                | 346 ms                                                 | 293 ms: 1.18x faster                                                      |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                     |
| bench_thread_pool        | 986 us                                                 | 853 us: 1.16x faster                                                      |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                     |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                     |
| sympy_expand             | 566 ms                                                 | 496 ms: 1.14x faster                                                      |
| mypy2                    | 894 ms                                                 | 783 ms: 1.14x faster                                                      |
| docutils                 | 3.30 sec                                               | 2.91 sec: 1.13x faster                                                    |
| regex_v8                 | 27.8 ms                                                | 24.6 ms: 1.13x faster                                                     |
| xml_etree_iterparse      | 115 ms                                                 | 103 ms: 1.13x faster                                                      |
| xml_etree_parse          | 168 ms                                                 | 150 ms: 1.12x faster                                                      |
| json                     | 5.69 ms                                                | 5.15 ms: 1.10x faster                                                     |
| json_loads               | 31.2 us                                                | 28.3 us: 1.10x faster                                                     |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.09x faster                                                      |
| sqlite_synth             | 3.02 us                                                | 2.86 us: 1.06x faster                                                     |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                      |
| mdp                      | 2.85 sec                                               | 2.84 sec: 1.00x faster                                                    |
| pidigits                 | 191 ms                                                 | 192 ms: 1.01x slower                                                      |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                      |
| pickle_list              | 5.08 us                                                | 5.17 us: 1.02x slower                                                     |
| async_generators         | 444 ms                                                 | 465 ms: 1.05x slower                                                      |
| regex_effbot             | 3.63 ms                                                | 3.80 ms: 1.05x slower                                                     |
| gc_traversal             | 3.62 ms                                                | 3.80 ms: 1.05x slower                                                     |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                     |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                     |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                     |
| pickle_dict              | 29.6 us                                                | 34.4 us: 1.16x slower                                                     |
| telco                    | 7.27 ms                                                | 8.67 ms: 1.19x slower                                                     |
| coverage                 | 79.4 ms                                                | 98.6 ms: 1.24x slower                                                     |
| python_startup_no_site   | 5.93 ms                                                | 7.60 ms: 1.28x slower                                                     |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                              |

Benchmark hidden because not significant (2): unpickle_list, bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-f7a4afd-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.19x