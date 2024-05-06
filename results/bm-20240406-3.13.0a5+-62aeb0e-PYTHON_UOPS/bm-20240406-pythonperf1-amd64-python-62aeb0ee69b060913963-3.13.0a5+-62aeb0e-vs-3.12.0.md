# Results vs. 3.12.0

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.02x slower
- HPT reliability: 99.78%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 226 ms: 1.03x slower                                                        |
| chameleon      | 4.98 ms                                                     | 5.06 ms: 1.02x slower                                                       |
| docutils       | 1.66 sec                                                    | 1.76 sec: 1.06x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 86.2 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 272 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 221 ms: 1.29x faster                                                        |
| async_tree_none            | 291 ms                                                      | 230 ms: 1.27x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 622 ms: 1.24x faster                                                        |
| async_tree_io              | 731 ms                                                      | 590 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 395 ms: 1.24x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 277 ms: 1.22x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.27x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| float          | 56.8 ms                                                     | 60.0 ms: 1.06x slower                                                       |
| nbody          | 71.9 ms                                                     | 83.2 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                       | 1.06x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 121 ms: 1.04x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.58 ms: 1.02x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 15.1 ms: 1.06x slower                                                       |
| regex_compile  | 87.5 ms                                                     | 107 ms: 1.23x slower                                                        |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 184 us: 1.06x faster                                                        |
| xml_etree_parse      | 93.0 ms                                                     | 91.1 ms: 1.02x faster                                                       |
| pickle               | 7.43 us                                                     | 7.50 us: 1.01x slower                                                       |
| json_dumps           | 5.70 ms                                                     | 5.77 ms: 1.01x slower                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 56.6 ms: 1.01x slower                                                       |
| pickle_dict          | 18.4 us                                                     | 19.0 us: 1.03x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.93 us: 1.04x slower                                                       |
| xml_etree_process    | 37.7 ms                                                     | 39.1 ms: 1.04x slower                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 67.8 ms: 1.04x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.54 us: 1.04x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.88 us: 1.05x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.52 sec: 1.11x slower                                                      |
| unpickle_pure_python | 133 us                                                      | 169 us: 1.27x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.04x slower                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 20.1 ms: 1.03x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 18.1 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 7.47 ms: 1.05x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.55 sec: 1.35x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 272 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 221 ms: 1.29x faster                                                        |
| async_tree_none            | 291 ms                                                      | 230 ms: 1.27x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 622 ms: 1.24x faster                                                        |
| async_tree_io              | 731 ms                                                      | 590 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 395 ms: 1.24x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 277 ms: 1.22x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 78.3 us: 1.21x faster                                                       |
| mypy2                      | 509 ms                                                      | 462 ms: 1.10x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.62 us: 1.09x faster                                                       |
| raytrace                   | 192 ms                                                      | 177 ms: 1.09x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 56.4 ns: 1.07x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 184 us: 1.06x faster                                                        |
| json                       | 3.05 ms                                                     | 2.88 ms: 1.06x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 65.7 ms: 1.05x faster                                                       |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.04x faster                                                        |
| tornado_http               | 89.5 ms                                                     | 86.2 ms: 1.04x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 78.0 ms: 1.03x faster                                                       |
| pidigits                   | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| bench_thread_pool          | 857 us                                                      | 835 us: 1.03x faster                                                        |
| regex_effbot               | 1.62 ms                                                     | 1.58 ms: 1.02x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 91.1 ms: 1.02x faster                                                       |
| deepcopy                   | 238 us                                                      | 235 us: 1.01x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.50 us: 1.01x slower                                                       |
| generators                 | 22.5 ms                                                     | 22.8 ms: 1.01x slower                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.77 ms: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 56.6 ms: 1.01x slower                                                       |
| chameleon                  | 4.98 ms                                                     | 5.06 ms: 1.02x slower                                                       |
| dulwich_log                | 44.3 ms                                                     | 45.0 ms: 1.02x slower                                                       |
| async_generators           | 239 ms                                                      | 244 ms: 1.02x slower                                                        |
| richards                   | 28.4 ms                                                     | 29.0 ms: 1.02x slower                                                       |
| logging_simple             | 6.28 us                                                     | 6.42 us: 1.02x slower                                                       |
| logging_format             | 6.72 us                                                     | 6.87 us: 1.02x slower                                                       |
| richards_super             | 32.1 ms                                                     | 33.0 ms: 1.03x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 19.0 us: 1.03x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.1 ms: 1.03x slower                                                       |
| comprehensions             | 14.1 us                                                     | 14.6 us: 1.03x slower                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1.05 ms: 1.03x slower                                                       |
| meteor_contest             | 74.6 ms                                                     | 77.1 ms: 1.03x slower                                                       |
| pycparser                  | 699 ms                                                      | 722 ms: 1.03x slower                                                        |
| 2to3                       | 218 ms                                                      | 226 ms: 1.03x slower                                                        |
| pickle_list                | 2.83 us                                                     | 2.93 us: 1.04x slower                                                       |
| xml_etree_process          | 37.7 ms                                                     | 39.1 ms: 1.04x slower                                                       |
| aiohttp                    | 884 us                                                      | 919 us: 1.04x slower                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 67.8 ms: 1.04x slower                                                       |
| sympy_sum                  | 91.5 ms                                                     | 95.3 ms: 1.04x slower                                                       |
| sqlglot_parse              | 804 us                                                      | 838 us: 1.04x slower                                                        |
| unpickle                   | 8.18 us                                                     | 8.54 us: 1.04x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.88 us: 1.05x slower                                                       |
| sqlglot_normalize          | 187 ms                                                      | 196 ms: 1.05x slower                                                        |
| mako                       | 7.09 ms                                                     | 7.47 ms: 1.05x slower                                                       |
| float                      | 56.8 ms                                                     | 60.0 ms: 1.06x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.76 sec: 1.06x slower                                                      |
| chaos                      | 43.3 ms                                                     | 45.9 ms: 1.06x slower                                                       |
| deepcopy_memo              | 23.7 us                                                     | 25.1 us: 1.06x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.1 ms: 1.06x slower                                                       |
| sympy_str                  | 175 ms                                                      | 186 ms: 1.06x slower                                                        |
| mdp                        | 1.37 sec                                                    | 1.47 sec: 1.07x slower                                                      |
| crypto_pyaes               | 48.5 ms                                                     | 52.1 ms: 1.07x slower                                                       |
| pprint_pformat             | 1.05 sec                                                    | 1.13 sec: 1.08x slower                                                      |
| pprint_safe_repr           | 513 ms                                                      | 553 ms: 1.08x slower                                                        |
| sympy_integrate            | 13.0 ms                                                     | 14.1 ms: 1.09x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 37.9 ms: 1.10x slower                                                       |
| sympy_expand               | 284 ms                                                      | 312 ms: 1.10x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 18.1 ms: 1.11x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.52 sec: 1.11x slower                                                      |
| coverage                   | 40.8 ms                                                     | 46.0 ms: 1.13x slower                                                       |
| go                         | 91.6 ms                                                     | 104 ms: 1.14x slower                                                        |
| nqueens                    | 62.8 ms                                                     | 72.0 ms: 1.15x slower                                                       |
| scimark_fft                | 184 ms                                                      | 212 ms: 1.15x slower                                                        |
| pyflate                    | 295 ms                                                      | 341 ms: 1.16x slower                                                        |
| nbody                      | 71.9 ms                                                     | 83.2 ms: 1.16x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 92.4 ms: 1.17x slower                                                       |
| deltablue                  | 2.16 ms                                                     | 2.54 ms: 1.18x slower                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 52.2 ms: 1.19x slower                                                       |
| fannkuch                   | 247 ms                                                      | 296 ms: 1.20x slower                                                        |
| telco                      | 4.13 ms                                                     | 4.96 ms: 1.20x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 915 us: 1.22x slower                                                        |
| regex_compile              | 87.5 ms                                                     | 107 ms: 1.23x slower                                                        |
| unpickle_pure_python       | 133 us                                                      | 169 us: 1.27x slower                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 3.28 ms: 1.28x slower                                                       |
| spectral_norm              | 66.9 ms                                                     | 86.6 ms: 1.29x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 5.54 ms: 1.35x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 81.2 ms: 1.38x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (3): asyncio_tcp, json_loads, deepcopy_reduce
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.78% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown