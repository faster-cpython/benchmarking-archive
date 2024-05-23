# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 881df50
- commit date: 2024-05-23
- overall geometric mean: 1.06x faster
- HPT reliability: 94.36%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.05x slower                                                            |
| chameleon      | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                           |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                          |
| html5lib       | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                           |
| tornado_http   | 98.1 ms                                                | 97.1 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.42x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                            |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 965 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.0 ms: 1.19x faster                                                           |
| float          | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                           |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.87 ms: 1.10x slower                                                           |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                                            |
| regex_v8       | 22.9 ms                                                | 26.5 ms: 1.16x slower                                                           |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.28x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.11 sec: 1.09x faster                                                          |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                            |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                           |
| unpickle_list        | 5.21 us                                                | 5.31 us: 1.02x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 82.5 ms: 1.02x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 57.9 ms: 1.02x slower                                                           |
| pickle_dict          | 34.6 us                                                | 35.6 us: 1.03x slower                                                           |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                           |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.15 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                           |
| django_template | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                           |
| genshi_xml      | 53.4 ms                                                | 58.5 ms: 1.10x slower                                                           |
| genshi_text     | 22.5 ms                                                | 25.6 ms: 1.14x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 171 us: 3.04x faster                                                            |
| generators                 | 74.9 ms                                                | 31.2 ms: 2.40x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.42x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                            |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                            |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 965 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                            |
| richards_super             | 61.9 ms                                                | 48.2 ms: 1.28x faster                                                           |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                                           |
| chaos                      | 71.9 ms                                                | 57.7 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                            |
| nbody                      | 96.0 ms                                                | 81.0 ms: 1.19x faster                                                           |
| richards                   | 49.8 ms                                                | 42.2 ms: 1.18x faster                                                           |
| coroutines                 | 27.0 ms                                                | 23.3 ms: 1.16x faster                                                           |
| crypto_pyaes               | 76.7 ms                                                | 66.6 ms: 1.15x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 62.3 ms: 1.14x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.4 ms: 1.13x faster                                                           |
| fannkuch                   | 405 ms                                                 | 360 ms: 1.13x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                            |
| raytrace                   | 309 ms                                                 | 281 ms: 1.10x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.68 us: 1.10x faster                                                           |
| logging_format             | 6.81 us                                                | 6.24 us: 1.09x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.11 sec: 1.09x faster                                                          |
| float                      | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                           |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                           |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                            |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                           |
| pprint_safe_repr           | 747 ms                                                 | 708 ms: 1.05x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.64 sec: 1.05x faster                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.67 ms: 1.05x faster                                                           |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                           |
| hexiom                     | 6.89 ms                                                | 6.60 ms: 1.04x faster                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.82 ms: 1.04x faster                                                           |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                            |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.79 ms: 1.04x faster                                                           |
| scimark_fft                | 345 ms                                                 | 334 ms: 1.03x faster                                                            |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                           |
| tornado_http               | 98.1 ms                                                | 97.1 ms: 1.01x faster                                                           |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                            |
| nqueens                    | 87.9 ms                                                | 87.2 ms: 1.01x faster                                                           |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                            |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                            |
| deepcopy                   | 365 us                                                 | 370 us: 1.01x slower                                                            |
| sympy_str                  | 297 ms                                                 | 301 ms: 1.01x slower                                                            |
| go                         | 149 ms                                                 | 151 ms: 1.02x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.31 us: 1.02x slower                                                           |
| gc_traversal               | 4.01 ms                                                | 4.08 ms: 1.02x slower                                                           |
| xml_etree_generate         | 81.1 ms                                                | 82.5 ms: 1.02x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 57.9 ms: 1.02x slower                                                           |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                          |
| sqlglot_optimize           | 55.3 ms                                                | 56.8 ms: 1.03x slower                                                           |
| pickle_dict                | 34.6 us                                                | 35.6 us: 1.03x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 865 us: 1.04x slower                                                            |
| pyflate                    | 434 ms                                                 | 450 ms: 1.04x slower                                                            |
| html5lib                   | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                           |
| dask                       | 365 ms                                                 | 380 ms: 1.04x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 22.4 ms: 1.04x slower                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.36 us: 1.05x slower                                                           |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                                            |
| 2to3                       | 264 ms                                                 | 279 ms: 1.05x slower                                                            |
| sympy_expand               | 484 ms                                                 | 514 ms: 1.06x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                           |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 69.4 ms: 1.07x slower                                                           |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.08x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                           |
| django_template            | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                           |
| genshi_xml                 | 53.4 ms                                                | 58.5 ms: 1.10x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.87 ms: 1.10x slower                                                           |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.11x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                                          |
| pickle_list                | 4.59 us                                                | 5.15 us: 1.12x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                                           |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                                            |
| genshi_text                | 22.5 ms                                                | 25.6 ms: 1.14x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 26.5 ms: 1.16x slower                                                           |
| coverage                   | 78.8 ms                                                | 93.8 ms: 1.19x slower                                                           |
| telco                      | 6.86 ms                                                | 8.34 ms: 1.22x slower                                                           |
| async_generators           | 374 ms                                                 | 463 ms: 1.24x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                                           |
| flaskblogging              | 7.28 ms                                                | 9.25 ms: 1.27x slower                                                           |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (2): bench_mp_pool, json
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 94.36% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x