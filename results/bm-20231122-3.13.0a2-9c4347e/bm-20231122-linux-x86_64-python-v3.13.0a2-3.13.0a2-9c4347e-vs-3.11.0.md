# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a2
- machine: linux-x86_64
- commit hash: 9c4347e
- commit date: 2023-11-22
- overall geometric mean: 1.03x faster
- HPT reliability: 90.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                       |
| chameleon      | 6.70 ms                                                | 6.93 ms: 1.03x slower                                      |
| docutils       | 2.66 sec                                               | 2.69 sec: 1.01x slower                                     |
| html5lib       | 64.8 ms                                                | 66.3 ms: 1.02x slower                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|---------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none           | 528 ms                                                 | 451 ms: 1.17x faster                                       |
| async_tree_memoization    | 639 ms                                                 | 583 ms: 1.10x faster                                       |
| async_tree_io             | 1.29 sec                                               | 1.22 sec: 1.05x faster                                     |
| async_tree_none_tg        | 491 ms                                                 | 471 ms: 1.04x faster                                       |
| async_tree_io_tg          | 1.29 sec                                               | 1.26 sec: 1.03x faster                                     |
| async_tree_cpu_io_mixed   | 749 ms                                                 | 733 ms: 1.02x faster                                       |
| async_tree_memoization_tg | 626 ms                                                 | 618 ms: 1.01x faster                                       |
| Geometric mean            | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.0 ms: 1.05x faster                                      |
| pidigits       | 194 ms                                                 | 197 ms: 1.02x slower                                       |
| float          | 78.9 ms                                                | 83.5 ms: 1.06x slower                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.57 ms: 1.02x slower                                      |
| regex_dna      | 205 ms                                                 | 219 ms: 1.07x slower                                       |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                      |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.23 sec: 1.04x faster                                     |
| pickle_pure_python   | 320 us                                                 | 313 us: 1.02x faster                                       |
| unpickle_list        | 5.21 us                                                | 5.12 us: 1.02x faster                                      |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                      |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                       |
| pickle_dict          | 34.6 us                                                | 34.9 us: 1.01x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 60.5 ms: 1.06x slower                                      |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 88.2 ms: 1.09x slower                                      |
| pickle_list          | 4.59 us                                                | 5.07 us: 1.10x slower                                      |
| unpickle             | 13.8 us                                                | 15.7 us: 1.13x slower                                      |
| Geometric mean       | (ref)                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 9.26 ms: 1.54x slower                                      |
| Geometric mean         | (ref)                                                  | 1.39x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                      |
| django_template | 33.5 ms                                                | 35.2 ms: 1.05x slower                                      |
| genshi_text     | 22.5 ms                                                | 23.8 ms: 1.06x slower                                      |
| mako            | 10.7 ms                                                | 11.7 ms: 1.09x slower                                      |
| Geometric mean  | (ref)                                                  | 1.04x slower                                               |

All benchmarks:
===============

| Benchmark                 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|---------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols  | 520 us                                                 | 119 us: 4.36x faster                                       |
| generators                | 74.9 ms                                                | 30.1 ms: 2.49x faster                                      |
| asyncio_tcp               | 875 ms                                                 | 501 ms: 1.75x faster                                       |
| asyncio_tcp_ssl           | 3.11 sec                                               | 1.84 sec: 1.69x faster                                     |
| pylint                    | 476 ms                                                 | 313 ms: 1.52x faster                                       |
| comprehensions            | 23.6 us                                                | 17.0 us: 1.38x faster                                      |
| json_dumps                | 13.3 ms                                                | 10.7 ms: 1.25x faster                                      |
| coroutines                | 27.0 ms                                                | 21.8 ms: 1.24x faster                                      |
| async_tree_none           | 528 ms                                                 | 451 ms: 1.17x faster                                       |
| deltablue                 | 3.92 ms                                                | 3.44 ms: 1.14x faster                                      |
| chaos                     | 71.9 ms                                                | 63.4 ms: 1.13x faster                                      |
| richards_super            | 61.9 ms                                                | 55.1 ms: 1.12x faster                                      |
| sympy_sum                 | 169 ms                                                 | 151 ms: 1.11x faster                                       |
| async_tree_memoization    | 639 ms                                                 | 583 ms: 1.10x faster                                       |
| sqlglot_parse             | 1.43 ms                                                | 1.31 ms: 1.09x faster                                      |
| hexiom                    | 6.89 ms                                                | 6.32 ms: 1.09x faster                                      |
| sympy_str                 | 297 ms                                                 | 273 ms: 1.09x faster                                       |
| raytrace                  | 309 ms                                                 | 284 ms: 1.08x faster                                       |
| unpickle_pure_python      | 242 us                                                 | 224 us: 1.08x faster                                       |
| sympy_integrate           | 21.5 ms                                                | 20.0 ms: 1.07x faster                                      |
| sqlglot_transpile         | 1.75 ms                                                | 1.64 ms: 1.07x faster                                      |
| djangocms                 | 33.5 us                                                | 31.4 us: 1.07x faster                                      |
| logging_simple            | 6.22 us                                                | 5.89 us: 1.06x faster                                      |
| nbody                     | 96.0 ms                                                | 91.0 ms: 1.05x faster                                      |
| sympy_expand              | 484 ms                                                 | 459 ms: 1.05x faster                                       |
| sqlglot_normalize         | 113 ms                                                 | 107 ms: 1.05x faster                                       |
| nqueens                   | 87.9 ms                                                | 83.5 ms: 1.05x faster                                      |
| async_tree_io             | 1.29 sec                                               | 1.22 sec: 1.05x faster                                     |
| mdp                       | 2.77 sec                                               | 2.64 sec: 1.05x faster                                     |
| logging_format            | 6.81 us                                                | 6.50 us: 1.05x faster                                      |
| crypto_pyaes              | 76.7 ms                                                | 73.3 ms: 1.05x faster                                      |
| async_tree_none_tg        | 491 ms                                                 | 471 ms: 1.04x faster                                       |
| tomli_loads               | 2.30 sec                                               | 2.23 sec: 1.04x faster                                     |
| deepcopy                  | 365 us                                                 | 354 us: 1.03x faster                                       |
| regex_compile             | 141 ms                                                 | 137 ms: 1.03x faster                                       |
| async_tree_io_tg          | 1.29 sec                                               | 1.26 sec: 1.03x faster                                     |
| genshi_xml                | 53.4 ms                                                | 52.1 ms: 1.03x faster                                      |
| pickle_pure_python        | 320 us                                                 | 313 us: 1.02x faster                                       |
| deepcopy_reduce           | 3.22 us                                                | 3.14 us: 1.02x faster                                      |
| async_tree_cpu_io_mixed   | 749 ms                                                 | 733 ms: 1.02x faster                                       |
| logging_silent            | 111 ns                                                 | 109 ns: 1.02x faster                                       |
| unpickle_list             | 5.21 us                                                | 5.12 us: 1.02x faster                                      |
| sqlglot_optimize          | 55.3 ms                                                | 54.3 ms: 1.02x faster                                      |
| json_loads                | 29.2 us                                                | 28.7 us: 1.02x faster                                      |
| async_tree_memoization_tg | 626 ms                                                 | 618 ms: 1.01x faster                                       |
| xml_etree_parse           | 164 ms                                                 | 162 ms: 1.01x faster                                       |
| pprint_pformat            | 1.55 sec                                               | 1.54 sec: 1.01x faster                                     |
| scimark_monte_carlo       | 70.7 ms                                                | 70.0 ms: 1.01x faster                                      |
| deepcopy_memo             | 40.2 us                                                | 39.8 us: 1.01x faster                                      |
| fannkuch                  | 405 ms                                                 | 402 ms: 1.01x faster                                       |
| go                        | 149 ms                                                 | 148 ms: 1.01x faster                                       |
| pickle_dict               | 34.6 us                                                | 34.9 us: 1.01x slower                                      |
| pprint_safe_repr          | 747 ms                                                 | 753 ms: 1.01x slower                                       |
| docutils                  | 2.66 sec                                               | 2.69 sec: 1.01x slower                                     |
| meteor_contest            | 109 ms                                                 | 110 ms: 1.01x slower                                       |
| pidigits                  | 194 ms                                                 | 197 ms: 1.02x slower                                       |
| regex_effbot              | 3.51 ms                                                | 3.57 ms: 1.02x slower                                      |
| scimark_sparse_mat_mult   | 5.03 ms                                                | 5.13 ms: 1.02x slower                                      |
| bench_thread_pool         | 834 us                                                 | 852 us: 1.02x slower                                       |
| html5lib                  | 64.8 ms                                                | 66.3 ms: 1.02x slower                                      |
| asyncio_websockets        | 550 ms                                                 | 563 ms: 1.02x slower                                       |
| spectral_norm             | 108 ms                                                 | 111 ms: 1.03x slower                                       |
| thrift                    | 784 us                                                 | 805 us: 1.03x slower                                       |
| 2to3                      | 264 ms                                                 | 272 ms: 1.03x slower                                       |
| chameleon                 | 6.70 ms                                                | 6.93 ms: 1.03x slower                                      |
| create_gc_cycles          | 1.43 ms                                                | 1.48 ms: 1.03x slower                                      |
| scimark_sor               | 121 ms                                                 | 126 ms: 1.04x slower                                       |
| dulwich_log               | 64.6 ms                                                | 67.6 ms: 1.05x slower                                      |
| aiohttp                   | 1.12 ms                                                | 1.17 ms: 1.05x slower                                      |
| django_template           | 33.5 ms                                                | 35.2 ms: 1.05x slower                                      |
| genshi_text               | 22.5 ms                                                | 23.8 ms: 1.06x slower                                      |
| gunicorn                  | 1.20 ms                                                | 1.27 ms: 1.06x slower                                      |
| float                     | 78.9 ms                                                | 83.5 ms: 1.06x slower                                      |
| xml_etree_process         | 56.9 ms                                                | 60.5 ms: 1.06x slower                                      |
| regex_dna                 | 205 ms                                                 | 219 ms: 1.07x slower                                       |
| pickle                    | 11.0 us                                                | 11.8 us: 1.07x slower                                      |
| scimark_fft               | 345 ms                                                 | 375 ms: 1.08x slower                                       |
| xml_etree_generate        | 81.1 ms                                                | 88.2 ms: 1.09x slower                                      |
| gc_traversal              | 4.01 ms                                                | 4.37 ms: 1.09x slower                                      |
| regex_v8                  | 22.9 ms                                                | 25.0 ms: 1.09x slower                                      |
| mako                      | 10.7 ms                                                | 11.7 ms: 1.09x slower                                      |
| pickle_list               | 4.59 us                                                | 5.07 us: 1.10x slower                                      |
| pyflate                   | 434 ms                                                 | 484 ms: 1.12x slower                                       |
| sqlite_synth              | 2.57 us                                                | 2.87 us: 1.12x slower                                      |
| unpickle                  | 13.8 us                                                | 15.7 us: 1.13x slower                                      |
| flaskblogging             | 7.28 ms                                                | 8.70 ms: 1.19x slower                                      |
| coverage                  | 78.8 ms                                                | 95.2 ms: 1.21x slower                                      |
| async_generators          | 374 ms                                                 | 459 ms: 1.23x slower                                       |
| telco                     | 6.86 ms                                                | 8.53 ms: 1.24x slower                                      |
| python_startup            | 8.56 ms                                                | 10.7 ms: 1.25x slower                                      |
| mypy2                     | 686 ms                                                 | 866 ms: 1.26x slower                                       |
| python_startup_no_site    | 6.01 ms                                                | 9.26 ms: 1.54x slower                                      |
| Geometric mean            | (ref)                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (9): tornado_http, bench_mp_pool, richards, async_tree_cpu_io_mixed_tg, json, xml_etree_iterparse, scimark_lu, pycparser, pathlib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 90.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x