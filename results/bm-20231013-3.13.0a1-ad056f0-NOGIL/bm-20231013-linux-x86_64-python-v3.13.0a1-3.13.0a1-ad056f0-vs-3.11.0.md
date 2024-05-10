# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a1
- machine: linux-x86_64
- commit hash: ad056f0
- commit date: 2023-10-13
- overall geometric mean: 1.02x slower
- HPT reliability: 74.50%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.59x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.04x slower                                       |
| chameleon      | 6.70 ms                                                | 7.13 ms: 1.06x slower                                      |
| docutils       | 2.66 sec                                               | 2.71 sec: 1.02x slower                                     |
| html5lib       | 64.8 ms                                                | 67.3 ms: 1.04x slower                                      |
| tornado_http   | 98.1 ms                                                | 99.1 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|---------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none           | 528 ms                                                 | 446 ms: 1.18x faster                                       |
| async_tree_memoization    | 639 ms                                                 | 572 ms: 1.12x faster                                       |
| async_tree_io             | 1.29 sec                                               | 1.21 sec: 1.06x faster                                     |
| async_tree_none_tg        | 491 ms                                                 | 463 ms: 1.06x faster                                       |
| async_tree_io_tg          | 1.29 sec                                               | 1.25 sec: 1.04x faster                                     |
| async_tree_cpu_io_mixed   | 749 ms                                                 | 726 ms: 1.03x faster                                       |
| async_tree_memoization_tg | 626 ms                                                 | 610 ms: 1.03x faster                                       |
| Geometric mean            | (ref)                                                  | 1.06x faster                                               |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                       |
| float          | 78.9 ms                                                | 83.4 ms: 1.06x slower                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 142 ms: 1.01x slower                                       |
| regex_effbot   | 3.51 ms                                                | 3.56 ms: 1.02x slower                                      |
| regex_dna      | 205 ms                                                 | 209 ms: 1.02x slower                                       |
| regex_v8       | 22.9 ms                                                | 25.3 ms: 1.10x slower                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                      |
| unpickle_pure_python | 242 us                                                 | 226 us: 1.07x faster                                       |
| json_loads           | 29.2 us                                                | 27.9 us: 1.05x faster                                      |
| pickle_pure_python   | 320 us                                                 | 307 us: 1.04x faster                                       |
| unpickle_list        | 5.21 us                                                | 5.08 us: 1.03x faster                                      |
| tomli_loads          | 2.30 sec                                               | 2.25 sec: 1.03x faster                                     |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                       |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                       |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                      |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 60.5 ms: 1.06x slower                                      |
| unpickle             | 13.8 us                                                | 14.9 us: 1.08x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.7 ms: 1.08x slower                                      |
| pickle_list          | 4.59 us                                                | 5.21 us: 1.14x slower                                      |
| Geometric mean       | (ref)                                                  | 1.00x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.05 ms: 1.17x slower                                      |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.21x slower                                      |
| Geometric mean         | (ref)                                                  | 1.19x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.0 ms: 1.03x faster                                      |
| genshi_text     | 22.5 ms                                                | 23.1 ms: 1.02x slower                                      |
| django_template | 33.5 ms                                                | 34.7 ms: 1.03x slower                                      |
| mako            | 10.7 ms                                                | 11.7 ms: 1.10x slower                                      |
| Geometric mean  | (ref)                                                  | 1.03x slower                                               |

All benchmarks:
===============

| Benchmark                 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0 |
|---------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols  | 520 us                                                 | 153 us: 3.38x faster                                       |
| generators                | 74.9 ms                                                | 29.5 ms: 2.54x faster                                      |
| asyncio_tcp               | 875 ms                                                 | 498 ms: 1.76x faster                                       |
| asyncio_tcp_ssl           | 3.11 sec                                               | 1.83 sec: 1.70x faster                                     |
| pylint                    | 476 ms                                                 | 328 ms: 1.45x faster                                       |
| json_dumps                | 13.3 ms                                                | 10.5 ms: 1.27x faster                                      |
| async_tree_none           | 528 ms                                                 | 446 ms: 1.18x faster                                       |
| deltablue                 | 3.92 ms                                                | 3.40 ms: 1.15x faster                                      |
| coroutines                | 27.0 ms                                                | 23.7 ms: 1.14x faster                                      |
| chaos                     | 71.9 ms                                                | 64.0 ms: 1.12x faster                                      |
| async_tree_memoization    | 639 ms                                                 | 572 ms: 1.12x faster                                       |
| richards_super            | 61.9 ms                                                | 56.0 ms: 1.11x faster                                      |
| comprehensions            | 23.6 us                                                | 21.5 us: 1.10x faster                                      |
| sqlglot_parse             | 1.43 ms                                                | 1.31 ms: 1.09x faster                                      |
| nqueens                   | 87.9 ms                                                | 81.0 ms: 1.09x faster                                      |
| raytrace                  | 309 ms                                                 | 285 ms: 1.08x faster                                       |
| mdp                       | 2.77 sec                                               | 2.58 sec: 1.08x faster                                     |
| hexiom                    | 6.89 ms                                                | 6.40 ms: 1.08x faster                                      |
| sqlglot_transpile         | 1.75 ms                                                | 1.63 ms: 1.07x faster                                      |
| unpickle_pure_python      | 242 us                                                 | 226 us: 1.07x faster                                       |
| async_tree_io             | 1.29 sec                                               | 1.21 sec: 1.06x faster                                     |
| async_tree_none_tg        | 491 ms                                                 | 463 ms: 1.06x faster                                       |
| sympy_sum                 | 169 ms                                                 | 160 ms: 1.05x faster                                       |
| json_loads                | 29.2 us                                                | 27.9 us: 1.05x faster                                      |
| sympy_expand              | 484 ms                                                 | 463 ms: 1.05x faster                                       |
| sqlglot_normalize         | 113 ms                                                 | 108 ms: 1.04x faster                                       |
| pickle_pure_python        | 320 us                                                 | 307 us: 1.04x faster                                       |
| sympy_str                 | 297 ms                                                 | 286 ms: 1.04x faster                                       |
| async_tree_io_tg          | 1.29 sec                                               | 1.25 sec: 1.04x faster                                     |
| sympy_integrate           | 21.5 ms                                                | 20.8 ms: 1.03x faster                                      |
| logging_simple            | 6.22 us                                                | 6.02 us: 1.03x faster                                      |
| async_tree_cpu_io_mixed   | 749 ms                                                 | 726 ms: 1.03x faster                                       |
| genshi_xml                | 53.4 ms                                                | 52.0 ms: 1.03x faster                                      |
| async_tree_memoization_tg | 626 ms                                                 | 610 ms: 1.03x faster                                       |
| unpickle_list             | 5.21 us                                                | 5.08 us: 1.03x faster                                      |
| tomli_loads               | 2.30 sec                                               | 2.25 sec: 1.03x faster                                     |
| xml_etree_parse           | 164 ms                                                 | 160 ms: 1.03x faster                                       |
| logging_silent            | 111 ns                                                 | 109 ns: 1.02x faster                                       |
| pidigits                  | 194 ms                                                 | 190 ms: 1.02x faster                                       |
| crypto_pyaes              | 76.7 ms                                                | 75.1 ms: 1.02x faster                                      |
| scimark_sparse_mat_mult   | 5.03 ms                                                | 4.93 ms: 1.02x faster                                      |
| go                        | 149 ms                                                 | 146 ms: 1.02x faster                                       |
| logging_format            | 6.81 us                                                | 6.71 us: 1.01x faster                                      |
| deepcopy_memo             | 40.2 us                                                | 39.6 us: 1.01x faster                                      |
| sqlglot_optimize          | 55.3 ms                                                | 54.5 ms: 1.01x faster                                      |
| deepcopy                  | 365 us                                                 | 361 us: 1.01x faster                                       |
| xml_etree_iterparse       | 108 ms                                                 | 107 ms: 1.01x faster                                       |
| pprint_pformat            | 1.55 sec                                               | 1.54 sec: 1.01x faster                                     |
| scimark_monte_carlo       | 70.7 ms                                                | 70.2 ms: 1.01x faster                                      |
| bench_mp_pool             | 24.0 ms                                                | 23.9 ms: 1.01x faster                                      |
| bench_thread_pool         | 834 us                                                 | 833 us: 1.00x faster                                       |
| regex_compile             | 141 ms                                                 | 142 ms: 1.01x slower                                       |
| pprint_safe_repr          | 747 ms                                                 | 752 ms: 1.01x slower                                       |
| tornado_http              | 98.1 ms                                                | 99.1 ms: 1.01x slower                                      |
| meteor_contest            | 109 ms                                                 | 111 ms: 1.01x slower                                       |
| regex_effbot              | 3.51 ms                                                | 3.56 ms: 1.02x slower                                      |
| docutils                  | 2.66 sec                                               | 2.71 sec: 1.02x slower                                     |
| regex_dna                 | 205 ms                                                 | 209 ms: 1.02x slower                                       |
| pickle_dict               | 34.6 us                                                | 35.4 us: 1.02x slower                                      |
| genshi_text               | 22.5 ms                                                | 23.1 ms: 1.02x slower                                      |
| asyncio_websockets        | 550 ms                                                 | 563 ms: 1.02x slower                                       |
| django_template           | 33.5 ms                                                | 34.7 ms: 1.03x slower                                      |
| gc_traversal              | 4.01 ms                                                | 4.15 ms: 1.04x slower                                      |
| fannkuch                  | 405 ms                                                 | 420 ms: 1.04x slower                                       |
| html5lib                  | 64.8 ms                                                | 67.3 ms: 1.04x slower                                      |
| 2to3                      | 264 ms                                                 | 276 ms: 1.04x slower                                       |
| scimark_sor               | 121 ms                                                 | 127 ms: 1.05x slower                                       |
| create_gc_cycles          | 1.43 ms                                                | 1.50 ms: 1.05x slower                                      |
| pycparser                 | 1.19 sec                                               | 1.24 sec: 1.05x slower                                     |
| aiohttp                   | 1.12 ms                                                | 1.18 ms: 1.06x slower                                      |
| pathlib                   | 18.5 ms                                                | 19.6 ms: 1.06x slower                                      |
| float                     | 78.9 ms                                                | 83.4 ms: 1.06x slower                                      |
| dulwich_log               | 64.6 ms                                                | 68.5 ms: 1.06x slower                                      |
| pickle                    | 11.0 us                                                | 11.7 us: 1.06x slower                                      |
| xml_etree_process         | 56.9 ms                                                | 60.5 ms: 1.06x slower                                      |
| gunicorn                  | 1.20 ms                                                | 1.27 ms: 1.06x slower                                      |
| chameleon                 | 6.70 ms                                                | 7.13 ms: 1.06x slower                                      |
| spectral_norm             | 108 ms                                                 | 116 ms: 1.08x slower                                       |
| unpickle                  | 13.8 us                                                | 14.9 us: 1.08x slower                                      |
| xml_etree_generate        | 81.1 ms                                                | 87.7 ms: 1.08x slower                                      |
| scimark_fft               | 345 ms                                                 | 375 ms: 1.08x slower                                       |
| mako                      | 10.7 ms                                                | 11.7 ms: 1.10x slower                                      |
| regex_v8                  | 22.9 ms                                                | 25.3 ms: 1.10x slower                                      |
| pyflate                   | 434 ms                                                 | 482 ms: 1.11x slower                                       |
| pickle_list               | 4.59 us                                                | 5.21 us: 1.14x slower                                      |
| python_startup_no_site    | 6.01 ms                                                | 7.05 ms: 1.17x slower                                      |
| flaskblogging             | 7.28 ms                                                | 8.77 ms: 1.20x slower                                      |
| sqlite_synth              | 2.57 us                                                | 3.11 us: 1.21x slower                                      |
| python_startup            | 8.56 ms                                                | 10.4 ms: 1.21x slower                                      |
| telco                     | 6.86 ms                                                | 8.41 ms: 1.23x slower                                      |
| mypy2                     | 686 ms                                                 | 863 ms: 1.26x slower                                       |
| async_generators          | 374 ms                                                 | 472 ms: 1.26x slower                                       |
| dask                      | 365 ms                                                 | 544 ms: 1.49x slower                                       |
| coverage                  | 78.8 ms                                                | 700 ms: 8.89x slower                                       |
| thrift                    | 784 us                                                 | 9.24 ms: 11.78x slower                                     |
| Geometric mean            | (ref)                                                  | 1.02x slower                                               |

Benchmark hidden because not significant (6): deepcopy_reduce, async_tree_cpu_io_mixed_tg, nbody, richards, json, scimark_lu
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: djangocms, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 74.50% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.59x