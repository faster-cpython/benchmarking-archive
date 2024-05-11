# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: linux-x86_64
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.06x slower
- HPT reliability: 98.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                       |
| chameleon      | 6.70 ms                                                | 8.24 ms: 1.23x slower                                      |
| docutils       | 2.66 sec                                               | 3.07 sec: 1.15x slower                                     |
| html5lib       | 64.8 ms                                                | 67.9 ms: 1.05x slower                                      |
| tornado_http   | 98.1 ms                                                | 98.6 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io              | 1.29 sec                                               | 796 ms: 1.62x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 828 ms: 1.56x faster                                       |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 458 ms: 1.37x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 476 ms: 1.34x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 377 ms: 1.30x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 646 ms: 1.16x faster                                       |
| Geometric mean             | (ref)                                                  | 1.37x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 78.9 ms                                                | 74.2 ms: 1.06x faster                                      |
| nbody          | 96.0 ms                                                | 104 ms: 1.09x slower                                       |
| Geometric mean | (ref)                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 141 ms: 1.00x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.60 ms: 1.03x slower                                      |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                      |
| regex_dna      | 205 ms                                                 | 232 ms: 1.13x slower                                       |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.6 ms: 1.15x faster                                      |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.08x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.23 sec: 1.03x faster                                     |
| unpickle_pure_python | 242 us                                                 | 237 us: 1.02x faster                                       |
| pickle_pure_python   | 320 us                                                 | 333 us: 1.04x slower                                       |
| pickle_list          | 4.59 us                                                | 4.88 us: 1.06x slower                                      |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                      |
| json_loads           | 29.2 us                                                | 32.2 us: 1.10x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 90.5 ms: 1.12x slower                                      |
| pickle_dict          | 34.6 us                                                | 41.2 us: 1.19x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 71.1 ms: 1.25x slower                                      |
| unpickle             | 13.8 us                                                | 18.0 us: 1.30x slower                                      |
| xml_etree_iterparse  | 108 ms                                                 | 166 ms: 1.53x slower                                       |
| Geometric mean       | (ref)                                                  | 1.09x slower                                               |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 12.0 ms: 1.40x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 10.0 ms: 1.67x slower                                      |
| Geometric mean         | (ref)                                                  | 1.53x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 54.7 ms: 1.02x slower                                      |
| genshi_text     | 22.5 ms                                                | 26.1 ms: 1.16x slower                                      |
| django_template | 33.5 ms                                                | 39.1 ms: 1.16x slower                                      |
| mako            | 10.7 ms                                                | 16.3 ms: 1.53x slower                                      |
| Geometric mean  | (ref)                                                  | 1.21x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 122 us: 4.26x faster                                       |
| generators                 | 74.9 ms                                                | 31.2 ms: 2.40x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                     |
| async_tree_io              | 1.29 sec                                               | 796 ms: 1.62x faster                                       |
| pylint                     | 476 ms                                                 | 296 ms: 1.61x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 828 ms: 1.56x faster                                       |
| gc_traversal               | 4.01 ms                                                | 2.57 ms: 1.56x faster                                      |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.03 ms: 1.39x faster                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 458 ms: 1.37x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 476 ms: 1.34x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 377 ms: 1.30x faster                                       |
| comprehensions             | 23.6 us                                                | 18.5 us: 1.27x faster                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                       |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.18x faster                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 646 ms: 1.16x faster                                       |
| json_dumps                 | 13.3 ms                                                | 11.6 ms: 1.15x faster                                      |
| richards_super             | 61.9 ms                                                | 56.3 ms: 1.10x faster                                      |
| chaos                      | 71.9 ms                                                | 66.2 ms: 1.09x faster                                      |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.08x faster                                       |
| float                      | 78.9 ms                                                | 74.2 ms: 1.06x faster                                      |
| hexiom                     | 6.89 ms                                                | 6.62 ms: 1.04x faster                                      |
| nqueens                    | 87.9 ms                                                | 84.7 ms: 1.04x faster                                      |
| raytrace                   | 309 ms                                                 | 298 ms: 1.04x faster                                       |
| tomli_loads                | 2.30 sec                                               | 2.23 sec: 1.03x faster                                     |
| bench_mp_pool              | 24.0 ms                                                | 23.4 ms: 1.03x faster                                      |
| unpickle_pure_python       | 242 us                                                 | 237 us: 1.02x faster                                       |
| crypto_pyaes               | 76.7 ms                                                | 75.5 ms: 1.02x faster                                      |
| richards                   | 49.8 ms                                                | 49.2 ms: 1.01x faster                                      |
| regex_compile              | 141 ms                                                 | 141 ms: 1.00x faster                                       |
| tornado_http               | 98.1 ms                                                | 98.6 ms: 1.01x slower                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.44 ms: 1.01x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 557 ms: 1.01x slower                                       |
| mypy2                      | 686 ms                                                 | 696 ms: 1.02x slower                                       |
| sqlglot_transpile          | 1.75 ms                                                | 1.78 ms: 1.02x slower                                      |
| genshi_xml                 | 53.4 ms                                                | 54.7 ms: 1.02x slower                                      |
| pathlib                    | 18.5 ms                                                | 19.0 ms: 1.02x slower                                      |
| regex_effbot               | 3.51 ms                                                | 3.60 ms: 1.03x slower                                      |
| logging_silent             | 111 ns                                                 | 114 ns: 1.03x slower                                       |
| sqlglot_normalize          | 113 ms                                                 | 116 ms: 1.03x slower                                       |
| logging_simple             | 6.22 us                                                | 6.43 us: 1.03x slower                                      |
| go                         | 149 ms                                                 | 154 ms: 1.04x slower                                       |
| scimark_lu                 | 116 ms                                                 | 121 ms: 1.04x slower                                       |
| pickle_pure_python         | 320 us                                                 | 333 us: 1.04x slower                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.25 ms: 1.04x slower                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 74.0 ms: 1.05x slower                                      |
| html5lib                   | 64.8 ms                                                | 67.9 ms: 1.05x slower                                      |
| logging_format             | 6.81 us                                                | 7.18 us: 1.05x slower                                      |
| fannkuch                   | 405 ms                                                 | 428 ms: 1.06x slower                                       |
| pprint_pformat             | 1.55 sec                                               | 1.64 sec: 1.06x slower                                     |
| meteor_contest             | 109 ms                                                 | 115 ms: 1.06x slower                                       |
| deltablue                  | 3.92 ms                                                | 4.16 ms: 1.06x slower                                      |
| pickle_list                | 4.59 us                                                | 4.88 us: 1.06x slower                                      |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.07x slower                                       |
| pprint_safe_repr           | 747 ms                                                 | 797 ms: 1.07x slower                                       |
| deepcopy                   | 365 us                                                 | 390 us: 1.07x slower                                       |
| dulwich_log                | 64.6 ms                                                | 69.0 ms: 1.07x slower                                      |
| sqlglot_optimize           | 55.3 ms                                                | 59.3 ms: 1.07x slower                                      |
| deepcopy_reduce            | 3.22 us                                                | 3.46 us: 1.08x slower                                      |
| nbody                      | 96.0 ms                                                | 104 ms: 1.09x slower                                       |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                       |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                       |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                      |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                      |
| scimark_fft                | 345 ms                                                 | 380 ms: 1.10x slower                                       |
| json_loads                 | 29.2 us                                                | 32.2 us: 1.10x slower                                      |
| json                       | 5.24 ms                                                | 5.81 ms: 1.11x slower                                      |
| sympy_integrate            | 21.5 ms                                                | 23.8 ms: 1.11x slower                                      |
| xml_etree_generate         | 81.1 ms                                                | 90.5 ms: 1.12x slower                                      |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                       |
| regex_dna                  | 205 ms                                                 | 232 ms: 1.13x slower                                       |
| deepcopy_memo              | 40.2 us                                                | 45.6 us: 1.13x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.27 ms: 1.14x slower                                      |
| gunicorn                   | 1.20 ms                                                | 1.37 ms: 1.15x slower                                      |
| docutils                   | 2.66 sec                                               | 3.07 sec: 1.15x slower                                     |
| genshi_text                | 22.5 ms                                                | 26.1 ms: 1.16x slower                                      |
| django_template            | 33.5 ms                                                | 39.1 ms: 1.16x slower                                      |
| sympy_str                  | 297 ms                                                 | 354 ms: 1.19x slower                                       |
| pickle_dict                | 34.6 us                                                | 41.2 us: 1.19x slower                                      |
| chameleon                  | 6.70 ms                                                | 8.24 ms: 1.23x slower                                      |
| sqlite_synth               | 2.57 us                                                | 3.17 us: 1.23x slower                                      |
| async_generators           | 374 ms                                                 | 463 ms: 1.24x slower                                       |
| xml_etree_process          | 56.9 ms                                                | 71.1 ms: 1.25x slower                                      |
| sympy_sum                  | 169 ms                                                 | 211 ms: 1.25x slower                                       |
| sympy_expand               | 484 ms                                                 | 623 ms: 1.29x slower                                       |
| unpickle                   | 13.8 us                                                | 18.0 us: 1.30x slower                                      |
| mdp                        | 2.77 sec                                               | 3.64 sec: 1.31x slower                                     |
| telco                      | 6.86 ms                                                | 9.09 ms: 1.32x slower                                      |
| python_startup             | 8.56 ms                                                | 12.0 ms: 1.40x slower                                      |
| mako                       | 10.7 ms                                                | 16.3 ms: 1.53x slower                                      |
| xml_etree_iterparse        | 108 ms                                                 | 166 ms: 1.53x slower                                       |
| python_startup_no_site     | 6.01 ms                                                | 10.0 ms: 1.67x slower                                      |
| flaskblogging              | 7.28 ms                                                | 18.7 ms: 2.57x slower                                      |
| bench_thread_pool          | 834 us                                                 | 2.42 ms: 2.91x slower                                      |
| coverage                   | 78.8 ms                                                | 712 ms: 9.04x slower                                       |
| thrift                     | 784 us                                                 | 9.43 ms: 12.03x slower                                     |
| Geometric mean             | (ref)                                                  | 1.06x slower                                               |

Benchmark hidden because not significant (3): unpickle_list, pidigits, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, djangocms, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.42% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x