# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 222 ms: 1.11x faster                                                          |
| chameleon      | 5.79 ms                                                     | 4.75 ms: 1.22x faster                                                         |
| docutils       | 1.92 sec                                                    | 1.73 sec: 1.11x faster                                                        |
| html5lib       | 51.0 ms                                                     | 36.8 ms: 1.39x faster                                                         |
| tornado_http   | 108 ms                                                      | 85.2 ms: 1.27x faster                                                         |
| Geometric mean | (ref)                                                       | 1.21x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 220 ms: 1.98x faster                                                          |
| async_tree_memoization  | 526 ms                                                      | 273 ms: 1.93x faster                                                          |
| async_tree_io           | 1.11 sec                                                    | 575 ms: 1.93x faster                                                          |
| async_tree_cpu_io_mixed | 638 ms                                                      | 379 ms: 1.68x faster                                                          |
| Geometric mean          | (ref)                                                       | 1.88x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                         |
| nbody          | 71.3 ms                                                     | 57.4 ms: 1.24x faster                                                         |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                       | 1.19x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 87.5 ms: 1.21x faster                                                         |
| regex_dna      | 136 ms                                                      | 116 ms: 1.17x faster                                                          |
| regex_effbot   | 1.66 ms                                                     | 1.56 ms: 1.06x faster                                                         |
| Geometric mean | (ref)                                                       | 1.11x faster                                                                  |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                         |
| pickle_pure_python   | 270 us                                                      | 178 us: 1.51x faster                                                          |
| unpickle_pure_python | 183 us                                                      | 131 us: 1.40x faster                                                          |
| tomli_loads          | 1.67 sec                                                    | 1.21 sec: 1.39x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 37.1 ms: 1.20x faster                                                         |
| unpickle             | 9.09 us                                                     | 8.48 us: 1.07x faster                                                         |
| xml_etree_parse      | 96.8 ms                                                     | 92.1 ms: 1.05x faster                                                         |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.03x faster                                                         |
| xml_etree_iterparse  | 65.0 ms                                                     | 64.1 ms: 1.01x faster                                                         |
| xml_etree_generate   | 55.5 ms                                                     | 55.0 ms: 1.01x faster                                                         |
| unpickle_list        | 2.71 us                                                     | 2.84 us: 1.05x slower                                                         |
| pickle               | 6.85 us                                                     | 7.40 us: 1.08x slower                                                         |
| pickle_dict          | 17.2 us                                                     | 18.8 us: 1.09x slower                                                         |
| pickle_list          | 2.75 us                                                     | 3.17 us: 1.15x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.12x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                         |
| python_startup_no_site | 15.5 ms                                                     | 19.6 ms: 1.26x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.71 ms: 1.58x faster                                                         |
| genshi_text     | 19.8 ms                                                     | 15.6 ms: 1.27x faster                                                         |
| django_template | 28.9 ms                                                     | 24.3 ms: 1.19x faster                                                         |
| genshi_xml      | 41.0 ms                                                     | 34.6 ms: 1.19x faster                                                         |
| Geometric mean  | (ref)                                                       | 1.30x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 73.0 us: 4.60x faster                                                         |
| deltablue                | 4.19 ms                                                     | 2.06 ms: 2.03x faster                                                         |
| async_tree_none          | 435 ms                                                      | 220 ms: 1.98x faster                                                          |
| async_tree_memoization   | 526 ms                                                      | 273 ms: 1.93x faster                                                          |
| async_tree_io            | 1.11 sec                                                    | 575 ms: 1.93x faster                                                          |
| pylint                   | 350 ms                                                      | 202 ms: 1.74x faster                                                          |
| logging_silent           | 94.6 ns                                                     | 55.0 ns: 1.72x faster                                                         |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 379 ms: 1.68x faster                                                          |
| richards_super           | 52.2 ms                                                     | 31.3 ms: 1.67x faster                                                         |
| json_dumps               | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                         |
| generators               | 32.4 ms                                                     | 20.4 ms: 1.59x faster                                                         |
| mako                     | 9.03 ms                                                     | 5.71 ms: 1.58x faster                                                         |
| chaos                    | 61.7 ms                                                     | 39.5 ms: 1.56x faster                                                         |
| sqlglot_parse            | 1.22 ms                                                     | 780 us: 1.56x faster                                                          |
| asyncio_tcp              | 732 ms                                                      | 471 ms: 1.56x faster                                                          |
| pickle_pure_python       | 270 us                                                      | 178 us: 1.51x faster                                                          |
| spectral_norm            | 77.3 ms                                                     | 51.2 ms: 1.51x faster                                                         |
| richards                 | 42.4 ms                                                     | 28.2 ms: 1.51x faster                                                         |
| comprehensions           | 16.5 us                                                     | 11.1 us: 1.49x faster                                                         |
| raytrace                 | 273 ms                                                      | 185 ms: 1.48x faster                                                          |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.44 sec: 1.47x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 1.01 ms: 1.46x faster                                                         |
| pyflate                  | 409 ms                                                      | 283 ms: 1.45x faster                                                          |
| go                       | 139 ms                                                      | 97.7 ms: 1.42x faster                                                         |
| unpickle_pure_python     | 183 us                                                      | 131 us: 1.40x faster                                                          |
| scimark_monte_carlo      | 57.3 ms                                                     | 41.1 ms: 1.39x faster                                                         |
| crypto_pyaes             | 62.5 ms                                                     | 45.0 ms: 1.39x faster                                                         |
| html5lib                 | 51.0 ms                                                     | 36.8 ms: 1.39x faster                                                         |
| tomli_loads              | 1.67 sec                                                    | 1.21 sec: 1.39x faster                                                        |
| pycparser                | 930 ms                                                      | 684 ms: 1.36x faster                                                          |
| deepcopy_memo            | 28.8 us                                                     | 21.5 us: 1.34x faster                                                         |
| scimark_sor              | 106 ms                                                      | 80.0 ms: 1.33x faster                                                         |
| float                    | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                         |
| pprint_safe_repr         | 592 ms                                                      | 465 ms: 1.27x faster                                                          |
| tornado_http             | 108 ms                                                      | 85.2 ms: 1.27x faster                                                         |
| pprint_pformat           | 1.22 sec                                                    | 961 ms: 1.27x faster                                                          |
| genshi_text              | 19.8 ms                                                     | 15.6 ms: 1.27x faster                                                         |
| nbody                    | 71.3 ms                                                     | 57.4 ms: 1.24x faster                                                         |
| dulwich_log              | 50.5 ms                                                     | 40.9 ms: 1.23x faster                                                         |
| chameleon                | 5.79 ms                                                     | 4.75 ms: 1.22x faster                                                         |
| sqlite_synth             | 1.91 us                                                     | 1.57 us: 1.22x faster                                                         |
| regex_compile            | 106 ms                                                      | 87.5 ms: 1.21x faster                                                         |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                         |
| xml_etree_process        | 44.5 ms                                                     | 37.1 ms: 1.20x faster                                                         |
| mdp                      | 1.78 sec                                                    | 1.49 sec: 1.19x faster                                                        |
| django_template          | 28.9 ms                                                     | 24.3 ms: 1.19x faster                                                         |
| sympy_sum                | 107 ms                                                      | 90.1 ms: 1.19x faster                                                         |
| genshi_xml               | 41.0 ms                                                     | 34.6 ms: 1.19x faster                                                         |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.30 ms: 1.18x faster                                                         |
| mypy2                    | 555 ms                                                      | 471 ms: 1.18x faster                                                          |
| regex_dna                | 136 ms                                                      | 116 ms: 1.17x faster                                                          |
| scimark_lu               | 85.8 ms                                                     | 73.2 ms: 1.17x faster                                                         |
| hexiom                   | 5.74 ms                                                     | 4.92 ms: 1.17x faster                                                         |
| bench_thread_pool        | 958 us                                                      | 833 us: 1.15x faster                                                          |
| deepcopy                 | 255 us                                                      | 225 us: 1.13x faster                                                          |
| sympy_str                | 194 ms                                                      | 172 ms: 1.13x faster                                                          |
| sympy_integrate          | 15.3 ms                                                     | 13.6 ms: 1.12x faster                                                         |
| scimark_fft              | 187 ms                                                      | 168 ms: 1.12x faster                                                          |
| docutils                 | 1.92 sec                                                    | 1.73 sec: 1.11x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 35.9 ms: 1.11x faster                                                         |
| deepcopy_reduce          | 2.20 us                                                     | 1.99 us: 1.11x faster                                                         |
| 2to3                     | 246 ms                                                      | 222 ms: 1.11x faster                                                          |
| fannkuch                 | 256 ms                                                      | 232 ms: 1.10x faster                                                          |
| aiohttp                  | 995 us                                                      | 903 us: 1.10x faster                                                          |
| sqlglot_normalize        | 205 ms                                                      | 187 ms: 1.10x faster                                                          |
| json                     | 3.14 ms                                                     | 2.87 ms: 1.09x faster                                                         |
| unpickle                 | 9.09 us                                                     | 8.48 us: 1.07x faster                                                         |
| nqueens                  | 66.6 ms                                                     | 62.5 ms: 1.07x faster                                                         |
| logging_format           | 6.76 us                                                     | 6.36 us: 1.06x faster                                                         |
| sympy_expand             | 314 ms                                                      | 296 ms: 1.06x faster                                                          |
| regex_effbot             | 1.66 ms                                                     | 1.56 ms: 1.06x faster                                                         |
| xml_etree_parse          | 96.8 ms                                                     | 92.1 ms: 1.05x faster                                                         |
| logging_simple           | 6.22 us                                                     | 5.92 us: 1.05x faster                                                         |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.03x faster                                                         |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                          |
| xml_etree_iterparse      | 65.0 ms                                                     | 64.1 ms: 1.01x faster                                                         |
| meteor_contest           | 75.9 ms                                                     | 75.1 ms: 1.01x faster                                                         |
| xml_etree_generate       | 55.5 ms                                                     | 55.0 ms: 1.01x faster                                                         |
| pathlib                  | 75.7 ms                                                     | 77.8 ms: 1.03x slower                                                         |
| unpickle_list            | 2.71 us                                                     | 2.84 us: 1.05x slower                                                         |
| python_startup           | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                         |
| create_gc_cycles         | 800 us                                                      | 856 us: 1.07x slower                                                          |
| pickle                   | 6.85 us                                                     | 7.40 us: 1.08x slower                                                         |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                         |
| async_generators         | 222 ms                                                      | 242 ms: 1.09x slower                                                          |
| bench_mp_pool            | 62.0 ms                                                     | 67.8 ms: 1.09x slower                                                         |
| pickle_dict              | 17.2 us                                                     | 18.8 us: 1.09x slower                                                         |
| unpack_sequence          | 39.6 ns                                                     | 44.7 ns: 1.13x slower                                                         |
| pickle_list              | 2.75 us                                                     | 3.17 us: 1.15x slower                                                         |
| coverage                 | 39.0 ms                                                     | 46.3 ms: 1.19x slower                                                         |
| telco                    | 3.94 ms                                                     | 4.72 ms: 1.20x slower                                                         |
| python_startup_no_site   | 15.5 ms                                                     | 19.6 ms: 1.26x slower                                                         |
| thrift                   | 617 us                                                      | 9.22 ms: 14.93x slower                                                        |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                                  |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown