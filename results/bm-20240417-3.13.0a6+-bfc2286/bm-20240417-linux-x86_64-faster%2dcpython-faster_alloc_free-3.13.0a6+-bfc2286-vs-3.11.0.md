# Results vs. 3.11.0

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: bfc2286
- commit date: 2024-04-17
- overall geometric mean: 1.06x faster
- HPT reliability: 97.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                         |
| docutils       | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                        |
| html5lib       | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                         |
| tornado_http   | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 912 ms: 1.41x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 924 ms: 1.40x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 598 ms: 1.27x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 602 ms: 1.24x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 84.7 ms: 1.13x faster                                                         |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                          |
| float          | 78.9 ms                                                | 77.6 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                         |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                                          |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                         |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                          |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                          |
| tomli_loads          | 2.30 sec                                               | 2.24 sec: 1.03x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                          |
| pickle_dict          | 34.6 us                                                | 36.0 us: 1.04x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                         |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                         |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.41 us: 1.18x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.07 ms: 1.18x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                         |
| mako            | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                         |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                         |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.52x faster                                                          |
| generators                 | 74.9 ms                                                | 29.5 ms: 2.54x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                        |
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                          |
| pylint                     | 476 ms                                                 | 321 ms: 1.48x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 912 ms: 1.41x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 924 ms: 1.40x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                          |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 598 ms: 1.27x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 602 ms: 1.24x faster                                                          |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                                         |
| chaos                      | 71.9 ms                                                | 60.4 ms: 1.19x faster                                                         |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                         |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                          |
| richards_super             | 61.9 ms                                                | 54.0 ms: 1.15x faster                                                         |
| nbody                      | 96.0 ms                                                | 84.7 ms: 1.13x faster                                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                          |
| nqueens                    | 87.9 ms                                                | 81.0 ms: 1.08x faster                                                         |
| hexiom                     | 6.89 ms                                                | 6.38 ms: 1.08x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.07x faster                                                          |
| logging_simple             | 6.22 us                                                | 5.81 us: 1.07x faster                                                         |
| pathlib                    | 18.5 ms                                                | 17.4 ms: 1.07x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.76 ms: 1.06x faster                                                         |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                         |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                                         |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                                          |
| logging_format             | 6.81 us                                                | 6.47 us: 1.05x faster                                                         |
| sympy_str                  | 297 ms                                                 | 283 ms: 1.05x faster                                                          |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                                         |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                          |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                         |
| tornado_http               | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                         |
| richards                   | 49.8 ms                                                | 48.0 ms: 1.04x faster                                                         |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                          |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                          |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                          |
| crypto_pyaes               | 76.7 ms                                                | 74.6 ms: 1.03x faster                                                         |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 68.9 ms: 1.03x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 2.24 sec: 1.03x faster                                                        |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                          |
| deepcopy                   | 365 us                                                 | 357 us: 1.02x faster                                                          |
| sympy_expand               | 484 ms                                                 | 476 ms: 1.02x faster                                                          |
| float                      | 78.9 ms                                                | 77.6 ms: 1.02x faster                                                         |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                          |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                          |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                                          |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                        |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                          |
| sqlglot_optimize           | 55.3 ms                                                | 55.5 ms: 1.00x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 840 us: 1.01x slower                                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.24 us: 1.01x slower                                                         |
| pprint_safe_repr           | 747 ms                                                 | 752 ms: 1.01x slower                                                          |
| mdp                        | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                        |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                                          |
| dask                       | 365 ms                                                 | 371 ms: 1.02x slower                                                          |
| scimark_sor                | 121 ms                                                 | 125 ms: 1.03x slower                                                          |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 66.7 ms: 1.03x slower                                                         |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                          |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.21 ms: 1.04x slower                                                         |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                         |
| pickle_dict                | 34.6 us                                                | 36.0 us: 1.04x slower                                                         |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                         |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                         |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                         |
| html5lib                   | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                         |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                         |
| chameleon                  | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                        |
| xml_etree_process          | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                         |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                          |
| scimark_fft                | 345 ms                                                 | 376 ms: 1.09x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                         |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                                          |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                         |
| pyflate                    | 434 ms                                                 | 483 ms: 1.11x slower                                                          |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                         |
| spectral_norm              | 108 ms                                                 | 122 ms: 1.13x slower                                                          |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.07 ms: 1.18x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.41 us: 1.18x slower                                                         |
| async_generators           | 374 ms                                                 | 446 ms: 1.19x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                         |
| coverage                   | 78.8 ms                                                | 97.7 ms: 1.24x slower                                                         |
| telco                      | 6.86 ms                                                | 8.60 ms: 1.25x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                  |

Benchmark hidden because not significant (3): pycparser, json, unpickle_list
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.08% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x