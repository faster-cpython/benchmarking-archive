# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-amd64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 220 ms: 1.12x faster                                                                  |
| chameleon      | 5.79 ms                                                     | 5.55 ms: 1.04x faster                                                                 |
| docutils       | 1.92 sec                                                    | 1.70 sec: 1.13x faster                                                                |
| html5lib       | 51.0 ms                                                     | 38.0 ms: 1.34x faster                                                                 |
| tornado_http   | 108 ms                                                      | 84.1 ms: 1.29x faster                                                                 |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_io           | 1.11 sec                                                    | 581 ms: 1.91x faster                                                                  |
| async_tree_none         | 435 ms                                                      | 232 ms: 1.87x faster                                                                  |
| async_tree_memoization  | 526 ms                                                      | 281 ms: 1.87x faster                                                                  |
| async_tree_cpu_io_mixed | 638 ms                                                      | 403 ms: 1.58x faster                                                                  |
| Geometric mean          | (ref)                                                       | 1.80x faster                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 53.0 ms: 1.16x faster                                                                 |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                                  |
| nbody          | 71.3 ms                                                     | 76.0 ms: 1.07x slower                                                                 |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 82.6 ms: 1.28x faster                                                                 |
| regex_dna      | 136 ms                                                      | 119 ms: 1.15x faster                                                                  |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                                 |
| regex_v8       | 15.4 ms                                                     | 18.0 ms: 1.16x slower                                                                 |
| Geometric mean | (ref)                                                       | 1.08x faster                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 6.07 ms: 1.51x faster                                                                 |
| unpickle_pure_python | 183 us                                                      | 139 us: 1.32x faster                                                                  |
| pickle_pure_python   | 270 us                                                      | 206 us: 1.31x faster                                                                  |
| tomli_loads          | 1.67 sec                                                    | 1.45 sec: 1.16x faster                                                                |
| unpickle             | 9.09 us                                                     | 8.48 us: 1.07x faster                                                                 |
| xml_etree_parse      | 96.8 ms                                                     | 90.9 ms: 1.07x faster                                                                 |
| xml_etree_process    | 44.5 ms                                                     | 41.7 ms: 1.07x faster                                                                 |
| json_loads           | 14.0 us                                                     | 13.9 us: 1.01x faster                                                                 |
| unpickle_list        | 2.71 us                                                     | 2.85 us: 1.05x slower                                                                 |
| xml_etree_generate   | 55.5 ms                                                     | 59.0 ms: 1.06x slower                                                                 |
| pickle               | 6.85 us                                                     | 7.35 us: 1.07x slower                                                                 |
| pickle_list          | 2.75 us                                                     | 3.00 us: 1.09x slower                                                                 |
| pickle_dict          | 17.2 us                                                     | 18.9 us: 1.10x slower                                                                 |
| Geometric mean       | (ref)                                                       | 1.07x faster                                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.1 ms: 1.02x faster                                                                 |
| python_startup_no_site | 15.5 ms                                                     | 17.9 ms: 1.15x slower                                                                 |
| Geometric mean         | (ref)                                                       | 1.06x slower                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 6.46 ms: 1.40x faster                                                                 |
| genshi_text    | 19.8 ms                                                     | 17.9 ms: 1.10x faster                                                                 |
| genshi_xml     | 41.0 ms                                                     | 37.7 ms: 1.09x faster                                                                 |
| Geometric mean | (ref)                                                       | 1.19x faster                                                                          |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 75.9 us: 4.43x faster                                                                 |
| deltablue                | 4.19 ms                                                     | 2.05 ms: 2.04x faster                                                                 |
| async_tree_io            | 1.11 sec                                                    | 581 ms: 1.91x faster                                                                  |
| async_tree_none          | 435 ms                                                      | 232 ms: 1.87x faster                                                                  |
| async_tree_memoization   | 526 ms                                                      | 281 ms: 1.87x faster                                                                  |
| pylint                   | 350 ms                                                      | 193 ms: 1.82x faster                                                                  |
| logging_silent           | 94.6 ns                                                     | 55.7 ns: 1.70x faster                                                                 |
| richards_super           | 52.2 ms                                                     | 30.9 ms: 1.69x faster                                                                 |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 403 ms: 1.58x faster                                                                  |
| go                       | 139 ms                                                      | 88.0 ms: 1.58x faster                                                                 |
| raytrace                 | 273 ms                                                      | 174 ms: 1.57x faster                                                                  |
| richards                 | 42.4 ms                                                     | 27.5 ms: 1.54x faster                                                                 |
| asyncio_tcp              | 732 ms                                                      | 476 ms: 1.54x faster                                                                  |
| json_dumps               | 9.16 ms                                                     | 6.07 ms: 1.51x faster                                                                 |
| sqlglot_parse            | 1.22 ms                                                     | 811 us: 1.50x faster                                                                  |
| chaos                    | 61.7 ms                                                     | 42.1 ms: 1.46x faster                                                                 |
| scimark_lu               | 85.8 ms                                                     | 59.6 ms: 1.44x faster                                                                 |
| sqlglot_transpile        | 1.48 ms                                                     | 1.03 ms: 1.43x faster                                                                 |
| hexiom                   | 5.74 ms                                                     | 4.07 ms: 1.41x faster                                                                 |
| mako                     | 9.03 ms                                                     | 6.46 ms: 1.40x faster                                                                 |
| generators               | 32.4 ms                                                     | 23.4 ms: 1.39x faster                                                                 |
| scimark_monte_carlo      | 57.3 ms                                                     | 41.9 ms: 1.37x faster                                                                 |
| pyflate                  | 409 ms                                                      | 299 ms: 1.37x faster                                                                  |
| comprehensions           | 16.5 us                                                     | 12.2 us: 1.35x faster                                                                 |
| html5lib                 | 51.0 ms                                                     | 38.0 ms: 1.34x faster                                                                 |
| scimark_sor              | 106 ms                                                      | 79.5 ms: 1.34x faster                                                                 |
| unpickle_pure_python     | 183 us                                                      | 139 us: 1.32x faster                                                                  |
| pickle_pure_python       | 270 us                                                      | 206 us: 1.31x faster                                                                  |
| tornado_http             | 108 ms                                                      | 84.1 ms: 1.29x faster                                                                 |
| regex_compile            | 106 ms                                                      | 82.6 ms: 1.28x faster                                                                 |
| mypy2                    | 555 ms                                                      | 435 ms: 1.28x faster                                                                  |
| crypto_pyaes             | 62.5 ms                                                     | 49.1 ms: 1.27x faster                                                                 |
| pycparser                | 930 ms                                                      | 742 ms: 1.25x faster                                                                  |
| deepcopy_memo            | 28.8 us                                                     | 22.9 us: 1.25x faster                                                                 |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.72 sec: 1.23x faster                                                                |
| spectral_norm            | 77.3 ms                                                     | 63.3 ms: 1.22x faster                                                                 |
| mdp                      | 1.78 sec                                                    | 1.47 sec: 1.21x faster                                                                |
| sympy_sum                | 107 ms                                                      | 88.8 ms: 1.20x faster                                                                 |
| dulwich_log              | 50.5 ms                                                     | 42.6 ms: 1.18x faster                                                                 |
| sympy_integrate          | 15.3 ms                                                     | 12.9 ms: 1.18x faster                                                                 |
| bench_thread_pool        | 958 us                                                      | 822 us: 1.17x faster                                                                  |
| float                    | 61.7 ms                                                     | 53.0 ms: 1.16x faster                                                                 |
| tomli_loads              | 1.67 sec                                                    | 1.45 sec: 1.16x faster                                                                |
| regex_dna                | 136 ms                                                      | 119 ms: 1.15x faster                                                                  |
| sympy_str                | 194 ms                                                      | 170 ms: 1.14x faster                                                                  |
| docutils                 | 1.92 sec                                                    | 1.70 sec: 1.13x faster                                                                |
| sqlite_synth             | 1.91 us                                                     | 1.71 us: 1.12x faster                                                                 |
| 2to3                     | 246 ms                                                      | 220 ms: 1.12x faster                                                                  |
| sqlglot_optimize         | 39.8 ms                                                     | 35.9 ms: 1.11x faster                                                                 |
| aiohttp                  | 995 us                                                      | 901 us: 1.10x faster                                                                  |
| genshi_text              | 19.8 ms                                                     | 17.9 ms: 1.10x faster                                                                 |
| pprint_pformat           | 1.22 sec                                                    | 1.11 sec: 1.10x faster                                                                |
| sympy_expand             | 314 ms                                                      | 287 ms: 1.10x faster                                                                  |
| genshi_xml               | 41.0 ms                                                     | 37.7 ms: 1.09x faster                                                                 |
| pprint_safe_repr         | 592 ms                                                      | 544 ms: 1.09x faster                                                                  |
| deepcopy                 | 255 us                                                      | 235 us: 1.09x faster                                                                  |
| sqlglot_normalize        | 205 ms                                                      | 191 ms: 1.07x faster                                                                  |
| unpickle                 | 9.09 us                                                     | 8.48 us: 1.07x faster                                                                 |
| xml_etree_parse          | 96.8 ms                                                     | 90.9 ms: 1.07x faster                                                                 |
| xml_etree_process        | 44.5 ms                                                     | 41.7 ms: 1.07x faster                                                                 |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                                 |
| coroutines               | 16.0 ms                                                     | 15.2 ms: 1.05x faster                                                                 |
| chameleon                | 5.79 ms                                                     | 5.55 ms: 1.04x faster                                                                 |
| json                     | 3.14 ms                                                     | 3.02 ms: 1.04x faster                                                                 |
| scimark_fft              | 187 ms                                                      | 183 ms: 1.03x faster                                                                  |
| python_startup           | 20.6 ms                                                     | 20.1 ms: 1.02x faster                                                                 |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.68 ms: 1.02x faster                                                                 |
| logging_format           | 6.76 us                                                     | 6.67 us: 1.01x faster                                                                 |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                                  |
| json_loads               | 14.0 us                                                     | 13.9 us: 1.01x faster                                                                 |
| deepcopy_reduce          | 2.20 us                                                     | 2.18 us: 1.01x faster                                                                 |
| nqueens                  | 66.6 ms                                                     | 66.3 ms: 1.01x faster                                                                 |
| meteor_contest           | 75.9 ms                                                     | 76.5 ms: 1.01x slower                                                                 |
| pathlib                  | 75.7 ms                                                     | 78.2 ms: 1.03x slower                                                                 |
| bench_mp_pool            | 62.0 ms                                                     | 64.5 ms: 1.04x slower                                                                 |
| unpickle_list            | 2.71 us                                                     | 2.85 us: 1.05x slower                                                                 |
| xml_etree_generate       | 55.5 ms                                                     | 59.0 ms: 1.06x slower                                                                 |
| nbody                    | 71.3 ms                                                     | 76.0 ms: 1.07x slower                                                                 |
| async_generators         | 222 ms                                                      | 238 ms: 1.07x slower                                                                  |
| pickle                   | 6.85 us                                                     | 7.35 us: 1.07x slower                                                                 |
| gc_traversal             | 1.41 ms                                                     | 1.53 ms: 1.09x slower                                                                 |
| pickle_list              | 2.75 us                                                     | 3.00 us: 1.09x slower                                                                 |
| pickle_dict              | 17.2 us                                                     | 18.9 us: 1.10x slower                                                                 |
| create_gc_cycles         | 800 us                                                      | 887 us: 1.11x slower                                                                  |
| python_startup_no_site   | 15.5 ms                                                     | 17.9 ms: 1.15x slower                                                                 |
| fannkuch                 | 256 ms                                                      | 297 ms: 1.16x slower                                                                  |
| regex_v8                 | 15.4 ms                                                     | 18.0 ms: 1.16x slower                                                                 |
| coverage                 | 39.0 ms                                                     | 47.7 ms: 1.22x slower                                                                 |
| telco                    | 3.94 ms                                                     | 5.40 ms: 1.37x slower                                                                 |
| thrift                   | 617 us                                                      | 8.77 ms: 14.21x slower                                                                |
| Geometric mean           | (ref)                                                       | 1.16x faster                                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, logging_simple
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: unknown