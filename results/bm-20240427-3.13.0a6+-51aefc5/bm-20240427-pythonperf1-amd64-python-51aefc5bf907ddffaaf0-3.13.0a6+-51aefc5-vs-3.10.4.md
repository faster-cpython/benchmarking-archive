# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 214 ms: 1.15x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.80 ms: 1.20x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.67 sec: 1.15x faster                                                      |
| html5lib       | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                       |
| tornado_http   | 108 ms                                                      | 92.1 ms: 1.18x faster                                                       |
| Geometric mean | (ref)                                                       | 1.21x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 278 ms: 1.89x faster                                                        |
| async_tree_none         | 435 ms                                                      | 231 ms: 1.89x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 612 ms: 1.81x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 398 ms: 1.60x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.79x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 51.6 ms: 1.20x faster                                                       |
| pidigits       | 149 ms                                                      | 148 ms: 1.01x faster                                                        |
| nbody          | 71.3 ms                                                     | 70.9 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 80.0 ms: 1.33x faster                                                       |
| regex_dna      | 136 ms                                                      | 125 ms: 1.09x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.62 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.76 ms: 1.59x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 180 us: 1.50x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 130 us: 1.41x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 37.8 ms: 1.18x faster                                                       |
| tomli_loads          | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                      |
| unpickle             | 9.09 us                                                     | 8.45 us: 1.08x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 91.4 ms: 1.06x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 64.3 ms: 1.01x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 55.2 ms: 1.01x faster                                                       |
| json_loads           | 14.0 us                                                     | 14.2 us: 1.01x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.77 us: 1.02x slower                                                       |
| pickle               | 6.85 us                                                     | 7.37 us: 1.08x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.97 us: 1.08x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 19.8 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.10x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.0 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 17.3 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.35 ms: 1.42x faster                                                       |
| django_template | 28.9 ms                                                     | 23.0 ms: 1.26x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 16.0 ms: 1.24x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 33.4 ms: 1.23x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.28x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 108 us: 3.12x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.00 ms: 2.09x faster                                                       |
| async_tree_memoization   | 526 ms                                                      | 278 ms: 1.89x faster                                                        |
| async_tree_none          | 435 ms                                                      | 231 ms: 1.89x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 612 ms: 1.81x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.2 ns: 1.78x faster                                                       |
| richards_super           | 52.2 ms                                                     | 31.3 ms: 1.67x faster                                                       |
| pylint                   | 350 ms                                                      | 212 ms: 1.65x faster                                                        |
| raytrace                 | 273 ms                                                      | 166 ms: 1.65x faster                                                        |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 398 ms: 1.60x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.76 ms: 1.59x faster                                                       |
| go                       | 139 ms                                                      | 87.5 ms: 1.59x faster                                                       |
| chaos                    | 61.7 ms                                                     | 39.0 ms: 1.58x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 771 us: 1.58x faster                                                        |
| richards                 | 42.4 ms                                                     | 27.6 ms: 1.54x faster                                                       |
| generators               | 32.4 ms                                                     | 21.5 ms: 1.51x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 180 us: 1.50x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 57.4 ms: 1.49x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 987 us: 1.49x faster                                                        |
| comprehensions           | 16.5 us                                                     | 11.1 us: 1.49x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 3.94 ms: 1.46x faster                                                       |
| mako                     | 9.03 ms                                                     | 6.35 ms: 1.42x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 130 us: 1.41x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 41.2 ms: 1.39x faster                                                       |
| pyflate                  | 409 ms                                                      | 295 ms: 1.38x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 45.6 ms: 1.37x faster                                                       |
| scimark_sor              | 106 ms                                                      | 77.8 ms: 1.36x faster                                                       |
| regex_compile            | 106 ms                                                      | 80.0 ms: 1.33x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 22.1 us: 1.30x faster                                                       |
| mypy2                    | 555 ms                                                      | 429 ms: 1.29x faster                                                        |
| mdp                      | 1.78 sec                                                    | 1.39 sec: 1.28x faster                                                      |
| spectral_norm            | 77.3 ms                                                     | 61.4 ms: 1.26x faster                                                       |
| django_template          | 28.9 ms                                                     | 23.0 ms: 1.26x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 40.3 ms: 1.25x faster                                                       |
| sympy_sum                | 107 ms                                                      | 85.5 ms: 1.25x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 16.0 ms: 1.24x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 33.4 ms: 1.23x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 993 ms: 1.23x faster                                                        |
| coroutines               | 16.0 ms                                                     | 13.1 ms: 1.22x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 487 ms: 1.22x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.22x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.80 ms: 1.20x faster                                                       |
| float                    | 61.7 ms                                                     | 51.6 ms: 1.20x faster                                                       |
| pycparser                | 930 ms                                                      | 780 ms: 1.19x faster                                                        |
| sympy_str                | 194 ms                                                      | 164 ms: 1.19x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 37.8 ms: 1.18x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.63 us: 1.18x faster                                                       |
| tornado_http             | 108 ms                                                      | 92.1 ms: 1.18x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                      |
| sqlglot_optimize         | 39.8 ms                                                     | 34.3 ms: 1.16x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.67 sec: 1.15x faster                                                      |
| 2to3                     | 246 ms                                                      | 214 ms: 1.15x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.84 sec: 1.15x faster                                                      |
| bench_thread_pool        | 958 us                                                      | 836 us: 1.15x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 181 ms: 1.13x faster                                                        |
| sympy_expand             | 314 ms                                                      | 279 ms: 1.13x faster                                                        |
| deepcopy                 | 255 us                                                      | 227 us: 1.12x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 60.1 ms: 1.11x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 664 ms: 1.10x faster                                                        |
| regex_dna                | 136 ms                                                      | 125 ms: 1.09x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 2.04 us: 1.08x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.45 us: 1.08x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.56 ms: 1.07x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 91.4 ms: 1.06x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 72.6 ms: 1.05x faster                                                       |
| aiohttp                  | 995 us                                                      | 955 us: 1.04x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.53 us: 1.04x faster                                                       |
| scimark_fft              | 187 ms                                                      | 181 ms: 1.03x faster                                                        |
| regex_effbot             | 1.66 ms                                                     | 1.62 ms: 1.02x faster                                                       |
| fannkuch                 | 256 ms                                                      | 252 ms: 1.01x faster                                                        |
| xml_etree_iterparse      | 65.0 ms                                                     | 64.3 ms: 1.01x faster                                                       |
| pidigits                 | 149 ms                                                      | 148 ms: 1.01x faster                                                        |
| logging_simple           | 6.22 us                                                     | 6.18 us: 1.01x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 55.2 ms: 1.01x faster                                                       |
| nbody                    | 71.3 ms                                                     | 70.9 ms: 1.01x faster                                                       |
| json_loads               | 14.0 us                                                     | 14.2 us: 1.01x slower                                                       |
| python_startup           | 20.6 ms                                                     | 21.0 ms: 1.02x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.77 us: 1.02x slower                                                       |
| pathlib                  | 75.7 ms                                                     | 81.3 ms: 1.07x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.37 us: 1.08x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.97 us: 1.08x slower                                                       |
| async_generators         | 222 ms                                                      | 239 ms: 1.08x slower                                                        |
| gc_traversal             | 1.41 ms                                                     | 1.56 ms: 1.11x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 17.3 ms: 1.12x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 69.7 ms: 1.12x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 910 us: 1.14x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 19.8 us: 1.15x slower                                                       |
| coverage                 | 39.0 ms                                                     | 45.2 ms: 1.16x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.89 ms: 1.24x slower                                                       |
| thrift                   | 617 us                                                      | 8.10 ms: 13.12x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.19x faster                                                                |

Benchmark hidden because not significant (2): json, regex_v8
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown