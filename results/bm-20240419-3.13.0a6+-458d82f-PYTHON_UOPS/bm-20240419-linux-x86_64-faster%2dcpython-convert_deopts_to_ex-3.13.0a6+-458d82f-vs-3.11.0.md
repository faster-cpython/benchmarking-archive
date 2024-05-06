# Results vs. 3.11.0

- fork: faster-cpython
- ref: convert_deopts_to_ex
- machine: linux-x86_64
- commit hash: 458d82f
- commit date: 2024-04-19
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.15x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.61 ms: 1.14x slower                                                            |
| docutils       | 2.66 sec                                               | 3.14 sec: 1.18x slower                                                           |
| html5lib       | 64.8 ms                                                | 72.2 ms: 1.11x slower                                                            |
| tornado_http   | 98.1 ms                                                | 102 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 376 ms: 1.41x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 357 ms: 1.38x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 467 ms: 1.34x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 966 ms: 1.34x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 976 ms: 1.32x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 503 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 629 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 635 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 192 ms: 1.01x faster                                                             |
| float          | 78.9 ms                                                | 89.2 ms: 1.13x slower                                                            |
| nbody          | 96.0 ms                                                | 122 ms: 1.27x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                            |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                            |
| regex_compile  | 141 ms                                                 | 181 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                             |
| pickle_dict          | 34.6 us                                                | 32.8 us: 1.06x faster                                                            |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 316 us: 1.01x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.33 us: 1.02x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 111 ms: 1.03x slower                                                             |
| pickle_list          | 4.59 us                                                | 4.83 us: 1.05x slower                                                            |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.55 sec: 1.11x slower                                                           |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 65.1 ms: 1.14x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 93.5 ms: 1.15x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 282 us: 1.17x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 64.7 ms: 1.21x slower                                                            |
| django_template | 33.5 ms                                                | 41.3 ms: 1.23x slower                                                            |
| genshi_text     | 22.5 ms                                                | 28.7 ms: 1.27x slower                                                            |
| mako            | 10.7 ms                                                | 13.6 ms: 1.28x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 124 us: 4.20x faster                                                             |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 533 ms: 1.64x faster                                                             |
| async_tree_none            | 528 ms                                                 | 376 ms: 1.41x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 357 ms: 1.38x faster                                                             |
| pylint                     | 476 ms                                                 | 350 ms: 1.36x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 467 ms: 1.34x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 966 ms: 1.34x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 976 ms: 1.32x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 503 ms: 1.27x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 629 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 635 ms: 1.18x faster                                                             |
| coroutines                 | 27.0 ms                                                | 24.3 ms: 1.11x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                             |
| pickle_dict                | 34.6 us                                                | 32.8 us: 1.06x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.80 ms: 1.05x faster                                                            |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                                            |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                             |
| json                       | 5.24 ms                                                | 5.14 ms: 1.02x faster                                                            |
| pidigits                   | 194 ms                                                 | 192 ms: 1.01x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 316 us: 1.01x faster                                                             |
| pathlib                    | 18.5 ms                                                | 18.7 ms: 1.01x slower                                                            |
| comprehensions             | 23.6 us                                                | 23.9 us: 1.01x slower                                                            |
| richards_super             | 61.9 ms                                                | 62.9 ms: 1.02x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.33 us: 1.02x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.84 sec: 1.02x slower                                                           |
| xml_etree_iterparse        | 108 ms                                                 | 111 ms: 1.03x slower                                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.48 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.81 ms: 1.03x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.34 us: 1.04x slower                                                            |
| tornado_http               | 98.1 ms                                                | 102 ms: 1.04x slower                                                             |
| deepcopy                   | 365 us                                                 | 384 us: 1.05x slower                                                             |
| pickle_list                | 4.59 us                                                | 4.83 us: 1.05x slower                                                            |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                                             |
| raytrace                   | 309 ms                                                 | 326 ms: 1.06x slower                                                             |
| bench_thread_pool          | 834 us                                                 | 886 us: 1.06x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                            |
| dask                       | 365 ms                                                 | 389 ms: 1.07x slower                                                             |
| deepcopy_memo              | 40.2 us                                                | 42.9 us: 1.07x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.27 sec: 1.07x slower                                                           |
| thrift                     | 784 us                                                 | 847 us: 1.08x slower                                                             |
| logging_simple             | 6.22 us                                                | 6.76 us: 1.09x slower                                                            |
| sympy_str                  | 297 ms                                                 | 325 ms: 1.09x slower                                                             |
| sympy_integrate            | 21.5 ms                                                | 23.5 ms: 1.10x slower                                                            |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                                             |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                            |
| logging_format             | 6.81 us                                                | 7.54 us: 1.11x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 2.55 sec: 1.11x slower                                                           |
| gunicorn                   | 1.20 ms                                                | 1.33 ms: 1.11x slower                                                            |
| deltablue                  | 3.92 ms                                                | 4.37 ms: 1.11x slower                                                            |
| html5lib                   | 64.8 ms                                                | 72.2 ms: 1.11x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.24 ms: 1.12x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 126 ms: 1.12x slower                                                             |
| sympy_expand               | 484 ms                                                 | 544 ms: 1.12x slower                                                             |
| chaos                      | 71.9 ms                                                | 80.9 ms: 1.13x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                            |
| float                      | 78.9 ms                                                | 89.2 ms: 1.13x slower                                                            |
| richards                   | 49.8 ms                                                | 56.3 ms: 1.13x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.61 ms: 1.14x slower                                                            |
| meteor_contest             | 109 ms                                                 | 125 ms: 1.14x slower                                                             |
| xml_etree_process          | 56.9 ms                                                | 65.1 ms: 1.14x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 93.5 ms: 1.15x slower                                                            |
| 2to3                       | 264 ms                                                 | 305 ms: 1.15x slower                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 64.2 ms: 1.16x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 75.1 ms: 1.16x slower                                                            |
| unpickle_pure_python       | 242 us                                                 | 282 us: 1.17x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 3.01 us: 1.17x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.14 sec: 1.18x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                            |
| mypy2                      | 686 ms                                                 | 829 ms: 1.21x slower                                                             |
| genshi_xml                 | 53.4 ms                                                | 64.7 ms: 1.21x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 94.1 ms: 1.23x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| django_template            | 33.5 ms                                                | 41.3 ms: 1.23x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.20 ms: 1.23x slower                                                            |
| nqueens                    | 87.9 ms                                                | 109 ms: 1.24x slower                                                             |
| fannkuch                   | 405 ms                                                 | 501 ms: 1.24x slower                                                             |
| coverage                   | 78.8 ms                                                | 97.9 ms: 1.24x slower                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 88.3 ms: 1.25x slower                                                            |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                             |
| nbody                      | 96.0 ms                                                | 122 ms: 1.27x slower                                                             |
| genshi_text                | 22.5 ms                                                | 28.7 ms: 1.27x slower                                                            |
| mako                       | 10.7 ms                                                | 13.6 ms: 1.28x slower                                                            |
| regex_compile              | 141 ms                                                 | 181 ms: 1.28x slower                                                             |
| go                         | 149 ms                                                 | 191 ms: 1.28x slower                                                             |
| pprint_pformat             | 1.55 sec                                               | 2.02 sec: 1.30x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 974 ms: 1.30x slower                                                             |
| scimark_sor                | 121 ms                                                 | 159 ms: 1.31x slower                                                             |
| scimark_fft                | 345 ms                                                 | 457 ms: 1.32x slower                                                             |
| telco                      | 6.86 ms                                                | 9.11 ms: 1.33x slower                                                            |
| spectral_norm              | 108 ms                                                 | 144 ms: 1.33x slower                                                             |
| pyflate                    | 434 ms                                                 | 600 ms: 1.38x slower                                                             |
| hexiom                     | 6.89 ms                                                | 9.65 ms: 1.40x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 173 ms: 1.48x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (2): djangocms, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.03x