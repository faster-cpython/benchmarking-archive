# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.06x faster
- HPT reliability: 89.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.09 ms: 1.06x slower                                                  |
| docutils       | 2.66 sec                                               | 2.89 sec: 1.08x slower                                                 |
| html5lib       | 64.8 ms                                                | 66.5 ms: 1.03x slower                                                  |
| tornado_http   | 98.1 ms                                                | 94.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 925 ms: 1.39x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 948 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                | 76.6 ms: 1.03x faster                                                  |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| nbody          | 96.0 ms                                                | 94.3 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                  |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                  |
| regex_dna      | 205 ms                                                 | 228 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 233 us: 1.04x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.01x slower                                                  |
| unpickle_list        | 5.21 us                                                | 5.32 us: 1.02x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                  |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                                  |
| unpickle             | 13.8 us                                                | 16.2 us: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.57 ms: 1.26x slower                                                  |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                  |
| genshi_xml      | 53.4 ms                                                | 53.8 ms: 1.01x slower                                                  |
| genshi_text     | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                  |
| django_template | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.62x faster                                                   |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 509 ms: 1.72x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                 |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                   |
| pylint                     | 476 ms                                                 | 333 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 925 ms: 1.39x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 948 ms: 1.37x faster                                                   |
| comprehensions             | 23.6 us                                                | 17.9 us: 1.32x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| richards_super             | 61.9 ms                                                | 48.8 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                   |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                                  |
| richards                   | 49.8 ms                                                | 42.6 ms: 1.17x faster                                                  |
| chaos                      | 71.9 ms                                                | 62.3 ms: 1.15x faster                                                  |
| raytrace                   | 309 ms                                                 | 270 ms: 1.14x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.57 ms: 1.12x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.61 ms: 1.09x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.82 us: 1.07x faster                                                  |
| logging_silent             | 111 ns                                                 | 104 ns: 1.06x faster                                                   |
| logging_format             | 6.81 us                                                | 6.45 us: 1.06x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.78 ms: 1.05x faster                                                  |
| djangocms                  | 33.5 us                                                | 32.0 us: 1.05x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                  |
| fannkuch                   | 405 ms                                                 | 388 ms: 1.05x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 233 us: 1.04x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| tornado_http               | 98.1 ms                                                | 94.9 ms: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.4 ms: 1.03x faster                                                  |
| float                      | 78.9 ms                                                | 76.6 ms: 1.03x faster                                                  |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 69.1 ms: 1.02x faster                                                  |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                   |
| scimark_fft                | 345 ms                                                 | 339 ms: 1.02x faster                                                   |
| nbody                      | 96.0 ms                                                | 94.3 ms: 1.02x faster                                                  |
| sympy_str                  | 297 ms                                                 | 292 ms: 1.02x faster                                                   |
| deepcopy                   | 365 us                                                 | 359 us: 1.02x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.80 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                 |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                                 |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                   |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.01x faster                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                                  |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 53.8 ms: 1.01x slower                                                  |
| sympy_expand               | 484 ms                                                 | 490 ms: 1.01x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.01x slower                                                  |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                   |
| nqueens                    | 87.9 ms                                                | 89.2 ms: 1.02x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 21.8 ms: 1.02x slower                                                  |
| dask                       | 365 ms                                                 | 372 ms: 1.02x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.32 us: 1.02x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 852 us: 1.02x slower                                                   |
| mdp                        | 2.77 sec                                               | 2.84 sec: 1.02x slower                                                 |
| html5lib                   | 64.8 ms                                                | 66.5 ms: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 806 us: 1.03x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 56.9 ms: 1.03x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                   |
| go                         | 149 ms                                                 | 153 ms: 1.03x slower                                                   |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.04x slower                                                   |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.09 ms: 1.06x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 68.7 ms: 1.06x slower                                                  |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.20 ms: 1.07x slower                                                  |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                                   |
| genshi_text                | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.29 ms: 1.08x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.89 sec: 1.08x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                                  |
| django_template            | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                  |
| pyflate                    | 434 ms                                                 | 476 ms: 1.10x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                  |
| regex_dna                  | 205 ms                                                 | 228 ms: 1.11x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                  |
| mypy2                      | 686 ms                                                 | 782 ms: 1.14x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.14x slower                                                   |
| unpickle                   | 13.8 us                                                | 16.2 us: 1.17x slower                                                  |
| async_generators           | 374 ms                                                 | 458 ms: 1.23x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                  |
| coverage                   | 78.8 ms                                                | 97.3 ms: 1.24x slower                                                  |
| telco                      | 6.86 ms                                                | 8.56 ms: 1.25x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.57 ms: 1.26x slower                                                  |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): bench_mp_pool, pprint_safe_repr
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 89.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x