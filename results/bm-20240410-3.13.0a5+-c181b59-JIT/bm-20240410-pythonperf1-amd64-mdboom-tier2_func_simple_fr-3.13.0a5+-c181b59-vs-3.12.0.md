# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 220 ms: 1.01x slower                                                        |
| chameleon      | 4.98 ms                                                     | 4.68 ms: 1.06x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 83.7 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 216 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_none            | 291 ms                                                      | 223 ms: 1.31x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 609 ms: 1.27x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 389 ms: 1.26x faster                                                        |
| async_tree_io              | 731 ms                                                      | 589 ms: 1.24x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.29x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 57.5 ms: 1.25x faster                                                       |
| float          | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.16x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 116 ms: 1.09x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                       |
| regex_compile  | 87.5 ms                                                     | 86.6 ms: 1.01x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|---------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python  | 195 us                                                      | 172 us: 1.13x faster                                                        |
| tomli_loads         | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                      |
| xml_etree_iterparse | 65.2 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| xml_etree_generate  | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| pickle              | 7.43 us                                                     | 7.22 us: 1.03x faster                                                       |
| xml_etree_parse     | 93.0 ms                                                     | 90.7 ms: 1.03x faster                                                       |
| xml_etree_process   | 37.7 ms                                                     | 36.8 ms: 1.02x faster                                                       |
| json_dumps          | 5.70 ms                                                     | 5.59 ms: 1.02x faster                                                       |
| unpickle_list       | 2.75 us                                                     | 2.78 us: 1.01x slower                                                       |
| pickle_dict         | 18.4 us                                                     | 18.8 us: 1.02x slower                                                       |
| pickle_list         | 2.83 us                                                     | 2.99 us: 1.06x slower                                                       |
| unpickle            | 8.18 us                                                     | 9.07 us: 1.11x slower                                                       |
| Geometric mean      | (ref)                                                       | 1.02x faster                                                                |

Benchmark hidden because not significant (2): json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.5 ms: 1.11x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.15x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.71 ms: 1.24x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.52 sec: 1.38x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 216 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_none            | 291 ms                                                      | 223 ms: 1.31x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.8 us: 1.31x faster                                                       |
| typing_runtime_protocols   | 95.1 us                                                     | 73.1 us: 1.30x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 51.6 ms: 1.30x faster                                                       |
| async_tree_io_tg           | 771 ms                                                      | 609 ms: 1.27x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 389 ms: 1.26x faster                                                        |
| nbody                      | 71.9 ms                                                     | 57.5 ms: 1.25x faster                                                       |
| mako                       | 7.09 ms                                                     | 5.71 ms: 1.24x faster                                                       |
| async_tree_io              | 731 ms                                                      | 589 ms: 1.24x faster                                                        |
| float                      | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                       |
| raytrace                   | 192 ms                                                      | 165 ms: 1.17x faster                                                        |
| generators                 | 22.5 ms                                                     | 19.7 ms: 1.14x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 53.0 ns: 1.14x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.4 ms: 1.14x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 172 us: 1.13x faster                                                        |
| tomli_loads                | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                      |
| mypy2                      | 509 ms                                                      | 450 ms: 1.13x faster                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.26 ms: 1.13x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.1 us: 1.12x faster                                                       |
| chaos                      | 43.3 ms                                                     | 38.7 ms: 1.12x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.57 us: 1.12x faster                                                       |
| scimark_fft                | 184 ms                                                      | 166 ms: 1.11x faster                                                        |
| pprint_pformat             | 1.05 sec                                                    | 945 ms: 1.11x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.71 us: 1.10x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.12 us: 1.10x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.10x faster                                                       |
| pprint_safe_repr           | 513 ms                                                      | 470 ms: 1.09x faster                                                        |
| regex_dna                  | 126 ms                                                      | 116 ms: 1.09x faster                                                        |
| crypto_pyaes               | 48.5 ms                                                     | 44.5 ms: 1.09x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 41.0 ms: 1.08x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| pyflate                    | 295 ms                                                      | 274 ms: 1.08x faster                                                        |
| pathlib                    | 80.5 ms                                                     | 74.9 ms: 1.07x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 83.7 ms: 1.07x faster                                                       |
| fannkuch                   | 247 ms                                                      | 232 ms: 1.06x faster                                                        |
| chameleon                  | 4.98 ms                                                     | 4.68 ms: 1.06x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.97 us: 1.06x faster                                                       |
| richards                   | 28.4 ms                                                     | 26.7 ms: 1.06x faster                                                       |
| deepcopy                   | 238 us                                                      | 224 us: 1.06x faster                                                        |
| richards_super             | 32.1 ms                                                     | 30.2 ms: 1.06x faster                                                       |
| json                       | 3.05 ms                                                     | 2.88 ms: 1.06x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 811 us: 1.06x faster                                                        |
| xml_etree_generate         | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| sympy_str                  | 175 ms                                                      | 167 ms: 1.05x faster                                                        |
| regex_effbot               | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                       |
| asyncio_tcp                | 487 ms                                                      | 468 ms: 1.04x faster                                                        |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| meteor_contest             | 74.6 ms                                                     | 72.3 ms: 1.03x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 780 us: 1.03x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 181 ms: 1.03x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 88.9 ms: 1.03x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.22 us: 1.03x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 90.7 ms: 1.03x faster                                                       |
| xml_etree_process          | 37.7 ms                                                     | 36.8 ms: 1.02x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 67.6 ms: 1.02x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.59 ms: 1.02x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1.00 ms: 1.02x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 62.0 ms: 1.01x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 86.6 ms: 1.01x faster                                                       |
| async_generators           | 239 ms                                                      | 238 ms: 1.01x faster                                                        |
| sympy_expand               | 284 ms                                                      | 282 ms: 1.01x faster                                                        |
| regex_v8                   | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                                       |
| 2to3                       | 218 ms                                                      | 220 ms: 1.01x slower                                                        |
| unpickle_list              | 2.75 us                                                     | 2.78 us: 1.01x slower                                                       |
| go                         | 91.6 ms                                                     | 92.7 ms: 1.01x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.02x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                      |
| aiohttp                    | 884 us                                                      | 902 us: 1.02x slower                                                        |
| pickle_dict                | 18.4 us                                                     | 18.8 us: 1.02x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.56 ms: 1.02x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.3 ms: 1.03x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                      |
| scimark_sor                | 78.8 ms                                                     | 83.0 ms: 1.05x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.99 us: 1.06x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.41 ms: 1.07x slower                                                       |
| python_startup             | 19.5 ms                                                     | 21.5 ms: 1.11x slower                                                       |
| unpickle                   | 8.18 us                                                     | 9.07 us: 1.11x slower                                                       |
| coverage                   | 40.8 ms                                                     | 45.3 ms: 1.11x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.71 ms: 1.14x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 899 us: 1.20x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 71.0 ms: 1.21x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (4): pycparser, json_loads, unpickle_pure_python, deltablue
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown