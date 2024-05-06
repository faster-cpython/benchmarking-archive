# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-amd64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 219 ms: 1.12x faster                                                     |
| chameleon      | 5.79 ms                                                     | 4.70 ms: 1.23x faster                                                    |
| docutils       | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                   |
| html5lib       | 51.0 ms                                                     | 35.7 ms: 1.43x faster                                                    |
| tornado_http   | 108 ms                                                      | 84.2 ms: 1.29x faster                                                    |
| Geometric mean | (ref)                                                       | 1.24x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 222 ms: 1.96x faster                                                     |
| async_tree_memoization  | 526 ms                                                      | 274 ms: 1.92x faster                                                     |
| async_tree_io           | 1.11 sec                                                    | 588 ms: 1.89x faster                                                     |
| async_tree_cpu_io_mixed | 638 ms                                                      | 393 ms: 1.62x faster                                                     |
| Geometric mean          | (ref)                                                       | 1.84x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.5 ms: 1.33x faster                                                    |
| nbody          | 71.3 ms                                                     | 56.9 ms: 1.25x faster                                                    |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                       | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 87.0 ms: 1.22x faster                                                    |
| regex_dna      | 136 ms                                                      | 118 ms: 1.15x faster                                                     |
| regex_v8       | 15.4 ms                                                     | 14.1 ms: 1.10x faster                                                    |
| regex_effbot   | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                       | 1.13x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                    |
| pickle_pure_python   | 270 us                                                      | 174 us: 1.55x faster                                                     |
| tomli_loads          | 1.67 sec                                                    | 1.18 sec: 1.42x faster                                                   |
| unpickle_pure_python | 183 us                                                      | 129 us: 1.42x faster                                                     |
| xml_etree_process    | 44.5 ms                                                     | 36.5 ms: 1.22x faster                                                    |
| xml_etree_generate   | 55.5 ms                                                     | 52.8 ms: 1.05x faster                                                    |
| xml_etree_parse      | 96.8 ms                                                     | 92.9 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 65.0 ms                                                     | 62.6 ms: 1.04x faster                                                    |
| unpickle_list        | 2.71 us                                                     | 2.74 us: 1.01x slower                                                    |
| pickle               | 6.85 us                                                     | 7.16 us: 1.05x slower                                                    |
| pickle_list          | 2.75 us                                                     | 2.93 us: 1.06x slower                                                    |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                             |

Benchmark hidden because not significant (2): json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.6 ms: 1.05x slower                                                    |
| python_startup_no_site | 15.5 ms                                                     | 19.5 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.68 ms: 1.59x faster                                                    |
| genshi_text    | 19.8 ms                                                     | 15.3 ms: 1.29x faster                                                    |
| genshi_xml     | 41.0 ms                                                     | 33.2 ms: 1.24x faster                                                    |
| Geometric mean | (ref)                                                       | 1.36x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 70.7 us: 4.75x faster                                                    |
| async_tree_none          | 435 ms                                                      | 222 ms: 1.96x faster                                                     |
| deltablue                | 4.19 ms                                                     | 2.16 ms: 1.93x faster                                                    |
| async_tree_memoization   | 526 ms                                                      | 274 ms: 1.92x faster                                                     |
| async_tree_io            | 1.11 sec                                                    | 588 ms: 1.89x faster                                                     |
| pylint                   | 350 ms                                                      | 194 ms: 1.81x faster                                                     |
| logging_silent           | 94.6 ns                                                     | 52.9 ns: 1.79x faster                                                    |
| raytrace                 | 273 ms                                                      | 161 ms: 1.69x faster                                                     |
| richards_super           | 52.2 ms                                                     | 31.1 ms: 1.68x faster                                                    |
| json_dumps               | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                    |
| generators               | 32.4 ms                                                     | 19.8 ms: 1.63x faster                                                    |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 393 ms: 1.62x faster                                                     |
| chaos                    | 61.7 ms                                                     | 38.3 ms: 1.61x faster                                                    |
| mako                     | 9.03 ms                                                     | 5.68 ms: 1.59x faster                                                    |
| asyncio_tcp              | 732 ms                                                      | 470 ms: 1.56x faster                                                     |
| sqlglot_parse            | 1.22 ms                                                     | 781 us: 1.56x faster                                                     |
| pickle_pure_python       | 270 us                                                      | 174 us: 1.55x faster                                                     |
| richards                 | 42.4 ms                                                     | 27.7 ms: 1.53x faster                                                    |
| go                       | 139 ms                                                      | 92.1 ms: 1.51x faster                                                    |
| pyflate                  | 409 ms                                                      | 272 ms: 1.51x faster                                                     |
| spectral_norm            | 77.3 ms                                                     | 51.4 ms: 1.50x faster                                                    |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.2 ms: 1.50x faster                                                    |
| comprehensions           | 16.5 us                                                     | 11.0 us: 1.49x faster                                                    |
| sqlglot_transpile        | 1.48 ms                                                     | 998 us: 1.48x faster                                                     |
| html5lib                 | 51.0 ms                                                     | 35.7 ms: 1.43x faster                                                    |
| tomli_loads              | 1.67 sec                                                    | 1.18 sec: 1.42x faster                                                   |
| crypto_pyaes             | 62.5 ms                                                     | 44.1 ms: 1.42x faster                                                    |
| unpickle_pure_python     | 183 us                                                      | 129 us: 1.42x faster                                                     |
| deepcopy_memo            | 28.8 us                                                     | 21.0 us: 1.37x faster                                                    |
| pycparser                | 930 ms                                                      | 694 ms: 1.34x faster                                                     |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.58 sec: 1.34x faster                                                   |
| float                    | 61.7 ms                                                     | 46.5 ms: 1.33x faster                                                    |
| hexiom                   | 5.74 ms                                                     | 4.42 ms: 1.30x faster                                                    |
| genshi_text              | 19.8 ms                                                     | 15.3 ms: 1.29x faster                                                    |
| tornado_http             | 108 ms                                                      | 84.2 ms: 1.29x faster                                                    |
| scimark_sor              | 106 ms                                                      | 82.8 ms: 1.28x faster                                                    |
| pprint_pformat           | 1.22 sec                                                    | 958 ms: 1.27x faster                                                     |
| nbody                    | 71.3 ms                                                     | 56.9 ms: 1.25x faster                                                    |
| genshi_xml               | 41.0 ms                                                     | 33.2 ms: 1.24x faster                                                    |
| pprint_safe_repr         | 592 ms                                                      | 479 ms: 1.24x faster                                                     |
| mypy2                    | 555 ms                                                      | 449 ms: 1.24x faster                                                     |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                    |
| chameleon                | 5.79 ms                                                     | 4.70 ms: 1.23x faster                                                    |
| dulwich_log              | 50.5 ms                                                     | 41.0 ms: 1.23x faster                                                    |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.23 ms: 1.22x faster                                                    |
| regex_compile            | 106 ms                                                      | 87.0 ms: 1.22x faster                                                    |
| xml_etree_process        | 44.5 ms                                                     | 36.5 ms: 1.22x faster                                                    |
| sqlite_synth             | 1.91 us                                                     | 1.57 us: 1.22x faster                                                    |
| mdp                      | 1.78 sec                                                    | 1.46 sec: 1.22x faster                                                   |
| scimark_lu               | 85.8 ms                                                     | 71.4 ms: 1.20x faster                                                    |
| sympy_sum                | 107 ms                                                      | 89.2 ms: 1.20x faster                                                    |
| bench_thread_pool        | 958 us                                                      | 806 us: 1.19x faster                                                     |
| sympy_str                | 194 ms                                                      | 167 ms: 1.17x faster                                                     |
| deepcopy                 | 255 us                                                      | 220 us: 1.16x faster                                                     |
| regex_dna                | 136 ms                                                      | 118 ms: 1.15x faster                                                     |
| sympy_integrate          | 15.3 ms                                                     | 13.3 ms: 1.15x faster                                                    |
| sqlglot_optimize         | 39.8 ms                                                     | 34.8 ms: 1.14x faster                                                    |
| docutils                 | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                   |
| sqlglot_normalize        | 205 ms                                                      | 180 ms: 1.14x faster                                                     |
| 2to3                     | 246 ms                                                      | 219 ms: 1.12x faster                                                     |
| fannkuch                 | 256 ms                                                      | 228 ms: 1.12x faster                                                     |
| scimark_fft              | 187 ms                                                      | 167 ms: 1.12x faster                                                     |
| deepcopy_reduce          | 2.20 us                                                     | 1.98 us: 1.12x faster                                                    |
| sympy_expand             | 314 ms                                                      | 283 ms: 1.11x faster                                                     |
| nqueens                  | 66.6 ms                                                     | 60.1 ms: 1.11x faster                                                    |
| logging_format           | 6.76 us                                                     | 6.15 us: 1.10x faster                                                    |
| regex_v8                 | 15.4 ms                                                     | 14.1 ms: 1.10x faster                                                    |
| json                     | 3.14 ms                                                     | 2.87 ms: 1.09x faster                                                    |
| aiohttp                  | 995 us                                                      | 911 us: 1.09x faster                                                     |
| logging_simple           | 6.22 us                                                     | 5.70 us: 1.09x faster                                                    |
| regex_effbot             | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                    |
| meteor_contest           | 75.9 ms                                                     | 72.1 ms: 1.05x faster                                                    |
| xml_etree_generate       | 55.5 ms                                                     | 52.8 ms: 1.05x faster                                                    |
| xml_etree_parse          | 96.8 ms                                                     | 92.9 ms: 1.04x faster                                                    |
| xml_etree_iterparse      | 65.0 ms                                                     | 62.6 ms: 1.04x faster                                                    |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                     |
| unpickle_list            | 2.71 us                                                     | 2.74 us: 1.01x slower                                                    |
| pathlib                  | 75.7 ms                                                     | 78.0 ms: 1.03x slower                                                    |
| pickle                   | 6.85 us                                                     | 7.16 us: 1.05x slower                                                    |
| python_startup           | 20.6 ms                                                     | 21.6 ms: 1.05x slower                                                    |
| async_generators         | 222 ms                                                      | 233 ms: 1.05x slower                                                     |
| pickle_list              | 2.75 us                                                     | 2.93 us: 1.06x slower                                                    |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                    |
| bench_mp_pool            | 62.0 ms                                                     | 67.7 ms: 1.09x slower                                                    |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                    |
| create_gc_cycles         | 800 us                                                      | 898 us: 1.12x slower                                                     |
| telco                    | 3.94 ms                                                     | 4.75 ms: 1.21x slower                                                    |
| coverage                 | 39.0 ms                                                     | 47.5 ms: 1.22x slower                                                    |
| python_startup_no_site   | 15.5 ms                                                     | 19.5 ms: 1.26x slower                                                    |
| thrift                   | 617 us                                                      | 8.79 ms: 14.24x slower                                                   |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                             |

Benchmark hidden because not significant (2): json_loads, unpickle
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown