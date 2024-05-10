# Results vs. 3.11.0

- fork: faster-cpython
- ref: test_perf_jit
- machine: linux-x86_64
- commit hash: 1973514
- commit date: 2024-05-10
- overall geometric mean: 1.03x faster
- HPT reliability: 96.56%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                     |
| chameleon      | 6.70 ms                                                | 6.94 ms: 1.04x slower                                                    |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                   |
| html5lib       | 64.8 ms                                                | 66.6 ms: 1.03x slower                                                    |
| tornado_http   | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                  | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 362 ms: 1.46x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 935 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.33x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 989 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.1 ms: 1.07x faster                                                    |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                     |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                     |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                    |
| regex_dna      | 205 ms                                                 | 220 ms: 1.07x slower                                                     |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.08 sec: 1.11x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.09x faster                                                     |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                                     |
| pickle_dict          | 34.6 us                                                | 34.0 us: 1.02x faster                                                    |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                                     |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| unpickle_list        | 5.21 us                                                | 5.48 us: 1.05x slower                                                    |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                    |
| xml_etree_process    | 56.9 ms                                                | 61.8 ms: 1.09x slower                                                    |
| xml_etree_generate   | 81.1 ms                                                | 89.5 ms: 1.10x slower                                                    |
| unpickle             | 13.8 us                                                | 16.2 us: 1.17x slower                                                    |
| pickle_list          | 4.59 us                                                | 5.63 us: 1.23x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                    |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.6 ms: 1.06x faster                                                    |
| genshi_text     | 22.5 ms                                                | 23.1 ms: 1.02x slower                                                    |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                    |
| mako            | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-faster%2dcpython-test_perf_jit-3.14.0a0-1973514 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 167 us: 3.11x faster                                                     |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                    |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                     |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                   |
| pylint                     | 476 ms                                                 | 317 ms: 1.50x faster                                                     |
| async_tree_none            | 528 ms                                                 | 362 ms: 1.46x faster                                                     |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 935 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 479 ms: 1.33x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 989 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                     |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                     |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                                    |
| chaos                      | 71.9 ms                                                | 60.4 ms: 1.19x faster                                                    |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                                    |
| raytrace                   | 309 ms                                                 | 268 ms: 1.15x faster                                                     |
| richards_super             | 61.9 ms                                                | 54.2 ms: 1.14x faster                                                    |
| tomli_loads                | 2.30 sec                                               | 2.08 sec: 1.11x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.64 us: 1.10x faster                                                    |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                    |
| hexiom                     | 6.89 ms                                                | 6.29 ms: 1.10x faster                                                    |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.09x faster                                                     |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                     |
| logging_format             | 6.81 us                                                | 6.30 us: 1.08x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                    |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                     |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.08x faster                                                   |
| nqueens                    | 87.9 ms                                                | 81.9 ms: 1.07x faster                                                    |
| nbody                      | 96.0 ms                                                | 90.1 ms: 1.07x faster                                                    |
| genshi_xml                 | 53.4 ms                                                | 50.6 ms: 1.06x faster                                                    |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                                     |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                    |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 3.82 ms: 1.05x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                                     |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                     |
| richards                   | 49.8 ms                                                | 47.8 ms: 1.04x faster                                                    |
| tornado_http               | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                    |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 68.5 ms: 1.03x faster                                                    |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                     |
| sympy_expand               | 484 ms                                                 | 474 ms: 1.02x faster                                                     |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                    |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                    |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                     |
| crypto_pyaes               | 76.7 ms                                                | 75.2 ms: 1.02x faster                                                    |
| pickle_dict                | 34.6 us                                                | 34.0 us: 1.02x faster                                                    |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                                     |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                    |
| bench_thread_pool          | 834 us                                                 | 831 us: 1.00x faster                                                     |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                     |
| fannkuch                   | 405 ms                                                 | 407 ms: 1.00x slower                                                     |
| scimark_lu                 | 116 ms                                                 | 117 ms: 1.01x slower                                                     |
| pprint_pformat             | 1.55 sec                                               | 1.57 sec: 1.01x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.12 ms: 1.02x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 65.9 ms: 1.02x slower                                                    |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                     |
| genshi_text                | 22.5 ms                                                | 23.1 ms: 1.02x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                     |
| thrift                     | 784 us                                                 | 805 us: 1.03x slower                                                     |
| html5lib                   | 64.8 ms                                                | 66.6 ms: 1.03x slower                                                    |
| pprint_safe_repr           | 747 ms                                                 | 771 ms: 1.03x slower                                                     |
| chameleon                  | 6.70 ms                                                | 6.94 ms: 1.04x slower                                                    |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                                     |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                    |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.05x slower                                                     |
| unpickle_list              | 5.21 us                                                | 5.48 us: 1.05x slower                                                    |
| json                       | 5.24 ms                                                | 5.53 ms: 1.05x slower                                                    |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                   |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                    |
| mako                       | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                    |
| regex_dna                  | 205 ms                                                 | 220 ms: 1.07x slower                                                     |
| xml_etree_process          | 56.9 ms                                                | 61.8 ms: 1.09x slower                                                    |
| scimark_fft                | 345 ms                                                 | 377 ms: 1.09x slower                                                     |
| xml_etree_generate         | 81.1 ms                                                | 89.5 ms: 1.10x slower                                                    |
| pyflate                    | 434 ms                                                 | 484 ms: 1.12x slower                                                     |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                    |
| unpickle                   | 13.8 us                                                | 16.2 us: 1.17x slower                                                    |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                    |
| async_generators           | 374 ms                                                 | 452 ms: 1.21x slower                                                     |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.22x slower                                                    |
| flaskblogging              | 7.28 ms                                                | 8.88 ms: 1.22x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.63 us: 1.23x slower                                                    |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                    |
| telco                      | 6.86 ms                                                | 177 ms: 25.77x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (4): deepcopy, sqlglot_optimize, deepcopy_reduce, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.56% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x