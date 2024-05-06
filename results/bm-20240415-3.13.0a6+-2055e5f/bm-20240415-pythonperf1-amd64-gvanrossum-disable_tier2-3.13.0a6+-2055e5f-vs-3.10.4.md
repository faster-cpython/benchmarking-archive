# Results vs. 3.10.4

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 211 ms: 1.16x faster                                                     |
| chameleon      | 5.79 ms                                                     | 4.87 ms: 1.19x faster                                                    |
| docutils       | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                   |
| html5lib       | 51.0 ms                                                     | 36.8 ms: 1.39x faster                                                    |
| tornado_http   | 108 ms                                                      | 82.6 ms: 1.31x faster                                                    |
| Geometric mean | (ref)                                                       | 1.24x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 229 ms: 1.90x faster                                                     |
| async_tree_memoization  | 526 ms                                                      | 278 ms: 1.89x faster                                                     |
| async_tree_io           | 1.11 sec                                                    | 606 ms: 1.83x faster                                                     |
| async_tree_cpu_io_mixed | 638 ms                                                      | 399 ms: 1.60x faster                                                     |
| Geometric mean          | (ref)                                                       | 1.80x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 53.0 ms: 1.16x faster                                                    |
| nbody          | 71.3 ms                                                     | 69.8 ms: 1.02x faster                                                    |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                       | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 80.8 ms: 1.31x faster                                                    |
| regex_dna      | 136 ms                                                      | 120 ms: 1.14x faster                                                     |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                       | 1.12x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.71 ms: 1.61x faster                                                    |
| pickle_pure_python   | 270 us                                                      | 183 us: 1.48x faster                                                     |
| unpickle_pure_python | 183 us                                                      | 133 us: 1.38x faster                                                     |
| tomli_loads          | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                   |
| xml_etree_process    | 44.5 ms                                                     | 38.5 ms: 1.16x faster                                                    |
| unpickle             | 9.09 us                                                     | 8.32 us: 1.09x faster                                                    |
| xml_etree_parse      | 96.8 ms                                                     | 92.3 ms: 1.05x faster                                                    |
| json_loads           | 14.0 us                                                     | 13.6 us: 1.03x faster                                                    |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.8 ms: 1.02x faster                                                    |
| xml_etree_generate   | 55.5 ms                                                     | 56.6 ms: 1.02x slower                                                    |
| pickle               | 6.85 us                                                     | 7.45 us: 1.09x slower                                                    |
| pickle_dict          | 17.2 us                                                     | 19.8 us: 1.15x slower                                                    |
| pickle_list          | 2.75 us                                                     | 3.18 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.09x faster                                                             |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.3 ms: 1.01x faster                                                    |
| python_startup_no_site | 15.5 ms                                                     | 16.8 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.36 ms: 1.42x faster                                                    |
| django_template | 28.9 ms                                                     | 23.3 ms: 1.24x faster                                                    |
| genshi_text     | 19.8 ms                                                     | 16.1 ms: 1.23x faster                                                    |
| genshi_xml      | 41.0 ms                                                     | 34.4 ms: 1.19x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.27x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|--------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 72.8 us: 4.61x faster                                                    |
| deltablue                | 4.19 ms                                                     | 2.05 ms: 2.04x faster                                                    |
| async_tree_none          | 435 ms                                                      | 229 ms: 1.90x faster                                                     |
| async_tree_memoization   | 526 ms                                                      | 278 ms: 1.89x faster                                                     |
| async_tree_io            | 1.11 sec                                                    | 606 ms: 1.83x faster                                                     |
| pylint                   | 350 ms                                                      | 209 ms: 1.68x faster                                                     |
| logging_silent           | 94.6 ns                                                     | 56.6 ns: 1.67x faster                                                    |
| raytrace                 | 273 ms                                                      | 168 ms: 1.63x faster                                                     |
| json_dumps               | 9.16 ms                                                     | 5.71 ms: 1.61x faster                                                    |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 399 ms: 1.60x faster                                                     |
| chaos                    | 61.7 ms                                                     | 38.8 ms: 1.59x faster                                                    |
| generators               | 32.4 ms                                                     | 20.8 ms: 1.56x faster                                                    |
| richards_super           | 52.2 ms                                                     | 33.7 ms: 1.55x faster                                                    |
| comprehensions           | 16.5 us                                                     | 10.7 us: 1.54x faster                                                    |
| sqlglot_parse            | 1.22 ms                                                     | 790 us: 1.54x faster                                                     |
| scimark_lu               | 85.8 ms                                                     | 56.1 ms: 1.53x faster                                                    |
| go                       | 139 ms                                                      | 91.0 ms: 1.53x faster                                                    |
| asyncio_tcp              | 732 ms                                                      | 481 ms: 1.52x faster                                                     |
| sqlglot_transpile        | 1.48 ms                                                     | 989 us: 1.49x faster                                                     |
| hexiom                   | 5.74 ms                                                     | 3.89 ms: 1.48x faster                                                    |
| pickle_pure_python       | 270 us                                                      | 183 us: 1.48x faster                                                     |
| mako                     | 9.03 ms                                                     | 6.36 ms: 1.42x faster                                                    |
| richards                 | 42.4 ms                                                     | 29.9 ms: 1.42x faster                                                    |
| pyflate                  | 409 ms                                                      | 289 ms: 1.41x faster                                                     |
| scimark_sor              | 106 ms                                                      | 76.2 ms: 1.39x faster                                                    |
| html5lib                 | 51.0 ms                                                     | 36.8 ms: 1.39x faster                                                    |
| crypto_pyaes             | 62.5 ms                                                     | 45.2 ms: 1.38x faster                                                    |
| unpickle_pure_python     | 183 us                                                      | 133 us: 1.38x faster                                                     |
| scimark_monte_carlo      | 57.3 ms                                                     | 41.7 ms: 1.37x faster                                                    |
| deepcopy_memo            | 28.8 us                                                     | 21.9 us: 1.31x faster                                                    |
| regex_compile            | 106 ms                                                      | 80.8 ms: 1.31x faster                                                    |
| tornado_http             | 108 ms                                                      | 82.6 ms: 1.31x faster                                                    |
| mypy2                    | 555 ms                                                      | 424 ms: 1.31x faster                                                     |
| mdp                      | 1.78 sec                                                    | 1.37 sec: 1.30x faster                                                   |
| sympy_sum                | 107 ms                                                      | 84.8 ms: 1.26x faster                                                    |
| pycparser                | 930 ms                                                      | 739 ms: 1.26x faster                                                     |
| dulwich_log              | 50.5 ms                                                     | 40.6 ms: 1.24x faster                                                    |
| django_template          | 28.9 ms                                                     | 23.3 ms: 1.24x faster                                                    |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.71 sec: 1.24x faster                                                   |
| genshi_text              | 19.8 ms                                                     | 16.1 ms: 1.23x faster                                                    |
| pprint_pformat           | 1.22 sec                                                    | 996 ms: 1.22x faster                                                     |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.21x faster                                                    |
| pprint_safe_repr         | 592 ms                                                      | 489 ms: 1.21x faster                                                     |
| sympy_str                | 194 ms                                                      | 162 ms: 1.20x faster                                                     |
| coroutines               | 16.0 ms                                                     | 13.4 ms: 1.20x faster                                                    |
| bench_thread_pool        | 958 us                                                      | 803 us: 1.19x faster                                                     |
| genshi_xml               | 41.0 ms                                                     | 34.4 ms: 1.19x faster                                                    |
| chameleon                | 5.79 ms                                                     | 4.87 ms: 1.19x faster                                                    |
| spectral_norm            | 77.3 ms                                                     | 65.8 ms: 1.17x faster                                                    |
| tomli_loads              | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                   |
| float                    | 61.7 ms                                                     | 53.0 ms: 1.16x faster                                                    |
| 2to3                     | 246 ms                                                      | 211 ms: 1.16x faster                                                     |
| docutils                 | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                   |
| sqlglot_optimize         | 39.8 ms                                                     | 34.3 ms: 1.16x faster                                                    |
| xml_etree_process        | 44.5 ms                                                     | 38.5 ms: 1.16x faster                                                    |
| deepcopy                 | 255 us                                                      | 222 us: 1.15x faster                                                     |
| sqlite_synth             | 1.91 us                                                     | 1.67 us: 1.15x faster                                                    |
| sympy_expand             | 314 ms                                                      | 276 ms: 1.14x faster                                                     |
| regex_dna                | 136 ms                                                      | 120 ms: 1.14x faster                                                     |
| aiohttp                  | 995 us                                                      | 880 us: 1.13x faster                                                     |
| sqlglot_normalize        | 205 ms                                                      | 182 ms: 1.13x faster                                                     |
| nqueens                  | 66.6 ms                                                     | 60.0 ms: 1.11x faster                                                    |
| unpickle                 | 9.09 us                                                     | 8.32 us: 1.09x faster                                                    |
| deepcopy_reduce          | 2.20 us                                                     | 2.03 us: 1.09x faster                                                    |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                    |
| xml_etree_parse          | 96.8 ms                                                     | 92.3 ms: 1.05x faster                                                    |
| logging_format           | 6.76 us                                                     | 6.52 us: 1.04x faster                                                    |
| logging_simple           | 6.22 us                                                     | 6.03 us: 1.03x faster                                                    |
| meteor_contest           | 75.9 ms                                                     | 73.6 ms: 1.03x faster                                                    |
| json_loads               | 14.0 us                                                     | 13.6 us: 1.03x faster                                                    |
| nbody                    | 71.3 ms                                                     | 69.8 ms: 1.02x faster                                                    |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.8 ms: 1.02x faster                                                    |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                     |
| python_startup           | 20.6 ms                                                     | 20.3 ms: 1.01x faster                                                    |
| fannkuch                 | 256 ms                                                      | 253 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.70 ms: 1.01x faster                                                    |
| scimark_fft              | 187 ms                                                      | 188 ms: 1.00x slower                                                     |
| pathlib                  | 75.7 ms                                                     | 76.1 ms: 1.01x slower                                                    |
| xml_etree_generate       | 55.5 ms                                                     | 56.6 ms: 1.02x slower                                                    |
| bench_mp_pool            | 62.0 ms                                                     | 64.7 ms: 1.04x slower                                                    |
| async_generators         | 222 ms                                                      | 234 ms: 1.06x slower                                                     |
| python_startup_no_site   | 15.5 ms                                                     | 16.8 ms: 1.08x slower                                                    |
| pickle                   | 6.85 us                                                     | 7.45 us: 1.09x slower                                                    |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                    |
| create_gc_cycles         | 800 us                                                      | 888 us: 1.11x slower                                                     |
| pickle_dict              | 17.2 us                                                     | 19.8 us: 1.15x slower                                                    |
| pickle_list              | 2.75 us                                                     | 3.18 us: 1.16x slower                                                    |
| coverage                 | 39.0 ms                                                     | 47.3 ms: 1.21x slower                                                    |
| telco                    | 3.94 ms                                                     | 5.05 ms: 1.28x slower                                                    |
| thrift                   | 617 us                                                      | 8.10 ms: 13.12x slower                                                   |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                             |

Benchmark hidden because not significant (3): json, regex_v8, unpickle_list
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240415-3.13.0a6+-2055e5f/bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown