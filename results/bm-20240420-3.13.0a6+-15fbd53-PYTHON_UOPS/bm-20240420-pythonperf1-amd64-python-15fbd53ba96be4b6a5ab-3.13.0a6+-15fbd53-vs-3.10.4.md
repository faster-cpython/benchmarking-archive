# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.13x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 224 ms: 1.10x faster                                                        |
| chameleon      | 5.79 ms                                                     | 5.02 ms: 1.15x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.74 sec: 1.10x faster                                                      |
| html5lib       | 51.0 ms                                                     | 40.5 ms: 1.26x faster                                                       |
| tornado_http   | 108 ms                                                      | 84.1 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 276 ms: 1.91x faster                                                        |
| async_tree_none         | 435 ms                                                      | 228 ms: 1.91x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 594 ms: 1.86x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 395 ms: 1.61x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.82x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 57.9 ms: 1.06x faster                                                       |
| pidigits       | 149 ms                                                      | 148 ms: 1.01x faster                                                        |
| nbody          | 71.3 ms                                                     | 83.1 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| regex_compile  | 106 ms                                                      | 103 ms: 1.03x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 15.2 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.70 ms: 1.61x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 185 us: 1.46x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 38.7 ms: 1.15x faster                                                       |
| tomli_loads          | 1.67 sec                                                    | 1.46 sec: 1.14x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 166 us: 1.11x faster                                                        |
| xml_etree_parse      | 96.8 ms                                                     | 90.0 ms: 1.08x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.54 us: 1.06x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 56.5 ms: 1.02x slower                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.86 us: 1.05x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| pickle               | 6.85 us                                                     | 7.53 us: 1.10x slower                                                       |
| pickle_list          | 2.75 us                                                     | 3.06 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.9 ms: 1.04x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 28.9 ms                                                     | 23.3 ms: 1.24x faster                                                       |
| mako            | 9.03 ms                                                     | 7.41 ms: 1.22x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 16.4 ms: 1.21x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 35.8 ms: 1.15x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.20x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 75.7 us: 4.44x faster                                                       |
| async_tree_memoization   | 526 ms                                                      | 276 ms: 1.91x faster                                                        |
| async_tree_none          | 435 ms                                                      | 228 ms: 1.91x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 594 ms: 1.86x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.49 ms: 1.68x faster                                                       |
| logging_silent           | 94.6 ns                                                     | 57.1 ns: 1.66x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 395 ms: 1.61x faster                                                        |
| richards_super           | 52.2 ms                                                     | 32.4 ms: 1.61x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.70 ms: 1.61x faster                                                       |
| pylint                   | 350 ms                                                      | 219 ms: 1.60x faster                                                        |
| generators               | 32.4 ms                                                     | 20.7 ms: 1.57x faster                                                       |
| raytrace                 | 273 ms                                                      | 176 ms: 1.55x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 477 ms: 1.53x faster                                                        |
| richards                 | 42.4 ms                                                     | 28.6 ms: 1.49x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 827 us: 1.47x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 185 us: 1.46x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.49 sec: 1.41x faster                                                      |
| sqlglot_transpile        | 1.48 ms                                                     | 1.04 ms: 1.41x faster                                                       |
| chaos                    | 61.7 ms                                                     | 44.6 ms: 1.38x faster                                                       |
| go                       | 139 ms                                                      | 102 ms: 1.37x faster                                                        |
| tornado_http             | 108 ms                                                      | 84.1 ms: 1.29x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 40.5 ms: 1.26x faster                                                       |
| pycparser                | 930 ms                                                      | 747 ms: 1.25x faster                                                        |
| django_template          | 28.9 ms                                                     | 23.3 ms: 1.24x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 50.5 ms: 1.24x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                       |
| mako                     | 9.03 ms                                                     | 7.41 ms: 1.22x faster                                                       |
| mypy2                    | 555 ms                                                      | 457 ms: 1.22x faster                                                        |
| pyflate                  | 409 ms                                                      | 336 ms: 1.22x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 16.4 ms: 1.21x faster                                                       |
| comprehensions           | 16.5 us                                                     | 13.8 us: 1.20x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.49 sec: 1.20x faster                                                      |
| sqlite_synth             | 1.91 us                                                     | 1.62 us: 1.18x faster                                                       |
| scimark_sor              | 106 ms                                                      | 91.1 ms: 1.17x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 43.4 ms: 1.16x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 24.8 us: 1.16x faster                                                       |
| chameleon                | 5.79 ms                                                     | 5.02 ms: 1.15x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 38.7 ms: 1.15x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 835 us: 1.15x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 35.8 ms: 1.15x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.46 sec: 1.14x faster                                                      |
| sympy_sum                | 107 ms                                                      | 94.7 ms: 1.13x faster                                                       |
| regex_dna                | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| deepcopy                 | 255 us                                                      | 229 us: 1.12x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 51.6 ms: 1.11x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 166 us: 1.11x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.8 ms: 1.10x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 1.11 sec: 1.10x faster                                                      |
| docutils                 | 1.92 sec                                                    | 1.74 sec: 1.10x faster                                                      |
| 2to3                     | 246 ms                                                      | 224 ms: 1.10x faster                                                        |
| hexiom                   | 5.74 ms                                                     | 5.24 ms: 1.10x faster                                                       |
| aiohttp                  | 995 us                                                      | 907 us: 1.10x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 187 ms: 1.10x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 78.3 ms: 1.10x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 542 ms: 1.09x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 36.6 ms: 1.09x faster                                                       |
| deepcopy_reduce          | 2.20 us                                                     | 2.04 us: 1.08x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 90.0 ms: 1.08x faster                                                       |
| sympy_str                | 194 ms                                                      | 181 ms: 1.07x faster                                                        |
| float                    | 61.7 ms                                                     | 57.9 ms: 1.06x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.54 us: 1.06x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.45 us: 1.05x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| python_startup           | 20.6 ms                                                     | 19.9 ms: 1.04x faster                                                       |
| sympy_expand             | 314 ms                                                      | 304 ms: 1.03x faster                                                        |
| regex_compile            | 106 ms                                                      | 103 ms: 1.03x faster                                                        |
| logging_simple           | 6.22 us                                                     | 6.06 us: 1.03x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 15.2 ms: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 148 ms: 1.01x faster                                                        |
| meteor_contest           | 75.9 ms                                                     | 76.4 ms: 1.01x slower                                                       |
| pathlib                  | 75.7 ms                                                     | 76.5 ms: 1.01x slower                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 56.5 ms: 1.02x slower                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| nqueens                  | 66.6 ms                                                     | 68.6 ms: 1.03x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 65.2 ms: 1.05x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.86 us: 1.05x slower                                                       |
| spectral_norm            | 77.3 ms                                                     | 81.7 ms: 1.06x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| async_generators         | 222 ms                                                      | 243 ms: 1.10x slower                                                        |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.53 us: 1.10x slower                                                       |
| scimark_fft              | 187 ms                                                      | 208 ms: 1.11x slower                                                        |
| fannkuch                 | 256 ms                                                      | 285 ms: 1.11x slower                                                        |
| pickle_list              | 2.75 us                                                     | 3.06 us: 1.11x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 900 us: 1.13x slower                                                        |
| nbody                    | 71.3 ms                                                     | 83.1 ms: 1.17x slower                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 3.30 ms: 1.21x slower                                                       |
| coverage                 | 39.0 ms                                                     | 49.1 ms: 1.26x slower                                                       |
| telco                    | 3.94 ms                                                     | 5.00 ms: 1.27x slower                                                       |
| thrift                   | 617 us                                                      | 9.18 ms: 14.87x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.13x faster                                                                |

Benchmark hidden because not significant (1): json
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: unknown