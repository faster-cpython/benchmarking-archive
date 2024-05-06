# Results vs. 3.11.0

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.16x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 332 ms: 1.25x slower                                                |
| chameleon      | 6.70 ms                                                | 8.07 ms: 1.20x slower                                               |
| docutils       | 2.66 sec                                               | 3.28 sec: 1.23x slower                                              |
| html5lib       | 64.8 ms                                                | 75.6 ms: 1.17x slower                                               |
| tornado_http   | 98.1 ms                                                | 104 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                  | 1.18x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 371 ms: 1.32x faster                                                |
| async_tree_none            | 528 ms                                                 | 400 ms: 1.32x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 480 ms: 1.30x faster                                                |
| async_tree_io              | 1.29 sec                                               | 995 ms: 1.29x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 529 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 649 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 660 ms: 1.14x faster                                                |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 195 ms: 1.00x slower                                                |
| float          | 78.9 ms                                                | 139 ms: 1.76x slower                                                |
| nbody          | 96.0 ms                                                | 203 ms: 2.12x slower                                                |
| Geometric mean | (ref)                                                  | 1.55x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.88 ms: 1.11x slower                                               |
| regex_dna      | 205 ms                                                 | 235 ms: 1.15x slower                                                |
| regex_v8       | 22.9 ms                                                | 27.2 ms: 1.19x slower                                               |
| regex_compile  | 141 ms                                                 | 223 ms: 1.58x slower                                                |
| Geometric mean | (ref)                                                  | 1.24x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                               |
| json_loads           | 29.2 us                                                | 27.9 us: 1.05x faster                                               |
| pickle_pure_python   | 320 us                                                 | 314 us: 1.02x faster                                                |
| xml_etree_parse      | 164 ms                                                 | 163 ms: 1.01x faster                                                |
| pickle_dict          | 34.6 us                                                | 35.8 us: 1.03x slower                                               |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                               |
| pickle_list          | 4.59 us                                                | 5.20 us: 1.13x slower                                               |
| unpickle             | 13.8 us                                                | 16.8 us: 1.22x slower                                               |
| xml_etree_iterparse  | 108 ms                                                 | 133 ms: 1.23x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 70.4 ms: 1.24x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 105 ms: 1.30x slower                                                |
| tomli_loads          | 2.30 sec                                               | 3.41 sec: 1.48x slower                                              |
| unpickle_pure_python | 242 us                                                 | 406 us: 1.68x slower                                                |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                        |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.13 ms: 1.19x slower                                               |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                               |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 64.7 ms: 1.21x slower                                               |
| genshi_text     | 22.5 ms                                                | 27.3 ms: 1.21x slower                                               |
| django_template | 33.5 ms                                                | 42.9 ms: 1.28x slower                                               |
| mako            | 10.7 ms                                                | 20.9 ms: 1.96x slower                                               |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 130 us: 4.00x faster                                                |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.71x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 371 ms: 1.32x faster                                                |
| pylint                     | 476 ms                                                 | 360 ms: 1.32x faster                                                |
| async_tree_none            | 528 ms                                                 | 400 ms: 1.32x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 480 ms: 1.30x faster                                                |
| async_tree_io              | 1.29 sec                                               | 995 ms: 1.29x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                              |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                               |
| async_tree_memoization     | 639 ms                                                 | 529 ms: 1.21x faster                                                |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 649 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 660 ms: 1.14x faster                                                |
| json_loads                 | 29.2 us                                                | 27.9 us: 1.05x faster                                               |
| djangocms                  | 33.5 us                                                | 32.1 us: 1.04x faster                                               |
| pickle_pure_python         | 320 us                                                 | 314 us: 1.02x faster                                                |
| logging_silent             | 111 ns                                                 | 109 ns: 1.02x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.95 ms: 1.01x faster                                               |
| xml_etree_parse            | 164 ms                                                 | 163 ms: 1.01x faster                                                |
| pidigits                   | 194 ms                                                 | 195 ms: 1.00x slower                                                |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.01x slower                                               |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                |
| pickle_dict                | 34.6 us                                                | 35.8 us: 1.03x slower                                               |
| deepcopy_reduce            | 3.22 us                                                | 3.41 us: 1.06x slower                                               |
| dask                       | 365 ms                                                 | 388 ms: 1.06x slower                                                |
| tornado_http               | 98.1 ms                                                | 104 ms: 1.06x slower                                                |
| mdp                        | 2.77 sec                                               | 2.99 sec: 1.08x slower                                              |
| thrift                     | 784 us                                                 | 846 us: 1.08x slower                                                |
| logging_simple             | 6.22 us                                                | 6.72 us: 1.08x slower                                               |
| deepcopy                   | 365 us                                                 | 395 us: 1.08x slower                                                |
| logging_format             | 6.81 us                                                | 7.42 us: 1.09x slower                                               |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                               |
| regex_effbot               | 3.51 ms                                                | 3.88 ms: 1.11x slower                                               |
| bench_thread_pool          | 834 us                                                 | 933 us: 1.12x slower                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.97 ms: 1.13x slower                                               |
| pickle_list                | 4.59 us                                                | 5.20 us: 1.13x slower                                               |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                               |
| gunicorn                   | 1.20 ms                                                | 1.36 ms: 1.13x slower                                               |
| sympy_sum                  | 169 ms                                                 | 192 ms: 1.13x slower                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.63 ms: 1.13x slower                                               |
| regex_dna                  | 205 ms                                                 | 235 ms: 1.15x slower                                                |
| sympy_expand               | 484 ms                                                 | 562 ms: 1.16x slower                                                |
| html5lib                   | 64.8 ms                                                | 75.6 ms: 1.17x slower                                               |
| pycparser                  | 1.19 sec                                               | 1.39 sec: 1.17x slower                                              |
| dulwich_log                | 64.6 ms                                                | 75.8 ms: 1.17x slower                                               |
| sympy_str                  | 297 ms                                                 | 349 ms: 1.17x slower                                                |
| sqlglot_normalize          | 113 ms                                                 | 134 ms: 1.19x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 7.13 ms: 1.19x slower                                               |
| sympy_integrate            | 21.5 ms                                                | 25.5 ms: 1.19x slower                                               |
| regex_v8                   | 22.9 ms                                                | 27.2 ms: 1.19x slower                                               |
| chameleon                  | 6.70 ms                                                | 8.07 ms: 1.20x slower                                               |
| genshi_xml                 | 53.4 ms                                                | 64.7 ms: 1.21x slower                                               |
| raytrace                   | 309 ms                                                 | 374 ms: 1.21x slower                                                |
| genshi_text                | 22.5 ms                                                | 27.3 ms: 1.21x slower                                               |
| mypy2                      | 686 ms                                                 | 833 ms: 1.22x slower                                                |
| unpickle                   | 13.8 us                                                | 16.8 us: 1.22x slower                                               |
| sqlite_synth               | 2.57 us                                                | 3.16 us: 1.23x slower                                               |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.23x slower                                               |
| docutils                   | 2.66 sec                                               | 3.28 sec: 1.23x slower                                              |
| xml_etree_iterparse        | 108 ms                                                 | 133 ms: 1.23x slower                                                |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                               |
| xml_etree_process          | 56.9 ms                                                | 70.4 ms: 1.24x slower                                               |
| 2to3                       | 264 ms                                                 | 332 ms: 1.25x slower                                                |
| deepcopy_memo              | 40.2 us                                                | 50.5 us: 1.26x slower                                               |
| deltablue                  | 3.92 ms                                                | 4.94 ms: 1.26x slower                                               |
| coverage                   | 78.8 ms                                                | 99.3 ms: 1.26x slower                                               |
| django_template            | 33.5 ms                                                | 42.9 ms: 1.28x slower                                               |
| sqlglot_optimize           | 55.3 ms                                                | 71.1 ms: 1.29x slower                                               |
| xml_etree_generate         | 81.1 ms                                                | 105 ms: 1.30x slower                                                |
| richards_super             | 61.9 ms                                                | 81.1 ms: 1.31x slower                                               |
| meteor_contest             | 109 ms                                                 | 144 ms: 1.32x slower                                                |
| async_generators           | 374 ms                                                 | 507 ms: 1.36x slower                                                |
| chaos                      | 71.9 ms                                                | 101 ms: 1.40x slower                                                |
| telco                      | 6.86 ms                                                | 9.71 ms: 1.42x slower                                               |
| scimark_sor                | 121 ms                                                 | 174 ms: 1.43x slower                                                |
| tomli_loads                | 2.30 sec                                               | 3.41 sec: 1.48x slower                                              |
| comprehensions             | 23.6 us                                                | 35.2 us: 1.49x slower                                               |
| richards                   | 49.8 ms                                                | 74.5 ms: 1.50x slower                                               |
| go                         | 149 ms                                                 | 226 ms: 1.52x slower                                                |
| regex_compile              | 141 ms                                                 | 223 ms: 1.58x slower                                                |
| crypto_pyaes               | 76.7 ms                                                | 127 ms: 1.66x slower                                                |
| pprint_pformat             | 1.55 sec                                               | 2.59 sec: 1.66x slower                                              |
| pprint_safe_repr           | 747 ms                                                 | 1.24 sec: 1.67x slower                                              |
| unpickle_pure_python       | 242 us                                                 | 406 us: 1.68x slower                                                |
| nqueens                    | 87.9 ms                                                | 151 ms: 1.72x slower                                                |
| float                      | 78.9 ms                                                | 139 ms: 1.76x slower                                                |
| scimark_lu                 | 116 ms                                                 | 208 ms: 1.79x slower                                                |
| scimark_fft                | 345 ms                                                 | 630 ms: 1.82x slower                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 9.27 ms: 1.84x slower                                               |
| fannkuch                   | 405 ms                                                 | 754 ms: 1.86x slower                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 138 ms: 1.95x slower                                                |
| mako                       | 10.7 ms                                                | 20.9 ms: 1.96x slower                                               |
| pyflate                    | 434 ms                                                 | 880 ms: 2.03x slower                                                |
| nbody                      | 96.0 ms                                                | 203 ms: 2.12x slower                                                |
| spectral_norm              | 108 ms                                                 | 237 ms: 2.19x slower                                                |
| hexiom                     | 6.89 ms                                                | 15.1 ms: 2.20x slower                                               |
| Geometric mean             | (ref)                                                  | 1.16x slower                                                        |

Benchmark hidden because not significant (3): json, bench_mp_pool, unpickle_list
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.03x