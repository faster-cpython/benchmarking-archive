# Results vs. 3.11.0

- fork: brandtbucher
- ref: hoist_partial
- machine: linux-x86_64
- commit hash: 1ce3b25
- commit date: 2024-05-09
- overall geometric mean: 1.02x faster
- HPT reliability: 89.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.17 ms: 1.07x slower                                                |
| docutils       | 2.66 sec                                               | 2.98 sec: 1.12x slower                                               |
| html5lib       | 64.8 ms                                                | 69.1 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 345 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 477 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 618 ms: 1.21x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                |
| nbody          | 96.0 ms                                                | 86.1 ms: 1.12x faster                                                |
| pidigits       | 194 ms                                                 | 197 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.01x faster                                                 |
| regex_effbot   | 3.51 ms                                                | 3.58 ms: 1.02x slower                                                |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                |
| regex_dna      | 205 ms                                                 | 226 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.18x faster                                               |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                 |
| pickle_dict          | 34.6 us                                                | 33.1 us: 1.05x faster                                                |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                |
| unpickle_list        | 5.21 us                                                | 5.27 us: 1.01x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 58.2 ms: 1.02x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 83.6 ms: 1.03x slower                                                |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                                |
| pickle_list          | 4.59 us                                                | 5.29 us: 1.15x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.70 ms: 1.28x slower                                                |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.62 ms: 1.11x faster                                                |
| django_template | 33.5 ms                                                | 36.5 ms: 1.09x slower                                                |
| genshi_xml      | 53.4 ms                                                | 58.7 ms: 1.10x slower                                                |
| genshi_text     | 22.5 ms                                                | 25.3 ms: 1.12x slower                                                |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 176 us: 2.95x faster                                                 |
| generators                 | 74.9 ms                                                | 30.2 ms: 2.48x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                               |
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                                 |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.44x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 345 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 477 ms: 1.34x faster                                                 |
| pylint                     | 476 ms                                                 | 357 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                               |
| richards_super             | 61.9 ms                                                | 49.1 ms: 1.26x faster                                                |
| chaos                      | 71.9 ms                                                | 58.8 ms: 1.22x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 618 ms: 1.21x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.18x faster                                               |
| richards                   | 49.8 ms                                                | 42.7 ms: 1.17x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.47 ms: 1.12x faster                                                |
| float                      | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                |
| nbody                      | 96.0 ms                                                | 86.1 ms: 1.12x faster                                                |
| mako                       | 10.7 ms                                                | 9.62 ms: 1.11x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 64.1 ms: 1.10x faster                                                |
| crypto_pyaes               | 76.7 ms                                                | 69.6 ms: 1.10x faster                                                |
| fannkuch                   | 405 ms                                                 | 368 ms: 1.10x faster                                                 |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                 |
| raytrace                   | 309 ms                                                 | 284 ms: 1.09x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                |
| scimark_fft                | 345 ms                                                 | 321 ms: 1.08x faster                                                 |
| spectral_norm              | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| deepcopy_memo              | 40.2 us                                                | 37.5 us: 1.07x faster                                                |
| logging_format             | 6.81 us                                                | 6.40 us: 1.06x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                 |
| deltablue                  | 3.92 ms                                                | 3.75 ms: 1.05x faster                                                |
| pickle_dict                | 34.6 us                                                | 33.1 us: 1.05x faster                                                |
| pprint_pformat             | 1.55 sec                                               | 1.50 sec: 1.04x faster                                               |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                 |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                                |
| pprint_safe_repr           | 747 ms                                                 | 724 ms: 1.03x faster                                                 |
| hexiom                     | 6.89 ms                                                | 6.69 ms: 1.03x faster                                                |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                               |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                |
| mdp                        | 2.77 sec                                               | 2.73 sec: 1.01x faster                                               |
| regex_compile              | 141 ms                                                 | 139 ms: 1.01x faster                                                 |
| go                         | 149 ms                                                 | 148 ms: 1.01x faster                                                 |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.27 us: 1.01x slower                                                |
| json                       | 5.24 ms                                                | 5.31 ms: 1.01x slower                                                |
| pidigits                   | 194 ms                                                 | 197 ms: 1.01x slower                                                 |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                 |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.02x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.58 ms: 1.02x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 58.2 ms: 1.02x slower                                                |
| gc_traversal               | 4.01 ms                                                | 4.11 ms: 1.02x slower                                                |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 83.6 ms: 1.03x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                 |
| pyflate                    | 434 ms                                                 | 449 ms: 1.03x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.34 us: 1.04x slower                                                |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 871 us: 1.04x slower                                                 |
| deepcopy                   | 365 us                                                 | 383 us: 1.05x slower                                                 |
| sympy_expand               | 484 ms                                                 | 512 ms: 1.06x slower                                                 |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 22.8 ms: 1.06x slower                                                |
| html5lib                   | 64.8 ms                                                | 69.1 ms: 1.07x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.17 ms: 1.07x slower                                                |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                                 |
| scimark_sor                | 121 ms                                                 | 132 ms: 1.08x slower                                                 |
| django_template            | 33.5 ms                                                | 36.5 ms: 1.09x slower                                                |
| dulwich_log                | 64.6 ms                                                | 70.4 ms: 1.09x slower                                                |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                |
| genshi_xml                 | 53.4 ms                                                | 58.7 ms: 1.10x slower                                                |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.11x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                |
| coverage                   | 78.8 ms                                                | 88.2 ms: 1.12x slower                                                |
| docutils                   | 2.66 sec                                               | 2.98 sec: 1.12x slower                                               |
| genshi_text                | 22.5 ms                                                | 25.3 ms: 1.12x slower                                                |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.13x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                                |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                                |
| pickle_list                | 4.59 us                                                | 5.29 us: 1.15x slower                                                |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.70 ms: 1.28x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.84 ms: 1.29x slower                                                |
| flaskblogging              | 7.28 ms                                                | 9.37 ms: 1.29x slower                                                |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                |
| telco                      | 6.86 ms                                                | 172 ms: 25.06x slower                                                |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (3): nqueens, tornado_http, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: djangocms, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 89.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x