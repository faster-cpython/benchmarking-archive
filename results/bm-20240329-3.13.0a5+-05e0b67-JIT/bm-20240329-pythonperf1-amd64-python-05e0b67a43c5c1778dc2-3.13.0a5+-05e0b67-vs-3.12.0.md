# Results vs. 3.12.0

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-amd64
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 4.98 ms                                                     | 4.78 ms: 1.04x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 84.8 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 202 ms: 1.41x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.39x faster                                                        |
| async_tree_none            | 291 ms                                                      | 216 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 376 ms: 1.30x faster                                                        |
| async_tree_io              | 731 ms                                                      | 574 ms: 1.27x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 613 ms: 1.26x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.32x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 58.8 ms: 1.22x faster                                                       |
| float          | 56.8 ms                                                     | 47.0 ms: 1.21x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.15x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 116 ms: 1.09x faster                                                        |
| regex_compile  | 87.5 ms                                                     | 84.6 ms: 1.03x faster                                                       |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 16.4 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 175 us: 1.12x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 61.2 ms: 1.06x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 53.4 ms: 1.05x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 128 us: 1.04x faster                                                        |
| xml_etree_process    | 37.7 ms                                                     | 36.4 ms: 1.04x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 91.6 ms: 1.02x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.61 ms: 1.02x faster                                                       |
| pickle               | 7.43 us                                                     | 7.32 us: 1.02x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.80 us: 1.02x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.88 us: 1.02x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.72 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 22.6 ms: 1.16x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 20.2 ms: 1.24x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.20x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.09 ms                                                     | 5.84 ms: 1.21x faster                                                       |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.47 sec: 1.43x faster                                                      |
| async_tree_none_tg         | 285 ms                                                      | 202 ms: 1.41x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.39x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 70.1 us: 1.36x faster                                                       |
| async_tree_none            | 291 ms                                                      | 216 ms: 1.35x faster                                                        |
| spectral_norm              | 66.9 ms                                                     | 51.1 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 376 ms: 1.30x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.9 us: 1.29x faster                                                       |
| async_tree_io              | 731 ms                                                      | 574 ms: 1.27x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 613 ms: 1.26x faster                                                        |
| nbody                      | 71.9 ms                                                     | 58.8 ms: 1.22x faster                                                       |
| mako                       | 7.09 ms                                                     | 5.84 ms: 1.21x faster                                                       |
| float                      | 56.8 ms                                                     | 47.0 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.26 ms: 1.13x faster                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                      |
| logging_silent             | 60.5 ns                                                     | 53.6 ns: 1.13x faster                                                       |
| mypy2                      | 509 ms                                                      | 452 ms: 1.13x faster                                                        |
| generators                 | 22.5 ms                                                     | 20.1 ms: 1.12x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 175 us: 1.12x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.58 us: 1.12x faster                                                       |
| chaos                      | 43.3 ms                                                     | 39.1 ms: 1.11x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 43.9 ms: 1.11x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 12.9 ms: 1.10x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.7 ms: 1.10x faster                                                       |
| regex_dna                  | 126 ms                                                      | 116 ms: 1.09x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 1.93 us: 1.09x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.9 us: 1.08x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.9 ms: 1.08x faster                                                       |
| scimark_fft                | 184 ms                                                      | 171 ms: 1.08x faster                                                        |
| fannkuch                   | 247 ms                                                      | 228 ms: 1.08x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 479 ms: 1.07x faster                                                        |
| raytrace                   | 192 ms                                                      | 180 ms: 1.07x faster                                                        |
| deepcopy                   | 238 us                                                      | 223 us: 1.07x faster                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 61.2 ms: 1.06x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 985 ms: 1.06x faster                                                        |
| tornado_http               | 89.5 ms                                                     | 84.8 ms: 1.06x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.37 us: 1.05x faster                                                       |
| logging_simple             | 6.28 us                                                     | 5.96 us: 1.05x faster                                                       |
| pyflate                    | 295 ms                                                      | 281 ms: 1.05x faster                                                        |
| xml_etree_generate         | 55.8 ms                                                     | 53.4 ms: 1.05x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.06 ms: 1.05x faster                                                       |
| sympy_str                  | 175 ms                                                      | 168 ms: 1.04x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 87.7 ms: 1.04x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.78 ms: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 128 us: 1.04x faster                                                        |
| asyncio_tcp                | 487 ms                                                      | 470 ms: 1.04x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 36.4 ms: 1.04x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 84.6 ms: 1.03x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 778 us: 1.03x faster                                                        |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 77.9 ms: 1.03x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 60.9 ms: 1.03x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 67.4 ms: 1.03x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1000 us: 1.02x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 73.1 ms: 1.02x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 91.6 ms: 1.02x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.61 ms: 1.02x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.32 us: 1.02x faster                                                       |
| richards_super             | 32.1 ms                                                     | 31.6 ms: 1.02x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 184 ms: 1.01x faster                                                        |
| json_loads                 | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| sympy_expand               | 284 ms                                                      | 287 ms: 1.01x slower                                                        |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.80 us: 1.02x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.88 us: 1.02x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                      |
| go                         | 91.6 ms                                                     | 93.5 ms: 1.02x slower                                                       |
| aiohttp                    | 884 us                                                      | 905 us: 1.02x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 35.4 ms: 1.03x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.3 ms: 1.03x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| scimark_sor                | 78.8 ms                                                     | 81.3 ms: 1.03x slower                                                       |
| async_generators           | 239 ms                                                      | 247 ms: 1.03x slower                                                        |
| unpickle                   | 8.18 us                                                     | 8.72 us: 1.07x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.57 ms: 1.11x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.69 ms: 1.14x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 855 us: 1.14x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 16.4 ms: 1.15x slower                                                       |
| python_startup             | 19.5 ms                                                     | 22.6 ms: 1.16x slower                                                       |
| coverage                   | 40.8 ms                                                     | 47.4 ms: 1.16x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 70.9 ms: 1.20x slower                                                       |
| unpack_sequence            | 37.5 ns                                                     | 46.5 ns: 1.24x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 20.2 ms: 1.24x slower                                                       |
| json                       | 3.05 ms                                                     | 4.10 ms: 1.35x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                                |

Benchmark hidden because not significant (5): bench_thread_pool, richards, django_template, 2to3, pycparser
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-05e0b67-JIT/bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown