# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 223 ms: 1.02x slower                                                        |
| chameleon      | 4.98 ms                                                     | 4.64 ms: 1.07x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 84.0 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 201 ms: 1.42x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 261 ms: 1.40x faster                                                        |
| async_tree_none            | 291 ms                                                      | 213 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 372 ms: 1.32x faster                                                        |
| async_tree_io              | 731 ms                                                      | 563 ms: 1.30x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 600 ms: 1.28x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 266 ms: 1.28x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.34x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 58.8 ms: 1.22x faster                                                       |
| float          | 56.8 ms                                                     | 46.8 ms: 1.21x faster                                                       |
| pidigits       | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.15x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 83.3 ms: 1.05x faster                                                       |
| regex_dna      | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 17.6 ms: 1.24x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.19 sec: 1.15x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 175 us: 1.12x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 53.5 ms: 1.04x faster                                                       |
| xml_etree_process    | 37.7 ms                                                     | 36.5 ms: 1.03x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                       |
| unpickle_list        | 2.75 us                                                     | 2.67 us: 1.03x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 130 us: 1.03x faster                                                        |
| pickle               | 7.43 us                                                     | 7.27 us: 1.02x faster                                                       |
| unpickle             | 8.18 us                                                     | 8.53 us: 1.04x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.96 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 22.5 ms: 1.16x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 20.4 ms: 1.25x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.20x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 5.61 ms: 1.26x faster                                                       |
| django_template | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.13x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 201 ms: 1.42x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 261 ms: 1.40x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.52 sec: 1.38x faster                                                      |
| async_tree_none            | 291 ms                                                      | 213 ms: 1.37x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 69.4 us: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 372 ms: 1.32x faster                                                        |
| spectral_norm              | 66.9 ms                                                     | 51.4 ms: 1.30x faster                                                       |
| async_tree_io              | 731 ms                                                      | 563 ms: 1.30x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 600 ms: 1.28x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 266 ms: 1.28x faster                                                        |
| mako                       | 7.09 ms                                                     | 5.61 ms: 1.26x faster                                                       |
| comprehensions             | 14.1 us                                                     | 11.3 us: 1.25x faster                                                       |
| nbody                      | 71.9 ms                                                     | 58.8 ms: 1.22x faster                                                       |
| float                      | 56.8 ms                                                     | 46.8 ms: 1.21x faster                                                       |
| generators                 | 22.5 ms                                                     | 19.5 ms: 1.16x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 52.7 ns: 1.15x faster                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.19 sec: 1.15x faster                                                      |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.24 ms: 1.14x faster                                                       |
| mypy2                      | 509 ms                                                      | 448 ms: 1.14x faster                                                        |
| pickle_pure_python         | 195 us                                                      | 175 us: 1.12x faster                                                        |
| chaos                      | 43.3 ms                                                     | 38.9 ms: 1.11x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.58 us: 1.11x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.4 ms: 1.11x faster                                                       |
| scimark_fft                | 184 ms                                                      | 167 ms: 1.10x faster                                                        |
| deepcopy_memo              | 23.7 us                                                     | 21.6 us: 1.10x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.92 us: 1.09x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.6 ms: 1.09x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 44.6 ms: 1.09x faster                                                       |
| raytrace                   | 192 ms                                                      | 178 ms: 1.08x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 475 ms: 1.08x faster                                                        |
| fannkuch                   | 247 ms                                                      | 229 ms: 1.08x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 972 ms: 1.08x faster                                                        |
| deltablue                  | 2.16 ms                                                     | 2.01 ms: 1.07x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.64 ms: 1.07x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.29 us: 1.07x faster                                                       |
| deepcopy                   | 238 us                                                      | 223 us: 1.07x faster                                                        |
| tornado_http               | 89.5 ms                                                     | 84.0 ms: 1.07x faster                                                       |
| logging_simple             | 6.28 us                                                     | 5.91 us: 1.06x faster                                                       |
| sympy_str                  | 175 ms                                                      | 165 ms: 1.06x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 86.8 ms: 1.05x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 83.3 ms: 1.05x faster                                                       |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 53.5 ms: 1.04x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 822 us: 1.04x faster                                                        |
| sqlglot_parse              | 804 us                                                      | 772 us: 1.04x faster                                                        |
| pyflate                    | 295 ms                                                      | 283 ms: 1.04x faster                                                        |
| pycparser                  | 699 ms                                                      | 671 ms: 1.04x faster                                                        |
| pidigits                   | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| sqlglot_transpile          | 1.02 ms                                                     | 986 us: 1.04x faster                                                        |
| pathlib                    | 80.5 ms                                                     | 77.8 ms: 1.03x faster                                                       |
| xml_etree_process          | 37.7 ms                                                     | 36.5 ms: 1.03x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                       |
| unpickle_list              | 2.75 us                                                     | 2.67 us: 1.03x faster                                                       |
| asyncio_tcp                | 487 ms                                                      | 473 ms: 1.03x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 130 us: 1.03x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.27 us: 1.02x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 73.2 ms: 1.02x faster                                                       |
| django_template            | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 184 ms: 1.02x faster                                                        |
| nqueens                    | 62.8 ms                                                     | 61.9 ms: 1.01x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                       |
| docutils                   | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                      |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| go                         | 91.6 ms                                                     | 93.0 ms: 1.02x slower                                                       |
| aiohttp                    | 884 us                                                      | 898 us: 1.02x slower                                                        |
| sympy_integrate            | 13.0 ms                                                     | 13.2 ms: 1.02x slower                                                       |
| richards_super             | 32.1 ms                                                     | 32.7 ms: 1.02x slower                                                       |
| 2to3                       | 218 ms                                                      | 223 ms: 1.02x slower                                                        |
| scimark_sor                | 78.8 ms                                                     | 80.5 ms: 1.02x slower                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 70.8 ms: 1.02x slower                                                       |
| richards                   | 28.4 ms                                                     | 29.1 ms: 1.02x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 35.5 ms: 1.03x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| async_generators           | 239 ms                                                      | 248 ms: 1.04x slower                                                        |
| unpickle                   | 8.18 us                                                     | 8.53 us: 1.04x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.96 us: 1.05x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.61 ms: 1.12x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 853 us: 1.13x slower                                                        |
| telco                      | 4.13 ms                                                     | 4.74 ms: 1.15x slower                                                       |
| coverage                   | 40.8 ms                                                     | 47.0 ms: 1.15x slower                                                       |
| python_startup             | 19.5 ms                                                     | 22.5 ms: 1.16x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 69.1 ms: 1.17x slower                                                       |
| unpack_sequence            | 37.5 ns                                                     | 44.0 ns: 1.17x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 17.6 ms: 1.24x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 20.4 ms: 1.25x slower                                                       |
| json                       | 3.05 ms                                                     | 3.88 ms: 1.27x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_dict, sympy_expand, json_loads
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown