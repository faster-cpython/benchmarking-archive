# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 211 ms: 1.03x faster                                                        |
| chameleon      | 4.98 ms                                                     | 4.91 ms: 1.01x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.64 sec: 1.01x faster                                                      |
| tornado_http   | 89.5 ms                                                     | 81.8 ms: 1.09x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 273 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 387 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 227 ms: 1.28x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 223 ms: 1.28x faster                                                        |
| async_tree_io              | 731 ms                                                      | 592 ms: 1.23x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 275 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 398 ms: 1.23x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 628 ms: 1.23x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.27x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 53.0 ms: 1.07x faster                                                       |
| pidigits       | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| nbody          | 71.9 ms                                                     | 72.4 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 79.7 ms: 1.10x faster                                                       |
| regex_dna      | 126 ms                                                      | 125 ms: 1.01x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 15.4 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 183 us: 1.07x faster                                                        |
| pickle               | 7.43 us                                                     | 7.20 us: 1.03x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| unpickle_list        | 2.75 us                                                     | 2.72 us: 1.01x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 56.2 ms: 1.01x slower                                                       |
| json_dumps           | 5.70 ms                                                     | 5.76 ms: 1.01x slower                                                       |
| xml_etree_process    | 37.7 ms                                                     | 38.2 ms: 1.01x slower                                                       |
| unpickle_pure_python | 133 us                                                      | 135 us: 1.02x slower                                                        |
| tomli_loads          | 1.37 sec                                                    | 1.42 sec: 1.04x slower                                                      |
| unpickle             | 8.18 us                                                     | 8.54 us: 1.04x slower                                                       |
| pickle_list          | 2.83 us                                                     | 3.22 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 16.9 ms: 1.04x slower                                                       |
| python_startup         | 19.5 ms                                                     | 20.4 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.46 ms: 1.10x faster                                                       |
| django_template | 22.9 ms                                                     | 22.4 ms: 1.03x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.06x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 273 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 387 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 227 ms: 1.28x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 223 ms: 1.28x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 74.9 us: 1.27x faster                                                       |
| comprehensions             | 14.1 us                                                     | 11.1 us: 1.27x faster                                                       |
| async_tree_io              | 731 ms                                                      | 592 ms: 1.23x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 275 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 398 ms: 1.23x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 628 ms: 1.23x faster                                                        |
| mypy2                      | 509 ms                                                      | 415 ms: 1.23x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.72 sec: 1.22x faster                                                      |
| raytrace                   | 192 ms                                                      | 172 ms: 1.12x faster                                                        |
| dulwich_log                | 44.3 ms                                                     | 39.7 ms: 1.12x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 79.7 ms: 1.10x faster                                                       |
| mako                       | 7.09 ms                                                     | 6.46 ms: 1.10x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 81.8 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.61 us: 1.09x faster                                                       |
| generators                 | 22.5 ms                                                     | 20.7 ms: 1.09x faster                                                       |
| chaos                      | 43.3 ms                                                     | 39.8 ms: 1.09x faster                                                       |
| sympy_str                  | 175 ms                                                      | 162 ms: 1.08x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 85.0 ms: 1.08x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 64.3 ms: 1.08x faster                                                       |
| float                      | 56.8 ms                                                     | 53.0 ms: 1.07x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 75.4 ms: 1.07x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 183 us: 1.07x faster                                                        |
| json                       | 3.05 ms                                                     | 2.87 ms: 1.06x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 59.2 ms: 1.06x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 45.7 ms: 1.06x faster                                                       |
| deepcopy                   | 238 us                                                      | 226 us: 1.05x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 57.4 ns: 1.05x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.6 ms: 1.05x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 178 ms: 1.05x faster                                                        |
| bench_thread_pool          | 857 us                                                      | 815 us: 1.05x faster                                                        |
| spectral_norm              | 66.9 ms                                                     | 64.2 ms: 1.04x faster                                                       |
| logging_simple             | 6.28 us                                                     | 6.03 us: 1.04x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 1.01 sec: 1.04x faster                                                      |
| pprint_safe_repr           | 513 ms                                                      | 494 ms: 1.04x faster                                                        |
| async_generators           | 239 ms                                                      | 231 ms: 1.04x faster                                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 42.1 ms: 1.04x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.47 us: 1.04x faster                                                       |
| scimark_lu                 | 58.9 ms                                                     | 56.9 ms: 1.04x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 988 us: 1.03x faster                                                        |
| sympy_expand               | 284 ms                                                      | 275 ms: 1.03x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.20 us: 1.03x faster                                                       |
| 2to3                       | 218 ms                                                      | 211 ms: 1.03x faster                                                        |
| pidigits                   | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| sqlglot_parse              | 804 us                                                      | 781 us: 1.03x faster                                                        |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                       |
| asyncio_tcp                | 487 ms                                                      | 474 ms: 1.03x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.03 us: 1.03x faster                                                       |
| hexiom                     | 4.10 ms                                                     | 3.99 ms: 1.03x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.10 ms: 1.03x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.6 ms: 1.03x faster                                                       |
| django_template            | 22.9 ms                                                     | 22.4 ms: 1.03x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 23.1 us: 1.02x faster                                                       |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| docutils                   | 1.66 sec                                                    | 1.64 sec: 1.01x faster                                                      |
| regex_dna                  | 126 ms                                                      | 125 ms: 1.01x faster                                                        |
| chameleon                  | 4.98 ms                                                     | 4.91 ms: 1.01x faster                                                       |
| mdp                        | 1.37 sec                                                    | 1.36 sec: 1.01x faster                                                      |
| unpickle_list              | 2.75 us                                                     | 2.72 us: 1.01x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                       |
| pyflate                    | 295 ms                                                      | 293 ms: 1.01x faster                                                        |
| meteor_contest             | 74.6 ms                                                     | 74.3 ms: 1.00x faster                                                       |
| scimark_sor                | 78.8 ms                                                     | 79.1 ms: 1.00x slower                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 56.2 ms: 1.01x slower                                                       |
| nbody                      | 71.9 ms                                                     | 72.4 ms: 1.01x slower                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.76 ms: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| xml_etree_process          | 37.7 ms                                                     | 38.2 ms: 1.01x slower                                                       |
| unpickle_pure_python       | 133 us                                                      | 135 us: 1.02x slower                                                        |
| richards_super             | 32.1 ms                                                     | 33.2 ms: 1.03x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.42 sec: 1.04x slower                                                      |
| python_startup_no_site     | 16.2 ms                                                     | 16.9 ms: 1.04x slower                                                       |
| richards                   | 28.4 ms                                                     | 29.5 ms: 1.04x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.54 us: 1.04x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.4 ms: 1.05x slower                                                       |
| fannkuch                   | 247 ms                                                      | 259 ms: 1.05x slower                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.70 ms: 1.06x slower                                                       |
| pycparser                  | 699 ms                                                      | 754 ms: 1.08x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 15.4 ms: 1.08x slower                                                       |
| coverage                   | 40.8 ms                                                     | 45.8 ms: 1.12x slower                                                       |
| pickle_list                | 2.83 us                                                     | 3.22 us: 1.14x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 901 us: 1.20x slower                                                        |
| telco                      | 4.13 ms                                                     | 5.00 ms: 1.21x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (6): xml_etree_iterparse, go, xml_etree_parse, pickle_dict, scimark_fft, aiohttp
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown