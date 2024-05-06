# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 752e183
- commit date: 2024-03-31
- overall geometric mean: 1.07x faster
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                   |
| chameleon      | 6.70 ms                                                | 6.85 ms: 1.02x slower                                  |
| docutils       | 2.66 sec                                               | 2.76 sec: 1.04x slower                                 |
| html5lib       | 64.8 ms                                                | 67.0 ms: 1.03x slower                                  |
| tornado_http   | 98.1 ms                                                | 95.0 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 339 ms: 1.45x faster                                   |
| async_tree_memoization     | 639 ms                                                 | 448 ms: 1.43x faster                                   |
| async_tree_io_tg           | 1.29 sec                                               | 921 ms: 1.41x faster                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 448 ms: 1.40x faster                                   |
| async_tree_io              | 1.29 sec                                               | 934 ms: 1.38x faster                                   |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 579 ms: 1.31x faster                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 596 ms: 1.26x faster                                   |
| Geometric mean             | (ref)                                                  | 1.37x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.5 ms: 1.07x faster                                  |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                   |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.06x faster                                   |
| regex_effbot   | 3.51 ms                                                | 3.76 ms: 1.07x slower                                  |
| regex_dna      | 205 ms                                                 | 222 ms: 1.09x slower                                   |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.14x slower                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.28x faster                                  |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                   |
| pickle_pure_python   | 320 us                                                 | 303 us: 1.06x faster                                   |
| tomli_loads          | 2.30 sec                                               | 2.22 sec: 1.04x faster                                 |
| pickle_dict          | 34.6 us                                                | 33.6 us: 1.03x faster                                  |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                  |
| unpickle_list        | 5.21 us                                                | 5.13 us: 1.02x faster                                  |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                  |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                  |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                  |
| pickle_list          | 4.59 us                                                | 4.96 us: 1.08x slower                                  |
| unpickle             | 13.8 us                                                | 18.5 us: 1.33x slower                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                  |
| python_startup_no_site | 6.01 ms                                                | 8.99 ms: 1.50x slower                                  |
| Geometric mean         | (ref)                                                  | 1.36x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.6 ms: 1.02x faster                                  |
| django_template | 33.5 ms                                                | 34.2 ms: 1.02x slower                                  |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                  |
| genshi_text     | 22.5 ms                                                | 24.3 ms: 1.08x slower                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.62x faster                                   |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                  |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                   |
| pylint                     | 476 ms                                                 | 280 ms: 1.70x faster                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.83 sec: 1.70x faster                                 |
| async_tree_none_tg         | 491 ms                                                 | 339 ms: 1.45x faster                                   |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.44x faster                                  |
| async_tree_memoization     | 639 ms                                                 | 448 ms: 1.43x faster                                   |
| async_tree_io_tg           | 1.29 sec                                               | 921 ms: 1.41x faster                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 448 ms: 1.40x faster                                   |
| async_tree_io              | 1.29 sec                                               | 934 ms: 1.38x faster                                   |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 579 ms: 1.31x faster                                   |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 596 ms: 1.26x faster                                   |
| deltablue                  | 3.92 ms                                                | 3.21 ms: 1.22x faster                                  |
| chaos                      | 71.9 ms                                                | 60.4 ms: 1.19x faster                                  |
| richards_super             | 61.9 ms                                                | 52.6 ms: 1.18x faster                                  |
| raytrace                   | 309 ms                                                 | 268 ms: 1.15x faster                                   |
| coroutines                 | 27.0 ms                                                | 23.5 ms: 1.15x faster                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.28 ms: 1.12x faster                                  |
| hexiom                     | 6.89 ms                                                | 6.18 ms: 1.11x faster                                  |
| logging_silent             | 111 ns                                                 | 100 ns: 1.11x faster                                   |
| nqueens                    | 87.9 ms                                                | 79.6 ms: 1.10x faster                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                  |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                   |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                   |
| sympy_str                  | 297 ms                                                 | 274 ms: 1.09x faster                                   |
| richards                   | 49.8 ms                                                | 45.9 ms: 1.09x faster                                  |
| nbody                      | 96.0 ms                                                | 89.5 ms: 1.07x faster                                  |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                  |
| mdp                        | 2.77 sec                                               | 2.60 sec: 1.07x faster                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.71 ms: 1.07x faster                                  |
| crypto_pyaes               | 76.7 ms                                                | 72.1 ms: 1.06x faster                                  |
| go                         | 149 ms                                                 | 140 ms: 1.06x faster                                   |
| pickle_pure_python         | 320 us                                                 | 303 us: 1.06x faster                                   |
| regex_compile              | 141 ms                                                 | 134 ms: 1.06x faster                                   |
| logging_simple             | 6.22 us                                                | 5.90 us: 1.05x faster                                  |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                  |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                  |
| fannkuch                   | 405 ms                                                 | 387 ms: 1.05x faster                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 67.6 ms: 1.05x faster                                  |
| sympy_expand               | 484 ms                                                 | 464 ms: 1.04x faster                                   |
| logging_format             | 6.81 us                                                | 6.56 us: 1.04x faster                                  |
| tomli_loads                | 2.30 sec                                               | 2.22 sec: 1.04x faster                                 |
| deepcopy                   | 365 us                                                 | 353 us: 1.04x faster                                   |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                 |
| tornado_http               | 98.1 ms                                                | 95.0 ms: 1.03x faster                                  |
| pickle_dict                | 34.6 us                                                | 33.6 us: 1.03x faster                                  |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                   |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                   |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                  |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.15 us: 1.02x faster                                  |
| pprint_safe_repr           | 747 ms                                                 | 735 ms: 1.02x faster                                   |
| unpickle_list              | 5.21 us                                                | 5.13 us: 1.02x faster                                  |
| genshi_xml                 | 53.4 ms                                                | 52.6 ms: 1.02x faster                                  |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                  |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                   |
| bench_thread_pool          | 834 us                                                 | 830 us: 1.01x faster                                   |
| gc_traversal               | 4.01 ms                                                | 4.00 ms: 1.00x faster                                  |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                  |
| django_template            | 33.5 ms                                                | 34.2 ms: 1.02x slower                                  |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                   |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                  |
| chameleon                  | 6.70 ms                                                | 6.85 ms: 1.02x slower                                  |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                   |
| pathlib                    | 18.5 ms                                                | 19.0 ms: 1.03x slower                                  |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                 |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.03x slower                                   |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                   |
| html5lib                   | 64.8 ms                                                | 67.0 ms: 1.03x slower                                  |
| docutils                   | 2.66 sec                                               | 2.76 sec: 1.04x slower                                 |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                   |
| dulwich_log                | 64.6 ms                                                | 67.6 ms: 1.05x slower                                  |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                  |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                  |
| aiohttp                    | 1.12 ms                                                | 1.18 ms: 1.06x slower                                  |
| pyflate                    | 434 ms                                                 | 460 ms: 1.06x slower                                   |
| gunicorn                   | 1.20 ms                                                | 1.28 ms: 1.07x slower                                  |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                  |
| regex_effbot               | 3.51 ms                                                | 3.76 ms: 1.07x slower                                  |
| mypy2                      | 686 ms                                                 | 737 ms: 1.07x slower                                   |
| genshi_text                | 22.5 ms                                                | 24.3 ms: 1.08x slower                                  |
| pickle_list                | 4.59 us                                                | 4.96 us: 1.08x slower                                  |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.09x slower                                   |
| scimark_fft                | 345 ms                                                 | 381 ms: 1.10x slower                                   |
| sqlite_synth               | 2.57 us                                                | 2.90 us: 1.13x slower                                  |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.14x slower                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.67 ms: 1.16x slower                                  |
| async_generators           | 374 ms                                                 | 443 ms: 1.18x slower                                   |
| coverage                   | 78.8 ms                                                | 97.6 ms: 1.24x slower                                  |
| unpack_sequence            | 43.5 ns                                                | 53.9 ns: 1.24x slower                                  |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                  |
| telco                      | 6.86 ms                                                | 8.54 ms: 1.24x slower                                  |
| unpickle                   | 13.8 us                                                | 18.5 us: 1.33x slower                                  |
| python_startup_no_site     | 6.01 ms                                                | 8.99 ms: 1.50x slower                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                           |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, dask, scimark_lu
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.69% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x