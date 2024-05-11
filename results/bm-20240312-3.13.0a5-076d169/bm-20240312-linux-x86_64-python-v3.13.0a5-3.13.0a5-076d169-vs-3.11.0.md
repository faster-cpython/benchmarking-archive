# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: linux-x86_64
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.05x faster
- HPT reliability: 99.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                       |
| chameleon      | 6.70 ms                                                | 6.83 ms: 1.02x slower                                      |
| html5lib       | 64.8 ms                                                | 67.4 ms: 1.04x slower                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                               |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 449 ms: 1.18x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 581 ms: 1.10x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 463 ms: 1.06x faster                                       |
| async_tree_io              | 1.29 sec                                               | 1.22 sec: 1.06x faster                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 595 ms: 1.05x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 1.24 sec: 1.05x faster                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 729 ms: 1.03x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 745 ms: 1.02x faster                                       |
| Geometric mean             | (ref)                                                  | 1.07x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 93.6 ms: 1.03x faster                                      |
| pidigits       | 194 ms                                                 | 189 ms: 1.02x faster                                       |
| float          | 78.9 ms                                                | 82.6 ms: 1.05x slower                                      |
| Geometric mean | (ref)                                                  | 1.00x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 133 ms: 1.06x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.54 ms: 1.01x slower                                      |
| regex_dna      | 205 ms                                                 | 216 ms: 1.05x slower                                       |
| regex_v8       | 22.9 ms                                                | 24.7 ms: 1.08x slower                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                      |
| unpickle_pure_python | 242 us                                                 | 217 us: 1.12x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                     |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                       |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                      |
| unpickle_list        | 5.21 us                                                | 5.05 us: 1.03x faster                                      |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                       |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                       |
| pickle_dict          | 34.6 us                                                | 35.7 us: 1.03x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 59.8 ms: 1.05x slower                                      |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.3 ms: 1.08x slower                                      |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                      |
| pickle_list          | 4.59 us                                                | 5.01 us: 1.09x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.22x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 8.99 ms: 1.49x slower                                      |
| Geometric mean         | (ref)                                                  | 1.35x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.0 ms: 1.03x faster                                      |
| django_template | 33.5 ms                                                | 33.8 ms: 1.01x slower                                      |
| genshi_text     | 22.5 ms                                                | 23.0 ms: 1.02x slower                                      |
| mako            | 10.7 ms                                                | 11.3 ms: 1.06x slower                                      |
| Geometric mean  | (ref)                                                  | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.63x faster                                       |
| generators                 | 74.9 ms                                                | 29.5 ms: 2.53x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 504 ms: 1.74x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                     |
| pylint                     | 476 ms                                                 | 312 ms: 1.53x faster                                       |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.44x faster                                      |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                      |
| coroutines                 | 27.0 ms                                                | 22.0 ms: 1.23x faster                                      |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.22x faster                                      |
| richards_super             | 61.9 ms                                                | 51.9 ms: 1.19x faster                                      |
| chaos                      | 71.9 ms                                                | 60.9 ms: 1.18x faster                                      |
| async_tree_none            | 528 ms                                                 | 449 ms: 1.18x faster                                       |
| raytrace                   | 309 ms                                                 | 263 ms: 1.17x faster                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.27 ms: 1.13x faster                                      |
| hexiom                     | 6.89 ms                                                | 6.13 ms: 1.12x faster                                      |
| logging_silent             | 111 ns                                                 | 99.5 ns: 1.12x faster                                      |
| unpickle_pure_python       | 242 us                                                 | 217 us: 1.12x faster                                       |
| sympy_sum                  | 169 ms                                                 | 153 ms: 1.10x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 581 ms: 1.10x faster                                       |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                      |
| mdp                        | 2.77 sec                                               | 2.53 sec: 1.09x faster                                     |
| nqueens                    | 87.9 ms                                                | 80.7 ms: 1.09x faster                                      |
| richards                   | 49.8 ms                                                | 45.9 ms: 1.09x faster                                      |
| sympy_str                  | 297 ms                                                 | 275 ms: 1.08x faster                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.68 ms: 1.08x faster                                      |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                      |
| go                         | 149 ms                                                 | 139 ms: 1.07x faster                                       |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                     |
| regex_compile              | 141 ms                                                 | 133 ms: 1.06x faster                                       |
| logging_simple             | 6.22 us                                                | 5.85 us: 1.06x faster                                      |
| async_tree_none_tg         | 491 ms                                                 | 463 ms: 1.06x faster                                       |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                      |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.04 us: 1.06x faster                                      |
| async_tree_io              | 1.29 sec                                               | 1.22 sec: 1.06x faster                                     |
| sqlglot_normalize          | 113 ms                                                 | 107 ms: 1.06x faster                                       |
| deepcopy                   | 365 us                                                 | 346 us: 1.06x faster                                       |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.05x faster                                      |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 595 ms: 1.05x faster                                       |
| crypto_pyaes               | 76.7 ms                                                | 73.0 ms: 1.05x faster                                      |
| async_tree_io_tg           | 1.29 sec                                               | 1.24 sec: 1.05x faster                                     |
| djangocms                  | 33.5 us                                                | 32.1 us: 1.04x faster                                      |
| logging_format             | 6.81 us                                                | 6.53 us: 1.04x faster                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 67.9 ms: 1.04x faster                                      |
| sympy_expand               | 484 ms                                                 | 466 ms: 1.04x faster                                       |
| unpickle_list              | 5.21 us                                                | 5.05 us: 1.03x faster                                      |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 729 ms: 1.03x faster                                       |
| genshi_xml                 | 53.4 ms                                                | 52.0 ms: 1.03x faster                                      |
| scimark_lu                 | 116 ms                                                 | 113 ms: 1.03x faster                                       |
| nbody                      | 96.0 ms                                                | 93.6 ms: 1.03x faster                                      |
| sqlglot_optimize           | 55.3 ms                                                | 53.9 ms: 1.03x faster                                      |
| pidigits                   | 194 ms                                                 | 189 ms: 1.02x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 745 ms: 1.02x faster                                       |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                      |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                       |
| fannkuch                   | 405 ms                                                 | 400 ms: 1.01x faster                                       |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                      |
| django_template            | 33.5 ms                                                | 33.8 ms: 1.01x slower                                      |
| regex_effbot               | 3.51 ms                                                | 3.54 ms: 1.01x slower                                      |
| bench_thread_pool          | 834 us                                                 | 842 us: 1.01x slower                                       |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                       |
| pprint_safe_repr           | 747 ms                                                 | 757 ms: 1.01x slower                                       |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                       |
| chameleon                  | 6.70 ms                                                | 6.83 ms: 1.02x slower                                      |
| genshi_text                | 22.5 ms                                                | 23.0 ms: 1.02x slower                                      |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                       |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                       |
| pickle_dict                | 34.6 us                                                | 35.7 us: 1.03x slower                                      |
| html5lib                   | 64.8 ms                                                | 67.4 ms: 1.04x slower                                      |
| dulwich_log                | 64.6 ms                                                | 67.3 ms: 1.04x slower                                      |
| float                      | 78.9 ms                                                | 82.6 ms: 1.05x slower                                      |
| scimark_fft                | 345 ms                                                 | 362 ms: 1.05x slower                                       |
| xml_etree_process          | 56.9 ms                                                | 59.8 ms: 1.05x slower                                      |
| regex_dna                  | 205 ms                                                 | 216 ms: 1.05x slower                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.52 ms: 1.06x slower                                      |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                      |
| mako                       | 10.7 ms                                                | 11.3 ms: 1.06x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.19 ms: 1.07x slower                                      |
| gunicorn                   | 1.20 ms                                                | 1.29 ms: 1.08x slower                                      |
| xml_etree_generate         | 81.1 ms                                                | 87.3 ms: 1.08x slower                                      |
| regex_v8                   | 22.9 ms                                                | 24.7 ms: 1.08x slower                                      |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                       |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                      |
| pickle_list                | 4.59 us                                                | 5.01 us: 1.09x slower                                      |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                      |
| async_generators           | 374 ms                                                 | 449 ms: 1.20x slower                                       |
| flaskblogging              | 7.28 ms                                                | 8.82 ms: 1.21x slower                                      |
| coverage                   | 78.8 ms                                                | 95.6 ms: 1.21x slower                                      |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.22x slower                                      |
| telco                      | 6.86 ms                                                | 8.60 ms: 1.25x slower                                      |
| mypy2                      | 686 ms                                                 | 871 ms: 1.27x slower                                       |
| python_startup_no_site     | 6.01 ms                                                | 8.99 ms: 1.49x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (8): spectral_norm, pycparser, pathlib, pprint_pformat, docutils, meteor_contest, tornado_http, thrift
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.59% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x