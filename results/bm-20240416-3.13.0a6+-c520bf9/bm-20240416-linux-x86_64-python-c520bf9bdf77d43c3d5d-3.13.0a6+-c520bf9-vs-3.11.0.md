# Results vs. 3.11.0

- fork: python
- ref: c520bf9bdf77d43c3d5d
- machine: linux-x86_64
- commit hash: c520bf9
- commit date: 2024-04-16
- overall geometric mean: 1.07x faster
- HPT reliability: 98.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                   |
| chameleon      | 6.70 ms                                                | 6.94 ms: 1.04x slower                                                  |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                 |
| html5lib       | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                  |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.38x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 936 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.0 ms: 1.07x faster                                                  |
| pidigits       | 194 ms                                                 | 206 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                   |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                                   |
| regex_effbot   | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                  |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 217 us: 1.11x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                 |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| unpickle_list        | 5.21 us                                                | 4.99 us: 1.05x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| xml_etree_process    | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                  |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 88.8 ms: 1.10x slower                                                  |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.33 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                  |
| mako            | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                  |
| genshi_text     | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                  |
| django_template | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.52x faster                                                   |
| generators                 | 74.9 ms                                                | 30.9 ms: 2.42x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 507 ms: 1.73x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.69x faster                                                 |
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                   |
| pylint                     | 476 ms                                                 | 320 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.40x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.38x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 936 ms: 1.37x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.26 ms: 1.20x faster                                                  |
| chaos                      | 71.9 ms                                                | 60.2 ms: 1.19x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                                  |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                                   |
| richards_super             | 61.9 ms                                                | 53.7 ms: 1.15x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 217 us: 1.11x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| nqueens                    | 87.9 ms                                                | 81.7 ms: 1.08x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.43 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                   |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.60 sec: 1.07x faster                                                 |
| nbody                      | 96.0 ms                                                | 90.0 ms: 1.07x faster                                                  |
| logging_format             | 6.81 us                                                | 6.40 us: 1.06x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.06x faster                                                  |
| djangocms                  | 33.5 us                                                | 31.5 us: 1.06x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.5 ms: 1.06x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.06x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.05x faster                                                  |
| unpickle_list              | 5.21 us                                                | 4.99 us: 1.05x faster                                                  |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                  |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                   |
| richards                   | 49.8 ms                                                | 47.9 ms: 1.04x faster                                                  |
| fannkuch                   | 405 ms                                                 | 391 ms: 1.04x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.87 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 68.4 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                 |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                   |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                  |
| deepcopy                   | 365 us                                                 | 356 us: 1.03x faster                                                   |
| sympy_expand               | 484 ms                                                 | 475 ms: 1.02x faster                                                   |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.01x faster                                                 |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 76.3 ms: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 55.6 ms: 1.00x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.23 us: 1.01x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 841 us: 1.01x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 754 ms: 1.01x slower                                                   |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                                   |
| dask                       | 365 ms                                                 | 371 ms: 1.02x slower                                                   |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                   |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 66.4 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.20 ms: 1.03x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.94 ms: 1.04x slower                                                  |
| html5lib                   | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                  |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                  |
| genshi_text                | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                  |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                                   |
| thrift                     | 784 us                                                 | 818 us: 1.04x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                  |
| pidigits                   | 194 ms                                                 | 206 ms: 1.06x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                 |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                                   |
| django_template            | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                  |
| scimark_fft                | 345 ms                                                 | 369 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                  |
| mypy2                      | 686 ms                                                 | 737 ms: 1.07x slower                                                   |
| pyflate                    | 434 ms                                                 | 471 ms: 1.09x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 88.8 ms: 1.10x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.33 us: 1.16x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                  |
| async_generators           | 374 ms                                                 | 445 ms: 1.19x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| telco                      | 6.86 ms                                                | 8.55 ms: 1.25x slower                                                  |
| coverage                   | 78.8 ms                                                | 98.6 ms: 1.25x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): float, scimark_lu, pickle_dict
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.55% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x