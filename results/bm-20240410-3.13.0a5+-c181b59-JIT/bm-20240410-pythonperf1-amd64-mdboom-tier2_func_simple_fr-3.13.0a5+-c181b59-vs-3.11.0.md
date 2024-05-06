# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 220 ms: 1.03x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.68 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                      |
| html5lib       | 38.9 ms                                                     | 35.2 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 83.7 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                        |
| async_tree_none            | 332 ms                                                      | 223 ms: 1.49x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 216 ms: 1.43x faster                                                        |
| async_tree_io              | 808 ms                                                      | 589 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 609 ms: 1.36x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.42x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 57.5 ms: 1.22x faster                                                       |
| float          | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 86.6 ms: 1.05x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.59 ms: 1.45x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 132 us: 1.18x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.7 ms: 1.08x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.0 ms: 1.01x slower                                                       |
| pickle_dict          | 18.5 us                                                     | 18.8 us: 1.02x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.78 us: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.22 us: 1.09x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.99 us: 1.11x slower                                                       |
| unpickle             | 7.57 us                                                     | 9.07 us: 1.20x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.5 ms: 1.09x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 19.6 ms: 1.16x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 5.71 ms: 1.33x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 15.4 ms: 1.19x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 34.7 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                       | 1.22x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 73.1 us: 4.46x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.7 ms: 1.73x faster                                                       |
| pylint                     | 323 ms                                                      | 195 ms: 1.66x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 468 ms: 1.55x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                        |
| async_tree_none            | 332 ms                                                      | 223 ms: 1.49x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.59 ms: 1.45x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.8 us: 1.45x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 216 ms: 1.43x faster                                                        |
| async_tree_io              | 808 ms                                                      | 589 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 609 ms: 1.36x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 53.0 ns: 1.35x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.52 sec: 1.33x faster                                                      |
| mako                       | 7.58 ms                                                     | 5.71 ms: 1.33x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 51.6 ms: 1.32x faster                                                       |
| raytrace                   | 213 ms                                                      | 165 ms: 1.30x faster                                                        |
| richards_super             | 38.7 ms                                                     | 30.2 ms: 1.28x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.7 ms: 1.25x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.16 ms: 1.25x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 21.1 us: 1.23x faster                                                       |
| nbody                      | 70.3 ms                                                     | 57.5 ms: 1.22x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 780 us: 1.22x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.71 us: 1.20x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 15.4 ms: 1.19x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 132 us: 1.18x faster                                                        |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.4 ms: 1.18x faster                                                       |
| richards                   | 31.4 ms                                                     | 26.7 ms: 1.18x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.12 us: 1.17x faster                                                       |
| float                      | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.00 ms: 1.16x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 34.7 ms: 1.15x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 945 ms: 1.15x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                                       |
| pyflate                    | 312 ms                                                      | 274 ms: 1.14x faster                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.26 ms: 1.14x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 41.0 ms: 1.13x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 88.9 ms: 1.13x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 470 ms: 1.13x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.68 ms: 1.12x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.12x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.43 sec: 1.11x faster                                                      |
| sympy_str                  | 185 ms                                                      | 167 ms: 1.11x faster                                                        |
| tornado_http               | 92.8 ms                                                     | 83.7 ms: 1.11x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 35.2 ms: 1.10x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 62.0 ms: 1.10x faster                                                       |
| deepcopy                   | 246 us                                                      | 224 us: 1.10x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 44.5 ms: 1.10x faster                                                       |
| fannkuch                   | 253 ms                                                      | 232 ms: 1.09x faster                                                        |
| go                         | 101 ms                                                      | 92.7 ms: 1.09x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| scimark_fft                | 179 ms                                                      | 166 ms: 1.08x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 90.7 ms: 1.08x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 811 us: 1.08x faster                                                        |
| sympy_expand               | 299 ms                                                      | 282 ms: 1.06x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 13.3 ms: 1.06x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 86.6 ms: 1.05x faster                                                       |
| pycparser                  | 720 ms                                                      | 686 ms: 1.05x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 181 ms: 1.05x faster                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 1.97 us: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.3 ms: 1.04x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 4.41 ms: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| mypy2                      | 459 ms                                                      | 450 ms: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.0 ms: 1.01x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.01x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 18.8 us: 1.02x slower                                                       |
| aiohttp                    | 883 us                                                      | 902 us: 1.02x slower                                                        |
| 2to3                       | 214 ms                                                      | 220 ms: 1.03x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.3 ms: 1.04x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 74.9 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 83.0 ms: 1.06x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.6 ms: 1.07x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.78 us: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.22 us: 1.09x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.5 ms: 1.09x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.99 us: 1.11x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 71.0 ms: 1.13x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.71 ms: 1.16x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 19.6 ms: 1.16x slower                                                       |
| unpickle                   | 7.57 us                                                     | 9.07 us: 1.20x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 899 us: 1.26x slower                                                        |
| async_generators           | 177 ms                                                      | 238 ms: 1.34x slower                                                        |
| thrift                     | 494 us                                                      | 8.68 ms: 17.57x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (2): json, regex_dna
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown