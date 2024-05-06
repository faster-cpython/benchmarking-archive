# Results vs. 3.12.0

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 213 ms: 1.02x faster                                                        |
| chameleon      | 4.98 ms                                                     | 4.93 ms: 1.01x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.64 sec: 1.02x faster                                                      |
| tornado_http   | 89.5 ms                                                     | 83.5 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 218 ms: 1.31x faster                                                        |
| async_tree_none            | 291 ms                                                      | 227 ms: 1.28x faster                                                        |
| async_tree_io              | 731 ms                                                      | 582 ms: 1.26x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 272 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 393 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 626 ms: 1.23x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.28x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 51.7 ms: 1.10x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                        |
| nbody          | 71.9 ms                                                     | 69.8 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 78.5 ms: 1.12x faster                                                       |
| regex_dna      | 126 ms                                                      | 118 ms: 1.07x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.58 ms: 1.03x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 16.4 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 179 us: 1.09x faster                                                        |
| pickle               | 7.43 us                                                     | 7.21 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 63.4 ms: 1.03x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 55.5 ms: 1.01x faster                                                       |
| xml_etree_process    | 37.7 ms                                                     | 37.9 ms: 1.00x slower                                                       |
| json_dumps           | 5.70 ms                                                     | 5.73 ms: 1.01x slower                                                       |
| unpickle_pure_python | 133 us                                                      | 134 us: 1.01x slower                                                        |
| pickle_dict          | 18.4 us                                                     | 18.7 us: 1.02x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.83 us: 1.03x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.58 us: 1.05x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.97 us: 1.05x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.45 sec: 1.06x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 19.8 ms: 1.02x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 18.4 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 6.38 ms: 1.11x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 71.4 us: 1.33x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 218 ms: 1.31x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.9 us: 1.29x faster                                                       |
| async_tree_none            | 291 ms                                                      | 227 ms: 1.28x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.64 sec: 1.27x faster                                                      |
| async_tree_io              | 731 ms                                                      | 582 ms: 1.26x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 272 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 393 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 626 ms: 1.23x faster                                                        |
| mypy2                      | 509 ms                                                      | 426 ms: 1.20x faster                                                        |
| raytrace                   | 192 ms                                                      | 164 ms: 1.17x faster                                                        |
| chaos                      | 43.3 ms                                                     | 38.5 ms: 1.13x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 78.5 ms: 1.12x faster                                                       |
| mako                       | 7.09 ms                                                     | 6.38 ms: 1.11x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.1 ms: 1.10x faster                                                       |
| float                      | 56.8 ms                                                     | 51.7 ms: 1.10x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.6 us: 1.10x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.61 us: 1.09x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 179 us: 1.09x faster                                                        |
| scimark_lu                 | 58.9 ms                                                     | 54.1 ms: 1.09x faster                                                       |
| scimark_sor                | 78.8 ms                                                     | 72.5 ms: 1.09x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 40.3 ms: 1.09x faster                                                       |
| hexiom                     | 4.10 ms                                                     | 3.79 ms: 1.08x faster                                                       |
| generators                 | 22.5 ms                                                     | 20.9 ms: 1.08x faster                                                       |
| deepcopy                   | 238 us                                                      | 221 us: 1.08x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 56.1 ns: 1.08x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 64.3 ms: 1.08x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 83.5 ms: 1.07x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.3 ms: 1.07x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 58.8 ms: 1.07x faster                                                       |
| regex_dna                  | 126 ms                                                      | 118 ms: 1.07x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 85.8 ms: 1.07x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 45.5 ms: 1.06x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 63.0 ms: 1.06x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 809 us: 1.06x faster                                                        |
| sympy_str                  | 175 ms                                                      | 165 ms: 1.06x faster                                                        |
| pprint_pformat             | 1.05 sec                                                    | 989 ms: 1.06x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 488 ms: 1.05x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 1.99 us: 1.05x faster                                                       |
| scimark_fft                | 184 ms                                                      | 176 ms: 1.05x faster                                                        |
| logging_simple             | 6.28 us                                                     | 6.01 us: 1.04x faster                                                       |
| json                       | 3.05 ms                                                     | 2.92 ms: 1.04x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.07 ms: 1.04x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.45 us: 1.04x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 776 us: 1.04x faster                                                        |
| async_generators           | 239 ms                                                      | 231 ms: 1.04x faster                                                        |
| pathlib                    | 80.5 ms                                                     | 77.8 ms: 1.03x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 988 us: 1.03x faster                                                        |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.21 us: 1.03x faster                                                       |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                       |
| pycparser                  | 699 ms                                                      | 677 ms: 1.03x faster                                                        |
| nbody                      | 71.9 ms                                                     | 69.8 ms: 1.03x faster                                                       |
| pyflate                    | 295 ms                                                      | 286 ms: 1.03x faster                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 63.4 ms: 1.03x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.58 ms: 1.03x faster                                                       |
| 2to3                       | 218 ms                                                      | 213 ms: 1.02x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 183 ms: 1.02x faster                                                        |
| docutils                   | 1.66 sec                                                    | 1.64 sec: 1.02x faster                                                      |
| chameleon                  | 4.98 ms                                                     | 4.93 ms: 1.01x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 73.9 ms: 1.01x faster                                                       |
| go                         | 91.6 ms                                                     | 90.9 ms: 1.01x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 55.5 ms: 1.01x faster                                                       |
| sympy_expand               | 284 ms                                                      | 282 ms: 1.01x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 37.9 ms: 1.00x slower                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.73 ms: 1.01x slower                                                       |
| unpickle_pure_python       | 133 us                                                      | 134 us: 1.01x slower                                                        |
| fannkuch                   | 247 ms                                                      | 250 ms: 1.01x slower                                                        |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                       |
| python_startup             | 19.5 ms                                                     | 19.8 ms: 1.02x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 18.7 us: 1.02x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| unpickle_list              | 2.75 us                                                     | 2.83 us: 1.03x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.58 us: 1.05x slower                                                       |
| richards                   | 28.4 ms                                                     | 29.8 ms: 1.05x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.97 us: 1.05x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.45 sec: 1.06x slower                                                      |
| coverage                   | 40.8 ms                                                     | 45.7 ms: 1.12x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 18.4 ms: 1.13x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.4 ms: 1.15x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 884 us: 1.18x slower                                                        |
| telco                      | 4.13 ms                                                     | 5.04 ms: 1.22x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                                |

Benchmark hidden because not significant (7): asyncio_tcp, scimark_sparse_mat_mult, richards_super, sqlglot_optimize, aiohttp, xml_etree_parse, json_loads
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown