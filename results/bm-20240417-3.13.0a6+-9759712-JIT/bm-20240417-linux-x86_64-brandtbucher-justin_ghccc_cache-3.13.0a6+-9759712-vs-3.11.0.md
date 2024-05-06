# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 9759712
- commit date: 2024-04-17
- overall geometric mean: 1.07x faster
- HPT reliability: 98.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.04x slower                                                       |
| chameleon      | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                      |
| docutils       | 2.66 sec                                               | 2.91 sec: 1.09x slower                                                     |
| html5lib       | 64.8 ms                                                | 67.9 ms: 1.05x slower                                                      |
| tornado_http   | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 922 ms: 1.40x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 951 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 616 ms: 1.22x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 77.1 ms: 1.24x faster                                                      |
| float          | 78.9 ms                                                | 72.9 ms: 1.08x faster                                                      |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                  | 1.11x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                       |
| regex_effbot   | 3.51 ms                                                | 3.77 ms: 1.08x slower                                                      |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                       |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                  | 1.07x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                      |
| tomli_loads          | 2.30 sec                                               | 1.93 sec: 1.20x faster                                                     |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                       |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                       |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                                      |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                       |
| unpickle_list        | 5.21 us                                                | 5.12 us: 1.02x faster                                                      |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                       |
| pickle_dict          | 34.6 us                                                | 34.1 us: 1.02x faster                                                      |
| xml_etree_process    | 56.9 ms                                                | 59.5 ms: 1.05x slower                                                      |
| pickle               | 11.0 us                                                | 11.6 us: 1.05x slower                                                      |
| pickle_list          | 4.59 us                                                | 4.91 us: 1.07x slower                                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                      |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.66 ms: 1.27x slower                                                      |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                      |
| genshi_xml      | 53.4 ms                                                | 54.2 ms: 1.01x slower                                                      |
| django_template | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                      |
| genshi_text     | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.65x faster                                                       |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                      |
| asyncio_tcp                | 875 ms                                                 | 512 ms: 1.71x faster                                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                     |
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                       |
| pylint                     | 476 ms                                                 | 334 ms: 1.43x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 922 ms: 1.40x faster                                                       |
| comprehensions             | 23.6 us                                                | 17.2 us: 1.38x faster                                                      |
| async_tree_memoization     | 639 ms                                                 | 467 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 951 ms: 1.36x faster                                                       |
| richards_super             | 61.9 ms                                                | 48.5 ms: 1.28x faster                                                      |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                       |
| nbody                      | 96.0 ms                                                | 77.1 ms: 1.24x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 616 ms: 1.22x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 1.93 sec: 1.20x faster                                                     |
| chaos                      | 71.9 ms                                                | 60.2 ms: 1.19x faster                                                      |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                                      |
| richards                   | 49.8 ms                                                | 42.9 ms: 1.16x faster                                                      |
| fannkuch                   | 405 ms                                                 | 350 ms: 1.16x faster                                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.34 ms: 1.16x faster                                                      |
| raytrace                   | 309 ms                                                 | 270 ms: 1.14x faster                                                       |
| scimark_fft                | 345 ms                                                 | 304 ms: 1.14x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 68.5 ms: 1.12x faster                                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 63.4 ms: 1.12x faster                                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                      |
| logging_simple             | 6.22 us                                                | 5.74 us: 1.08x faster                                                      |
| spectral_norm              | 108 ms                                                 | 99.8 ms: 1.08x faster                                                      |
| float                      | 78.9 ms                                                | 72.9 ms: 1.08x faster                                                      |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                       |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                       |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.08x faster                                                      |
| logging_format             | 6.81 us                                                | 6.37 us: 1.07x faster                                                      |
| deltablue                  | 3.92 ms                                                | 3.67 ms: 1.07x faster                                                      |
| djangocms                  | 33.5 us                                                | 31.5 us: 1.06x faster                                                      |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                      |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                      |
| pprint_pformat             | 1.55 sec                                               | 1.48 sec: 1.05x faster                                                     |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                       |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                                      |
| pprint_safe_repr           | 747 ms                                                 | 722 ms: 1.04x faster                                                       |
| json                       | 5.24 ms                                                | 5.08 ms: 1.03x faster                                                      |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                       |
| hexiom                     | 6.89 ms                                                | 6.71 ms: 1.03x faster                                                      |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                      |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                       |
| tornado_http               | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                      |
| unpickle_list              | 5.21 us                                                | 5.12 us: 1.02x faster                                                      |
| deepcopy                   | 365 us                                                 | 359 us: 1.02x faster                                                       |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                       |
| pickle_dict                | 34.6 us                                                | 34.1 us: 1.02x faster                                                      |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                       |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                                      |
| mdp                        | 2.77 sec                                               | 2.75 sec: 1.01x faster                                                     |
| sympy_str                  | 297 ms                                                 | 295 ms: 1.01x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.00x faster                                                       |
| genshi_xml                 | 53.4 ms                                                | 54.2 ms: 1.01x slower                                                      |
| pyflate                    | 434 ms                                                 | 441 ms: 1.02x slower                                                       |
| sympy_integrate            | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                      |
| sympy_expand               | 484 ms                                                 | 496 ms: 1.02x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                       |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                                     |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                       |
| bench_thread_pool          | 834 us                                                 | 864 us: 1.04x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.3 ms: 1.04x slower                                                      |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                                       |
| 2to3                       | 264 ms                                                 | 276 ms: 1.04x slower                                                       |
| xml_etree_process          | 56.9 ms                                                | 59.5 ms: 1.05x slower                                                      |
| html5lib                   | 64.8 ms                                                | 67.9 ms: 1.05x slower                                                      |
| thrift                     | 784 us                                                 | 825 us: 1.05x slower                                                       |
| pickle                     | 11.0 us                                                | 11.6 us: 1.05x slower                                                      |
| django_template            | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                      |
| genshi_text                | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                      |
| chameleon                  | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 124 ms: 1.07x slower                                                       |
| pickle_list                | 4.59 us                                                | 4.91 us: 1.07x slower                                                      |
| dulwich_log                | 64.6 ms                                                | 69.1 ms: 1.07x slower                                                      |
| xml_etree_generate         | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                      |
| regex_effbot               | 3.51 ms                                                | 3.77 ms: 1.08x slower                                                      |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                                      |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                      |
| docutils                   | 2.66 sec                                               | 2.91 sec: 1.09x slower                                                     |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                       |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                      |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.11x slower                                                      |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                      |
| mypy2                      | 686 ms                                                 | 782 ms: 1.14x slower                                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                      |
| coverage                   | 78.8 ms                                                | 97.8 ms: 1.24x slower                                                      |
| telco                      | 6.86 ms                                                | 8.52 ms: 1.24x slower                                                      |
| async_generators           | 374 ms                                                 | 471 ms: 1.26x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.66 ms: 1.27x slower                                                      |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                               |

Benchmark hidden because not significant (5): gc_traversal, meteor_contest, sqlglot_normalize, bench_mp_pool, nqueens
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.70% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x