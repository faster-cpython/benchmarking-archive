# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 216 ms: 1.01x faster                                                        |
| chameleon      | 4.98 ms                                                     | 4.69 ms: 1.06x faster                                                       |
| tornado_http   | 89.5 ms                                                     | 81.7 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 255 ms: 1.44x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 211 ms: 1.35x faster                                                        |
| async_tree_none            | 291 ms                                                      | 216 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 263 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 383 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 605 ms: 1.28x faster                                                        |
| async_tree_io              | 731 ms                                                      | 585 ms: 1.25x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.32x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 58.2 ms: 1.24x faster                                                       |
| float          | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.16x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 117 ms: 1.08x faster                                                        |
| regex_compile  | 87.5 ms                                                     | 84.3 ms: 1.04x faster                                                       |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.17 sec: 1.17x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 171 us: 1.14x faster                                                        |
| unpickle_pure_python | 133 us                                                      | 124 us: 1.08x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 60.5 ms: 1.08x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 52.2 ms: 1.07x faster                                                       |
| xml_etree_process    | 37.7 ms                                                     | 36.0 ms: 1.05x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 89.7 ms: 1.04x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.56 ms: 1.02x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.6 us: 1.02x faster                                                       |
| pickle               | 7.43 us                                                     | 7.41 us: 1.00x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.67 us: 1.06x slower                                                       |
| pickle_list          | 2.83 us                                                     | 3.02 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 17.9 ms: 1.10x slower                                                       |
| python_startup         | 19.5 ms                                                     | 21.5 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 5.58 ms: 1.27x faster                                                       |
| django_template | 22.9 ms                                                     | 21.5 ms: 1.07x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.16x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 255 ms: 1.44x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.52 sec: 1.37x faster                                                      |
| typing_runtime_protocols   | 95.1 us                                                     | 70.1 us: 1.36x faster                                                       |
| async_tree_none_tg         | 285 ms                                                      | 211 ms: 1.35x faster                                                        |
| async_tree_none            | 291 ms                                                      | 216 ms: 1.35x faster                                                        |
| spectral_norm              | 66.9 ms                                                     | 50.0 ms: 1.34x faster                                                       |
| comprehensions             | 14.1 us                                                     | 10.6 us: 1.34x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 263 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 383 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 605 ms: 1.28x faster                                                        |
| mako                       | 7.09 ms                                                     | 5.58 ms: 1.27x faster                                                       |
| async_tree_io              | 731 ms                                                      | 585 ms: 1.25x faster                                                        |
| nbody                      | 71.9 ms                                                     | 58.2 ms: 1.24x faster                                                       |
| float                      | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                       |
| raytrace                   | 192 ms                                                      | 161 ms: 1.19x faster                                                        |
| tomli_loads                | 1.37 sec                                                    | 1.17 sec: 1.17x faster                                                      |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.21 ms: 1.16x faster                                                       |
| generators                 | 22.5 ms                                                     | 19.5 ms: 1.16x faster                                                       |
| mypy2                      | 509 ms                                                      | 441 ms: 1.15x faster                                                        |
| pickle_pure_python         | 195 us                                                      | 171 us: 1.14x faster                                                        |
| chaos                      | 43.3 ms                                                     | 38.2 ms: 1.13x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.6 ms: 1.13x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 42.8 ms: 1.13x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 53.5 ns: 1.13x faster                                                       |
| pprint_safe_repr           | 513 ms                                                      | 457 ms: 1.12x faster                                                        |
| dulwich_log                | 44.3 ms                                                     | 39.5 ms: 1.12x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 935 ms: 1.12x faster                                                        |
| scimark_fft                | 184 ms                                                      | 165 ms: 1.12x faster                                                        |
| pyflate                    | 295 ms                                                      | 264 ms: 1.12x faster                                                        |
| deepcopy_memo              | 23.7 us                                                     | 21.2 us: 1.12x faster                                                       |
| deepcopy                   | 238 us                                                      | 215 us: 1.11x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.69 us: 1.10x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.61 us: 1.10x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 81.7 ms: 1.10x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.91 us: 1.09x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.16 us: 1.09x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 787 us: 1.09x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                       |
| regex_dna                  | 126 ms                                                      | 117 ms: 1.08x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 124 us: 1.08x faster                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 60.5 ms: 1.08x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 52.2 ms: 1.07x faster                                                       |
| django_template            | 22.9 ms                                                     | 21.5 ms: 1.07x faster                                                       |
| fannkuch                   | 247 ms                                                      | 231 ms: 1.07x faster                                                        |
| chameleon                  | 4.98 ms                                                     | 4.69 ms: 1.06x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 76.0 ms: 1.06x faster                                                       |
| sympy_str                  | 175 ms                                                      | 166 ms: 1.05x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 36.0 ms: 1.05x faster                                                       |
| sympy_sum                  | 91.5 ms                                                     | 87.9 ms: 1.04x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 772 us: 1.04x faster                                                        |
| nqueens                    | 62.8 ms                                                     | 60.4 ms: 1.04x faster                                                       |
| richards_super             | 32.1 ms                                                     | 30.9 ms: 1.04x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 84.3 ms: 1.04x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 180 ms: 1.04x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 89.7 ms: 1.04x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 985 us: 1.04x faster                                                        |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| richards                   | 28.4 ms                                                     | 27.4 ms: 1.04x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 67.2 ms: 1.03x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.56 ms: 1.02x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 72.9 ms: 1.02x faster                                                       |
| json_loads                 | 13.9 us                                                     | 13.6 us: 1.02x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.12 ms: 1.02x faster                                                       |
| async_generators           | 239 ms                                                      | 235 ms: 1.02x faster                                                        |
| 2to3                       | 218 ms                                                      | 216 ms: 1.01x faster                                                        |
| go                         | 91.6 ms                                                     | 91.0 ms: 1.01x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.41 us: 1.00x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 34.7 ms: 1.01x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 80.2 ms: 1.02x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.2 ms: 1.02x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.67 us: 1.06x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.35 ms: 1.06x slower                                                       |
| pickle_list                | 2.83 us                                                     | 3.02 us: 1.07x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.48 sec: 1.08x slower                                                      |
| python_startup_no_site     | 16.2 ms                                                     | 17.9 ms: 1.10x slower                                                       |
| python_startup             | 19.5 ms                                                     | 21.5 ms: 1.11x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.76 ms: 1.15x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 891 us: 1.18x slower                                                        |
| coverage                   | 40.8 ms                                                     | 48.9 ms: 1.20x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 75.0 ms: 1.27x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (7): asyncio_tcp, json, pycparser, unpickle_list, sympy_expand, docutils, aiohttp
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown