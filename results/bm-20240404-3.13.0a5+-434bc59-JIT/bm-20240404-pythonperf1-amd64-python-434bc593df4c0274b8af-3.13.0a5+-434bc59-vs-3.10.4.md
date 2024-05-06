# Results vs. 3.10.4

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-amd64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.23x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 218 ms: 1.13x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.69 ms: 1.23x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.69 sec: 1.14x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.1 ms: 1.46x faster                                                       |
| tornado_http   | 108 ms                                                      | 82.8 ms: 1.31x faster                                                       |
| Geometric mean | (ref)                                                       | 1.25x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 217 ms: 2.01x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 266 ms: 1.98x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 581 ms: 1.91x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 384 ms: 1.66x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.88x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.7 ms: 1.32x faster                                                       |
| nbody          | 71.3 ms                                                     | 57.0 ms: 1.25x faster                                                       |
| pidigits       | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.19x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 86.5 ms: 1.23x faster                                                       |
| regex_dna      | 136 ms                                                      | 119 ms: 1.14x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 14.6 ms: 1.06x faster                                                       |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.58 ms: 1.64x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 172 us: 1.56x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.17 sec: 1.43x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 129 us: 1.42x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 36.2 ms: 1.23x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 59.7 ms: 1.09x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 89.5 ms: 1.08x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 52.4 ms: 1.06x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.66 us: 1.05x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.02x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.77 us: 1.02x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.89 us: 1.05x slower                                                       |
| pickle               | 6.85 us                                                     | 7.33 us: 1.07x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.15x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 19.7 ms: 1.27x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.73 ms: 1.58x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 14.8 ms: 1.34x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 32.4 ms: 1.27x faster                                                       |
| Geometric mean | (ref)                                                       | 1.39x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 71.8 us: 4.68x faster                                                       |
| async_tree_none          | 435 ms                                                      | 217 ms: 2.01x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 266 ms: 1.98x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.14 ms: 1.96x faster                                                       |
| async_tree_io            | 1.11 sec                                                    | 581 ms: 1.91x faster                                                        |
| pylint                   | 350 ms                                                      | 193 ms: 1.82x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.4 ns: 1.77x faster                                                       |
| richards_super           | 52.2 ms                                                     | 30.2 ms: 1.73x faster                                                       |
| raytrace                 | 273 ms                                                      | 164 ms: 1.66x faster                                                        |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 384 ms: 1.66x faster                                                        |
| generators               | 32.4 ms                                                     | 19.6 ms: 1.65x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.58 ms: 1.64x faster                                                       |
| chaos                    | 61.7 ms                                                     | 38.3 ms: 1.61x faster                                                       |
| richards                 | 42.4 ms                                                     | 26.7 ms: 1.59x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 769 us: 1.58x faster                                                        |
| mako                     | 9.03 ms                                                     | 5.73 ms: 1.58x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 172 us: 1.56x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 476 ms: 1.54x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 50.7 ms: 1.53x faster                                                       |
| go                       | 139 ms                                                      | 92.1 ms: 1.51x faster                                                       |
| pyflate                  | 409 ms                                                      | 271 ms: 1.51x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 985 us: 1.50x faster                                                        |
| comprehensions           | 16.5 us                                                     | 11.1 us: 1.49x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.0 ms: 1.47x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.1 ms: 1.46x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.47 sec: 1.43x faster                                                      |
| tomli_loads              | 1.67 sec                                                    | 1.17 sec: 1.43x faster                                                      |
| unpickle_pure_python     | 183 us                                                      | 129 us: 1.42x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 44.5 ms: 1.40x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 21.0 us: 1.37x faster                                                       |
| pycparser                | 930 ms                                                      | 690 ms: 1.35x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 14.8 ms: 1.34x faster                                                       |
| scimark_sor              | 106 ms                                                      | 80.0 ms: 1.33x faster                                                       |
| float                    | 61.7 ms                                                     | 46.7 ms: 1.32x faster                                                       |
| tornado_http             | 108 ms                                                      | 82.8 ms: 1.31x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 4.41 ms: 1.30x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 942 ms: 1.30x faster                                                        |
| mdp                      | 1.78 sec                                                    | 1.38 sec: 1.29x faster                                                      |
| pprint_safe_repr         | 592 ms                                                      | 463 ms: 1.28x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 32.4 ms: 1.27x faster                                                       |
| nbody                    | 71.3 ms                                                     | 57.0 ms: 1.25x faster                                                       |
| mypy2                    | 555 ms                                                      | 446 ms: 1.24x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 69.5 ms: 1.24x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 40.9 ms: 1.23x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.69 ms: 1.23x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.2 ms: 1.23x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.22 ms: 1.23x faster                                                       |
| regex_compile            | 106 ms                                                      | 86.5 ms: 1.23x faster                                                       |
| sympy_sum                | 107 ms                                                      | 87.7 ms: 1.22x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.57 us: 1.22x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 808 us: 1.19x faster                                                        |
| sympy_str                | 194 ms                                                      | 166 ms: 1.17x faster                                                        |
| deepcopy                 | 255 us                                                      | 219 us: 1.17x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.2 ms: 1.16x faster                                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 34.4 ms: 1.16x faster                                                       |
| sqlglot_normalize        | 205 ms                                                      | 178 ms: 1.15x faster                                                        |
| regex_dna                | 136 ms                                                      | 119 ms: 1.14x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.69 sec: 1.14x faster                                                      |
| deepcopy_reduce          | 2.20 us                                                     | 1.95 us: 1.13x faster                                                       |
| 2to3                     | 246 ms                                                      | 218 ms: 1.13x faster                                                        |
| scimark_fft              | 187 ms                                                      | 166 ms: 1.13x faster                                                        |
| aiohttp                  | 995 us                                                      | 893 us: 1.11x faster                                                        |
| sympy_expand             | 314 ms                                                      | 283 ms: 1.11x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.10 us: 1.11x faster                                                       |
| json                     | 3.14 ms                                                     | 2.86 ms: 1.10x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.68 us: 1.10x faster                                                       |
| nqueens                  | 66.6 ms                                                     | 61.0 ms: 1.09x faster                                                       |
| fannkuch                 | 256 ms                                                      | 234 ms: 1.09x faster                                                        |
| xml_etree_iterparse      | 65.0 ms                                                     | 59.7 ms: 1.09x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 89.5 ms: 1.08x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 71.5 ms: 1.06x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 52.4 ms: 1.06x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 14.6 ms: 1.06x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.05x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.66 us: 1.05x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| unpickle_list            | 2.71 us                                                     | 2.77 us: 1.02x slower                                                       |
| pathlib                  | 75.7 ms                                                     | 77.6 ms: 1.03x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.89 us: 1.05x slower                                                       |
| async_generators         | 222 ms                                                      | 234 ms: 1.06x slower                                                        |
| python_startup           | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.33 us: 1.07x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 67.7 ms: 1.09x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.10x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 904 us: 1.13x slower                                                        |
| coverage                 | 39.0 ms                                                     | 46.7 ms: 1.20x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.80 ms: 1.22x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 19.7 ms: 1.27x slower                                                       |
| thrift                   | 617 us                                                      | 8.76 ms: 14.20x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.23x faster                                                                |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.22x
- 95% likely to have a speedup of 1.21x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown