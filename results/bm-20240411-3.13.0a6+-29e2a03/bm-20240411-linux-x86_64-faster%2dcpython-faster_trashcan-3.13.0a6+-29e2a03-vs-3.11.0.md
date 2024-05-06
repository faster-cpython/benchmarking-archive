# Results vs. 3.11.0

- fork: faster-cpython
- ref: faster_trashcan
- machine: linux-x86_64
- commit hash: 29e2a03
- commit date: 2024-04-11
- overall geometric mean: 1.07x faster
- HPT reliability: 99.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.01x slower                                                        |
| chameleon      | 6.70 ms                                                | 6.80 ms: 1.02x slower                                                       |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                      |
| html5lib       | 64.8 ms                                                | 68.1 ms: 1.05x slower                                                       |
| tornado_http   | 98.1 ms                                                | 94.2 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                        |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 943 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                        |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.0 ms: 1.09x faster                                                       |
| float          | 78.9 ms                                                | 78.0 ms: 1.01x faster                                                       |
| pidigits       | 194 ms                                                 | 203 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                        |
| regex_effbot   | 3.51 ms                                                | 3.81 ms: 1.09x slower                                                       |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                        |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                       |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                        |
| pickle_pure_python   | 320 us                                                 | 298 us: 1.07x faster                                                        |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                      |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                        |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                       |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                        |
| unpickle_list        | 5.21 us                                                | 5.34 us: 1.02x slower                                                       |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                       |
| xml_etree_process    | 56.9 ms                                                | 60.5 ms: 1.06x slower                                                       |
| xml_etree_generate   | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                       |
| pickle_list          | 4.59 us                                                | 4.94 us: 1.08x slower                                                       |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.06 ms: 1.17x slower                                                       |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.3 ms: 1.04x faster                                                       |
| mako           | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                       |
| genshi_text    | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.58x faster                                                        |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                       |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                        |
| pylint                     | 476 ms                                                 | 277 ms: 1.72x faster                                                        |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                      |
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                        |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                        |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.42x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 943 ms: 1.37x faster                                                        |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                        |
| deltablue                  | 3.92 ms                                                | 3.17 ms: 1.24x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                        |
| chaos                      | 71.9 ms                                                | 60.0 ms: 1.20x faster                                                       |
| raytrace                   | 309 ms                                                 | 261 ms: 1.18x faster                                                        |
| richards_super             | 61.9 ms                                                | 52.9 ms: 1.17x faster                                                       |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                                       |
| logging_silent             | 111 ns                                                 | 96.0 ns: 1.16x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                       |
| hexiom                     | 6.89 ms                                                | 6.26 ms: 1.10x faster                                                       |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                       |
| nbody                      | 96.0 ms                                                | 88.0 ms: 1.09x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                        |
| logging_simple             | 6.22 us                                                | 5.74 us: 1.08x faster                                                       |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                        |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.07x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 298 us: 1.07x faster                                                        |
| richards                   | 49.8 ms                                                | 46.5 ms: 1.07x faster                                                       |
| logging_format             | 6.81 us                                                | 6.37 us: 1.07x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                      |
| deepcopy_memo              | 40.2 us                                                | 37.6 us: 1.07x faster                                                       |
| nqueens                    | 87.9 ms                                                | 82.2 ms: 1.07x faster                                                       |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                        |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                       |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                                        |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                        |
| genshi_xml                 | 53.4 ms                                                | 51.3 ms: 1.04x faster                                                       |
| tornado_http               | 98.1 ms                                                | 94.2 ms: 1.04x faster                                                       |
| fannkuch                   | 405 ms                                                 | 390 ms: 1.04x faster                                                        |
| sympy_expand               | 484 ms                                                 | 469 ms: 1.03x faster                                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 68.5 ms: 1.03x faster                                                       |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                        |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                      |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                        |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                                      |
| gc_traversal               | 4.01 ms                                                | 3.95 ms: 1.02x faster                                                       |
| deepcopy                   | 365 us                                                 | 360 us: 1.01x faster                                                        |
| float                      | 78.9 ms                                                | 78.0 ms: 1.01x faster                                                       |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                       |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 75.9 ms: 1.01x faster                                                       |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                        |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 55.2 ms: 1.00x faster                                                       |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                       |
| pathlib                    | 18.5 ms                                                | 18.7 ms: 1.01x slower                                                       |
| scimark_sor                | 121 ms                                                 | 122 ms: 1.01x slower                                                        |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                        |
| deepcopy_reduce            | 3.22 us                                                | 3.26 us: 1.01x slower                                                       |
| 2to3                       | 264 ms                                                 | 268 ms: 1.01x slower                                                        |
| chameleon                  | 6.70 ms                                                | 6.80 ms: 1.02x slower                                                       |
| json                       | 5.24 ms                                                | 5.35 ms: 1.02x slower                                                       |
| unpickle_list              | 5.21 us                                                | 5.34 us: 1.02x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 66.8 ms: 1.03x slower                                                       |
| thrift                     | 784 us                                                 | 811 us: 1.03x slower                                                        |
| genshi_text                | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                       |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.05x slower                                                        |
| pidigits                   | 194 ms                                                 | 203 ms: 1.05x slower                                                        |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                       |
| html5lib                   | 64.8 ms                                                | 68.1 ms: 1.05x slower                                                       |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                       |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                      |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.33 ms: 1.06x slower                                                       |
| xml_etree_process          | 56.9 ms                                                | 60.5 ms: 1.06x slower                                                       |
| mypy2                      | 686 ms                                                 | 736 ms: 1.07x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                       |
| pickle_list                | 4.59 us                                                | 4.94 us: 1.08x slower                                                       |
| regex_effbot               | 3.51 ms                                                | 3.81 ms: 1.09x slower                                                       |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                        |
| scimark_fft                | 345 ms                                                 | 378 ms: 1.09x slower                                                        |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                       |
| pyflate                    | 434 ms                                                 | 479 ms: 1.11x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                       |
| sqlite_synth               | 2.57 us                                                | 2.99 us: 1.16x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.06 ms: 1.17x slower                                                       |
| async_generators           | 374 ms                                                 | 439 ms: 1.18x slower                                                        |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                       |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                       |
| coverage                   | 78.8 ms                                                | 97.6 ms: 1.24x slower                                                       |
| telco                      | 6.86 ms                                                | 8.74 ms: 1.27x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                |

Benchmark hidden because not significant (4): pprint_safe_repr, scimark_lu, bench_thread_pool, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.18% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x