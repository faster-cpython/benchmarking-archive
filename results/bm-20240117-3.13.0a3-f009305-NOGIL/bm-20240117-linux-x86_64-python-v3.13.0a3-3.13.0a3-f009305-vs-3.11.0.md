# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: linux-x86_64
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 290 ms: 1.10x slower                                       |
| chameleon      | 6.70 ms                                                | 7.87 ms: 1.18x slower                                      |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                     |
| html5lib       | 64.8 ms                                                | 70.5 ms: 1.09x slower                                      |
| tornado_http   | 98.1 ms                                                | 102 ms: 1.04x slower                                       |
| Geometric mean | (ref)                                                  | 1.10x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 537 ms: 1.09x slower                                       |
| async_tree_memoization     | 639 ms                                                 | 704 ms: 1.10x slower                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 848 ms: 1.11x slower                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 838 ms: 1.12x slower                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 702 ms: 1.12x slower                                       |
| async_tree_io              | 1.29 sec                                               | 1.49 sec: 1.16x slower                                     |
| async_tree_io_tg           | 1.29 sec                                               | 1.50 sec: 1.16x slower                                     |
| Geometric mean             | (ref)                                                  | 1.11x slower                                               |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 186 ms: 1.04x faster                                       |
| nbody          | 96.0 ms                                                | 105 ms: 1.10x slower                                       |
| float          | 78.9 ms                                                | 88.3 ms: 1.12x slower                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.02x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.52 ms: 1.00x slower                                      |
| regex_v8       | 22.9 ms                                                | 23.7 ms: 1.04x slower                                      |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                       |
| Geometric mean | (ref)                                                  | 1.02x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.0 ms: 1.21x faster                                      |
| unpickle_list        | 5.21 us                                                | 4.99 us: 1.05x faster                                      |
| pickle               | 11.0 us                                                | 10.6 us: 1.04x faster                                      |
| pickle_dict          | 34.6 us                                                | 33.2 us: 1.04x faster                                      |
| unpickle_pure_python | 242 us                                                 | 234 us: 1.03x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.24 sec: 1.03x faster                                     |
| pickle_pure_python   | 320 us                                                 | 318 us: 1.01x faster                                       |
| json_loads           | 29.2 us                                                | 29.3 us: 1.01x slower                                      |
| xml_etree_parse      | 164 ms                                                 | 172 ms: 1.05x slower                                       |
| xml_etree_iterparse  | 108 ms                                                 | 114 ms: 1.05x slower                                       |
| pickle_list          | 4.59 us                                                | 4.87 us: 1.06x slower                                      |
| unpickle             | 13.8 us                                                | 15.8 us: 1.14x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 65.4 ms: 1.15x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 94.2 ms: 1.16x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 12.1 ms: 1.41x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 10.5 ms: 1.74x slower                                      |
| Geometric mean         | (ref)                                                  | 1.57x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 55.0 ms: 1.03x slower                                      |
| genshi_text     | 22.5 ms                                                | 24.6 ms: 1.09x slower                                      |
| django_template | 33.5 ms                                                | 37.3 ms: 1.11x slower                                      |
| mako            | 10.7 ms                                                | 12.0 ms: 1.13x slower                                      |
| Geometric mean  | (ref)                                                  | 1.09x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 124 us: 4.20x faster                                       |
| generators                 | 74.9 ms                                                | 32.3 ms: 2.32x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.90 sec: 1.63x faster                                     |
| pylint                     | 476 ms                                                 | 335 ms: 1.42x faster                                       |
| comprehensions             | 23.6 us                                                | 17.7 us: 1.34x faster                                      |
| json_dumps                 | 13.3 ms                                                | 11.0 ms: 1.21x faster                                      |
| coroutines                 | 27.0 ms                                                | 23.6 ms: 1.15x faster                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.26 ms: 1.14x faster                                      |
| gc_traversal               | 4.01 ms                                                | 3.52 ms: 1.14x faster                                      |
| richards_super             | 61.9 ms                                                | 56.0 ms: 1.10x faster                                      |
| deltablue                  | 3.92 ms                                                | 3.56 ms: 1.10x faster                                      |
| chaos                      | 71.9 ms                                                | 65.2 ms: 1.10x faster                                      |
| raytrace                   | 309 ms                                                 | 291 ms: 1.06x faster                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.36 ms: 1.05x faster                                      |
| unpickle_list              | 5.21 us                                                | 4.99 us: 1.05x faster                                      |
| pidigits                   | 194 ms                                                 | 186 ms: 1.04x faster                                       |
| pickle                     | 11.0 us                                                | 10.6 us: 1.04x faster                                      |
| pickle_dict                | 34.6 us                                                | 33.2 us: 1.04x faster                                      |
| hexiom                     | 6.89 ms                                                | 6.64 ms: 1.04x faster                                      |
| unpickle_pure_python       | 242 us                                                 | 234 us: 1.03x faster                                       |
| nqueens                    | 87.9 ms                                                | 85.2 ms: 1.03x faster                                      |
| crypto_pyaes               | 76.7 ms                                                | 74.5 ms: 1.03x faster                                      |
| tomli_loads                | 2.30 sec                                               | 2.24 sec: 1.03x faster                                     |
| sqlglot_transpile          | 1.75 ms                                                | 1.71 ms: 1.03x faster                                      |
| bench_mp_pool              | 24.0 ms                                                | 23.5 ms: 1.02x faster                                      |
| regex_compile              | 141 ms                                                 | 139 ms: 1.02x faster                                       |
| pickle_pure_python         | 320 us                                                 | 318 us: 1.01x faster                                       |
| logging_silent             | 111 ns                                                 | 111 ns: 1.00x slower                                       |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.00x slower                                       |
| regex_effbot               | 3.51 ms                                                | 3.52 ms: 1.00x slower                                      |
| json_loads                 | 29.2 us                                                | 29.3 us: 1.01x slower                                      |
| go                         | 149 ms                                                 | 149 ms: 1.01x slower                                       |
| deepcopy                   | 365 us                                                 | 368 us: 1.01x slower                                       |
| asyncio_websockets         | 550 ms                                                 | 560 ms: 1.02x slower                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                      |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                      |
| logging_format             | 6.81 us                                                | 6.96 us: 1.02x slower                                      |
| pathlib                    | 18.5 ms                                                | 18.9 ms: 1.02x slower                                      |
| genshi_xml                 | 53.4 ms                                                | 55.0 ms: 1.03x slower                                      |
| scimark_lu                 | 116 ms                                                 | 120 ms: 1.03x slower                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.3 ms: 1.04x slower                                      |
| regex_v8                   | 22.9 ms                                                | 23.7 ms: 1.04x slower                                      |
| tornado_http               | 98.1 ms                                                | 102 ms: 1.04x slower                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 74.0 ms: 1.05x slower                                      |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.05x slower                                       |
| xml_etree_parse            | 164 ms                                                 | 172 ms: 1.05x slower                                       |
| xml_etree_iterparse        | 108 ms                                                 | 114 ms: 1.05x slower                                       |
| pprint_pformat             | 1.55 sec                                               | 1.64 sec: 1.05x slower                                     |
| mdp                        | 2.77 sec                                               | 2.93 sec: 1.05x slower                                     |
| deepcopy_memo              | 40.2 us                                                | 42.4 us: 1.05x slower                                      |
| dulwich_log                | 64.6 ms                                                | 68.4 ms: 1.06x slower                                      |
| meteor_contest             | 109 ms                                                 | 115 ms: 1.06x slower                                       |
| pickle_list                | 4.59 us                                                | 4.87 us: 1.06x slower                                      |
| pprint_safe_repr           | 747 ms                                                 | 796 ms: 1.06x slower                                       |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                       |
| sympy_integrate            | 21.5 ms                                                | 23.0 ms: 1.07x slower                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.42 ms: 1.08x slower                                      |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                       |
| pycparser                  | 1.19 sec                                               | 1.29 sec: 1.08x slower                                     |
| html5lib                   | 64.8 ms                                                | 70.5 ms: 1.09x slower                                      |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                      |
| async_tree_none_tg         | 491 ms                                                 | 537 ms: 1.09x slower                                       |
| nbody                      | 96.0 ms                                                | 105 ms: 1.10x slower                                       |
| 2to3                       | 264 ms                                                 | 290 ms: 1.10x slower                                       |
| async_tree_memoization     | 639 ms                                                 | 704 ms: 1.10x slower                                       |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                       |
| aiohttp                    | 1.12 ms                                                | 1.23 ms: 1.11x slower                                      |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                     |
| gunicorn                   | 1.20 ms                                                | 1.33 ms: 1.11x slower                                      |
| django_template            | 33.5 ms                                                | 37.3 ms: 1.11x slower                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 848 ms: 1.11x slower                                       |
| float                      | 78.9 ms                                                | 88.3 ms: 1.12x slower                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 838 ms: 1.12x slower                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 702 ms: 1.12x slower                                       |
| mako                       | 10.7 ms                                                | 12.0 ms: 1.13x slower                                      |
| scimark_fft                | 345 ms                                                 | 391 ms: 1.13x slower                                       |
| unpickle                   | 13.8 us                                                | 15.8 us: 1.14x slower                                      |
| xml_etree_process          | 56.9 ms                                                | 65.4 ms: 1.15x slower                                      |
| sympy_str                  | 297 ms                                                 | 342 ms: 1.15x slower                                       |
| async_tree_io              | 1.29 sec                                               | 1.49 sec: 1.16x slower                                     |
| async_tree_io_tg           | 1.29 sec                                               | 1.50 sec: 1.16x slower                                     |
| xml_etree_generate         | 81.1 ms                                                | 94.2 ms: 1.16x slower                                      |
| chameleon                  | 6.70 ms                                                | 7.87 ms: 1.18x slower                                      |
| sqlite_synth               | 2.57 us                                                | 3.15 us: 1.22x slower                                      |
| async_generators           | 374 ms                                                 | 476 ms: 1.27x slower                                       |
| sympy_sum                  | 169 ms                                                 | 216 ms: 1.28x slower                                       |
| telco                      | 6.86 ms                                                | 9.10 ms: 1.33x slower                                      |
| sympy_expand               | 484 ms                                                 | 644 ms: 1.33x slower                                       |
| python_startup             | 8.56 ms                                                | 12.1 ms: 1.41x slower                                      |
| mypy2                      | 686 ms                                                 | 1.18 sec: 1.73x slower                                     |
| flaskblogging              | 7.28 ms                                                | 12.6 ms: 1.73x slower                                      |
| python_startup_no_site     | 6.01 ms                                                | 10.5 ms: 1.74x slower                                      |
| bench_thread_pool          | 834 us                                                 | 2.54 ms: 3.04x slower                                      |
| coverage                   | 78.8 ms                                                | 690 ms: 8.76x slower                                       |
| thrift                     | 784 us                                                 | 9.30 ms: 11.86x slower                                     |
| fannkuch                   | 405 ms                                                 | 4.97 sec: 12.26x slower                                    |
| Geometric mean             | (ref)                                                  | 1.11x slower                                               |

Benchmark hidden because not significant (3): richards, logging_simple, async_tree_none
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, djangocms, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.12x