# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-x86
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 242 ms: 1.10x faster                                                          |
| chameleon      | 6.42 ms                                                         | 5.89 ms: 1.09x faster                                                         |
| docutils       | 1.95 sec                                                        | 1.84 sec: 1.06x faster                                                        |
| html5lib       | 52.1 ms                                                         | 44.1 ms: 1.18x faster                                                         |
| tornado_http   | 118 ms                                                          | 95.7 ms: 1.23x faster                                                         |
| Geometric mean | (ref)                                                           | 1.13x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 459 ms: 2.01x faster                                                          |
| async_tree_io           | 940 ms                                                          | 523 ms: 1.80x faster                                                          |
| async_tree_none         | 394 ms                                                          | 219 ms: 1.80x faster                                                          |
| async_tree_memoization  | 467 ms                                                          | 271 ms: 1.72x faster                                                          |
| Geometric mean          | (ref)                                                           | 1.83x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 196 ms: 2.56x faster                                                          |
| float          | 69.6 ms                                                         | 43.4 ms: 1.60x faster                                                         |
| nbody          | 79.1 ms                                                         | 53.7 ms: 1.47x faster                                                         |
| Geometric mean | (ref)                                                           | 1.82x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 98.7 ms: 1.18x faster                                                         |
| regex_dna      | 131 ms                                                          | 118 ms: 1.10x faster                                                          |
| regex_v8       | 15.8 ms                                                         | 16.0 ms: 1.01x slower                                                         |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                         |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.72 ms: 1.46x faster                                                         |
| unpickle_pure_python | 189 us                                                          | 139 us: 1.36x faster                                                          |
| tomli_loads          | 1.91 sec                                                        | 1.45 sec: 1.32x faster                                                        |
| pickle_pure_python   | 280 us                                                          | 218 us: 1.29x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 41.7 ms: 1.15x faster                                                         |
| xml_etree_iterparse  | 70.8 ms                                                         | 62.1 ms: 1.14x faster                                                         |
| xml_etree_parse      | 120 ms                                                          | 107 ms: 1.12x faster                                                          |
| json_loads           | 22.4 us                                                         | 20.4 us: 1.10x faster                                                         |
| xml_etree_generate   | 61.6 ms                                                         | 58.4 ms: 1.06x faster                                                         |
| pickle               | 7.83 us                                                         | 7.67 us: 1.02x faster                                                         |
| pickle_dict          | 18.2 us                                                         | 19.7 us: 1.08x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                  |

Benchmark hidden because not significant (3): unpickle_list, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.3 ms: 1.06x slower                                                         |
| python_startup_no_site | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 5.42 ms: 1.68x faster                                                         |
| django_template | 36.0 ms                                                         | 31.3 ms: 1.15x faster                                                         |
| genshi_text     | 21.0 ms                                                         | 20.1 ms: 1.05x faster                                                         |
| genshi_xml      | 46.6 ms                                                         | 45.6 ms: 1.02x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.20x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 90.3 us: 4.38x faster                                                         |
| pidigits                 | 502 ms                                                          | 196 ms: 2.56x faster                                                          |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 459 ms: 2.01x faster                                                          |
| async_tree_io            | 940 ms                                                          | 523 ms: 1.80x faster                                                          |
| async_tree_none          | 394 ms                                                          | 219 ms: 1.80x faster                                                          |
| pylint                   | 384 ms                                                          | 215 ms: 1.79x faster                                                          |
| async_tree_memoization   | 467 ms                                                          | 271 ms: 1.72x faster                                                          |
| crypto_pyaes             | 81.3 ms                                                         | 47.7 ms: 1.71x faster                                                         |
| deltablue                | 4.04 ms                                                         | 2.38 ms: 1.69x faster                                                         |
| mako                     | 9.10 ms                                                         | 5.42 ms: 1.68x faster                                                         |
| logging_silent           | 97.9 ns                                                         | 59.4 ns: 1.65x faster                                                         |
| float                    | 69.6 ms                                                         | 43.4 ms: 1.60x faster                                                         |
| spectral_norm            | 80.2 ms                                                         | 50.4 ms: 1.59x faster                                                         |
| comprehensions           | 17.7 us                                                         | 11.2 us: 1.58x faster                                                         |
| scimark_monte_carlo      | 61.9 ms                                                         | 39.8 ms: 1.55x faster                                                         |
| pyflate                  | 422 ms                                                          | 280 ms: 1.50x faster                                                          |
| nbody                    | 79.1 ms                                                         | 53.7 ms: 1.47x faster                                                         |
| json_dumps               | 9.82 ms                                                         | 6.72 ms: 1.46x faster                                                         |
| sqlglot_parse            | 1.33 ms                                                         | 923 us: 1.44x faster                                                          |
| fannkuch                 | 317 ms                                                          | 223 ms: 1.42x faster                                                          |
| chaos                    | 74.4 ms                                                         | 53.1 ms: 1.40x faster                                                         |
| raytrace                 | 303 ms                                                          | 220 ms: 1.38x faster                                                          |
| generators               | 31.6 ms                                                         | 23.1 ms: 1.36x faster                                                         |
| unpickle_pure_python     | 189 us                                                          | 139 us: 1.36x faster                                                          |
| sqlglot_transpile        | 1.58 ms                                                         | 1.17 ms: 1.36x faster                                                         |
| scimark_sor              | 115 ms                                                          | 85.6 ms: 1.34x faster                                                         |
| hexiom                   | 6.13 ms                                                         | 4.61 ms: 1.33x faster                                                         |
| go                       | 146 ms                                                          | 110 ms: 1.33x faster                                                          |
| richards_super           | 49.9 ms                                                         | 37.8 ms: 1.32x faster                                                         |
| tomli_loads              | 1.91 sec                                                        | 1.45 sec: 1.32x faster                                                        |
| pycparser                | 1.04 sec                                                        | 799 ms: 1.30x faster                                                          |
| pickle_pure_python       | 280 us                                                          | 218 us: 1.29x faster                                                          |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 2.54 ms: 1.28x faster                                                         |
| scimark_fft              | 216 ms                                                          | 171 ms: 1.26x faster                                                          |
| tornado_http             | 118 ms                                                          | 95.7 ms: 1.23x faster                                                         |
| sqlite_synth             | 2.29 us                                                         | 1.87 us: 1.22x faster                                                         |
| coroutines               | 17.9 ms                                                         | 14.7 ms: 1.22x faster                                                         |
| nqueens                  | 87.1 ms                                                         | 71.7 ms: 1.21x faster                                                         |
| deepcopy_memo            | 29.6 us                                                         | 24.5 us: 1.21x faster                                                         |
| asyncio_tcp              | 744 ms                                                          | 619 ms: 1.20x faster                                                          |
| scimark_lu               | 89.8 ms                                                         | 75.2 ms: 1.19x faster                                                         |
| richards                 | 40.3 ms                                                         | 34.0 ms: 1.18x faster                                                         |
| pprint_pformat           | 1.37 sec                                                        | 1.16 sec: 1.18x faster                                                        |
| regex_compile            | 117 ms                                                          | 98.7 ms: 1.18x faster                                                         |
| html5lib                 | 52.1 ms                                                         | 44.1 ms: 1.18x faster                                                         |
| sympy_sum                | 122 ms                                                          | 104 ms: 1.17x faster                                                          |
| pprint_safe_repr         | 658 ms                                                          | 569 ms: 1.16x faster                                                          |
| xml_etree_process        | 48.1 ms                                                         | 41.7 ms: 1.15x faster                                                         |
| django_template          | 36.0 ms                                                         | 31.3 ms: 1.15x faster                                                         |
| xml_etree_iterparse      | 70.8 ms                                                         | 62.1 ms: 1.14x faster                                                         |
| bench_thread_pool        | 1.12 ms                                                         | 990 us: 1.13x faster                                                          |
| sympy_str                | 229 ms                                                          | 203 ms: 1.13x faster                                                          |
| mdp                      | 1.83 sec                                                        | 1.62 sec: 1.13x faster                                                        |
| xml_etree_parse          | 120 ms                                                          | 107 ms: 1.12x faster                                                          |
| sympy_integrate          | 16.6 ms                                                         | 15.0 ms: 1.11x faster                                                         |
| regex_dna                | 131 ms                                                          | 118 ms: 1.10x faster                                                          |
| 2to3                     | 265 ms                                                          | 242 ms: 1.10x faster                                                          |
| json_loads               | 22.4 us                                                         | 20.4 us: 1.10x faster                                                         |
| json                     | 4.76 ms                                                         | 4.37 ms: 1.09x faster                                                         |
| chameleon                | 6.42 ms                                                         | 5.89 ms: 1.09x faster                                                         |
| sympy_expand             | 391 ms                                                          | 359 ms: 1.09x faster                                                          |
| meteor_contest           | 80.0 ms                                                         | 73.8 ms: 1.08x faster                                                         |
| deepcopy                 | 310 us                                                          | 288 us: 1.07x faster                                                          |
| sqlglot_optimize         | 44.7 ms                                                         | 41.6 ms: 1.07x faster                                                         |
| sqlglot_normalize        | 230 ms                                                          | 215 ms: 1.07x faster                                                          |
| deepcopy_reduce          | 2.68 us                                                         | 2.54 us: 1.06x faster                                                         |
| docutils                 | 1.95 sec                                                        | 1.84 sec: 1.06x faster                                                        |
| xml_etree_generate       | 61.6 ms                                                         | 58.4 ms: 1.06x faster                                                         |
| genshi_text              | 21.0 ms                                                         | 20.1 ms: 1.05x faster                                                         |
| genshi_xml               | 46.6 ms                                                         | 45.6 ms: 1.02x faster                                                         |
| pickle                   | 7.83 us                                                         | 7.67 us: 1.02x faster                                                         |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                        |
| regex_v8                 | 15.8 ms                                                         | 16.0 ms: 1.01x slower                                                         |
| pathlib                  | 81.2 ms                                                         | 85.8 ms: 1.06x slower                                                         |
| create_gc_cycles         | 694 us                                                          | 734 us: 1.06x slower                                                          |
| python_startup           | 22.9 ms                                                         | 24.3 ms: 1.06x slower                                                         |
| logging_format           | 7.91 us                                                         | 8.43 us: 1.07x slower                                                         |
| logging_simple           | 7.29 us                                                         | 7.81 us: 1.07x slower                                                         |
| bench_mp_pool            | 66.4 ms                                                         | 71.7 ms: 1.08x slower                                                         |
| pickle_dict              | 18.2 us                                                         | 19.7 us: 1.08x slower                                                         |
| gc_traversal             | 1.28 ms                                                         | 1.45 ms: 1.13x slower                                                         |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                         |
| async_generators         | 241 ms                                                          | 283 ms: 1.17x slower                                                          |
| python_startup_no_site   | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                         |
| telco                    | 4.83 ms                                                         | 5.87 ms: 1.21x slower                                                         |
| unpack_sequence          | 40.0 ns                                                         | 70.2 ns: 1.75x slower                                                         |
| coverage                 | 46.6 ms                                                         | 486 ms: 10.43x slower                                                         |
| thrift                   | 902 us                                                          | 10.6 ms: 11.78x slower                                                        |
| Geometric mean           | (ref)                                                           | 1.15x faster                                                                  |

Benchmark hidden because not significant (3): unpickle_list, pickle_list, unpickle
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: unknown