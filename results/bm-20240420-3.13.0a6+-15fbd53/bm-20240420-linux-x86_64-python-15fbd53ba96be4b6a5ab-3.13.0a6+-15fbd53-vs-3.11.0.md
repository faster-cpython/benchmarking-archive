# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.07x faster
- HPT reliability: 99.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.01x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                  |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                 |
| html5lib       | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                  |
| tornado_http   | 98.1 ms                                                | 94.2 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 926 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.7 ms: 1.08x faster                                                  |
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                  |
| regex_v8       | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                  |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 213 us: 1.13x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                   |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 157 ms: 1.04x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.6 us: 1.03x slower                                                  |
| unpickle_list        | 5.21 us                                                | 5.46 us: 1.05x slower                                                  |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 87.1 ms: 1.07x slower                                                  |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.16 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.9 ms: 1.01x faster                                                  |
| mako            | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                  |
| django_template | 33.5 ms                                                | 35.0 ms: 1.04x slower                                                  |
| genshi_text     | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.45x faster                                                   |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.50x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                 |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                   |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 926 ms: 1.39x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.24 ms: 1.21x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                                  |
| chaos                      | 71.9 ms                                                | 60.6 ms: 1.19x faster                                                  |
| raytrace                   | 309 ms                                                 | 262 ms: 1.18x faster                                                   |
| richards_super             | 61.9 ms                                                | 53.0 ms: 1.17x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 213 us: 1.13x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                  |
| logging_silent             | 111 ns                                                 | 100 ns: 1.11x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.23 ms: 1.11x faster                                                  |
| nqueens                    | 87.9 ms                                                | 79.9 ms: 1.10x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                                  |
| nbody                      | 96.0 ms                                                | 88.7 ms: 1.08x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 37.4 us: 1.07x faster                                                  |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                   |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                 |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                                  |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                  |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.95 us: 1.04x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 157 ms: 1.04x faster                                                   |
| tornado_http               | 98.1 ms                                                | 94.2 ms: 1.04x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.04x faster                                                   |
| logging_format             | 6.81 us                                                | 6.57 us: 1.04x faster                                                  |
| sympy_expand               | 484 ms                                                 | 469 ms: 1.03x faster                                                   |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                 |
| fannkuch                   | 405 ms                                                 | 393 ms: 1.03x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 68.7 ms: 1.03x faster                                                  |
| go                         | 149 ms                                                 | 145 ms: 1.03x faster                                                   |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                                   |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 75.4 ms: 1.02x faster                                                  |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.73 sec: 1.02x faster                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 54.7 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 740 ms: 1.01x faster                                                   |
| genshi_xml                 | 53.4 ms                                                | 52.9 ms: 1.01x faster                                                  |
| bench_thread_pool          | 834 us                                                 | 830 us: 1.01x faster                                                   |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                   |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                  |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.25 us: 1.01x slower                                                  |
| 2to3                       | 264 ms                                                 | 268 ms: 1.01x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 66.0 ms: 1.02x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.6 us: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                   |
| html5lib                   | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.23 ms: 1.04x slower                                                  |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                                   |
| django_template            | 33.5 ms                                                | 35.0 ms: 1.04x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.46 us: 1.05x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                 |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                  |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                  |
| mypy2                      | 686 ms                                                 | 735 ms: 1.07x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 87.1 ms: 1.07x slower                                                  |
| genshi_text                | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                  |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                   |
| scimark_fft                | 345 ms                                                 | 374 ms: 1.08x slower                                                   |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                  |
| pyflate                    | 434 ms                                                 | 483 ms: 1.11x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.16 us: 1.12x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.97 us: 1.16x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                  |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.74 ms: 1.22x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| coverage                   | 78.8 ms                                                | 97.5 ms: 1.24x slower                                                  |
| telco                      | 6.86 ms                                                | 8.74 ms: 1.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_iterparse, bench_mp_pool, float, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.81% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x