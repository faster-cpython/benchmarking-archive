# Results vs. 3.11.0

- fork: faster-cpython
- ref: move_set_ip_to_exits
- machine: linux-x86_64
- commit hash: ed60e2e
- commit date: 2024-04-19
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 311 ms: 1.18x slower                                                             |
| chameleon      | 6.70 ms                                                | 8.08 ms: 1.21x slower                                                            |
| docutils       | 2.66 sec                                               | 3.15 sec: 1.18x slower                                                           |
| html5lib       | 64.8 ms                                                | 72.9 ms: 1.13x slower                                                            |
| tornado_http   | 98.1 ms                                                | 104 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                  | 1.15x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 383 ms: 1.38x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 367 ms: 1.34x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 968 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 476 ms: 1.32x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1000 ms: 1.29x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 511 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 640 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 646 ms: 1.16x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 200 ms: 1.03x slower                                                             |
| float          | 78.9 ms                                                | 93.3 ms: 1.18x slower                                                            |
| nbody          | 96.0 ms                                                | 127 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                            |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8       | 22.9 ms                                                | 26.0 ms: 1.13x slower                                                            |
| regex_compile  | 141 ms                                                 | 191 ms: 1.35x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                             |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 310 us: 1.03x faster                                                             |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 110 ms: 1.02x slower                                                             |
| unpickle_list        | 5.21 us                                                | 5.46 us: 1.05x slower                                                            |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.11 us: 1.11x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 65.0 ms: 1.14x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.69 sec: 1.17x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 96.0 ms: 1.18x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 303 us: 1.25x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.10 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 63.1 ms: 1.18x slower                                                            |
| genshi_text     | 22.5 ms                                                | 26.7 ms: 1.18x slower                                                            |
| django_template | 33.5 ms                                                | 42.8 ms: 1.28x slower                                                            |
| mako            | 10.7 ms                                                | 13.7 ms: 1.28x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 129 us: 4.04x faster                                                             |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.50x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 514 ms: 1.70x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                           |
| async_tree_none            | 528 ms                                                 | 383 ms: 1.38x faster                                                             |
| pylint                     | 476 ms                                                 | 348 ms: 1.37x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 367 ms: 1.34x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 968 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 476 ms: 1.32x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1000 ms: 1.29x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 511 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 640 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 646 ms: 1.16x faster                                                             |
| coroutines                 | 27.0 ms                                                | 23.8 ms: 1.14x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                             |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                                            |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                                            |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 310 us: 1.03x faster                                                             |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                                            |
| djangocms                  | 33.5 us                                                | 32.9 us: 1.02x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 110 ms: 1.02x slower                                                             |
| comprehensions             | 23.6 us                                                | 24.3 us: 1.03x slower                                                            |
| pidigits                   | 194 ms                                                 | 200 ms: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| logging_simple             | 6.22 us                                                | 6.46 us: 1.04x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                           |
| unpickle_list              | 5.21 us                                                | 5.46 us: 1.05x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.38 us: 1.05x slower                                                            |
| dask                       | 365 ms                                                 | 383 ms: 1.05x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                            |
| richards_super             | 61.9 ms                                                | 65.0 ms: 1.05x slower                                                            |
| logging_format             | 6.81 us                                                | 7.16 us: 1.05x slower                                                            |
| tornado_http               | 98.1 ms                                                | 104 ms: 1.06x slower                                                             |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 889 us: 1.07x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 180 ms: 1.07x slower                                                             |
| deepcopy                   | 365 us                                                 | 390 us: 1.07x slower                                                             |
| thrift                     | 784 us                                                 | 841 us: 1.07x slower                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.88 ms: 1.07x slower                                                            |
| deltablue                  | 3.92 ms                                                | 4.23 ms: 1.08x slower                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.55 ms: 1.08x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 23.5 ms: 1.10x slower                                                            |
| sympy_str                  | 297 ms                                                 | 328 ms: 1.10x slower                                                             |
| gunicorn                   | 1.20 ms                                                | 1.33 ms: 1.11x slower                                                            |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| raytrace                   | 309 ms                                                 | 343 ms: 1.11x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.11 us: 1.11x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.24 ms: 1.12x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.32 sec: 1.12x slower                                                           |
| html5lib                   | 64.8 ms                                                | 72.9 ms: 1.13x slower                                                            |
| sympy_expand               | 484 ms                                                 | 546 ms: 1.13x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 26.0 ms: 1.13x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 128 ms: 1.13x slower                                                             |
| xml_etree_process          | 56.9 ms                                                | 65.0 ms: 1.14x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 74.3 ms: 1.15x slower                                                            |
| richards                   | 49.8 ms                                                | 57.3 ms: 1.15x slower                                                            |
| deepcopy_memo              | 40.2 us                                                | 46.3 us: 1.15x slower                                                            |
| chaos                      | 71.9 ms                                                | 83.3 ms: 1.16x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 2.69 sec: 1.17x slower                                                           |
| 2to3                       | 264 ms                                                 | 311 ms: 1.18x slower                                                             |
| genshi_xml                 | 53.4 ms                                                | 63.1 ms: 1.18x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.10 ms: 1.18x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.15 sec: 1.18x slower                                                           |
| float                      | 78.9 ms                                                | 93.3 ms: 1.18x slower                                                            |
| genshi_text                | 22.5 ms                                                | 26.7 ms: 1.18x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 96.0 ms: 1.18x slower                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 65.9 ms: 1.19x slower                                                            |
| mypy2                      | 686 ms                                                 | 817 ms: 1.19x slower                                                             |
| meteor_contest             | 109 ms                                                 | 131 ms: 1.20x slower                                                             |
| chameleon                  | 6.70 ms                                                | 8.08 ms: 1.21x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 3.14 us: 1.22x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.23x slower                                                            |
| scimark_sor                | 121 ms                                                 | 151 ms: 1.25x slower                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.30 ms: 1.25x slower                                                            |
| unpickle_pure_python       | 242 us                                                 | 303 us: 1.25x slower                                                             |
| coverage                   | 78.8 ms                                                | 98.8 ms: 1.25x slower                                                            |
| fannkuch                   | 405 ms                                                 | 515 ms: 1.27x slower                                                             |
| django_template            | 33.5 ms                                                | 42.8 ms: 1.28x slower                                                            |
| async_generators           | 374 ms                                                 | 479 ms: 1.28x slower                                                             |
| mako                       | 10.7 ms                                                | 13.7 ms: 1.28x slower                                                            |
| go                         | 149 ms                                                 | 191 ms: 1.29x slower                                                             |
| scimark_fft                | 345 ms                                                 | 448 ms: 1.30x slower                                                             |
| spectral_norm              | 108 ms                                                 | 141 ms: 1.30x slower                                                             |
| crypto_pyaes               | 76.7 ms                                                | 100 ms: 1.31x slower                                                             |
| nbody                      | 96.0 ms                                                | 127 ms: 1.32x slower                                                             |
| nqueens                    | 87.9 ms                                                | 117 ms: 1.33x slower                                                             |
| regex_compile              | 141 ms                                                 | 191 ms: 1.35x slower                                                             |
| telco                      | 6.86 ms                                                | 9.60 ms: 1.40x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 1.07 sec: 1.43x slower                                                           |
| pprint_pformat             | 1.55 sec                                               | 2.26 sec: 1.45x slower                                                           |
| hexiom                     | 6.89 ms                                                | 10.2 ms: 1.48x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 172 ms: 1.48x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 106 ms: 1.49x slower                                                             |
| pyflate                    | 434 ms                                                 | 672 ms: 1.55x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                                     |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.03x