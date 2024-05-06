
# Results vs. 3.10.4

- fork: python
- ref: v3.12.1
- machine: windows-amd64
- commit hash: 2305ca5
- commit date: 2023-12-07
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 215 ms: 1.14x faster                                        |
| chameleon      | 5.79 ms                                                     | 5.06 ms: 1.14x faster                                       |
| docutils       | 1.92 sec                                                    | 1.60 sec: 1.20x faster                                      |
| tornado_http   | 108 ms                                                      | 87.0 ms: 1.25x faster                                       |
| Geometric mean | (ref)                                                       | 1.18x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 340 ms: 1.55x faster                                        |
| async_tree_io           | 1.11 sec                                                    | 731 ms: 1.52x faster                                        |
| async_tree_none         | 435 ms                                                      | 288 ms: 1.51x faster                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 483 ms: 1.32x faster                                        |
| Geometric mean          | (ref)                                                       | 1.47x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 61.7 ms                                                     | 54.3 ms: 1.14x faster                                       |
| nbody          | 71.3 ms                                                     | 69.5 ms: 1.03x faster                                       |
| pidigits       | 149 ms                                                      | 151 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                       | 1.05x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 85.0 ms: 1.25x faster                                       |
| regex_dna      | 136 ms                                                      | 121 ms: 1.12x faster                                        |
| regex_v8       | 15.4 ms                                                     | 14.1 ms: 1.09x faster                                       |
| regex_effbot   | 1.66 ms                                                     | 1.63 ms: 1.02x faster                                       |
| Geometric mean | (ref)                                                       | 1.12x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.69 ms: 1.61x faster                                       |
| pickle_pure_python   | 270 us                                                      | 193 us: 1.39x faster                                        |
| unpickle_pure_python | 183 us                                                      | 133 us: 1.38x faster                                        |
| tomli_loads          | 1.67 sec                                                    | 1.36 sec: 1.23x faster                                      |
| xml_etree_process    | 44.5 ms                                                     | 38.4 ms: 1.16x faster                                       |
| unpickle             | 9.09 us                                                     | 8.13 us: 1.12x faster                                       |
| xml_etree_parse      | 96.8 ms                                                     | 92.8 ms: 1.04x faster                                       |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.02x faster                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 64.0 ms: 1.01x faster                                       |
| unpickle_list        | 2.71 us                                                     | 2.68 us: 1.01x faster                                       |
| pickle               | 6.85 us                                                     | 6.95 us: 1.01x slower                                       |
| xml_etree_generate   | 55.5 ms                                                     | 57.1 ms: 1.03x slower                                       |
| pickle_list          | 2.75 us                                                     | 2.85 us: 1.03x slower                                       |
| pickle_dict          | 17.2 us                                                     | 18.2 us: 1.06x slower                                       |
| Geometric mean       | (ref)                                                       | 1.12x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.5 ms: 1.06x faster                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                       |
| Geometric mean         | (ref)                                                       | 1.00x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.89 ms: 1.31x faster                                       |
| django_template | 28.9 ms                                                     | 23.7 ms: 1.22x faster                                       |
| Geometric mean  | (ref)                                                       | 1.26x faster                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 76.4 us: 4.40x faster                                       |
| deltablue                | 4.19 ms                                                     | 2.14 ms: 1.96x faster                                       |
| richards_super           | 52.2 ms                                                     | 30.5 ms: 1.71x faster                                       |
| json_dumps               | 9.16 ms                                                     | 5.69 ms: 1.61x faster                                       |
| go                       | 139 ms                                                      | 87.8 ms: 1.58x faster                                       |
| richards                 | 42.4 ms                                                     | 26.9 ms: 1.58x faster                                       |
| asyncio_tcp              | 732 ms                                                      | 470 ms: 1.56x faster                                        |
| async_tree_memoization   | 526 ms                                                      | 340 ms: 1.55x faster                                        |
| logging_silent           | 94.6 ns                                                     | 62.1 ns: 1.52x faster                                       |
| async_tree_io            | 1.11 sec                                                    | 731 ms: 1.52x faster                                        |
| async_tree_none          | 435 ms                                                      | 288 ms: 1.51x faster                                        |
| sqlglot_parse            | 1.22 ms                                                     | 821 us: 1.48x faster                                        |
| scimark_lu               | 85.8 ms                                                     | 59.4 ms: 1.44x faster                                       |
| generators               | 32.4 ms                                                     | 22.6 ms: 1.43x faster                                       |
| chaos                    | 61.7 ms                                                     | 43.2 ms: 1.43x faster                                       |
| hexiom                   | 5.74 ms                                                     | 4.03 ms: 1.43x faster                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 1.04 ms: 1.42x faster                                       |
| raytrace                 | 273 ms                                                      | 193 ms: 1.41x faster                                        |
| pickle_pure_python       | 270 us                                                      | 193 us: 1.39x faster                                        |
| pyflate                  | 409 ms                                                      | 294 ms: 1.39x faster                                        |
| unpickle_pure_python     | 183 us                                                      | 133 us: 1.38x faster                                        |
| scimark_sor              | 106 ms                                                      | 77.8 ms: 1.37x faster                                       |
| pycparser                | 930 ms                                                      | 687 ms: 1.35x faster                                        |
| crypto_pyaes             | 62.5 ms                                                     | 46.5 ms: 1.34x faster                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 483 ms: 1.32x faster                                        |
| mako                     | 9.03 ms                                                     | 6.89 ms: 1.31x faster                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 44.1 ms: 1.30x faster                                       |
| mdp                      | 1.78 sec                                                    | 1.38 sec: 1.29x faster                                      |
| regex_compile            | 106 ms                                                      | 85.0 ms: 1.25x faster                                       |
| tornado_http             | 108 ms                                                      | 87.0 ms: 1.25x faster                                       |
| sqlalchemy_imperative    | 11.4 ms                                                     | 9.23 ms: 1.24x faster                                       |
| tomli_loads              | 1.67 sec                                                    | 1.36 sec: 1.23x faster                                      |
| spectral_norm            | 77.3 ms                                                     | 63.2 ms: 1.22x faster                                       |
| sqlalchemy_declarative   | 103 ms                                                      | 84.7 ms: 1.22x faster                                       |
| django_template          | 28.9 ms                                                     | 23.7 ms: 1.22x faster                                       |
| deepcopy_memo            | 28.8 us                                                     | 23.7 us: 1.21x faster                                       |
| dask                     | 313 ms                                                      | 259 ms: 1.21x faster                                        |
| sympy_sum                | 107 ms                                                      | 89.1 ms: 1.20x faster                                       |
| docutils                 | 1.92 sec                                                    | 1.60 sec: 1.20x faster                                      |
| sympy_integrate          | 15.3 ms                                                     | 12.9 ms: 1.19x faster                                       |
| comprehensions           | 16.5 us                                                     | 13.9 us: 1.18x faster                                       |
| pprint_pformat           | 1.22 sec                                                    | 1.04 sec: 1.17x faster                                      |
| dulwich_log              | 50.5 ms                                                     | 43.2 ms: 1.17x faster                                       |
| pprint_safe_repr         | 592 ms                                                      | 511 ms: 1.16x faster                                        |
| xml_etree_process        | 44.5 ms                                                     | 38.4 ms: 1.16x faster                                       |
| aiohttp                  | 995 us                                                      | 864 us: 1.15x faster                                        |
| 2to3                     | 246 ms                                                      | 215 ms: 1.14x faster                                        |
| chameleon                | 5.79 ms                                                     | 5.06 ms: 1.14x faster                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 34.8 ms: 1.14x faster                                       |
| float                    | 61.7 ms                                                     | 54.3 ms: 1.14x faster                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.86 sec: 1.13x faster                                      |
| coroutines               | 16.0 ms                                                     | 14.1 ms: 1.13x faster                                       |
| sympy_str                | 194 ms                                                      | 173 ms: 1.13x faster                                        |
| regex_dna                | 136 ms                                                      | 121 ms: 1.12x faster                                        |
| unpickle                 | 9.09 us                                                     | 8.13 us: 1.12x faster                                       |
| bench_thread_pool        | 958 us                                                      | 859 us: 1.11x faster                                        |
| mypy2                    | 555 ms                                                      | 501 ms: 1.11x faster                                        |
| sympy_expand             | 314 ms                                                      | 284 ms: 1.11x faster                                        |
| sqlglot_normalize        | 205 ms                                                      | 187 ms: 1.10x faster                                        |
| deepcopy                 | 255 us                                                      | 233 us: 1.10x faster                                        |
| create_gc_cycles         | 800 us                                                      | 730 us: 1.10x faster                                        |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.49 ms: 1.10x faster                                       |
| regex_v8                 | 15.4 ms                                                     | 14.1 ms: 1.09x faster                                       |
| sqlite_synth             | 1.91 us                                                     | 1.76 us: 1.08x faster                                       |
| json                     | 3.14 ms                                                     | 2.93 ms: 1.07x faster                                       |
| fannkuch                 | 256 ms                                                      | 239 ms: 1.07x faster                                        |
| nqueens                  | 66.6 ms                                                     | 62.6 ms: 1.06x faster                                       |
| python_startup           | 20.6 ms                                                     | 19.5 ms: 1.06x faster                                       |
| scimark_fft              | 187 ms                                                      | 179 ms: 1.05x faster                                        |
| xml_etree_parse          | 96.8 ms                                                     | 92.8 ms: 1.04x faster                                       |
| deepcopy_reduce          | 2.20 us                                                     | 2.13 us: 1.04x faster                                       |
| meteor_contest           | 75.9 ms                                                     | 73.7 ms: 1.03x faster                                       |
| nbody                    | 71.3 ms                                                     | 69.5 ms: 1.03x faster                                       |
| coverage                 | 39.0 ms                                                     | 38.2 ms: 1.02x faster                                       |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.02x faster                                       |
| regex_effbot             | 1.66 ms                                                     | 1.63 ms: 1.02x faster                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 64.0 ms: 1.01x faster                                       |
| unpickle_list            | 2.71 us                                                     | 2.68 us: 1.01x faster                                       |
| pickle                   | 6.85 us                                                     | 6.95 us: 1.01x slower                                       |
| pidigits                 | 149 ms                                                      | 151 ms: 1.02x slower                                        |
| logging_format           | 6.76 us                                                     | 6.87 us: 1.02x slower                                       |
| logging_simple           | 6.22 us                                                     | 6.39 us: 1.03x slower                                       |
| xml_etree_generate       | 55.5 ms                                                     | 57.1 ms: 1.03x slower                                       |
| pickle_list              | 2.75 us                                                     | 2.85 us: 1.03x slower                                       |
| telco                    | 3.94 ms                                                     | 4.12 ms: 1.05x slower                                       |
| bench_mp_pool            | 62.0 ms                                                     | 65.3 ms: 1.05x slower                                       |
| gc_traversal             | 1.41 ms                                                     | 1.48 ms: 1.05x slower                                       |
| python_startup_no_site   | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                       |
| pickle_dict              | 17.2 us                                                     | 18.2 us: 1.06x slower                                       |
| pathlib                  | 75.7 ms                                                     | 80.7 ms: 1.07x slower                                       |
| async_generators         | 222 ms                                                      | 237 ms: 1.07x slower                                        |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                |

Benchmark hidden because not significant (1): unpack_sequence
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
Ignored benchmarks (4) of results/bm-20231207-3.12.1-2305ca5/bm-20231207-pythonperf1-amd64-python-v3.12.1-3.12.1-2305ca5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg


# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x


# Memory

- memory change: unknown