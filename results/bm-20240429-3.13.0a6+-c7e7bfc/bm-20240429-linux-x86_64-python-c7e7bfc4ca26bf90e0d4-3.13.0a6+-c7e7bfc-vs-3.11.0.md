# Results vs. 3.11.0

- fork: python
- ref: c7e7bfc4ca26bf90e0d4
- machine: linux-x86_64
- commit hash: c7e7bfc
- commit date: 2024-04-29
- overall geometric mean: 1.07x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 267 ms: 1.01x slower                                                   |
| chameleon      | 6.70 ms                                                | 6.95 ms: 1.04x slower                                                  |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                 |
| html5lib       | 64.8 ms                                                | 66.2 ms: 1.02x slower                                                  |
| tornado_http   | 98.1 ms                                                | 93.6 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 331 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 436 ms: 1.44x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.38x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                  |
| float          | 78.9 ms                                                | 78.0 ms: 1.01x faster                                                  |
| pidigits       | 194 ms                                                 | 212 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.06x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.9 ms: 1.09x slower                                                  |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 212 us: 1.14x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.14 sec: 1.08x faster                                                 |
| json_loads           | 29.2 us                                                | 27.3 us: 1.07x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                   |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.17 us: 1.01x faster                                                  |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 59.4 ms: 1.04x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 86.3 ms: 1.06x slower                                                  |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                  |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.0 ms: 1.03x faster                                                  |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                  |
| genshi_text     | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                  |
| django_template | 33.5 ms                                                | 35.0 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 164 us: 3.17x faster                                                   |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.50x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                 |
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                   |
| pylint                     | 476 ms                                                 | 317 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 331 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 436 ms: 1.44x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.39x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.38x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.21 ms: 1.22x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.21x faster                                                  |
| chaos                      | 71.9 ms                                                | 60.4 ms: 1.19x faster                                                  |
| raytrace                   | 309 ms                                                 | 261 ms: 1.18x faster                                                   |
| richards_super             | 61.9 ms                                                | 53.7 ms: 1.15x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 212 us: 1.14x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.28 ms: 1.12x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.13 ms: 1.12x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 153 ms: 1.10x faster                                                   |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                   |
| nbody                      | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.73 us: 1.09x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.70 ms: 1.08x faster                                                  |
| logging_format             | 6.81 us                                                | 6.33 us: 1.08x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.14 sec: 1.08x faster                                                 |
| sympy_str                  | 297 ms                                                 | 277 ms: 1.07x faster                                                   |
| nqueens                    | 87.9 ms                                                | 81.9 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 37.6 us: 1.07x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.3 us: 1.07x faster                                                  |
| sympy_integrate            | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                   |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                                  |
| regex_compile              | 141 ms                                                 | 134 ms: 1.06x faster                                                   |
| fannkuch                   | 405 ms                                                 | 385 ms: 1.05x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.64 sec: 1.05x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                  |
| richards                   | 49.8 ms                                                | 47.3 ms: 1.05x faster                                                  |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                                   |
| tornado_http               | 98.1 ms                                                | 93.6 ms: 1.05x faster                                                  |
| sympy_expand               | 484 ms                                                 | 464 ms: 1.04x faster                                                   |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| deepcopy                   | 365 us                                                 | 353 us: 1.03x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 68.6 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                 |
| genshi_xml                 | 53.4 ms                                                | 52.0 ms: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.7 ms: 1.03x faster                                                  |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 732 ms: 1.02x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.6 ms: 1.02x faster                                                  |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| float                      | 78.9 ms                                                | 78.0 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 54.6 ms: 1.01x faster                                                  |
| unpickle_list              | 5.21 us                                                | 5.17 us: 1.01x faster                                                  |
| bench_thread_pool          | 834 us                                                 | 827 us: 1.01x faster                                                   |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                   |
| 2to3                       | 264 ms                                                 | 267 ms: 1.01x slower                                                   |
| html5lib                   | 64.8 ms                                                | 66.2 ms: 1.02x slower                                                  |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 66.1 ms: 1.02x slower                                                  |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                   |
| spectral_norm              | 108 ms                                                 | 111 ms: 1.03x slower                                                   |
| genshi_text                | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.95 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.22 ms: 1.04x slower                                                  |
| thrift                     | 784 us                                                 | 815 us: 1.04x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.16 ms: 1.04x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                  |
| django_template            | 33.5 ms                                                | 35.0 ms: 1.04x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.4 ms: 1.04x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                 |
| scimark_fft                | 345 ms                                                 | 366 ms: 1.06x slower                                                   |
| pyflate                    | 434 ms                                                 | 461 ms: 1.06x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 86.3 ms: 1.06x slower                                                  |
| mypy2                      | 686 ms                                                 | 732 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 24.9 ms: 1.09x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                                  |
| pidigits                   | 194 ms                                                 | 212 ms: 1.09x slower                                                   |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.14x slower                                                  |
| coverage                   | 78.8 ms                                                | 91.0 ms: 1.16x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                  |
| async_generators           | 374 ms                                                 | 446 ms: 1.19x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.74 ms: 1.22x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| telco                      | 6.86 ms                                                | 8.62 ms: 1.26x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): deepcopy_reduce, dask, scimark_sor
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.03x