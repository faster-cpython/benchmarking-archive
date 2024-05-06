# Results vs. 3.11.0

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 250c073
- commit date: 2024-04-23
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                                             |
| chameleon      | 6.70 ms                                                | 8.01 ms: 1.20x slower                                                            |
| docutils       | 2.66 sec                                               | 3.09 sec: 1.16x slower                                                           |
| html5lib       | 64.8 ms                                                | 71.8 ms: 1.11x slower                                                            |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 375 ms: 1.41x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 353 ms: 1.39x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 463 ms: 1.35x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 966 ms: 1.33x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 972 ms: 1.33x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 502 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 628 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 212 ms: 1.09x slower                                                             |
| float          | 78.9 ms                                                | 91.1 ms: 1.15x slower                                                            |
| nbody          | 96.0 ms                                                | 123 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                            |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                            |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                                             |
| regex_compile  | 141 ms                                                 | 182 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.9 ms: 1.23x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.08x faster                                                             |
| json_loads           | 29.2 us                                                | 28.2 us: 1.03x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 318 us: 1.01x faster                                                             |
| pickle_dict          | 34.6 us                                                | 35.5 us: 1.03x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 112 ms: 1.04x slower                                                             |
| unpickle_list        | 5.21 us                                                | 5.41 us: 1.04x slower                                                            |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.12 us: 1.12x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 64.0 ms: 1.12x slower                                                            |
| unpickle             | 13.8 us                                                | 15.7 us: 1.14x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 92.9 ms: 1.15x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 286 us: 1.18x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.18 ms: 1.19x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 59.0 ms: 1.10x slower                                                            |
| genshi_text     | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                            |
| django_template | 33.5 ms                                                | 40.9 ms: 1.22x slower                                                            |
| mako            | 10.7 ms                                                | 13.7 ms: 1.28x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 123 us: 4.22x faster                                                             |
| generators                 | 74.9 ms                                                | 30.2 ms: 2.48x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 528 ms: 1.66x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                           |
| async_tree_none            | 528 ms                                                 | 375 ms: 1.41x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 353 ms: 1.39x faster                                                             |
| pylint                     | 476 ms                                                 | 349 ms: 1.36x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 463 ms: 1.35x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 966 ms: 1.33x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 972 ms: 1.33x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 502 ms: 1.27x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.9 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 628 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                             |
| coroutines                 | 27.0 ms                                                | 24.0 ms: 1.13x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.08x faster                                                             |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.2 us: 1.03x faster                                                            |
| djangocms                  | 33.5 us                                                | 32.5 us: 1.03x faster                                                            |
| comprehensions             | 23.6 us                                                | 23.2 us: 1.02x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.96 ms: 1.01x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 318 us: 1.01x faster                                                             |
| pathlib                    | 18.5 ms                                                | 18.4 ms: 1.01x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.78 sec: 1.00x slower                                                           |
| richards_super             | 61.9 ms                                                | 62.3 ms: 1.01x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.5 us: 1.03x slower                                                            |
| logging_simple             | 6.22 us                                                | 6.40 us: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 112 ms: 1.04x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.41 us: 1.04x slower                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.82 ms: 1.04x slower                                                            |
| raytrace                   | 309 ms                                                 | 322 ms: 1.04x slower                                                             |
| deepcopy                   | 365 us                                                 | 381 us: 1.04x slower                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.36 us: 1.04x slower                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.50 ms: 1.05x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                            |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.05x slower                                                             |
| dask                       | 365 ms                                                 | 385 ms: 1.05x slower                                                             |
| bench_thread_pool          | 834 us                                                 | 880 us: 1.06x slower                                                             |
| thrift                     | 784 us                                                 | 827 us: 1.06x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.06x slower                                                             |
| logging_format             | 6.81 us                                                | 7.28 us: 1.07x slower                                                            |
| deltablue                  | 3.92 ms                                                | 4.21 ms: 1.07x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.27 sec: 1.07x slower                                                           |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| pidigits                   | 194 ms                                                 | 212 ms: 1.09x slower                                                             |
| sympy_str                  | 297 ms                                                 | 326 ms: 1.10x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                            |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                                             |
| chaos                      | 71.9 ms                                                | 78.9 ms: 1.10x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                           |
| genshi_xml                 | 53.4 ms                                                | 59.0 ms: 1.10x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.23 ms: 1.11x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.33 ms: 1.11x slower                                                            |
| html5lib                   | 64.8 ms                                                | 71.8 ms: 1.11x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 125 ms: 1.11x slower                                                             |
| deepcopy_memo              | 40.2 us                                                | 44.6 us: 1.11x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 23.9 ms: 1.11x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.12 us: 1.12x slower                                                            |
| richards                   | 49.8 ms                                                | 55.6 ms: 1.12x slower                                                            |
| meteor_contest             | 109 ms                                                 | 122 ms: 1.12x slower                                                             |
| genshi_text                | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 64.0 ms: 1.12x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 73.2 ms: 1.13x slower                                                            |
| sympy_expand               | 484 ms                                                 | 550 ms: 1.13x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.14x slower                                                            |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 92.9 ms: 1.15x slower                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 63.5 ms: 1.15x slower                                                            |
| float                      | 78.9 ms                                                | 91.1 ms: 1.15x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.99 us: 1.16x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.09 sec: 1.16x slower                                                           |
| unpickle_pure_python       | 242 us                                                 | 286 us: 1.18x slower                                                             |
| mypy2                      | 686 ms                                                 | 818 ms: 1.19x slower                                                             |
| python_startup_no_site     | 6.01 ms                                                | 7.18 ms: 1.19x slower                                                            |
| chameleon                  | 6.70 ms                                                | 8.01 ms: 1.20x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 92.5 ms: 1.21x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.12 ms: 1.22x slower                                                            |
| django_template            | 33.5 ms                                                | 40.9 ms: 1.22x slower                                                            |
| nqueens                    | 87.9 ms                                                | 108 ms: 1.23x slower                                                             |
| fannkuch                   | 405 ms                                                 | 498 ms: 1.23x slower                                                             |
| coverage                   | 78.8 ms                                                | 97.3 ms: 1.24x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.97 sec: 1.27x slower                                                           |
| async_generators           | 374 ms                                                 | 475 ms: 1.27x slower                                                             |
| pprint_safe_repr           | 747 ms                                                 | 952 ms: 1.27x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 90.5 ms: 1.28x slower                                                            |
| nbody                      | 96.0 ms                                                | 123 ms: 1.28x slower                                                             |
| mako                       | 10.7 ms                                                | 13.7 ms: 1.28x slower                                                            |
| regex_compile              | 141 ms                                                 | 182 ms: 1.28x slower                                                             |
| scimark_sor                | 121 ms                                                 | 157 ms: 1.29x slower                                                             |
| go                         | 149 ms                                                 | 193 ms: 1.30x slower                                                             |
| spectral_norm              | 108 ms                                                 | 142 ms: 1.32x slower                                                             |
| scimark_fft                | 345 ms                                                 | 460 ms: 1.33x slower                                                             |
| telco                      | 6.86 ms                                                | 9.30 ms: 1.36x slower                                                            |
| pyflate                    | 434 ms                                                 | 595 ms: 1.37x slower                                                             |
| hexiom                     | 6.89 ms                                                | 9.53 ms: 1.38x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 168 ms: 1.44x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (2): bench_mp_pool, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.04x