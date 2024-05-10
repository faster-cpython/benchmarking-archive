# Results vs. 3.11.0

- fork: python
- ref: 35b5eaa176a5bae8a0ca
- machine: linux-x86_64
- commit hash: 35b5eaa
- commit date: 2024-05-09
- overall geometric mean: 1.03x faster
- HPT reliability: 98.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                  |
| chameleon      | 6.70 ms                                                | 6.87 ms: 1.02x slower                                                 |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                |
| html5lib       | 64.8 ms                                                | 67.0 ms: 1.03x slower                                                 |
| tornado_http   | 98.1 ms                                                | 93.7 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 361 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 346 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 931 ms: 1.38x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 474 ms: 1.35x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 983 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 618 ms: 1.21x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.6 ms: 1.08x faster                                                 |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                  |
| float          | 78.9 ms                                                | 77.1 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                  |
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                 |
| regex_v8       | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                 |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.25x faster                                                 |
| tomli_loads          | 2.30 sec                                               | 2.06 sec: 1.12x faster                                                |
| unpickle_pure_python | 242 us                                                 | 217 us: 1.11x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                  |
| pickle_dict          | 34.6 us                                                | 33.9 us: 1.02x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.01x faster                                                  |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| unpickle_list        | 5.21 us                                                | 5.47 us: 1.05x slower                                                 |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 87.4 ms: 1.08x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.20 us: 1.13x slower                                                 |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.21x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.9 ms: 1.05x faster                                                 |
| mako            | 10.7 ms                                                | 10.6 ms: 1.01x faster                                                 |
| django_template | 33.5 ms                                                | 33.8 ms: 1.01x slower                                                 |
| genshi_text     | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                  |
| generators                 | 74.9 ms                                                | 29.4 ms: 2.54x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                |
| pylint                     | 476 ms                                                 | 317 ms: 1.50x faster                                                  |
| async_tree_none            | 528 ms                                                 | 361 ms: 1.46x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 346 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 931 ms: 1.38x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 474 ms: 1.35x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 983 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 618 ms: 1.21x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.24 ms: 1.21x faster                                                 |
| chaos                      | 71.9 ms                                                | 60.0 ms: 1.20x faster                                                 |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                  |
| richards_super             | 61.9 ms                                                | 53.8 ms: 1.15x faster                                                 |
| coroutines                 | 27.0 ms                                                | 23.6 ms: 1.14x faster                                                 |
| hexiom                     | 6.89 ms                                                | 6.11 ms: 1.13x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 2.06 sec: 1.12x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 217 us: 1.11x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.62 ms: 1.11x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.68 us: 1.10x faster                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                 |
| nqueens                    | 87.9 ms                                                | 81.0 ms: 1.08x faster                                                 |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                  |
| nbody                      | 96.0 ms                                                | 88.6 ms: 1.08x faster                                                 |
| logging_format             | 6.81 us                                                | 6.30 us: 1.08x faster                                                 |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                  |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.06x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.63 sec: 1.05x faster                                                |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                  |
| genshi_xml                 | 53.4 ms                                                | 50.9 ms: 1.05x faster                                                 |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                  |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                 |
| tornado_http               | 98.1 ms                                                | 93.7 ms: 1.05x faster                                                 |
| richards                   | 49.8 ms                                                | 47.9 ms: 1.04x faster                                                 |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 73.9 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 68.3 ms: 1.04x faster                                                 |
| sympy_expand               | 484 ms                                                 | 471 ms: 1.03x faster                                                  |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                  |
| float                      | 78.9 ms                                                | 77.1 ms: 1.02x faster                                                 |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                 |
| pickle_dict                | 34.6 us                                                | 33.9 us: 1.02x faster                                                 |
| fannkuch                   | 405 ms                                                 | 398 ms: 1.02x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.7 ms: 1.01x faster                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                                 |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                 |
| mako                       | 10.7 ms                                                | 10.6 ms: 1.01x faster                                                 |
| bench_thread_pool          | 834 us                                                 | 832 us: 1.00x faster                                                  |
| django_template            | 33.5 ms                                                | 33.8 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.57 sec: 1.01x slower                                                |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                  |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 65.6 ms: 1.02x slower                                                 |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.87 ms: 1.02x slower                                                 |
| pprint_safe_repr           | 747 ms                                                 | 766 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.17 ms: 1.03x slower                                                 |
| html5lib                   | 64.8 ms                                                | 67.0 ms: 1.03x slower                                                 |
| json                       | 5.24 ms                                                | 5.44 ms: 1.04x slower                                                 |
| genshi_text                | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                 |
| thrift                     | 784 us                                                 | 819 us: 1.04x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.47 us: 1.05x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.06x slower                                                  |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                 |
| scimark_fft                | 345 ms                                                 | 372 ms: 1.08x slower                                                  |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 87.4 ms: 1.08x slower                                                 |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                  |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.20 us: 1.13x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                 |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                 |
| coverage                   | 78.8 ms                                                | 93.4 ms: 1.19x slower                                                 |
| async_generators           | 374 ms                                                 | 448 ms: 1.20x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.21x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 8.92 ms: 1.22x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                 |
| telco                      | 6.86 ms                                                | 176 ms: 25.69x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (3): scimark_lu, deepcopy, pycparser
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.39% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x