# Results vs. 3.10.4

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 210 ms: 1.17x faster                                                        |
| chameleon      | 5.79 ms                                                     | 5.01 ms: 1.16x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.64 sec: 1.17x faster                                                      |
| html5lib       | 51.0 ms                                                     | 36.2 ms: 1.41x faster                                                       |
| tornado_http   | 108 ms                                                      | 82.2 ms: 1.32x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 224 ms: 1.94x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 272 ms: 1.93x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 597 ms: 1.86x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 394 ms: 1.62x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.83x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 51.6 ms: 1.20x faster                                                       |
| nbody          | 71.3 ms                                                     | 70.2 ms: 1.02x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 79.8 ms: 1.33x faster                                                       |
| regex_dna      | 136 ms                                                      | 122 ms: 1.12x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.64 ms: 1.62x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 179 us: 1.50x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 129 us: 1.42x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.41 sec: 1.19x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 37.7 ms: 1.18x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.36 us: 1.09x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 91.2 ms: 1.06x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 64.0 ms: 1.02x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.80 us: 1.03x slower                                                       |
| pickle               | 6.85 us                                                     | 7.14 us: 1.04x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.94 us: 1.07x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.12x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.3 ms: 1.02x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 17.0 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 6.38 ms: 1.42x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 16.5 ms: 1.20x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 35.6 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                       | 1.25x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 73.8 us: 4.55x faster                                                       |
| deltablue                | 4.19 ms                                                     | 2.04 ms: 2.06x faster                                                       |
| async_tree_none          | 435 ms                                                      | 224 ms: 1.94x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 272 ms: 1.93x faster                                                        |
| pylint                   | 350 ms                                                      | 188 ms: 1.87x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 597 ms: 1.86x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 56.8 ns: 1.67x faster                                                       |
| raytrace                 | 273 ms                                                      | 165 ms: 1.66x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.64 ms: 1.62x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 394 ms: 1.62x faster                                                        |
| richards_super           | 52.2 ms                                                     | 32.3 ms: 1.62x faster                                                       |
| chaos                    | 61.7 ms                                                     | 39.2 ms: 1.57x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 776 us: 1.57x faster                                                        |
| go                       | 139 ms                                                      | 90.0 ms: 1.54x faster                                                       |
| comprehensions           | 16.5 us                                                     | 10.8 us: 1.53x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 481 ms: 1.52x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 57.0 ms: 1.51x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 982 us: 1.50x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 179 us: 1.50x faster                                                        |
| richards                 | 42.4 ms                                                     | 28.3 ms: 1.50x faster                                                       |
| generators               | 32.4 ms                                                     | 21.7 ms: 1.49x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 3.87 ms: 1.48x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 129 us: 1.42x faster                                                        |
| pyflate                  | 409 ms                                                      | 289 ms: 1.42x faster                                                        |
| mako                     | 9.03 ms                                                     | 6.38 ms: 1.42x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 40.6 ms: 1.41x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 36.2 ms: 1.41x faster                                                       |
| scimark_sor              | 106 ms                                                      | 76.6 ms: 1.39x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 45.7 ms: 1.37x faster                                                       |
| mypy2                    | 555 ms                                                      | 418 ms: 1.33x faster                                                        |
| regex_compile            | 106 ms                                                      | 79.8 ms: 1.33x faster                                                       |
| tornado_http             | 108 ms                                                      | 82.2 ms: 1.32x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 22.3 us: 1.29x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.68 sec: 1.26x faster                                                      |
| dulwich_log              | 50.5 ms                                                     | 40.3 ms: 1.25x faster                                                       |
| sympy_sum                | 107 ms                                                      | 85.4 ms: 1.25x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 63.3 ms: 1.22x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 1.00 sec: 1.22x faster                                                      |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.21x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                       |
| pycparser                | 930 ms                                                      | 772 ms: 1.21x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 491 ms: 1.20x faster                                                        |
| mdp                      | 1.78 sec                                                    | 1.49 sec: 1.20x faster                                                      |
| genshi_text              | 19.8 ms                                                     | 16.5 ms: 1.20x faster                                                       |
| sympy_str                | 194 ms                                                      | 163 ms: 1.20x faster                                                        |
| float                    | 61.7 ms                                                     | 51.6 ms: 1.20x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.41 sec: 1.19x faster                                                      |
| bench_thread_pool        | 958 us                                                      | 811 us: 1.18x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 37.7 ms: 1.18x faster                                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 34.0 ms: 1.17x faster                                                       |
| 2to3                     | 246 ms                                                      | 210 ms: 1.17x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.64 sec: 1.17x faster                                                      |
| sqlite_synth             | 1.91 us                                                     | 1.64 us: 1.16x faster                                                       |
| chameleon                | 5.79 ms                                                     | 5.01 ms: 1.16x faster                                                       |
| deepcopy                 | 255 us                                                      | 222 us: 1.15x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 35.6 ms: 1.15x faster                                                       |
| sympy_expand             | 314 ms                                                      | 274 ms: 1.15x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 179 ms: 1.14x faster                                                        |
| aiohttp                  | 995 us                                                      | 885 us: 1.12x faster                                                        |
| regex_dna                | 136 ms                                                      | 122 ms: 1.12x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 60.8 ms: 1.10x faster                                                       |
| deepcopy_reduce          | 2.20 us                                                     | 2.02 us: 1.09x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.36 us: 1.09x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 91.2 ms: 1.06x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.42 us: 1.05x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 72.8 ms: 1.04x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.98 us: 1.04x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.66 ms: 1.02x faster                                                       |
| python_startup           | 20.6 ms                                                     | 20.3 ms: 1.02x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 64.0 ms: 1.02x faster                                                       |
| nbody                    | 71.3 ms                                                     | 70.2 ms: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| scimark_fft              | 187 ms                                                      | 185 ms: 1.01x faster                                                        |
| pathlib                  | 75.7 ms                                                     | 75.2 ms: 1.01x faster                                                       |
| fannkuch                 | 256 ms                                                      | 257 ms: 1.01x slower                                                        |
| unpickle_list            | 2.71 us                                                     | 2.80 us: 1.03x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 64.2 ms: 1.03x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.14 us: 1.04x slower                                                       |
| async_generators         | 222 ms                                                      | 235 ms: 1.06x slower                                                        |
| pickle_list              | 2.75 us                                                     | 2.94 us: 1.07x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 17.0 ms: 1.09x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 895 us: 1.12x slower                                                        |
| coverage                 | 39.0 ms                                                     | 46.0 ms: 1.18x slower                                                       |
| telco                    | 3.94 ms                                                     | 5.05 ms: 1.28x slower                                                       |
| thrift                   | 617 us                                                      | 8.03 ms: 13.01x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                                |

Benchmark hidden because not significant (3): json, xml_etree_generate, regex_v8
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown