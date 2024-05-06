# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 222 ms: 1.11x faster                                                          |
| chameleon      | 5.79 ms                                                     | 4.81 ms: 1.20x faster                                                         |
| docutils       | 1.92 sec                                                    | 1.72 sec: 1.12x faster                                                        |
| html5lib       | 51.0 ms                                                     | 35.6 ms: 1.43x faster                                                         |
| tornado_http   | 108 ms                                                      | 83.6 ms: 1.30x faster                                                         |
| Geometric mean | (ref)                                                       | 1.23x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 222 ms: 1.96x faster                                                          |
| async_tree_memoization  | 526 ms                                                      | 268 ms: 1.96x faster                                                          |
| async_tree_io           | 1.11 sec                                                    | 588 ms: 1.88x faster                                                          |
| async_tree_cpu_io_mixed | 638 ms                                                      | 386 ms: 1.65x faster                                                          |
| Geometric mean          | (ref)                                                       | 1.86x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                         |
| nbody          | 71.3 ms                                                     | 59.0 ms: 1.21x faster                                                         |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 86.6 ms: 1.22x faster                                                         |
| regex_dna      | 136 ms                                                      | 116 ms: 1.17x faster                                                          |
| regex_v8       | 15.4 ms                                                     | 14.4 ms: 1.07x faster                                                         |
| regex_effbot   | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.53 ms: 1.66x faster                                                         |
| pickle_pure_python   | 270 us                                                      | 173 us: 1.56x faster                                                          |
| unpickle_pure_python | 183 us                                                      | 129 us: 1.42x faster                                                          |
| tomli_loads          | 1.67 sec                                                    | 1.21 sec: 1.38x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 36.6 ms: 1.22x faster                                                         |
| xml_etree_parse      | 96.8 ms                                                     | 90.3 ms: 1.07x faster                                                         |
| unpickle             | 9.09 us                                                     | 8.55 us: 1.06x faster                                                         |
| xml_etree_iterparse  | 65.0 ms                                                     | 61.3 ms: 1.06x faster                                                         |
| xml_etree_generate   | 55.5 ms                                                     | 53.1 ms: 1.05x faster                                                         |
| json_loads           | 14.0 us                                                     | 13.6 us: 1.03x faster                                                         |
| unpickle_list        | 2.71 us                                                     | 2.82 us: 1.04x slower                                                         |
| pickle               | 6.85 us                                                     | 7.29 us: 1.06x slower                                                         |
| pickle_dict          | 17.2 us                                                     | 18.5 us: 1.08x slower                                                         |
| pickle_list          | 2.75 us                                                     | 3.16 us: 1.15x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                         |
| python_startup_no_site | 15.5 ms                                                     | 19.7 ms: 1.27x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.64 ms: 1.60x faster                                                         |
| genshi_text    | 19.8 ms                                                     | 15.4 ms: 1.29x faster                                                         |
| genshi_xml     | 41.0 ms                                                     | 35.7 ms: 1.15x faster                                                         |
| Geometric mean | (ref)                                                       | 1.33x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 75.2 us: 4.47x faster                                                         |
| async_tree_none          | 435 ms                                                      | 222 ms: 1.96x faster                                                          |
| async_tree_memoization   | 526 ms                                                      | 268 ms: 1.96x faster                                                          |
| deltablue                | 4.19 ms                                                     | 2.15 ms: 1.95x faster                                                         |
| async_tree_io            | 1.11 sec                                                    | 588 ms: 1.88x faster                                                          |
| logging_silent           | 94.6 ns                                                     | 53.1 ns: 1.78x faster                                                         |
| pylint                   | 350 ms                                                      | 198 ms: 1.77x faster                                                          |
| richards_super           | 52.2 ms                                                     | 29.9 ms: 1.75x faster                                                         |
| generators               | 32.4 ms                                                     | 19.3 ms: 1.68x faster                                                         |
| json_dumps               | 9.16 ms                                                     | 5.53 ms: 1.66x faster                                                         |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 386 ms: 1.65x faster                                                          |
| raytrace                 | 273 ms                                                      | 167 ms: 1.64x faster                                                          |
| richards                 | 42.4 ms                                                     | 26.5 ms: 1.60x faster                                                         |
| mako                     | 9.03 ms                                                     | 5.64 ms: 1.60x faster                                                         |
| sqlglot_parse            | 1.22 ms                                                     | 774 us: 1.57x faster                                                          |
| pickle_pure_python       | 270 us                                                      | 173 us: 1.56x faster                                                          |
| go                       | 139 ms                                                      | 89.9 ms: 1.55x faster                                                         |
| chaos                    | 61.7 ms                                                     | 40.0 ms: 1.54x faster                                                         |
| asyncio_tcp              | 732 ms                                                      | 481 ms: 1.52x faster                                                          |
| pyflate                  | 409 ms                                                      | 270 ms: 1.52x faster                                                          |
| spectral_norm            | 77.3 ms                                                     | 51.9 ms: 1.49x faster                                                         |
| sqlglot_transpile        | 1.48 ms                                                     | 997 us: 1.48x faster                                                          |
| comprehensions           | 16.5 us                                                     | 11.3 us: 1.46x faster                                                         |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.7 ms: 1.44x faster                                                         |
| html5lib                 | 51.0 ms                                                     | 35.6 ms: 1.43x faster                                                         |
| unpickle_pure_python     | 183 us                                                      | 129 us: 1.42x faster                                                          |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.49 sec: 1.42x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 44.5 ms: 1.40x faster                                                         |
| tomli_loads              | 1.67 sec                                                    | 1.21 sec: 1.38x faster                                                        |
| pycparser                | 930 ms                                                      | 677 ms: 1.37x faster                                                          |
| float                    | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                         |
| deepcopy_memo            | 28.8 us                                                     | 21.9 us: 1.31x faster                                                         |
| scimark_sor              | 106 ms                                                      | 80.9 ms: 1.31x faster                                                         |
| tornado_http             | 108 ms                                                      | 83.6 ms: 1.30x faster                                                         |
| genshi_text              | 19.8 ms                                                     | 15.4 ms: 1.29x faster                                                         |
| pprint_pformat           | 1.22 sec                                                    | 952 ms: 1.28x faster                                                          |
| pprint_safe_repr         | 592 ms                                                      | 471 ms: 1.26x faster                                                          |
| coroutines               | 16.0 ms                                                     | 12.9 ms: 1.24x faster                                                         |
| regex_compile            | 106 ms                                                      | 86.6 ms: 1.22x faster                                                         |
| dulwich_log              | 50.5 ms                                                     | 41.2 ms: 1.22x faster                                                         |
| sqlite_synth             | 1.91 us                                                     | 1.56 us: 1.22x faster                                                         |
| xml_etree_process        | 44.5 ms                                                     | 36.6 ms: 1.22x faster                                                         |
| scimark_lu               | 85.8 ms                                                     | 70.7 ms: 1.21x faster                                                         |
| nbody                    | 71.3 ms                                                     | 59.0 ms: 1.21x faster                                                         |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.26 ms: 1.21x faster                                                         |
| chameleon                | 5.79 ms                                                     | 4.81 ms: 1.20x faster                                                         |
| hexiom                   | 5.74 ms                                                     | 4.81 ms: 1.19x faster                                                         |
| bench_thread_pool        | 958 us                                                      | 803 us: 1.19x faster                                                          |
| mypy2                    | 555 ms                                                      | 467 ms: 1.19x faster                                                          |
| sympy_sum                | 107 ms                                                      | 90.9 ms: 1.18x faster                                                         |
| regex_dna                | 136 ms                                                      | 116 ms: 1.17x faster                                                          |
| mdp                      | 1.78 sec                                                    | 1.53 sec: 1.16x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 35.7 ms: 1.15x faster                                                         |
| sympy_str                | 194 ms                                                      | 172 ms: 1.13x faster                                                          |
| scimark_fft              | 187 ms                                                      | 167 ms: 1.12x faster                                                          |
| deepcopy_reduce          | 2.20 us                                                     | 1.97 us: 1.12x faster                                                         |
| deepcopy                 | 255 us                                                      | 229 us: 1.12x faster                                                          |
| docutils                 | 1.92 sec                                                    | 1.72 sec: 1.12x faster                                                        |
| fannkuch                 | 256 ms                                                      | 230 ms: 1.11x faster                                                          |
| sympy_integrate          | 15.3 ms                                                     | 13.8 ms: 1.11x faster                                                         |
| 2to3                     | 246 ms                                                      | 222 ms: 1.11x faster                                                          |
| sqlglot_normalize        | 205 ms                                                      | 186 ms: 1.11x faster                                                          |
| sqlglot_optimize         | 39.8 ms                                                     | 36.0 ms: 1.10x faster                                                         |
| aiohttp                  | 995 us                                                      | 911 us: 1.09x faster                                                          |
| json                     | 3.14 ms                                                     | 2.89 ms: 1.09x faster                                                         |
| logging_format           | 6.76 us                                                     | 6.27 us: 1.08x faster                                                         |
| sympy_expand             | 314 ms                                                      | 293 ms: 1.07x faster                                                          |
| xml_etree_parse          | 96.8 ms                                                     | 90.3 ms: 1.07x faster                                                         |
| regex_v8                 | 15.4 ms                                                     | 14.4 ms: 1.07x faster                                                         |
| regex_effbot             | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                         |
| unpickle                 | 9.09 us                                                     | 8.55 us: 1.06x faster                                                         |
| logging_simple           | 6.22 us                                                     | 5.86 us: 1.06x faster                                                         |
| xml_etree_iterparse      | 65.0 ms                                                     | 61.3 ms: 1.06x faster                                                         |
| nqueens                  | 66.6 ms                                                     | 63.3 ms: 1.05x faster                                                         |
| xml_etree_generate       | 55.5 ms                                                     | 53.1 ms: 1.05x faster                                                         |
| json_loads               | 14.0 us                                                     | 13.6 us: 1.03x faster                                                         |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                          |
| pathlib                  | 75.7 ms                                                     | 77.9 ms: 1.03x slower                                                         |
| unpickle_list            | 2.71 us                                                     | 2.82 us: 1.04x slower                                                         |
| python_startup           | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                         |
| pickle                   | 6.85 us                                                     | 7.29 us: 1.06x slower                                                         |
| pickle_dict              | 17.2 us                                                     | 18.5 us: 1.08x slower                                                         |
| bench_mp_pool            | 62.0 ms                                                     | 67.7 ms: 1.09x slower                                                         |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                         |
| async_generators         | 222 ms                                                      | 243 ms: 1.10x slower                                                          |
| create_gc_cycles         | 800 us                                                      | 891 us: 1.11x slower                                                          |
| pickle_list              | 2.75 us                                                     | 3.16 us: 1.15x slower                                                         |
| telco                    | 3.94 ms                                                     | 4.76 ms: 1.21x slower                                                         |
| coverage                 | 39.0 ms                                                     | 47.5 ms: 1.22x slower                                                         |
| python_startup_no_site   | 15.5 ms                                                     | 19.7 ms: 1.27x slower                                                         |
| thrift                   | 617 us                                                      | 9.17 ms: 14.85x slower                                                        |
| Geometric mean           | (ref)                                                       | 1.21x faster                                                                  |

Benchmark hidden because not significant (1): meteor_contest
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown