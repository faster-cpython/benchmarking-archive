# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b1
- machine: linux-x86_64
- commit hash: 2268289
- commit date: 2024-05-08
- overall geometric mean: 1.02x faster
- HPT reliability: 91.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                       |
| chameleon      | 6.70 ms                                                | 7.11 ms: 1.06x slower                                      |
| docutils       | 2.66 sec                                               | 2.86 sec: 1.07x slower                                     |
| html5lib       | 64.8 ms                                                | 68.4 ms: 1.06x slower                                      |
| tornado_http   | 98.1 ms                                                | 95.8 ms: 1.02x faster                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 346 ms: 1.42x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                       |
| async_tree_io              | 1.29 sec                                               | 936 ms: 1.37x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 477 ms: 1.34x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 987 ms: 1.31x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 589 ms: 1.29x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 619 ms: 1.21x faster                                       |
| Geometric mean             | (ref)                                                  | 1.35x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.8 ms: 1.09x faster                                      |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                       |
| float          | 78.9 ms                                                | 78.5 ms: 1.01x faster                                      |
| Geometric mean | (ref)                                                  | 1.04x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                      |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                       |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.15x slower                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.28x faster                                      |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.08x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.22 sec: 1.04x faster                                     |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                       |
| pickle_pure_python   | 320 us                                                 | 311 us: 1.03x faster                                       |
| pickle_dict          | 34.6 us                                                | 33.8 us: 1.02x faster                                      |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                      |
| unpickle_list        | 5.21 us                                                | 5.38 us: 1.03x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 60.3 ms: 1.06x slower                                      |
| pickle               | 11.0 us                                                | 11.8 us: 1.08x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.7 ms: 1.08x slower                                      |
| pickle_list          | 4.59 us                                                | 5.30 us: 1.16x slower                                      |
| unpickle             | 13.8 us                                                | 17.0 us: 1.23x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.19 ms: 1.20x slower                                      |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                      |
| Geometric mean         | (ref)                                                  | 1.22x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                      |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                      |
| genshi_text     | 22.5 ms                                                | 23.1 ms: 1.03x slower                                      |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                      |
| Geometric mean  | (ref)                                                  | 1.02x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 170 us: 3.07x faster                                       |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.56x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                     |
| pylint                     | 476 ms                                                 | 321 ms: 1.48x faster                                       |
| async_tree_none            | 528 ms                                                 | 363 ms: 1.45x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 346 ms: 1.42x faster                                       |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.39x faster                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                       |
| async_tree_io              | 1.29 sec                                               | 936 ms: 1.37x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 477 ms: 1.34x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 987 ms: 1.31x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 589 ms: 1.29x faster                                       |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                      |
| chaos                      | 71.9 ms                                                | 58.8 ms: 1.22x faster                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 619 ms: 1.21x faster                                       |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                      |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                      |
| raytrace                   | 309 ms                                                 | 267 ms: 1.15x faster                                       |
| hexiom                     | 6.89 ms                                                | 6.15 ms: 1.12x faster                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                      |
| nbody                      | 96.0 ms                                                | 87.8 ms: 1.09x faster                                      |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.08x faster                                       |
| nqueens                    | 87.9 ms                                                | 81.4 ms: 1.08x faster                                      |
| richards_super             | 61.9 ms                                                | 57.4 ms: 1.08x faster                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                      |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.07x faster                                       |
| mdp                        | 2.77 sec                                               | 2.60 sec: 1.07x faster                                     |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                      |
| logging_simple             | 6.22 us                                                | 5.91 us: 1.05x faster                                      |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                       |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                      |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                       |
| sympy_str                  | 297 ms                                                 | 284 ms: 1.05x faster                                       |
| gc_traversal               | 4.01 ms                                                | 3.85 ms: 1.04x faster                                      |
| logging_format             | 6.81 us                                                | 6.54 us: 1.04x faster                                      |
| tomli_loads                | 2.30 sec                                               | 2.22 sec: 1.04x faster                                     |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                      |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                       |
| fannkuch                   | 405 ms                                                 | 393 ms: 1.03x faster                                       |
| pickle_pure_python         | 320 us                                                 | 311 us: 1.03x faster                                       |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                       |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                      |
| pickle_dict                | 34.6 us                                                | 33.8 us: 1.02x faster                                      |
| tornado_http               | 98.1 ms                                                | 95.8 ms: 1.02x faster                                      |
| deepcopy_memo              | 40.2 us                                                | 39.4 us: 1.02x faster                                      |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                       |
| sympy_expand               | 484 ms                                                 | 477 ms: 1.02x faster                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 69.9 ms: 1.01x faster                                      |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                      |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                       |
| crypto_pyaes               | 76.7 ms                                                | 76.2 ms: 1.01x faster                                      |
| float                      | 78.9 ms                                                | 78.5 ms: 1.01x faster                                      |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                      |
| deepcopy                   | 365 us                                                 | 366 us: 1.00x slower                                       |
| bench_thread_pool          | 834 us                                                 | 839 us: 1.01x slower                                       |
| sqlglot_optimize           | 55.3 ms                                                | 55.8 ms: 1.01x slower                                      |
| pprint_pformat             | 1.55 sec                                               | 1.57 sec: 1.01x slower                                     |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.26 us: 1.01x slower                                      |
| richards                   | 49.8 ms                                                | 50.5 ms: 1.02x slower                                      |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                     |
| dask                       | 365 ms                                                 | 372 ms: 1.02x slower                                       |
| thrift                     | 784 us                                                 | 801 us: 1.02x slower                                       |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                       |
| genshi_text                | 22.5 ms                                                | 23.1 ms: 1.03x slower                                      |
| pprint_safe_repr           | 747 ms                                                 | 767 ms: 1.03x slower                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.18 ms: 1.03x slower                                      |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                       |
| unpickle_list              | 5.21 us                                                | 5.38 us: 1.03x slower                                      |
| json                       | 5.24 ms                                                | 5.41 ms: 1.03x slower                                      |
| dulwich_log                | 64.6 ms                                                | 67.0 ms: 1.04x slower                                      |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                       |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                      |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                      |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                       |
| html5lib                   | 64.8 ms                                                | 68.4 ms: 1.06x slower                                      |
| xml_etree_process          | 56.9 ms                                                | 60.3 ms: 1.06x slower                                      |
| chameleon                  | 6.70 ms                                                | 7.11 ms: 1.06x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.20 ms: 1.07x slower                                      |
| docutils                   | 2.66 sec                                               | 2.86 sec: 1.07x slower                                     |
| pickle                     | 11.0 us                                                | 11.8 us: 1.08x slower                                      |
| gunicorn                   | 1.20 ms                                                | 1.29 ms: 1.08x slower                                      |
| scimark_fft                | 345 ms                                                 | 373 ms: 1.08x slower                                       |
| xml_etree_generate         | 81.1 ms                                                | 87.7 ms: 1.08x slower                                      |
| mypy2                      | 686 ms                                                 | 743 ms: 1.08x slower                                       |
| pyflate                    | 434 ms                                                 | 473 ms: 1.09x slower                                       |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                       |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.15x slower                                      |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                      |
| pickle_list                | 4.59 us                                                | 5.30 us: 1.16x slower                                      |
| coverage                   | 78.8 ms                                                | 92.4 ms: 1.17x slower                                      |
| python_startup_no_site     | 6.01 ms                                                | 7.19 ms: 1.20x slower                                      |
| async_generators           | 374 ms                                                 | 452 ms: 1.21x slower                                       |
| unpickle                   | 13.8 us                                                | 17.0 us: 1.23x slower                                      |
| flaskblogging              | 7.28 ms                                                | 9.05 ms: 1.24x slower                                      |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                      |
| telco                      | 6.86 ms                                                | 173 ms: 25.16x slower                                      |
| Geometric mean             | (ref)                                                  | 1.02x faster                                               |

Benchmark hidden because not significant (2): xml_etree_iterparse, sqlglot_normalize
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 91.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x