# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 214 ms: 1.02x faster                                                        |
| chameleon      | 4.98 ms                                                     | 4.80 ms: 1.04x faster                                                       |
| tornado_http   | 89.5 ms                                                     | 92.1 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 274 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.30x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 224 ms: 1.27x faster                                                        |
| async_tree_none            | 291 ms                                                      | 231 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 398 ms: 1.23x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 631 ms: 1.22x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 278 ms: 1.22x faster                                                        |
| async_tree_io              | 731 ms                                                      | 612 ms: 1.19x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.25x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 51.6 ms: 1.10x faster                                                       |
| pidigits       | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| nbody          | 71.9 ms                                                     | 70.9 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 80.0 ms: 1.09x faster                                                       |
| regex_dna      | 126 ms                                                      | 125 ms: 1.01x faster                                                        |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 180 us: 1.09x faster                                                        |
| unpickle_pure_python | 133 us                                                      | 130 us: 1.03x faster                                                        |
| xml_etree_parse      | 93.0 ms                                                     | 91.4 ms: 1.02x faster                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 64.3 ms: 1.01x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 55.2 ms: 1.01x faster                                                       |
| pickle               | 7.43 us                                                     | 7.37 us: 1.01x faster                                                       |
| unpickle_list        | 2.75 us                                                     | 2.77 us: 1.01x slower                                                       |
| json_dumps           | 5.70 ms                                                     | 5.76 ms: 1.01x slower                                                       |
| json_loads           | 13.9 us                                                     | 14.2 us: 1.02x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.45 us: 1.03x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.43 sec: 1.05x slower                                                      |
| pickle_list          | 2.83 us                                                     | 2.97 us: 1.05x slower                                                       |
| pickle_dict          | 18.4 us                                                     | 19.8 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 17.3 ms: 1.07x slower                                                       |
| python_startup         | 19.5 ms                                                     | 21.0 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.09 ms                                                     | 6.35 ms: 1.12x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 274 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.30x faster                                                        |
| comprehensions             | 14.1 us                                                     | 11.1 us: 1.27x faster                                                       |
| async_tree_none_tg         | 285 ms                                                      | 224 ms: 1.27x faster                                                        |
| async_tree_none            | 291 ms                                                      | 231 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 398 ms: 1.23x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 631 ms: 1.22x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 278 ms: 1.22x faster                                                        |
| async_tree_io              | 731 ms                                                      | 612 ms: 1.19x faster                                                        |
| mypy2                      | 509 ms                                                      | 429 ms: 1.19x faster                                                        |
| raytrace                   | 192 ms                                                      | 166 ms: 1.16x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.84 sec: 1.14x faster                                                      |
| logging_silent             | 60.5 ns                                                     | 53.2 ns: 1.14x faster                                                       |
| mako                       | 7.09 ms                                                     | 6.35 ms: 1.12x faster                                                       |
| chaos                      | 43.3 ms                                                     | 39.0 ms: 1.11x faster                                                       |
| float                      | 56.8 ms                                                     | 51.6 ms: 1.10x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.3 ms: 1.10x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 80.0 ms: 1.09x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.09x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 61.4 ms: 1.09x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 180 us: 1.09x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.63 us: 1.08x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.00 ms: 1.08x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 22.1 us: 1.07x faster                                                       |
| sympy_sum                  | 91.5 ms                                                     | 85.5 ms: 1.07x faster                                                       |
| sympy_str                  | 175 ms                                                      | 164 ms: 1.07x faster                                                        |
| crypto_pyaes               | 48.5 ms                                                     | 45.6 ms: 1.06x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.2 ms: 1.06x faster                                                       |
| pprint_safe_repr           | 513 ms                                                      | 487 ms: 1.05x faster                                                        |
| pprint_pformat             | 1.05 sec                                                    | 993 ms: 1.05x faster                                                        |
| generators                 | 22.5 ms                                                     | 21.5 ms: 1.05x faster                                                       |
| deepcopy                   | 238 us                                                      | 227 us: 1.05x faster                                                        |
| go                         | 91.6 ms                                                     | 87.5 ms: 1.05x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 60.1 ms: 1.05x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 771 us: 1.04x faster                                                        |
| hexiom                     | 4.10 ms                                                     | 3.94 ms: 1.04x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.80 ms: 1.04x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 987 us: 1.04x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 181 ms: 1.03x faster                                                        |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                       |
| richards                   | 28.4 ms                                                     | 27.6 ms: 1.03x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.53 us: 1.03x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 72.6 ms: 1.03x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 2.04 us: 1.03x faster                                                       |
| pidigits                   | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 130 us: 1.03x faster                                                        |
| richards_super             | 32.1 ms                                                     | 31.3 ms: 1.03x faster                                                       |
| scimark_lu                 | 58.9 ms                                                     | 57.4 ms: 1.03x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 836 us: 1.02x faster                                                        |
| scimark_fft                | 184 ms                                                      | 181 ms: 1.02x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 91.4 ms: 1.02x faster                                                       |
| 2to3                       | 218 ms                                                      | 214 ms: 1.02x faster                                                        |
| sympy_expand               | 284 ms                                                      | 279 ms: 1.02x faster                                                        |
| logging_simple             | 6.28 us                                                     | 6.18 us: 1.02x faster                                                       |
| nbody                      | 71.9 ms                                                     | 70.9 ms: 1.01x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 64.3 ms: 1.01x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 55.2 ms: 1.01x faster                                                       |
| scimark_sor                | 78.8 ms                                                     | 77.8 ms: 1.01x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.37 us: 1.01x faster                                                       |
| regex_dna                  | 126 ms                                                      | 125 ms: 1.01x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 34.3 ms: 1.01x faster                                                       |
| unpickle_list              | 2.75 us                                                     | 2.77 us: 1.01x slower                                                       |
| pathlib                    | 80.5 ms                                                     | 81.3 ms: 1.01x slower                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.76 ms: 1.01x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.39 sec: 1.01x slower                                                      |
| fannkuch                   | 247 ms                                                      | 252 ms: 1.02x slower                                                        |
| json_loads                 | 13.9 us                                                     | 14.2 us: 1.02x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.56 ms: 1.03x slower                                                       |
| tornado_http               | 89.5 ms                                                     | 92.1 ms: 1.03x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.45 us: 1.03x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.43 sec: 1.05x slower                                                      |
| pickle_list                | 2.83 us                                                     | 2.97 us: 1.05x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 17.3 ms: 1.07x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 19.8 us: 1.08x slower                                                       |
| python_startup             | 19.5 ms                                                     | 21.0 ms: 1.08x slower                                                       |
| aiohttp                    | 884 us                                                      | 955 us: 1.08x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                       |
| coverage                   | 40.8 ms                                                     | 45.2 ms: 1.11x slower                                                       |
| pycparser                  | 699 ms                                                      | 780 ms: 1.12x slower                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 108 us: 1.13x slower                                                        |
| telco                      | 4.13 ms                                                     | 4.89 ms: 1.18x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 910 us: 1.21x slower                                                        |
| asyncio_tcp                | 487 ms                                                      | 664 ms: 1.36x slower                                                        |
| Geometric mean             | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (9): async_generators, scimark_sparse_mat_mult, xml_etree_process, django_template, pyflate, docutils, regex_effbot, json, bench_mp_pool
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown