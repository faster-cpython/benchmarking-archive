# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 217 ms: 1.01x faster                                                      |
| chameleon      | 4.98 ms                                                     | 4.86 ms: 1.03x faster                                                     |
| docutils       | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                    |
| tornado_http   | 89.5 ms                                                     | 83.5 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                       | 1.02x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 201 ms: 1.42x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.39x faster                                                      |
| async_tree_none            | 291 ms                                                      | 213 ms: 1.37x faster                                                      |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 376 ms: 1.30x faster                                                      |
| async_tree_io              | 731 ms                                                      | 565 ms: 1.29x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 265 ms: 1.28x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 610 ms: 1.26x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.33x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 57.7 ms: 1.25x faster                                                     |
| float          | 56.8 ms                                                     | 47.3 ms: 1.20x faster                                                     |
| pidigits       | 152 ms                                                      | 146 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                       | 1.16x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 119 ms: 1.06x faster                                                      |
| regex_compile  | 87.5 ms                                                     | 83.3 ms: 1.05x faster                                                     |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                     |
| regex_v8       | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                       | 1.03x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.20 sec: 1.14x faster                                                    |
| pickle_pure_python   | 195 us                                                      | 174 us: 1.12x faster                                                      |
| xml_etree_iterparse  | 65.2 ms                                                     | 61.4 ms: 1.06x faster                                                     |
| xml_etree_generate   | 55.8 ms                                                     | 53.3 ms: 1.05x faster                                                     |
| xml_etree_process    | 37.7 ms                                                     | 36.3 ms: 1.04x faster                                                     |
| unpickle_pure_python | 133 us                                                      | 129 us: 1.04x faster                                                      |
| json_dumps           | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                     |
| xml_etree_parse      | 93.0 ms                                                     | 91.5 ms: 1.02x faster                                                     |
| pickle               | 7.43 us                                                     | 7.37 us: 1.01x faster                                                     |
| pickle_dict          | 18.4 us                                                     | 18.3 us: 1.01x faster                                                     |
| pickle_list          | 2.83 us                                                     | 2.91 us: 1.03x slower                                                     |
| json_loads           | 13.9 us                                                     | 14.4 us: 1.04x slower                                                     |
| unpickle             | 8.18 us                                                     | 8.70 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                              |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 22.3 ms: 1.15x slower                                                     |
| python_startup_no_site | 16.2 ms                                                     | 20.3 ms: 1.25x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.20x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 5.75 ms: 1.23x faster                                                     |
| django_template | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.12x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 201 ms: 1.42x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.39x faster                                                      |
| typing_runtime_protocols   | 95.1 us                                                     | 69.0 us: 1.38x faster                                                     |
| async_tree_none            | 291 ms                                                      | 213 ms: 1.37x faster                                                      |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.55 sec: 1.36x faster                                                    |
| spectral_norm              | 66.9 ms                                                     | 51.1 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 376 ms: 1.30x faster                                                      |
| async_tree_io              | 731 ms                                                      | 565 ms: 1.29x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 265 ms: 1.28x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 610 ms: 1.26x faster                                                      |
| comprehensions             | 14.1 us                                                     | 11.3 us: 1.25x faster                                                     |
| nbody                      | 71.9 ms                                                     | 57.7 ms: 1.25x faster                                                     |
| mako                       | 7.09 ms                                                     | 5.75 ms: 1.23x faster                                                     |
| float                      | 56.8 ms                                                     | 47.3 ms: 1.20x faster                                                     |
| generators                 | 22.5 ms                                                     | 19.3 ms: 1.16x faster                                                     |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.22 ms: 1.15x faster                                                     |
| logging_silent             | 60.5 ns                                                     | 52.8 ns: 1.15x faster                                                     |
| mypy2                      | 509 ms                                                      | 446 ms: 1.14x faster                                                      |
| tomli_loads                | 1.37 sec                                                    | 1.20 sec: 1.14x faster                                                    |
| pickle_pure_python         | 195 us                                                      | 174 us: 1.12x faster                                                      |
| coroutines                 | 14.3 ms                                                     | 12.8 ms: 1.11x faster                                                     |
| deepcopy_memo              | 23.7 us                                                     | 21.3 us: 1.11x faster                                                     |
| chaos                      | 43.3 ms                                                     | 39.0 ms: 1.11x faster                                                     |
| sqlite_synth               | 1.76 us                                                     | 1.59 us: 1.10x faster                                                     |
| crypto_pyaes               | 48.5 ms                                                     | 44.0 ms: 1.10x faster                                                     |
| deepcopy_reduce            | 2.09 us                                                     | 1.90 us: 1.10x faster                                                     |
| pprint_safe_repr           | 513 ms                                                      | 467 ms: 1.10x faster                                                      |
| deepcopy                   | 238 us                                                      | 217 us: 1.10x faster                                                      |
| pprint_pformat             | 1.05 sec                                                    | 953 ms: 1.10x faster                                                      |
| raytrace                   | 192 ms                                                      | 176 ms: 1.10x faster                                                      |
| scimark_monte_carlo        | 43.7 ms                                                     | 40.3 ms: 1.09x faster                                                     |
| scimark_fft                | 184 ms                                                      | 170 ms: 1.09x faster                                                      |
| logging_simple             | 6.28 us                                                     | 5.80 us: 1.08x faster                                                     |
| fannkuch                   | 247 ms                                                      | 229 ms: 1.08x faster                                                      |
| logging_format             | 6.72 us                                                     | 6.23 us: 1.08x faster                                                     |
| dulwich_log                | 44.3 ms                                                     | 41.2 ms: 1.07x faster                                                     |
| tornado_http               | 89.5 ms                                                     | 83.5 ms: 1.07x faster                                                     |
| deltablue                  | 2.16 ms                                                     | 2.02 ms: 1.07x faster                                                     |
| pyflate                    | 295 ms                                                      | 278 ms: 1.06x faster                                                      |
| xml_etree_iterparse        | 65.2 ms                                                     | 61.4 ms: 1.06x faster                                                     |
| regex_dna                  | 126 ms                                                      | 119 ms: 1.06x faster                                                      |
| sympy_str                  | 175 ms                                                      | 166 ms: 1.05x faster                                                      |
| asyncio_tcp                | 487 ms                                                      | 464 ms: 1.05x faster                                                      |
| regex_compile              | 87.5 ms                                                     | 83.3 ms: 1.05x faster                                                     |
| nqueens                    | 62.8 ms                                                     | 59.8 ms: 1.05x faster                                                     |
| xml_etree_generate         | 55.8 ms                                                     | 53.3 ms: 1.05x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 772 us: 1.04x faster                                                      |
| pathlib                    | 80.5 ms                                                     | 77.4 ms: 1.04x faster                                                     |
| pidigits                   | 152 ms                                                      | 146 ms: 1.04x faster                                                      |
| bench_thread_pool          | 857 us                                                      | 824 us: 1.04x faster                                                      |
| sympy_sum                  | 91.5 ms                                                     | 88.1 ms: 1.04x faster                                                     |
| xml_etree_process          | 37.7 ms                                                     | 36.3 ms: 1.04x faster                                                     |
| unpickle_pure_python       | 133 us                                                      | 129 us: 1.04x faster                                                      |
| json_dumps                 | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                     |
| sqlglot_normalize          | 187 ms                                                      | 181 ms: 1.03x faster                                                      |
| meteor_contest             | 74.6 ms                                                     | 72.3 ms: 1.03x faster                                                     |
| sqlglot_transpile          | 1.02 ms                                                     | 990 us: 1.03x faster                                                      |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                     |
| bench_mp_pool              | 69.2 ms                                                     | 67.3 ms: 1.03x faster                                                     |
| json                       | 3.05 ms                                                     | 2.97 ms: 1.03x faster                                                     |
| chameleon                  | 4.98 ms                                                     | 4.86 ms: 1.03x faster                                                     |
| django_template            | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                     |
| xml_etree_parse            | 93.0 ms                                                     | 91.5 ms: 1.02x faster                                                     |
| pickle                     | 7.43 us                                                     | 7.37 us: 1.01x faster                                                     |
| pickle_dict                | 18.4 us                                                     | 18.3 us: 1.01x faster                                                     |
| 2to3                       | 218 ms                                                      | 217 ms: 1.01x faster                                                      |
| async_generators           | 239 ms                                                      | 241 ms: 1.01x slower                                                      |
| gc_traversal               | 1.52 ms                                                     | 1.53 ms: 1.01x slower                                                     |
| go                         | 91.6 ms                                                     | 92.2 ms: 1.01x slower                                                     |
| mdp                        | 1.37 sec                                                    | 1.38 sec: 1.01x slower                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 34.9 ms: 1.01x slower                                                     |
| richards                   | 28.4 ms                                                     | 28.7 ms: 1.01x slower                                                     |
| docutils                   | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                    |
| aiohttp                    | 884 us                                                      | 899 us: 1.02x slower                                                      |
| sympy_integrate            | 13.0 ms                                                     | 13.2 ms: 1.02x slower                                                     |
| pickle_list                | 2.83 us                                                     | 2.91 us: 1.03x slower                                                     |
| regex_v8                   | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                     |
| json_loads                 | 13.9 us                                                     | 14.4 us: 1.04x slower                                                     |
| unpickle                   | 8.18 us                                                     | 8.70 us: 1.06x slower                                                     |
| scimark_sor                | 78.8 ms                                                     | 83.8 ms: 1.06x slower                                                     |
| hexiom                     | 4.10 ms                                                     | 4.53 ms: 1.11x slower                                                     |
| telco                      | 4.13 ms                                                     | 4.65 ms: 1.13x slower                                                     |
| create_gc_cycles           | 752 us                                                      | 855 us: 1.14x slower                                                      |
| coverage                   | 40.8 ms                                                     | 46.6 ms: 1.14x slower                                                     |
| python_startup             | 19.5 ms                                                     | 22.3 ms: 1.15x slower                                                     |
| unpack_sequence            | 37.5 ns                                                     | 45.6 ns: 1.22x slower                                                     |
| python_startup_no_site     | 16.2 ms                                                     | 20.3 ms: 1.25x slower                                                     |
| scimark_lu                 | 58.9 ms                                                     | 79.9 ms: 1.36x slower                                                     |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                              |

Benchmark hidden because not significant (4): unpickle_list, sympy_expand, richards_super, pycparser
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown