# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 303 ms: 1.06x slower                                                       |
| chameleon      | 7.23 ms                                                      | 7.52 ms: 1.04x slower                                                      |
| docutils       | 2.87 sec                                                     | 3.11 sec: 1.08x slower                                                     |
| tornado_http   | 121 ms                                                       | 124 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                        | 1.05x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 343 ms: 1.26x faster                                                       |
| async_tree_none            | 452 ms                                                       | 362 ms: 1.25x faster                                                       |
| async_tree_memoization_tg  | 540 ms                                                       | 443 ms: 1.22x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 584 ms: 1.19x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 891 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 600 ms: 1.16x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 912 ms: 1.16x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                       |
| float          | 76.6 ms                                                      | 78.6 ms: 1.03x slower                                                      |
| nbody          | 88.0 ms                                                      | 103 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                        | 1.06x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 245 ms: 1.03x slower                                                       |
| regex_effbot   | 3.57 ms                                                      | 3.69 ms: 1.03x slower                                                      |
| regex_compile  | 144 ms                                                       | 151 ms: 1.05x slower                                                       |
| regex_v8       | 23.6 ms                                                      | 25.8 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                        | 1.05x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.7 us: 1.06x faster                                                      |
| unpickle_list        | 4.66 us                                                      | 4.56 us: 1.02x faster                                                      |
| pickle_pure_python   | 318 us                                                       | 313 us: 1.02x faster                                                       |
| pickle               | 10.5 us                                                      | 10.4 us: 1.01x faster                                                      |
| xml_etree_generate   | 86.1 ms                                                      | 86.0 ms: 1.00x faster                                                      |
| xml_etree_process    | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                      |
| pickle_list          | 4.43 us                                                      | 4.49 us: 1.01x slower                                                      |
| xml_etree_iterparse  | 103 ms                                                       | 105 ms: 1.02x slower                                                       |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                      |
| json_loads           | 24.4 us                                                      | 25.6 us: 1.05x slower                                                      |
| tomli_loads          | 2.16 sec                                                     | 2.36 sec: 1.09x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 244 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                      |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                      |
| django_template | 38.2 ms                                                      | 39.7 ms: 1.04x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 119 us: 1.27x faster                                                       |
| async_tree_none_tg         | 431 ms                                                       | 343 ms: 1.26x faster                                                       |
| async_tree_none            | 452 ms                                                       | 362 ms: 1.25x faster                                                       |
| async_tree_memoization_tg  | 540 ms                                                       | 443 ms: 1.22x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 584 ms: 1.19x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 891 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 600 ms: 1.16x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 912 ms: 1.16x faster                                                       |
| generators                 | 37.4 ms                                                      | 33.1 ms: 1.13x faster                                                      |
| comprehensions             | 21.9 us                                                      | 20.4 us: 1.07x faster                                                      |
| pickle_dict                | 32.5 us                                                      | 30.7 us: 1.06x faster                                                      |
| coroutines                 | 23.0 ms                                                      | 22.5 ms: 1.02x faster                                                      |
| unpickle_list              | 4.66 us                                                      | 4.56 us: 1.02x faster                                                      |
| pickle_pure_python         | 318 us                                                       | 313 us: 1.02x faster                                                       |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.01x faster                                                       |
| logging_format             | 7.48 us                                                      | 7.38 us: 1.01x faster                                                      |
| sqlite_synth               | 2.77 us                                                      | 2.74 us: 1.01x faster                                                      |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                       |
| pickle                     | 10.5 us                                                      | 10.4 us: 1.01x faster                                                      |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                     |
| xml_etree_generate         | 86.1 ms                                                      | 86.0 ms: 1.00x faster                                                      |
| xml_etree_process          | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                      |
| crypto_pyaes               | 80.3 ms                                                      | 81.1 ms: 1.01x slower                                                      |
| pickle_list                | 4.43 us                                                      | 4.49 us: 1.01x slower                                                      |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                       |
| pathlib                    | 18.9 ms                                                      | 19.2 ms: 1.02x slower                                                      |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                     |
| tornado_http               | 121 ms                                                       | 124 ms: 1.02x slower                                                       |
| mako                       | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                      |
| xml_etree_iterparse        | 103 ms                                                       | 105 ms: 1.02x slower                                                       |
| regex_dna                  | 239 ms                                                       | 245 ms: 1.03x slower                                                       |
| float                      | 76.6 ms                                                      | 78.6 ms: 1.03x slower                                                      |
| raytrace                   | 298 ms                                                       | 306 ms: 1.03x slower                                                       |
| sqlglot_transpile          | 1.78 ms                                                      | 1.83 ms: 1.03x slower                                                      |
| sqlglot_parse              | 1.38 ms                                                      | 1.42 ms: 1.03x slower                                                      |
| mdp                        | 2.57 sec                                                     | 2.65 sec: 1.03x slower                                                     |
| regex_effbot               | 3.57 ms                                                      | 3.69 ms: 1.03x slower                                                      |
| dask                       | 392 ms                                                       | 406 ms: 1.03x slower                                                       |
| django_template            | 38.2 ms                                                      | 39.7 ms: 1.04x slower                                                      |
| chameleon                  | 7.23 ms                                                      | 7.52 ms: 1.04x slower                                                      |
| bench_mp_pool              | 4.76 ms                                                      | 4.96 ms: 1.04x slower                                                      |
| sqlglot_normalize          | 116 ms                                                       | 121 ms: 1.04x slower                                                       |
| sympy_expand               | 484 ms                                                       | 505 ms: 1.04x slower                                                       |
| regex_compile              | 144 ms                                                       | 151 ms: 1.05x slower                                                       |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                      |
| deepcopy_memo              | 36.8 us                                                      | 38.5 us: 1.05x slower                                                      |
| meteor_contest             | 128 ms                                                       | 134 ms: 1.05x slower                                                       |
| logging_silent             | 94.4 ns                                                      | 99.0 ns: 1.05x slower                                                      |
| json_loads                 | 24.4 us                                                      | 25.6 us: 1.05x slower                                                      |
| json                       | 5.12 ms                                                      | 5.40 ms: 1.06x slower                                                      |
| sympy_integrate            | 23.9 ms                                                      | 25.4 ms: 1.06x slower                                                      |
| dulwich_log                | 65.4 ms                                                      | 69.4 ms: 1.06x slower                                                      |
| 2to3                       | 285 ms                                                       | 303 ms: 1.06x slower                                                       |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.50 ms: 1.07x slower                                                      |
| deepcopy                   | 368 us                                                       | 395 us: 1.07x slower                                                       |
| spectral_norm              | 91.6 ms                                                      | 99.0 ms: 1.08x slower                                                      |
| docutils                   | 2.87 sec                                                     | 3.11 sec: 1.08x slower                                                     |
| pprint_pformat             | 1.65 sec                                                     | 1.79 sec: 1.08x slower                                                     |
| regex_v8                   | 23.6 ms                                                      | 25.8 ms: 1.09x slower                                                      |
| chaos                      | 64.0 ms                                                      | 69.8 ms: 1.09x slower                                                      |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                      |
| tomli_loads                | 2.16 sec                                                     | 2.36 sec: 1.09x slower                                                     |
| sqlglot_optimize           | 57.5 ms                                                      | 62.9 ms: 1.10x slower                                                      |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.10x slower                                                      |
| pprint_safe_repr           | 807 ms                                                       | 902 ms: 1.12x slower                                                       |
| scimark_monte_carlo        | 69.0 ms                                                      | 77.9 ms: 1.13x slower                                                      |
| create_gc_cycles           | 1.59 ms                                                      | 1.80 ms: 1.13x slower                                                      |
| scimark_fft                | 301 ms                                                       | 341 ms: 1.13x slower                                                       |
| telco                      | 6.96 ms                                                      | 8.10 ms: 1.16x slower                                                      |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                      |
| unpickle_pure_python       | 210 us                                                       | 244 us: 1.16x slower                                                       |
| fannkuch                   | 350 ms                                                       | 408 ms: 1.17x slower                                                       |
| nbody                      | 88.0 ms                                                      | 103 ms: 1.17x slower                                                       |
| richards_super             | 51.3 ms                                                      | 60.2 ms: 1.17x slower                                                      |
| richards                   | 45.7 ms                                                      | 53.7 ms: 1.17x slower                                                      |
| deltablue                  | 3.24 ms                                                      | 3.80 ms: 1.17x slower                                                      |
| bench_thread_pool          | 950 us                                                       | 1.12 ms: 1.18x slower                                                      |
| pyflate                    | 439 ms                                                       | 522 ms: 1.19x slower                                                       |
| coverage                   | 66.7 ms                                                      | 80.3 ms: 1.20x slower                                                      |
| nqueens                    | 89.9 ms                                                      | 109 ms: 1.21x slower                                                       |
| go                         | 150 ms                                                       | 182 ms: 1.22x slower                                                       |
| gc_traversal               | 3.48 ms                                                      | 4.36 ms: 1.25x slower                                                      |
| scimark_lu                 | 98.8 ms                                                      | 130 ms: 1.31x slower                                                       |
| hexiom                     | 5.96 ms                                                      | 8.00 ms: 1.34x slower                                                      |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                      |
| scimark_sor                | 109 ms                                                       | 160 ms: 1.47x slower                                                       |
| unpack_sequence            | 53.2 ns                                                      | 107 ns: 2.00x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                               |

Benchmark hidden because not significant (8): async_generators, unpickle, sympy_str, sympy_sum, deepcopy_reduce, mypy2, logging_simple, xml_etree_parse
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 0.99x