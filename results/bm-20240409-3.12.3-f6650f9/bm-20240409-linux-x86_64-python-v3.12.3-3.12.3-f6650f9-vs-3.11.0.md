# Results vs. 3.11.0

- fork: python
- ref: v3.12.3
- machine: linux-x86_64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.05x faster
- HPT reliability: 96.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 266 ms: 1.01x slower                                   |
| chameleon      | 6.70 ms                                                | 6.94 ms: 1.04x slower                                  |
| docutils       | 2.66 sec                                               | 2.73 sec: 1.03x slower                                 |
| tornado_http   | 98.1 ms                                                | 96.9 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 481 ms: 1.10x faster                                   |
| async_tree_memoization     | 639 ms                                                 | 586 ms: 1.09x faster                                   |
| async_tree_io              | 1.29 sec                                               | 1.18 sec: 1.09x faster                                 |
| async_tree_none_tg         | 491 ms                                                 | 455 ms: 1.08x faster                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 584 ms: 1.07x faster                                   |
| async_tree_io_tg           | 1.29 sec                                               | 1.22 sec: 1.06x faster                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 736 ms: 1.03x faster                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 734 ms: 1.02x faster                                   |
| Geometric mean             | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 93.1 ms: 1.03x faster                                  |
| pidigits       | 194 ms                                                 | 197 ms: 1.02x slower                                   |
| float          | 78.9 ms                                                | 83.5 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                   |
| regex_v8       | 22.9 ms                                                | 23.3 ms: 1.02x slower                                  |
| regex_dna      | 205 ms                                                 | 211 ms: 1.03x slower                                   |
| regex_effbot   | 3.51 ms                                                | 3.77 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                  |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.09x faster                                   |
| unpickle_list        | 5.21 us                                                | 5.04 us: 1.04x faster                                  |
| tomli_loads          | 2.30 sec                                               | 2.23 sec: 1.03x faster                                 |
| pickle_pure_python   | 320 us                                                 | 313 us: 1.02x faster                                   |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                   |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.01x slower                                  |
| json_loads           | 29.2 us                                                | 29.9 us: 1.02x slower                                  |
| xml_etree_process    | 56.9 ms                                                | 60.1 ms: 1.06x slower                                  |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                  |
| xml_etree_generate   | 81.1 ms                                                | 88.9 ms: 1.10x slower                                  |
| pickle_list          | 4.59 us                                                | 5.05 us: 1.10x slower                                  |
| unpickle             | 13.8 us                                                | 15.8 us: 1.14x slower                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 9.54 ms: 1.12x slower                                  |
| python_startup_no_site | 6.01 ms                                                | 6.87 ms: 1.14x slower                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.6 ms: 1.06x faster                                  |
| genshi_text     | 22.5 ms                                                | 22.1 ms: 1.02x faster                                  |
| django_template | 33.5 ms                                                | 34.2 ms: 1.02x slower                                  |
| mako            | 10.7 ms                                                | 11.1 ms: 1.04x slower                                  |
| Geometric mean  | (ref)                                                  | 1.00x faster                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 119 us: 4.36x faster                                   |
| generators                 | 74.9 ms                                                | 28.6 ms: 2.62x faster                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                 |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                   |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                   |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.44x faster                                  |
| richards_super             | 61.9 ms                                                | 48.9 ms: 1.27x faster                                  |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                  |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                  |
| richards                   | 49.8 ms                                                | 42.5 ms: 1.17x faster                                  |
| coroutines                 | 27.0 ms                                                | 23.3 ms: 1.16x faster                                  |
| logging_silent             | 111 ns                                                 | 96.6 ns: 1.15x faster                                  |
| chaos                      | 71.9 ms                                                | 64.9 ms: 1.11x faster                                  |
| go                         | 149 ms                                                 | 135 ms: 1.10x faster                                   |
| hexiom                     | 6.89 ms                                                | 6.27 ms: 1.10x faster                                  |
| async_tree_none            | 528 ms                                                 | 481 ms: 1.10x faster                                   |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                   |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.09x faster                                   |
| async_tree_memoization     | 639 ms                                                 | 586 ms: 1.09x faster                                   |
| async_tree_io              | 1.29 sec                                               | 1.18 sec: 1.09x faster                                 |
| sympy_str                  | 297 ms                                                 | 274 ms: 1.08x faster                                   |
| nqueens                    | 87.9 ms                                                | 81.2 ms: 1.08x faster                                  |
| async_tree_none_tg         | 491 ms                                                 | 455 ms: 1.08x faster                                   |
| gc_traversal               | 4.01 ms                                                | 3.73 ms: 1.08x faster                                  |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 584 ms: 1.07x faster                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                  |
| async_tree_io_tg           | 1.29 sec                                               | 1.22 sec: 1.06x faster                                 |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                  |
| genshi_xml                 | 53.4 ms                                                | 50.6 ms: 1.06x faster                                  |
| sqlglot_normalize          | 113 ms                                                 | 107 ms: 1.05x faster                                   |
| deepcopy_memo              | 40.2 us                                                | 38.2 us: 1.05x faster                                  |
| sympy_expand               | 484 ms                                                 | 462 ms: 1.05x faster                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.67 ms: 1.05x faster                                  |
| coverage                   | 78.8 ms                                                | 75.2 ms: 1.05x faster                                  |
| raytrace                   | 309 ms                                                 | 297 ms: 1.04x faster                                   |
| unpickle_list              | 5.21 us                                                | 5.04 us: 1.04x faster                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 736 ms: 1.03x faster                                   |
| tomli_loads                | 2.30 sec                                               | 2.23 sec: 1.03x faster                                 |
| deepcopy                   | 365 us                                                 | 354 us: 1.03x faster                                   |
| nbody                      | 96.0 ms                                                | 93.1 ms: 1.03x faster                                  |
| sqlglot_optimize           | 55.3 ms                                                | 53.9 ms: 1.03x faster                                  |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                 |
| pickle_pure_python         | 320 us                                                 | 313 us: 1.02x faster                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 734 ms: 1.02x faster                                   |
| sqlalchemy_imperative      | 18.3 ms                                                | 18.0 ms: 1.02x faster                                  |
| genshi_text                | 22.5 ms                                                | 22.1 ms: 1.02x faster                                  |
| logging_simple             | 6.22 us                                                | 6.12 us: 1.02x faster                                  |
| logging_format             | 6.81 us                                                | 6.73 us: 1.01x faster                                  |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                 |
| tornado_http               | 98.1 ms                                                | 96.9 ms: 1.01x faster                                  |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                   |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                   |
| fannkuch                   | 405 ms                                                 | 402 ms: 1.01x faster                                   |
| pprint_safe_repr           | 747 ms                                                 | 742 ms: 1.01x faster                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                  |
| bench_thread_pool          | 834 us                                                 | 838 us: 1.00x slower                                   |
| 2to3                       | 264 ms                                                 | 266 ms: 1.01x slower                                   |
| mdp                        | 2.77 sec                                               | 2.80 sec: 1.01x slower                                 |
| mypy2                      | 686 ms                                                 | 694 ms: 1.01x slower                                   |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                   |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.01x slower                                  |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.01x slower                                  |
| aiohttp                    | 1.12 ms                                                | 1.13 ms: 1.02x slower                                  |
| pidigits                   | 194 ms                                                 | 197 ms: 1.02x slower                                   |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                  |
| django_template            | 33.5 ms                                                | 34.2 ms: 1.02x slower                                  |
| regex_v8                   | 22.9 ms                                                | 23.3 ms: 1.02x slower                                  |
| dulwich_log                | 64.6 ms                                                | 66.0 ms: 1.02x slower                                  |
| gunicorn                   | 1.20 ms                                                | 1.22 ms: 1.02x slower                                  |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                   |
| json_loads                 | 29.2 us                                                | 29.9 us: 1.02x slower                                  |
| docutils                   | 2.66 sec                                               | 2.73 sec: 1.03x slower                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.47 ms: 1.03x slower                                  |
| regex_dna                  | 205 ms                                                 | 211 ms: 1.03x slower                                   |
| sqlalchemy_declarative     | 140 ms                                                 | 145 ms: 1.03x slower                                   |
| chameleon                  | 6.70 ms                                                | 6.94 ms: 1.04x slower                                  |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.04x slower                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 73.4 ms: 1.04x slower                                  |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                   |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.04x slower                                  |
| scimark_lu                 | 116 ms                                                 | 121 ms: 1.04x slower                                   |
| thrift                     | 784 us                                                 | 821 us: 1.05x slower                                   |
| pyflate                    | 434 ms                                                 | 458 ms: 1.06x slower                                   |
| xml_etree_process          | 56.9 ms                                                | 60.1 ms: 1.06x slower                                  |
| float                      | 78.9 ms                                                | 83.5 ms: 1.06x slower                                  |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                  |
| telco                      | 6.86 ms                                                | 7.35 ms: 1.07x slower                                  |
| regex_effbot               | 3.51 ms                                                | 3.77 ms: 1.07x slower                                  |
| scimark_fft                | 345 ms                                                 | 378 ms: 1.09x slower                                   |
| xml_etree_generate         | 81.1 ms                                                | 88.9 ms: 1.10x slower                                  |
| crypto_pyaes               | 76.7 ms                                                | 84.3 ms: 1.10x slower                                  |
| pickle_list                | 4.59 us                                                | 5.05 us: 1.10x slower                                  |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                  |
| python_startup             | 8.56 ms                                                | 9.54 ms: 1.12x slower                                  |
| python_startup_no_site     | 6.01 ms                                                | 6.87 ms: 1.14x slower                                  |
| unpickle                   | 13.8 us                                                | 15.8 us: 1.14x slower                                  |
| async_generators           | 374 ms                                                 | 457 ms: 1.22x slower                                   |
| Geometric mean             | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (5): scimark_sparse_mat_mult, html5lib, xml_etree_iterparse, dask, deepcopy_reduce
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, unpack_sequence

# HPT report

- Reliability score: 96.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x