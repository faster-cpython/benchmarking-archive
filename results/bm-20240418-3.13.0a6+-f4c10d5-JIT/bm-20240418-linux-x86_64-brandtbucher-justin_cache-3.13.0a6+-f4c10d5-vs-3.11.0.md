# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_cache
- machine: linux-x86_64
- commit hash: f4c10d5
- commit date: 2024-04-18
- overall geometric mean: 1.05x faster
- HPT reliability: 57.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                |
| docutils       | 2.66 sec                                               | 2.92 sec: 1.10x slower                                               |
| html5lib       | 64.8 ms                                                | 67.4 ms: 1.04x slower                                                |
| tornado_http   | 98.1 ms                                                | 96.6 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 362 ms: 1.46x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 941 ms: 1.37x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.37x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.3 ms: 1.10x faster                                                |
| float          | 78.9 ms                                                | 77.7 ms: 1.02x faster                                                |
| pidigits       | 194 ms                                                 | 210 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 144 ms: 1.02x slower                                                 |
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                 |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.01 sec: 1.14x faster                                               |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                                |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                 |
| unpickle_pure_python | 242 us                                                 | 236 us: 1.03x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 109 ms: 1.01x slower                                                 |
| unpickle_list        | 5.21 us                                                | 5.27 us: 1.01x slower                                                |
| pickle_dict          | 34.6 us                                                | 36.0 us: 1.04x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 60.4 ms: 1.06x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 88.1 ms: 1.09x slower                                                |
| pickle               | 11.0 us                                                | 12.0 us: 1.10x slower                                                |
| unpickle             | 13.8 us                                                | 15.7 us: 1.14x slower                                                |
| pickle_list          | 4.59 us                                                | 5.33 us: 1.16x slower                                                |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.69 ms: 1.28x slower                                                |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 54.9 ms: 1.03x slower                                                |
| django_template | 33.5 ms                                                | 36.2 ms: 1.08x slower                                                |
| mako            | 10.7 ms                                                | 11.5 ms: 1.08x slower                                                |
| genshi_text     | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.65x faster                                                 |
| generators                 | 74.9 ms                                                | 30.5 ms: 2.45x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 512 ms: 1.71x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                               |
| async_tree_none            | 528 ms                                                 | 362 ms: 1.46x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                 |
| pylint                     | 476 ms                                                 | 335 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 941 ms: 1.37x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.37x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                 |
| comprehensions             | 23.6 us                                                | 18.3 us: 1.29x faster                                                |
| richards_super             | 61.9 ms                                                | 49.0 ms: 1.26x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                 |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                                |
| tomli_loads                | 2.30 sec                                               | 2.01 sec: 1.14x faster                                               |
| richards                   | 49.8 ms                                                | 43.6 ms: 1.14x faster                                                |
| chaos                      | 71.9 ms                                                | 63.3 ms: 1.14x faster                                                |
| raytrace                   | 309 ms                                                 | 275 ms: 1.12x faster                                                 |
| nbody                      | 96.0 ms                                                | 87.3 ms: 1.10x faster                                                |
| logging_simple             | 6.22 us                                                | 5.75 us: 1.08x faster                                                |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                |
| logging_format             | 6.81 us                                                | 6.36 us: 1.07x faster                                                |
| deltablue                  | 3.92 ms                                                | 3.69 ms: 1.06x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 38.2 us: 1.05x faster                                                |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.64 sec: 1.05x faster                                               |
| scimark_monte_carlo        | 70.7 ms                                                | 67.9 ms: 1.04x faster                                                |
| fannkuch                   | 405 ms                                                 | 389 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.83 ms: 1.04x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.85 ms: 1.04x faster                                                |
| djangocms                  | 33.5 us                                                | 32.2 us: 1.04x faster                                                |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                |
| crypto_pyaes               | 76.7 ms                                                | 73.9 ms: 1.04x faster                                                |
| json                       | 5.24 ms                                                | 5.09 ms: 1.03x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 236 us: 1.03x faster                                                 |
| deepcopy                   | 365 us                                                 | 356 us: 1.02x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                 |
| float                      | 78.9 ms                                                | 77.7 ms: 1.02x faster                                                |
| tornado_http               | 98.1 ms                                                | 96.6 ms: 1.01x faster                                                |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                               |
| scimark_fft                | 345 ms                                                 | 341 ms: 1.01x faster                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                               |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                                |
| go                         | 149 ms                                                 | 148 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 747 ms                                                 | 751 ms: 1.00x slower                                                 |
| sympy_str                  | 297 ms                                                 | 299 ms: 1.01x slower                                                 |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 170 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 108 ms                                                 | 109 ms: 1.01x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.27 us: 1.01x slower                                                |
| regex_compile              | 141 ms                                                 | 144 ms: 1.02x slower                                                 |
| dask                       | 365 ms                                                 | 374 ms: 1.03x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 54.9 ms: 1.03x slower                                                |
| hexiom                     | 6.89 ms                                                | 7.09 ms: 1.03x slower                                                |
| sympy_integrate            | 21.5 ms                                                | 22.1 ms: 1.03x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                 |
| meteor_contest             | 109 ms                                                 | 113 ms: 1.03x slower                                                 |
| sympy_expand               | 484 ms                                                 | 501 ms: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 863 us: 1.03x slower                                                 |
| html5lib                   | 64.8 ms                                                | 67.4 ms: 1.04x slower                                                |
| pickle_dict                | 34.6 us                                                | 36.0 us: 1.04x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 57.8 ms: 1.05x slower                                                |
| thrift                     | 784 us                                                 | 821 us: 1.05x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                                 |
| chameleon                  | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                |
| nqueens                    | 87.9 ms                                                | 93.0 ms: 1.06x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 60.4 ms: 1.06x slower                                                |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                 |
| django_template            | 33.5 ms                                                | 36.2 ms: 1.08x slower                                                |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                 |
| mako                       | 10.7 ms                                                | 11.5 ms: 1.08x slower                                                |
| dulwich_log                | 64.6 ms                                                | 69.9 ms: 1.08x slower                                                |
| pidigits                   | 194 ms                                                 | 210 ms: 1.08x slower                                                 |
| genshi_text                | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                |
| xml_etree_generate         | 81.1 ms                                                | 88.1 ms: 1.09x slower                                                |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                                |
| scimark_sor                | 121 ms                                                 | 132 ms: 1.09x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                |
| pickle                     | 11.0 us                                                | 12.0 us: 1.10x slower                                                |
| docutils                   | 2.66 sec                                               | 2.92 sec: 1.10x slower                                               |
| pyflate                    | 434 ms                                                 | 479 ms: 1.10x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.88 us: 1.12x slower                                                |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.14x slower                                                |
| mypy2                      | 686 ms                                                 | 782 ms: 1.14x slower                                                 |
| scimark_lu                 | 116 ms                                                 | 134 ms: 1.15x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.33 us: 1.16x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.23x slower                                                |
| async_generators           | 374 ms                                                 | 460 ms: 1.23x slower                                                 |
| coverage                   | 78.8 ms                                                | 98.2 ms: 1.25x slower                                                |
| telco                      | 6.86 ms                                                | 8.56 ms: 1.25x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 7.69 ms: 1.28x slower                                                |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 57.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x