# Results vs. 3.11.0

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.07x faster
- HPT reliability: 99.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                |
| chameleon      | 6.70 ms                                                | 7.10 ms: 1.06x slower                                               |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                              |
| html5lib       | 64.8 ms                                                | 65.8 ms: 1.01x slower                                               |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.49x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 915 ms: 1.41x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                |
| async_tree_io              | 1.29 sec                                               | 943 ms: 1.37x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.2 ms: 1.10x faster                                               |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                |
| float          | 78.9 ms                                                | 78.3 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                               |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                               |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.26x faster                                               |
| unpickle_pure_python | 242 us                                                 | 214 us: 1.13x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                              |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                               |
| unpickle_list        | 5.21 us                                                | 5.03 us: 1.04x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                |
| pickle_dict          | 34.6 us                                                | 34.3 us: 1.01x faster                                               |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                |
| xml_etree_process    | 56.9 ms                                                | 60.9 ms: 1.07x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 87.8 ms: 1.08x slower                                               |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                               |
| pickle_list          | 4.59 us                                                | 5.13 us: 1.12x slower                                               |
| unpickle             | 13.8 us                                                | 16.6 us: 1.20x slower                                               |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.08 ms: 1.18x slower                                               |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                               |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.4 ms: 1.04x faster                                               |
| mako            | 10.7 ms                                                | 10.7 ms: 1.01x slower                                               |
| genshi_text     | 22.5 ms                                                | 23.3 ms: 1.03x slower                                               |
| django_template | 33.5 ms                                                | 35.5 ms: 1.06x slower                                               |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.58x faster                                                |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                              |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.49x faster                                                |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 915 ms: 1.41x faster                                                |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                               |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                |
| async_tree_io              | 1.29 sec                                               | 943 ms: 1.37x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.26x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                |
| deltablue                  | 3.92 ms                                                | 3.21 ms: 1.22x faster                                               |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                               |
| chaos                      | 71.9 ms                                                | 60.5 ms: 1.19x faster                                               |
| richards_super             | 61.9 ms                                                | 52.7 ms: 1.17x faster                                               |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 214 us: 1.13x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.28 ms: 1.12x faster                                               |
| hexiom                     | 6.89 ms                                                | 6.14 ms: 1.12x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.58 ms: 1.11x faster                                               |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                |
| nbody                      | 96.0 ms                                                | 87.2 ms: 1.10x faster                                               |
| gc_traversal               | 4.01 ms                                                | 3.68 ms: 1.09x faster                                               |
| deepcopy_memo              | 40.2 us                                                | 37.0 us: 1.09x faster                                               |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.07x faster                                                |
| nqueens                    | 87.9 ms                                                | 81.9 ms: 1.07x faster                                               |
| djangocms                  | 33.5 us                                                | 31.4 us: 1.07x faster                                               |
| logging_simple             | 6.22 us                                                | 5.85 us: 1.06x faster                                               |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                              |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                                |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                               |
| richards                   | 49.8 ms                                                | 47.3 ms: 1.05x faster                                               |
| go                         | 149 ms                                                 | 141 ms: 1.05x faster                                                |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                               |
| logging_format             | 6.81 us                                                | 6.50 us: 1.05x faster                                               |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                               |
| crypto_pyaes               | 76.7 ms                                                | 73.5 ms: 1.04x faster                                               |
| genshi_xml                 | 53.4 ms                                                | 51.4 ms: 1.04x faster                                               |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                               |
| unpickle_list              | 5.21 us                                                | 5.03 us: 1.04x faster                                               |
| scimark_monte_carlo        | 70.7 ms                                                | 68.2 ms: 1.04x faster                                               |
| mdp                        | 2.77 sec                                               | 2.68 sec: 1.03x faster                                              |
| fannkuch                   | 405 ms                                                 | 394 ms: 1.03x faster                                                |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.03x faster                                              |
| deepcopy                   | 365 us                                                 | 356 us: 1.03x faster                                                |
| sympy_expand               | 484 ms                                                 | 475 ms: 1.02x faster                                                |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                |
| json                       | 5.24 ms                                                | 5.18 ms: 1.01x faster                                               |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                              |
| pickle_dict                | 34.6 us                                                | 34.3 us: 1.01x faster                                               |
| float                      | 78.9 ms                                                | 78.3 ms: 1.01x faster                                               |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                               |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                                |
| pprint_safe_repr           | 747 ms                                                 | 756 ms: 1.01x slower                                                |
| html5lib                   | 64.8 ms                                                | 65.8 ms: 1.01x slower                                               |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                |
| dulwich_log                | 64.6 ms                                                | 66.0 ms: 1.02x slower                                               |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.17 ms: 1.03x slower                                               |
| genshi_text                | 22.5 ms                                                | 23.3 ms: 1.03x slower                                               |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                                |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                               |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                              |
| django_template            | 33.5 ms                                                | 35.5 ms: 1.06x slower                                               |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                               |
| chameleon                  | 6.70 ms                                                | 7.10 ms: 1.06x slower                                               |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                               |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.07x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 60.9 ms: 1.07x slower                                               |
| pyflate                    | 434 ms                                                 | 465 ms: 1.07x slower                                                |
| mypy2                      | 686 ms                                                 | 736 ms: 1.07x slower                                                |
| xml_etree_generate         | 81.1 ms                                                | 87.8 ms: 1.08x slower                                               |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                               |
| scimark_fft                | 345 ms                                                 | 378 ms: 1.09x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                               |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                |
| pickle_list                | 4.59 us                                                | 5.13 us: 1.12x slower                                               |
| sqlite_synth               | 2.57 us                                                | 2.98 us: 1.16x slower                                               |
| python_startup_no_site     | 6.01 ms                                                | 7.08 ms: 1.18x slower                                               |
| async_generators           | 374 ms                                                 | 447 ms: 1.20x slower                                                |
| unpickle                   | 13.8 us                                                | 16.6 us: 1.20x slower                                               |
| create_gc_cycles           | 1.43 ms                                                | 1.74 ms: 1.21x slower                                               |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                               |
| coverage                   | 78.8 ms                                                | 98.0 ms: 1.24x slower                                               |
| telco                      | 6.86 ms                                                | 8.71 ms: 1.27x slower                                               |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                        |

Benchmark hidden because not significant (6): bench_mp_pool, deepcopy_reduce, sqlglot_optimize, meteor_contest, bench_thread_pool, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.45% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x