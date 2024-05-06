# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.04x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 220 ms: 1.01x slower                                                      |
| chameleon      | 4.98 ms                                                     | 4.74 ms: 1.05x faster                                                     |
| docutils       | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                    |
| tornado_http   | 89.5 ms                                                     | 83.9 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                       | 1.02x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 202 ms: 1.41x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                      |
| async_tree_none            | 291 ms                                                      | 216 ms: 1.35x faster                                                      |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 380 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 375 ms: 1.31x faster                                                      |
| async_tree_io              | 731 ms                                                      | 570 ms: 1.28x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 611 ms: 1.26x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.32x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 59.0 ms: 1.22x faster                                                     |
| float          | 56.8 ms                                                     | 47.2 ms: 1.20x faster                                                     |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                       | 1.15x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 118 ms: 1.07x faster                                                      |
| regex_effbot   | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                     |
| regex_compile  | 87.5 ms                                                     | 89.1 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 172 us: 1.14x faster                                                      |
| xml_etree_iterparse  | 65.2 ms                                                     | 61.3 ms: 1.06x faster                                                     |
| xml_etree_generate   | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| xml_etree_parse      | 93.0 ms                                                     | 89.6 ms: 1.04x faster                                                     |
| pickle               | 7.43 us                                                     | 7.16 us: 1.04x faster                                                     |
| tomli_loads          | 1.37 sec                                                    | 1.32 sec: 1.04x faster                                                    |
| json_dumps           | 5.70 ms                                                     | 5.57 ms: 1.02x faster                                                     |
| xml_etree_process    | 37.7 ms                                                     | 37.0 ms: 1.02x faster                                                     |
| pickle_list          | 2.83 us                                                     | 2.88 us: 1.02x slower                                                     |
| unpickle_pure_python | 133 us                                                      | 136 us: 1.02x slower                                                      |
| json_loads           | 13.9 us                                                     | 14.5 us: 1.05x slower                                                     |
| unpickle             | 8.18 us                                                     | 8.56 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (2): unpickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.9 ms: 1.13x slower                                                     |
| python_startup_no_site | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.08 ms: 1.17x faster                                                     |
| django_template | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.09x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 202 ms: 1.41x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                      |
| async_tree_none            | 291 ms                                                      | 216 ms: 1.35x faster                                                      |
| typing_runtime_protocols   | 95.1 us                                                     | 70.6 us: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 380 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 375 ms: 1.31x faster                                                      |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.63 sec: 1.29x faster                                                    |
| async_tree_io              | 731 ms                                                      | 570 ms: 1.28x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.27x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 611 ms: 1.26x faster                                                      |
| nbody                      | 71.9 ms                                                     | 59.0 ms: 1.22x faster                                                     |
| spectral_norm              | 66.9 ms                                                     | 55.6 ms: 1.20x faster                                                     |
| float                      | 56.8 ms                                                     | 47.2 ms: 1.20x faster                                                     |
| comprehensions             | 14.1 us                                                     | 12.0 us: 1.18x faster                                                     |
| mako                       | 7.09 ms                                                     | 6.08 ms: 1.17x faster                                                     |
| logging_silent             | 60.5 ns                                                     | 53.1 ns: 1.14x faster                                                     |
| pickle_pure_python         | 195 us                                                      | 172 us: 1.14x faster                                                      |
| mypy2                      | 509 ms                                                      | 453 ms: 1.13x faster                                                      |
| generators                 | 22.5 ms                                                     | 20.3 ms: 1.11x faster                                                     |
| sqlite_synth               | 1.76 us                                                     | 1.60 us: 1.10x faster                                                     |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.09x faster                                                     |
| deepcopy                   | 238 us                                                      | 219 us: 1.09x faster                                                      |
| dulwich_log                | 44.3 ms                                                     | 40.9 ms: 1.08x faster                                                     |
| chaos                      | 43.3 ms                                                     | 40.1 ms: 1.08x faster                                                     |
| deepcopy_reduce            | 2.09 us                                                     | 1.94 us: 1.08x faster                                                     |
| raytrace                   | 192 ms                                                      | 178 ms: 1.08x faster                                                      |
| crypto_pyaes               | 48.5 ms                                                     | 44.9 ms: 1.08x faster                                                     |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.38 ms: 1.07x faster                                                     |
| regex_dna                  | 126 ms                                                      | 118 ms: 1.07x faster                                                      |
| deltablue                  | 2.16 ms                                                     | 2.02 ms: 1.07x faster                                                     |
| tornado_http               | 89.5 ms                                                     | 83.9 ms: 1.07x faster                                                     |
| deepcopy_memo              | 23.7 us                                                     | 22.3 us: 1.06x faster                                                     |
| xml_etree_iterparse        | 65.2 ms                                                     | 61.3 ms: 1.06x faster                                                     |
| xml_etree_generate         | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| chameleon                  | 4.98 ms                                                     | 4.74 ms: 1.05x faster                                                     |
| sympy_sum                  | 91.5 ms                                                     | 87.9 ms: 1.04x faster                                                     |
| sympy_str                  | 175 ms                                                      | 168 ms: 1.04x faster                                                      |
| regex_effbot               | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                     |
| xml_etree_parse            | 93.0 ms                                                     | 89.6 ms: 1.04x faster                                                     |
| pathlib                    | 80.5 ms                                                     | 77.5 ms: 1.04x faster                                                     |
| pickle                     | 7.43 us                                                     | 7.16 us: 1.04x faster                                                     |
| logging_simple             | 6.28 us                                                     | 6.05 us: 1.04x faster                                                     |
| scimark_fft                | 184 ms                                                      | 178 ms: 1.04x faster                                                      |
| tomli_loads                | 1.37 sec                                                    | 1.32 sec: 1.04x faster                                                    |
| pprint_safe_repr           | 513 ms                                                      | 496 ms: 1.04x faster                                                      |
| bench_thread_pool          | 857 us                                                      | 828 us: 1.03x faster                                                      |
| scimark_monte_carlo        | 43.7 ms                                                     | 42.3 ms: 1.03x faster                                                     |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                      |
| logging_format             | 6.72 us                                                     | 6.51 us: 1.03x faster                                                     |
| bench_mp_pool              | 69.2 ms                                                     | 67.3 ms: 1.03x faster                                                     |
| sqlglot_normalize          | 187 ms                                                      | 182 ms: 1.03x faster                                                      |
| json_dumps                 | 5.70 ms                                                     | 5.57 ms: 1.02x faster                                                     |
| xml_etree_process          | 37.7 ms                                                     | 37.0 ms: 1.02x faster                                                     |
| django_template            | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                     |
| meteor_contest             | 74.6 ms                                                     | 73.4 ms: 1.02x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 796 us: 1.01x faster                                                      |
| pprint_pformat             | 1.05 sec                                                    | 1.03 sec: 1.01x faster                                                    |
| sqlglot_transpile          | 1.02 ms                                                     | 1.01 ms: 1.01x faster                                                     |
| pyflate                    | 295 ms                                                      | 296 ms: 1.01x slower                                                      |
| 2to3                       | 218 ms                                                      | 220 ms: 1.01x slower                                                      |
| nqueens                    | 62.8 ms                                                     | 63.6 ms: 1.01x slower                                                     |
| docutils                   | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                    |
| regex_compile              | 87.5 ms                                                     | 89.1 ms: 1.02x slower                                                     |
| async_generators           | 239 ms                                                      | 244 ms: 1.02x slower                                                      |
| sympy_expand               | 284 ms                                                      | 290 ms: 1.02x slower                                                      |
| pickle_list                | 2.83 us                                                     | 2.88 us: 1.02x slower                                                     |
| aiohttp                    | 884 us                                                      | 903 us: 1.02x slower                                                      |
| unpickle_pure_python       | 133 us                                                      | 136 us: 1.02x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 35.3 ms: 1.02x slower                                                     |
| sympy_integrate            | 13.0 ms                                                     | 13.4 ms: 1.03x slower                                                     |
| pycparser                  | 699 ms                                                      | 725 ms: 1.04x slower                                                      |
| json_loads                 | 13.9 us                                                     | 14.5 us: 1.05x slower                                                     |
| unpickle                   | 8.18 us                                                     | 8.56 us: 1.05x slower                                                     |
| go                         | 91.6 ms                                                     | 96.7 ms: 1.06x slower                                                     |
| fannkuch                   | 247 ms                                                      | 263 ms: 1.07x slower                                                      |
| scimark_sor                | 78.8 ms                                                     | 84.1 ms: 1.07x slower                                                     |
| richards_super             | 32.1 ms                                                     | 34.4 ms: 1.07x slower                                                     |
| richards                   | 28.4 ms                                                     | 31.0 ms: 1.09x slower                                                     |
| coverage                   | 40.8 ms                                                     | 44.7 ms: 1.10x slower                                                     |
| mdp                        | 1.37 sec                                                    | 1.54 sec: 1.12x slower                                                    |
| python_startup             | 19.5 ms                                                     | 21.9 ms: 1.13x slower                                                     |
| create_gc_cycles           | 752 us                                                      | 851 us: 1.13x slower                                                      |
| telco                      | 4.13 ms                                                     | 4.91 ms: 1.19x slower                                                     |
| python_startup_no_site     | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                     |
| hexiom                     | 4.10 ms                                                     | 5.22 ms: 1.27x slower                                                     |
| scimark_lu                 | 58.9 ms                                                     | 75.5 ms: 1.28x slower                                                     |
| unpack_sequence            | 37.5 ns                                                     | 57.5 ns: 1.53x slower                                                     |
| Geometric mean             | (ref)                                                       | 1.04x faster                                                              |

Benchmark hidden because not significant (6): asyncio_tcp, unpickle_list, regex_v8, gc_traversal, pickle_dict, json
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown