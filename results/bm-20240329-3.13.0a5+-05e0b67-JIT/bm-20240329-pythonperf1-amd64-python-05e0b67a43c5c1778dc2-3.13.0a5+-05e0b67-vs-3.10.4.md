# Results vs. 3.10.4

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-amd64
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 218 ms: 1.13x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.78 ms: 1.21x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.69 sec: 1.13x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.8 ms: 1.42x faster                                                       |
| tornado_http   | 108 ms                                                      | 84.8 ms: 1.28x faster                                                       |
| Geometric mean | (ref)                                                       | 1.23x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 216 ms: 2.02x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 268 ms: 1.96x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 574 ms: 1.93x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 376 ms: 1.70x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.90x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 47.0 ms: 1.31x faster                                                       |
| nbody          | 71.3 ms                                                     | 58.8 ms: 1.21x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.17x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 84.6 ms: 1.25x faster                                                       |
| regex_dna      | 136 ms                                                      | 116 ms: 1.17x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.61 ms: 1.63x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 175 us: 1.54x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 128 us: 1.43x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.21 sec: 1.38x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 36.4 ms: 1.22x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 61.2 ms: 1.06x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 91.6 ms: 1.06x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.72 us: 1.04x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 53.4 ms: 1.04x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.80 us: 1.03x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.88 us: 1.05x slower                                                       |
| pickle               | 6.85 us                                                     | 7.32 us: 1.07x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 22.6 ms: 1.09x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 20.2 ms: 1.30x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.19x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.84 ms: 1.55x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 15.1 ms: 1.31x faster                                                       |
| django_template | 28.9 ms                                                     | 22.8 ms: 1.27x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 34.2 ms: 1.20x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.32x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 70.1 us: 4.80x faster                                                       |
| deltablue                | 4.19 ms                                                     | 2.06 ms: 2.03x faster                                                       |
| async_tree_none          | 435 ms                                                      | 216 ms: 2.02x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 268 ms: 1.96x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 574 ms: 1.93x faster                                                        |
| pylint                   | 350 ms                                                      | 190 ms: 1.84x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.6 ns: 1.76x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 376 ms: 1.70x faster                                                        |
| richards_super           | 52.2 ms                                                     | 31.6 ms: 1.65x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.61 ms: 1.63x faster                                                       |
| generators               | 32.4 ms                                                     | 20.1 ms: 1.61x faster                                                       |
| chaos                    | 61.7 ms                                                     | 39.1 ms: 1.58x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 778 us: 1.56x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 470 ms: 1.56x faster                                                        |
| mako                     | 9.03 ms                                                     | 5.84 ms: 1.55x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 175 us: 1.54x faster                                                        |
| raytrace                 | 273 ms                                                      | 180 ms: 1.52x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 51.1 ms: 1.51x faster                                                       |
| comprehensions           | 16.5 us                                                     | 10.9 us: 1.51x faster                                                       |
| richards                 | 42.4 ms                                                     | 28.2 ms: 1.50x faster                                                       |
| go                       | 139 ms                                                      | 93.5 ms: 1.49x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 1000 us: 1.48x faster                                                       |
| pyflate                  | 409 ms                                                      | 281 ms: 1.46x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.7 ms: 1.44x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.47 sec: 1.44x faster                                                      |
| unpickle_pure_python     | 183 us                                                      | 128 us: 1.43x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 43.9 ms: 1.43x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.8 ms: 1.42x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.21 sec: 1.38x faster                                                      |
| pycparser                | 930 ms                                                      | 702 ms: 1.33x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 21.9 us: 1.31x faster                                                       |
| float                    | 61.7 ms                                                     | 47.0 ms: 1.31x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 15.1 ms: 1.31x faster                                                       |
| scimark_sor              | 106 ms                                                      | 81.3 ms: 1.31x faster                                                       |
| tornado_http             | 108 ms                                                      | 84.8 ms: 1.28x faster                                                       |
| django_template          | 28.9 ms                                                     | 22.8 ms: 1.27x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.41 sec: 1.26x faster                                                      |
| hexiom                   | 5.74 ms                                                     | 4.57 ms: 1.26x faster                                                       |
| regex_compile            | 106 ms                                                      | 84.6 ms: 1.25x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 985 ms: 1.24x faster                                                        |
| coroutines               | 16.0 ms                                                     | 12.9 ms: 1.24x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 479 ms: 1.24x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 40.9 ms: 1.23x faster                                                       |
| mypy2                    | 555 ms                                                      | 452 ms: 1.23x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 36.4 ms: 1.22x faster                                                       |
| sympy_sum                | 107 ms                                                      | 87.7 ms: 1.22x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.58 us: 1.21x faster                                                       |
| nbody                    | 71.3 ms                                                     | 58.8 ms: 1.21x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.78 ms: 1.21x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 70.9 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.26 ms: 1.21x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 34.2 ms: 1.20x faster                                                       |
| regex_dna                | 136 ms                                                      | 116 ms: 1.17x faster                                                        |
| sympy_str                | 194 ms                                                      | 168 ms: 1.16x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.3 ms: 1.15x faster                                                       |
| deepcopy                 | 255 us                                                      | 223 us: 1.15x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.93 us: 1.14x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 840 us: 1.14x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.69 sec: 1.13x faster                                                      |
| 2to3                     | 246 ms                                                      | 218 ms: 1.13x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 35.4 ms: 1.12x faster                                                       |
| fannkuch                 | 256 ms                                                      | 228 ms: 1.12x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 184 ms: 1.11x faster                                                        |
| aiohttp                  | 995 us                                                      | 905 us: 1.10x faster                                                        |
| scimark_fft              | 187 ms                                                      | 171 ms: 1.10x faster                                                        |
| sympy_expand             | 314 ms                                                      | 287 ms: 1.09x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 60.9 ms: 1.09x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.37 us: 1.06x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 61.2 ms: 1.06x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 91.6 ms: 1.06x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.96 us: 1.04x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.72 us: 1.04x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 53.4 ms: 1.04x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 73.1 ms: 1.04x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| pathlib                  | 75.7 ms                                                     | 77.9 ms: 1.03x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.80 us: 1.03x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.88 us: 1.05x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.32 us: 1.07x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 855 us: 1.07x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 67.4 ms: 1.09x slower                                                       |
| python_startup           | 20.6 ms                                                     | 22.6 ms: 1.09x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                       |
| async_generators         | 222 ms                                                      | 247 ms: 1.12x slower                                                        |
| unpack_sequence          | 39.6 ns                                                     | 46.5 ns: 1.17x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.69 ms: 1.19x slower                                                       |
| coverage                 | 39.0 ms                                                     | 47.4 ms: 1.22x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 20.2 ms: 1.30x slower                                                       |
| json                     | 3.14 ms                                                     | 4.10 ms: 1.31x slower                                                       |
| thrift                   | 617 us                                                      | 9.06 ms: 14.67x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                                |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-05e0b67-JIT/bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown