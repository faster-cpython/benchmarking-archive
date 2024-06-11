# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: linux-x86_64
- commit hash: f837cc6
- commit date: 2024-06-10
- overall geometric mean: 1.07x faster
- HPT reliability: 99.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                 |
| docutils       | 2.66 sec                                               | 2.93 sec: 1.10x slower                                               |
| html5lib       | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                |
| tornado_http   | 98.1 ms                                                | 96.9 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 340 ms: 1.44x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 914 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                 |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 482 ms: 1.33x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 972 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 631 ms: 1.19x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 82.5 ms: 1.16x faster                                                |
| float          | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                 |
| regex_effbot   | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                |
| tomli_loads          | 2.30 sec                                               | 1.92 sec: 1.20x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                 |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 297 us: 1.08x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                |
| xml_etree_generate   | 81.1 ms                                                | 82.2 ms: 1.01x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 59.0 ms: 1.04x slower                                                |
| unpickle_list        | 5.21 us                                                | 5.44 us: 1.04x slower                                                |
| pickle_dict          | 34.6 us                                                | 36.4 us: 1.05x slower                                                |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                |
| pickle_list          | 4.59 us                                                | 5.39 us: 1.18x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.20 ms: 1.20x slower                                                |
| python_startup         | 8.56 ms                                                | 10.8 ms: 1.26x slower                                                |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.83 ms: 1.08x faster                                                |
| genshi_xml      | 53.4 ms                                                | 58.2 ms: 1.09x slower                                                |
| django_template | 33.5 ms                                                | 36.5 ms: 1.09x slower                                                |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-linux-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.01x faster                                                 |
| generators                 | 74.9 ms                                                | 30.8 ms: 2.43x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                               |
| async_tree_none_tg         | 491 ms                                                 | 340 ms: 1.44x faster                                                 |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 914 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                 |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                 |
| pylint                     | 476 ms                                                 | 352 ms: 1.35x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 482 ms: 1.33x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 972 ms: 1.32x faster                                                 |
| richards_super             | 61.9 ms                                                | 47.3 ms: 1.31x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                                 |
| chaos                      | 71.9 ms                                                | 60.0 ms: 1.20x faster                                                |
| tomli_loads                | 2.30 sec                                               | 1.92 sec: 1.20x faster                                               |
| richards                   | 49.8 ms                                                | 41.8 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 631 ms: 1.19x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                |
| nbody                      | 96.0 ms                                                | 82.5 ms: 1.16x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.41 ms: 1.14x faster                                                |
| pathlib                    | 18.5 ms                                                | 16.3 ms: 1.14x faster                                                |
| crypto_pyaes               | 76.7 ms                                                | 67.7 ms: 1.13x faster                                                |
| fannkuch                   | 405 ms                                                 | 358 ms: 1.13x faster                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 62.8 ms: 1.13x faster                                                |
| raytrace                   | 309 ms                                                 | 277 ms: 1.11x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.67 us: 1.10x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                 |
| float                      | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                 |
| scimark_fft                | 345 ms                                                 | 318 ms: 1.09x faster                                                 |
| mako                       | 10.7 ms                                                | 9.83 ms: 1.08x faster                                                |
| logging_format             | 6.81 us                                                | 6.29 us: 1.08x faster                                                |
| pickle_pure_python         | 320 us                                                 | 297 us: 1.08x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.07x faster                                               |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                               |
| spectral_norm              | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 37.8 us: 1.06x faster                                                |
| pprint_safe_repr           | 747 ms                                                 | 709 ms: 1.05x faster                                                 |
| deltablue                  | 3.92 ms                                                | 3.73 ms: 1.05x faster                                                |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                 |
| hexiom                     | 6.89 ms                                                | 6.63 ms: 1.04x faster                                                |
| pycparser                  | 1.19 sec                                               | 1.14 sec: 1.04x faster                                               |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                 |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                 |
| nqueens                    | 87.9 ms                                                | 86.2 ms: 1.02x faster                                                |
| tornado_http               | 98.1 ms                                                | 96.9 ms: 1.01x faster                                                |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                 |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                 |
| sympy_str                  | 297 ms                                                 | 299 ms: 1.01x slower                                                 |
| deepcopy                   | 365 us                                                 | 368 us: 1.01x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.55 ms: 1.01x slower                                                |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                 |
| gc_traversal               | 4.01 ms                                                | 4.06 ms: 1.01x slower                                                |
| xml_etree_generate         | 81.1 ms                                                | 82.2 ms: 1.01x slower                                                |
| json                       | 5.24 ms                                                | 5.32 ms: 1.01x slower                                                |
| deepcopy_reduce            | 3.22 us                                                | 3.30 us: 1.03x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 56.8 ms: 1.03x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                 |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 59.0 ms: 1.04x slower                                                |
| unpickle_list              | 5.21 us                                                | 5.44 us: 1.04x slower                                                |
| thrift                     | 784 us                                                 | 819 us: 1.04x slower                                                 |
| sympy_expand               | 484 ms                                                 | 507 ms: 1.05x slower                                                 |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                |
| bench_thread_pool          | 834 us                                                 | 876 us: 1.05x slower                                                 |
| pyflate                    | 434 ms                                                 | 456 ms: 1.05x slower                                                 |
| pickle_dict                | 34.6 us                                                | 36.4 us: 1.05x slower                                                |
| html5lib                   | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                |
| dulwich_log                | 64.6 ms                                                | 68.6 ms: 1.06x slower                                                |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.08x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 58.2 ms: 1.09x slower                                                |
| django_template            | 33.5 ms                                                | 36.5 ms: 1.09x slower                                                |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                |
| docutils                   | 2.66 sec                                               | 2.93 sec: 1.10x slower                                               |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                |
| scimark_sor                | 121 ms                                                 | 137 ms: 1.13x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.39 us: 1.18x slower                                                |
| coverage                   | 78.8 ms                                                | 92.8 ms: 1.18x slower                                                |
| telco                      | 6.86 ms                                                | 8.12 ms: 1.18x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 7.20 ms: 1.20x slower                                                |
| async_generators           | 374 ms                                                 | 464 ms: 1.24x slower                                                 |
| python_startup             | 8.56 ms                                                | 10.8 ms: 1.26x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.81 ms: 1.26x slower                                                |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                         |

Benchmark hidden because not significant (2): bench_mp_pool, sqlglot_normalize
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.38% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x