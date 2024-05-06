# Results vs. 3.11.0

- fork: python
- ref: 7e6fa5fceddc3f4721c0
- machine: linux-x86_64
- commit hash: 7e6fa5f
- commit date: 2024-04-19
- overall geometric mean: 1.03x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 301 ms: 1.14x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.58 ms: 1.13x slower                                                  |
| docutils       | 2.66 sec                                               | 3.08 sec: 1.16x slower                                                 |
| html5lib       | 64.8 ms                                                | 71.9 ms: 1.11x slower                                                  |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 379 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 352 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 463 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 980 ms: 1.32x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 979 ms: 1.31x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 506 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 624 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 637 ms: 1.18x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.01x faster                                                   |
| float          | 78.9 ms                                                | 89.3 ms: 1.13x slower                                                  |
| nbody          | 96.0 ms                                                | 121 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.54 ms: 1.01x slower                                                  |
| regex_dna      | 205 ms                                                 | 222 ms: 1.09x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                  |
| regex_compile  | 141 ms                                                 | 179 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads           | 29.2 us                                                | 27.3 us: 1.07x faster                                                  |
| unpickle_list        | 5.21 us                                                | 5.10 us: 1.02x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 316 us: 1.01x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 112 ms: 1.04x slower                                                   |
| pickle_dict          | 34.6 us                                                | 36.1 us: 1.04x slower                                                  |
| pickle               | 11.0 us                                                | 12.2 us: 1.11x slower                                                  |
| tomli_loads          | 2.30 sec                                               | 2.55 sec: 1.11x slower                                                 |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 63.9 ms: 1.12x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 93.0 ms: 1.15x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.37 us: 1.17x slower                                                  |
| unpickle_pure_python | 242 us                                                 | 286 us: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 59.7 ms: 1.12x slower                                                  |
| genshi_text     | 22.5 ms                                                | 26.2 ms: 1.16x slower                                                  |
| django_template | 33.5 ms                                                | 40.8 ms: 1.22x slower                                                  |
| mako            | 10.7 ms                                                | 13.5 ms: 1.27x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 119 us: 4.37x faster                                                   |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 516 ms: 1.70x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                 |
| async_tree_none            | 528 ms                                                 | 379 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 352 ms: 1.39x faster                                                   |
| pylint                     | 476 ms                                                 | 344 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 463 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 980 ms: 1.32x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 979 ms: 1.31x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 506 ms: 1.26x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 624 ms: 1.22x faster                                                   |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 637 ms: 1.18x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| json_loads                 | 29.2 us                                                | 27.3 us: 1.07x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.76 ms: 1.07x faster                                                  |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                   |
| djangocms                  | 33.5 us                                                | 32.4 us: 1.03x faster                                                  |
| json                       | 5.24 ms                                                | 5.12 ms: 1.02x faster                                                  |
| unpickle_list              | 5.21 us                                                | 5.10 us: 1.02x faster                                                  |
| pathlib                    | 18.5 ms                                                | 18.2 ms: 1.02x faster                                                  |
| pidigits                   | 194 ms                                                 | 191 ms: 1.01x faster                                                   |
| pickle_pure_python         | 320 us                                                 | 316 us: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| comprehensions             | 23.6 us                                                | 23.5 us: 1.00x faster                                                  |
| richards_super             | 61.9 ms                                                | 62.4 ms: 1.01x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.54 ms: 1.01x slower                                                  |
| logging_simple             | 6.22 us                                                | 6.41 us: 1.03x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                   |
| logging_format             | 6.81 us                                                | 7.05 us: 1.03x slower                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 112 ms: 1.04x slower                                                   |
| deepcopy                   | 365 us                                                 | 380 us: 1.04x slower                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.82 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.35 us: 1.04x slower                                                  |
| pickle_dict                | 34.6 us                                                | 36.1 us: 1.04x slower                                                  |
| dask                       | 365 ms                                                 | 381 ms: 1.04x slower                                                   |
| raytrace                   | 309 ms                                                 | 322 ms: 1.04x slower                                                   |
| deltablue                  | 3.92 ms                                                | 4.10 ms: 1.05x slower                                                  |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.05x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 177 ms: 1.05x slower                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.50 ms: 1.05x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 884 us: 1.06x slower                                                   |
| thrift                     | 784 us                                                 | 838 us: 1.07x slower                                                   |
| pycparser                  | 1.19 sec                                               | 1.28 sec: 1.08x slower                                                 |
| mdp                        | 2.77 sec                                               | 2.99 sec: 1.08x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 23.2 ms: 1.08x slower                                                  |
| sympy_str                  | 297 ms                                                 | 322 ms: 1.08x slower                                                   |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.09x slower                                                   |
| sqlglot_normalize          | 113 ms                                                 | 123 ms: 1.09x slower                                                   |
| chaos                      | 71.9 ms                                                | 78.5 ms: 1.09x slower                                                  |
| meteor_contest             | 109 ms                                                 | 120 ms: 1.10x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                  |
| sympy_expand               | 484 ms                                                 | 536 ms: 1.11x slower                                                   |
| pickle                     | 11.0 us                                                | 12.2 us: 1.11x slower                                                  |
| tomli_loads                | 2.30 sec                                               | 2.55 sec: 1.11x slower                                                 |
| aiohttp                    | 1.12 ms                                                | 1.24 ms: 1.11x slower                                                  |
| html5lib                   | 64.8 ms                                                | 71.9 ms: 1.11x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 59.7 ms: 1.12x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                  |
| richards                   | 49.8 ms                                                | 55.9 ms: 1.12x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 63.9 ms: 1.12x slower                                                  |
| float                      | 78.9 ms                                                | 89.3 ms: 1.13x slower                                                  |
| chameleon                  | 6.70 ms                                                | 7.58 ms: 1.13x slower                                                  |
| deepcopy_memo              | 40.2 us                                                | 45.5 us: 1.13x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 73.4 ms: 1.14x slower                                                  |
| 2to3                       | 264 ms                                                 | 301 ms: 1.14x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 63.2 ms: 1.14x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 93.0 ms: 1.15x slower                                                  |
| docutils                   | 2.66 sec                                               | 3.08 sec: 1.16x slower                                                 |
| genshi_text                | 22.5 ms                                                | 26.2 ms: 1.16x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.37 us: 1.17x slower                                                  |
| mypy2                      | 686 ms                                                 | 806 ms: 1.18x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 286 us: 1.18x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 3.05 us: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.98 ms: 1.19x slower                                                  |
| crypto_pyaes               | 76.7 ms                                                | 91.6 ms: 1.19x slower                                                  |
| django_template            | 33.5 ms                                                | 40.8 ms: 1.22x slower                                                  |
| nqueens                    | 87.9 ms                                                | 107 ms: 1.22x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                  |
| fannkuch                   | 405 ms                                                 | 502 ms: 1.24x slower                                                   |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                  |
| go                         | 149 ms                                                 | 185 ms: 1.25x slower                                                   |
| scimark_sor                | 121 ms                                                 | 151 ms: 1.25x slower                                                   |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 88.8 ms: 1.26x slower                                                  |
| nbody                      | 96.0 ms                                                | 121 ms: 1.26x slower                                                   |
| regex_compile              | 141 ms                                                 | 179 ms: 1.26x slower                                                   |
| mako                       | 10.7 ms                                                | 13.5 ms: 1.27x slower                                                  |
| scimark_fft                | 345 ms                                                 | 445 ms: 1.29x slower                                                   |
| pprint_pformat             | 1.55 sec                                               | 2.01 sec: 1.29x slower                                                 |
| pprint_safe_repr           | 747 ms                                                 | 966 ms: 1.29x slower                                                   |
| spectral_norm              | 108 ms                                                 | 144 ms: 1.33x slower                                                   |
| telco                      | 6.86 ms                                                | 9.19 ms: 1.34x slower                                                  |
| pyflate                    | 434 ms                                                 | 600 ms: 1.38x slower                                                   |
| hexiom                     | 6.89 ms                                                | 9.55 ms: 1.39x slower                                                  |
| scimark_lu                 | 116 ms                                                 | 166 ms: 1.43x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.03x