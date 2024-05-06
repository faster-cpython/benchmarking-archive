# Results vs. 3.11.0

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.05x faster
- HPT reliability: 84.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.16 ms: 1.07x slower                                                |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                               |
| html5lib       | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                |
| tornado_http   | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 359 ms: 1.47x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 341 ms: 1.44x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.40x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 935 ms: 1.38x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 955 ms: 1.36x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.9 ms: 1.06x faster                                                |
| float          | 78.9 ms                                                | 76.5 ms: 1.03x faster                                                |
| pidigits       | 194 ms                                                 | 210 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.00x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                 |
| regex_effbot   | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                 |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.03 sec: 1.14x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.08x faster                                                 |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                |
| xml_etree_iterparse  | 108 ms                                                 | 103 ms: 1.05x faster                                                 |
| unpickle_pure_python | 242 us                                                 | 231 us: 1.05x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                                 |
| unpickle_list        | 5.21 us                                                | 5.27 us: 1.01x slower                                                |
| pickle_dict          | 34.6 us                                                | 35.0 us: 1.01x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 87.5 ms: 1.08x slower                                                |
| pickle               | 11.0 us                                                | 11.9 us: 1.09x slower                                                |
| pickle_list          | 4.59 us                                                | 5.02 us: 1.09x slower                                                |
| unpickle             | 13.8 us                                                | 16.4 us: 1.19x slower                                                |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.4 ms: 1.02x faster                                                |
| genshi_xml      | 53.4 ms                                                | 57.2 ms: 1.07x slower                                                |
| django_template | 33.5 ms                                                | 36.8 ms: 1.10x slower                                                |
| genshi_text     | 22.5 ms                                                | 25.7 ms: 1.14x slower                                                |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.01x faster                                                 |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.48x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 523 ms: 1.67x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                               |
| async_tree_none            | 528 ms                                                 | 359 ms: 1.47x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 341 ms: 1.44x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.40x faster                                                 |
| pylint                     | 476 ms                                                 | 343 ms: 1.39x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 935 ms: 1.38x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 955 ms: 1.36x faster                                                 |
| comprehensions             | 23.6 us                                                | 18.0 us: 1.31x faster                                                |
| richards_super             | 61.9 ms                                                | 48.5 ms: 1.28x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                 |
| richards                   | 49.8 ms                                                | 42.4 ms: 1.17x faster                                                |
| coroutines                 | 27.0 ms                                                | 23.3 ms: 1.16x faster                                                |
| tomli_loads                | 2.30 sec                                               | 2.03 sec: 1.14x faster                                               |
| chaos                      | 71.9 ms                                                | 63.5 ms: 1.13x faster                                                |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                                 |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                 |
| fannkuch                   | 405 ms                                                 | 372 ms: 1.09x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.08x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.79 ms: 1.06x faster                                                |
| logging_simple             | 6.22 us                                                | 5.89 us: 1.06x faster                                                |
| nbody                      | 96.0 ms                                                | 90.9 ms: 1.06x faster                                                |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                |
| mdp                        | 2.77 sec                                               | 2.63 sec: 1.05x faster                                               |
| xml_etree_iterparse        | 108 ms                                                 | 103 ms: 1.05x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 231 us: 1.05x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                                 |
| logging_format             | 6.81 us                                                | 6.52 us: 1.04x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 67.8 ms: 1.04x faster                                                |
| crypto_pyaes               | 76.7 ms                                                | 73.9 ms: 1.04x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 38.9 us: 1.03x faster                                                |
| djangocms                  | 33.5 us                                                | 32.4 us: 1.03x faster                                                |
| float                      | 78.9 ms                                                | 76.5 ms: 1.03x faster                                                |
| mako                       | 10.7 ms                                                | 10.4 ms: 1.02x faster                                                |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                               |
| scimark_fft                | 345 ms                                                 | 338 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.93 ms: 1.02x faster                                                |
| tornado_http               | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                 |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.00x faster                                                 |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.00x slower                                                 |
| deepcopy                   | 365 us                                                 | 367 us: 1.00x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.27 us: 1.01x slower                                                |
| spectral_norm              | 108 ms                                                 | 109 ms: 1.01x slower                                                 |
| pickle_dict                | 34.6 us                                                | 35.0 us: 1.01x slower                                                |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                 |
| nqueens                    | 87.9 ms                                                | 90.2 ms: 1.03x slower                                                |
| sympy_expand               | 484 ms                                                 | 498 ms: 1.03x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                |
| dask                       | 365 ms                                                 | 377 ms: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 863 us: 1.03x slower                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 57.4 ms: 1.04x slower                                                |
| sympy_integrate            | 21.5 ms                                                | 22.3 ms: 1.04x slower                                                |
| go                         | 149 ms                                                 | 155 ms: 1.04x slower                                                 |
| thrift                     | 784 us                                                 | 828 us: 1.06x slower                                                 |
| html5lib                   | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.16 ms: 1.07x slower                                                |
| genshi_xml                 | 53.4 ms                                                | 57.2 ms: 1.07x slower                                                |
| pyflate                    | 434 ms                                                 | 468 ms: 1.08x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 87.5 ms: 1.08x slower                                                |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 69.8 ms: 1.08x slower                                                |
| pidigits                   | 194 ms                                                 | 210 ms: 1.08x slower                                                 |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                 |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.09x slower                                                |
| django_template            | 33.5 ms                                                | 36.8 ms: 1.10x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                               |
| sqlite_synth               | 2.57 us                                                | 2.88 us: 1.12x slower                                                |
| genshi_text                | 22.5 ms                                                | 25.7 ms: 1.14x slower                                                |
| scimark_lu                 | 116 ms                                                 | 134 ms: 1.15x slower                                                 |
| coverage                   | 78.8 ms                                                | 92.6 ms: 1.18x slower                                                |
| mypy2                      | 686 ms                                                 | 806 ms: 1.18x slower                                                 |
| unpickle                   | 13.8 us                                                | 16.4 us: 1.19x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.23x slower                                                |
| telco                      | 6.86 ms                                                | 8.48 ms: 1.24x slower                                                |
| async_generators           | 374 ms                                                 | 465 ms: 1.25x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (7): deltablue, pycparser, pprint_safe_repr, bench_mp_pool, sympy_str, deepcopy_reduce, hexiom
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 84.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x