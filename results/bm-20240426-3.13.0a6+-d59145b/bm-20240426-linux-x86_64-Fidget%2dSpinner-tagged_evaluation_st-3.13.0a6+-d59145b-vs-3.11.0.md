# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: d59145b
- commit date: 2024-04-26
- overall geometric mean: 1.07x faster
- HPT reliability: 99.68%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 267 ms: 1.01x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                            |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                           |
| html5lib       | 64.8 ms                                                | 65.8 ms: 1.02x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.8 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 351 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 916 ms: 1.41x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.4 ms: 1.06x faster                                                            |
| pidigits       | 194 ms                                                 | 189 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 77.8 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                            |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.7 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 213 us: 1.13x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                             |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.20 sec: 1.05x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                             |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 86.3 ms: 1.06x slower                                                            |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.03 us: 1.10x slower                                                            |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                            |
| mako            | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                            |
| django_template | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                            |
| genshi_text     | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 159 us: 3.27x faster                                                             |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.56x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| pylint                     | 476 ms                                                 | 315 ms: 1.51x faster                                                             |
| async_tree_none            | 528 ms                                                 | 351 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 916 ms: 1.41x faster                                                             |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.39x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.16 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                             |
| chaos                      | 71.9 ms                                                | 59.4 ms: 1.21x faster                                                            |
| raytrace                   | 309 ms                                                 | 257 ms: 1.20x faster                                                             |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                                            |
| richards_super             | 61.9 ms                                                | 52.5 ms: 1.18x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 213 us: 1.13x faster                                                             |
| logging_silent             | 111 ns                                                 | 98.0 ns: 1.13x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.27 ms: 1.12x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.58 ms: 1.11x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 153 ms: 1.10x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.25 ms: 1.10x faster                                                            |
| nqueens                    | 87.9 ms                                                | 80.7 ms: 1.09x faster                                                            |
| sympy_str                  | 297 ms                                                 | 274 ms: 1.08x faster                                                             |
| richards                   | 49.8 ms                                                | 46.0 ms: 1.08x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.78 us: 1.08x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                                            |
| logging_format             | 6.81 us                                                | 6.36 us: 1.07x faster                                                            |
| go                         | 149 ms                                                 | 139 ms: 1.07x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                             |
| djangocms                  | 33.5 us                                                | 31.5 us: 1.06x faster                                                            |
| nbody                      | 96.0 ms                                                | 90.4 ms: 1.06x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 37.9 us: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                                            |
| sympy_expand               | 484 ms                                                 | 463 ms: 1.05x faster                                                             |
| tomli_loads                | 2.30 sec                                               | 2.20 sec: 1.05x faster                                                           |
| tornado_http               | 98.1 ms                                                | 93.8 ms: 1.05x faster                                                            |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 73.7 ms: 1.04x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.04x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                             |
| fannkuch                   | 405 ms                                                 | 394 ms: 1.03x faster                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.89 ms: 1.03x faster                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.13 us: 1.03x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                            |
| deepcopy                   | 365 us                                                 | 356 us: 1.03x faster                                                             |
| pidigits                   | 194 ms                                                 | 189 ms: 1.02x faster                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 69.4 ms: 1.02x faster                                                            |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 54.5 ms: 1.02x faster                                                            |
| float                      | 78.9 ms                                                | 77.8 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| bench_thread_pool          | 834 us                                                 | 827 us: 1.01x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.76 sec: 1.00x faster                                                           |
| scimark_lu                 | 116 ms                                                 | 117 ms: 1.01x slower                                                             |
| 2to3                       | 264 ms                                                 | 267 ms: 1.01x slower                                                             |
| html5lib                   | 64.8 ms                                                | 65.8 ms: 1.02x slower                                                            |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 65.9 ms: 1.02x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.03x slower                                                             |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                            |
| thrift                     | 784 us                                                 | 815 us: 1.04x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.16 ms: 1.04x slower                                                            |
| django_template            | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                            |
| mypy2                      | 686 ms                                                 | 729 ms: 1.06x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 86.3 ms: 1.06x slower                                                            |
| scimark_fft                | 345 ms                                                 | 371 ms: 1.07x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.03 us: 1.10x slower                                                            |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.7 ms: 1.12x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                            |
| async_generators           | 374 ms                                                 | 443 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                            |
| coverage                   | 78.8 ms                                                | 96.5 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.50 ms: 1.24x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (5): bench_mp_pool, dask, scimark_sor, pprint_safe_repr, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.68% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x