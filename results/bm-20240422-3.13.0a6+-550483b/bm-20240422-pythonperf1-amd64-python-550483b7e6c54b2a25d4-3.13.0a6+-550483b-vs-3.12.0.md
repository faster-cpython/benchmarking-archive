# Results vs. 3.12.0

- fork: python
- ref: 550483b7e6c54b2a25d4
- machine: windows-amd64
- commit hash: 550483b
- commit date: 2024-04-22
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 211 ms: 1.03x faster                                                        |
| chameleon      | 4.98 ms                                                     | 4.69 ms: 1.06x faster                                                       |
| tornado_http   | 89.5 ms                                                     | 81.7 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 269 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 226 ms: 1.29x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 222 ms: 1.29x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 394 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 624 ms: 1.24x faster                                                        |
| async_tree_io              | 731 ms                                                      | 597 ms: 1.22x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.27x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 51.9 ms: 1.09x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                        |
| nbody          | 71.9 ms                                                     | 69.6 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 77.8 ms: 1.12x faster                                                       |
| regex_dna      | 126 ms                                                      | 115 ms: 1.09x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 179 us: 1.09x faster                                                        |
| unpickle_pure_python | 133 us                                                      | 128 us: 1.04x faster                                                        |
| pickle               | 7.43 us                                                     | 7.17 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 63.6 ms: 1.02x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 55.0 ms: 1.02x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 91.7 ms: 1.01x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.64 ms: 1.01x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.5 us: 1.01x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.78 us: 1.01x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.40 sec: 1.03x slower                                                      |
| pickle_list          | 2.83 us                                                     | 3.06 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 19.5 ms                                                     | 19.7 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.30 ms: 1.12x faster                                                       |
| django_template | 22.9 ms                                                     | 21.9 ms: 1.05x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.08x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 269 ms: 1.36x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.8 us: 1.30x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 226 ms: 1.29x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 222 ms: 1.29x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 74.1 us: 1.28x faster                                                       |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 394 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 624 ms: 1.24x faster                                                        |
| async_tree_io              | 731 ms                                                      | 597 ms: 1.22x faster                                                        |
| mypy2                      | 509 ms                                                      | 418 ms: 1.22x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.73 sec: 1.21x faster                                                      |
| raytrace                   | 192 ms                                                      | 161 ms: 1.20x faster                                                        |
| mako                       | 7.09 ms                                                     | 6.30 ms: 1.12x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 77.8 ms: 1.12x faster                                                       |
| chaos                      | 43.3 ms                                                     | 38.7 ms: 1.12x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 39.6 ms: 1.12x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 81.7 ms: 1.10x faster                                                       |
| float                      | 56.8 ms                                                     | 51.9 ms: 1.09x faster                                                       |
| regex_dna                  | 126 ms                                                      | 115 ms: 1.09x faster                                                        |
| deepcopy_memo              | 23.7 us                                                     | 21.7 us: 1.09x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 1.98 ms: 1.09x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 40.0 ms: 1.09x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 179 us: 1.09x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.62 us: 1.09x faster                                                       |
| sympy_str                  | 175 ms                                                      | 161 ms: 1.09x faster                                                        |
| bench_mp_pool              | 69.2 ms                                                     | 63.7 ms: 1.09x faster                                                       |
| sympy_sum                  | 91.5 ms                                                     | 84.6 ms: 1.08x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                       |
| deepcopy                   | 238 us                                                      | 222 us: 1.07x faster                                                        |
| nqueens                    | 62.8 ms                                                     | 58.5 ms: 1.07x faster                                                       |
| hexiom                     | 4.10 ms                                                     | 3.84 ms: 1.07x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 45.4 ms: 1.07x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.69 ms: 1.06x faster                                                       |
| go                         | 91.6 ms                                                     | 86.3 ms: 1.06x faster                                                       |
| scimark_sor                | 78.8 ms                                                     | 74.2 ms: 1.06x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 760 us: 1.06x faster                                                        |
| bench_thread_pool          | 857 us                                                      | 810 us: 1.06x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.95 us: 1.05x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 76.5 ms: 1.05x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 994 ms: 1.05x faster                                                        |
| sqlglot_transpile          | 1.02 ms                                                     | 972 us: 1.05x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 489 ms: 1.05x faster                                                        |
| spectral_norm              | 66.9 ms                                                     | 63.8 ms: 1.05x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.41 us: 1.05x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 179 ms: 1.05x faster                                                        |
| django_template            | 22.9 ms                                                     | 21.9 ms: 1.05x faster                                                       |
| unpickle_pure_python       | 133 us                                                      | 128 us: 1.04x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.01 us: 1.04x faster                                                       |
| async_generators           | 239 ms                                                      | 230 ms: 1.04x faster                                                        |
| scimark_lu                 | 58.9 ms                                                     | 56.5 ms: 1.04x faster                                                       |
| sympy_integrate            | 13.0 ms                                                     | 12.5 ms: 1.04x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                       |
| sympy_expand               | 284 ms                                                      | 273 ms: 1.04x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.17 us: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                        |
| nbody                      | 71.9 ms                                                     | 69.6 ms: 1.03x faster                                                       |
| 2to3                       | 218 ms                                                      | 211 ms: 1.03x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 33.6 ms: 1.03x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 63.6 ms: 1.02x faster                                                       |
| richards                   | 28.4 ms                                                     | 27.7 ms: 1.02x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 59.1 ns: 1.02x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 73.0 ms: 1.02x faster                                                       |
| generators                 | 22.5 ms                                                     | 22.1 ms: 1.02x faster                                                       |
| richards_super             | 32.1 ms                                                     | 31.5 ms: 1.02x faster                                                       |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 55.0 ms: 1.02x faster                                                       |
| scimark_fft                | 184 ms                                                      | 182 ms: 1.01x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 91.7 ms: 1.01x faster                                                       |
| aiohttp                    | 884 us                                                      | 874 us: 1.01x faster                                                        |
| json_dumps                 | 5.70 ms                                                     | 5.64 ms: 1.01x faster                                                       |
| pickle_dict                | 18.4 us                                                     | 18.5 us: 1.01x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.78 us: 1.01x slower                                                       |
| python_startup             | 19.5 ms                                                     | 19.7 ms: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.40 sec: 1.03x slower                                                      |
| fannkuch                   | 247 ms                                                      | 255 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.70 ms: 1.06x slower                                                       |
| pycparser                  | 699 ms                                                      | 741 ms: 1.06x slower                                                        |
| mdp                        | 1.37 sec                                                    | 1.46 sec: 1.07x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| pickle_list                | 2.83 us                                                     | 3.06 us: 1.08x slower                                                       |
| coverage                   | 40.8 ms                                                     | 46.0 ms: 1.13x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.89 ms: 1.19x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 898 us: 1.19x slower                                                        |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (7): asyncio_tcp, pyflate, python_startup_no_site, json, docutils, xml_etree_process, unpickle
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240422-3.13.0a6+-550483b/bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown