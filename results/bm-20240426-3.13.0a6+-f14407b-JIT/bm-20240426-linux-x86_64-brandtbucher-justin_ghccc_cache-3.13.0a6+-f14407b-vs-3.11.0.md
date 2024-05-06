# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: f14407b
- commit date: 2024-04-26
- overall geometric mean: 1.07x faster
- HPT reliability: 97.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                       |
| chameleon      | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                      |
| docutils       | 2.66 sec                                               | 2.93 sec: 1.10x slower                                                     |
| html5lib       | 64.8 ms                                                | 68.1 ms: 1.05x slower                                                      |
| tornado_http   | 98.1 ms                                                | 95.6 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 438 ms: 1.43x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 921 ms: 1.40x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 947 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.0 ms: 1.20x faster                                                      |
| float          | 78.9 ms                                                | 73.1 ms: 1.08x faster                                                      |
| pidigits       | 194 ms                                                 | 210 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                  | 1.06x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 141 ms: 1.00x faster                                                       |
| regex_v8       | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                      |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                       |
| regex_effbot   | 3.51 ms                                                | 4.23 ms: 1.21x slower                                                      |
| Geometric mean | (ref)                                                  | 1.09x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                      |
| tomli_loads          | 2.30 sec                                               | 1.93 sec: 1.19x faster                                                     |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                       |
| unpickle_pure_python | 242 us                                                 | 226 us: 1.07x faster                                                       |
| json_loads           | 29.2 us                                                | 27.4 us: 1.06x faster                                                      |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| pickle_pure_python   | 320 us                                                 | 308 us: 1.04x faster                                                       |
| unpickle_list        | 5.21 us                                                | 5.14 us: 1.01x faster                                                      |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                                      |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                      |
| xml_etree_generate   | 81.1 ms                                                | 86.8 ms: 1.07x slower                                                      |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                      |
| pickle_list          | 4.59 us                                                | 5.09 us: 1.11x slower                                                      |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.66 ms: 1.27x slower                                                      |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.0 ms: 1.06x faster                                                      |
| genshi_xml      | 53.4 ms                                                | 54.1 ms: 1.01x slower                                                      |
| django_template | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                      |
| genshi_text     | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.45x faster                                                       |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                      |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.71x faster                                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                     |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                       |
| pylint                     | 476 ms                                                 | 332 ms: 1.43x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 438 ms: 1.43x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 921 ms: 1.40x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                       |
| comprehensions             | 23.6 us                                                | 17.2 us: 1.37x faster                                                      |
| async_tree_io_tg           | 1.29 sec                                               | 947 ms: 1.37x faster                                                       |
| richards_super             | 61.9 ms                                                | 48.9 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.26x faster                                                       |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                       |
| nbody                      | 96.0 ms                                                | 80.0 ms: 1.20x faster                                                      |
| tomli_loads                | 2.30 sec                                               | 1.93 sec: 1.19x faster                                                     |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                      |
| chaos                      | 71.9 ms                                                | 61.0 ms: 1.18x faster                                                      |
| richards                   | 49.8 ms                                                | 42.4 ms: 1.18x faster                                                      |
| fannkuch                   | 405 ms                                                 | 357 ms: 1.14x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 67.6 ms: 1.13x faster                                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 62.5 ms: 1.13x faster                                                      |
| raytrace                   | 309 ms                                                 | 274 ms: 1.13x faster                                                       |
| scimark_fft                | 345 ms                                                 | 310 ms: 1.12x faster                                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.55 ms: 1.11x faster                                                      |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                      |
| spectral_norm              | 108 ms                                                 | 99.2 ms: 1.09x faster                                                      |
| float                      | 78.9 ms                                                | 73.1 ms: 1.08x faster                                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                      |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                       |
| unpickle_pure_python       | 242 us                                                 | 226 us: 1.07x faster                                                       |
| json_loads                 | 29.2 us                                                | 27.4 us: 1.06x faster                                                      |
| pprint_pformat             | 1.55 sec                                               | 1.46 sec: 1.06x faster                                                     |
| mako                       | 10.7 ms                                                | 10.0 ms: 1.06x faster                                                      |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.72 ms: 1.06x faster                                                      |
| logging_simple             | 6.22 us                                                | 5.92 us: 1.05x faster                                                      |
| hexiom                     | 6.89 ms                                                | 6.57 ms: 1.05x faster                                                      |
| logging_format             | 6.81 us                                                | 6.52 us: 1.04x faster                                                      |
| djangocms                  | 33.5 us                                                | 32.2 us: 1.04x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 308 us: 1.04x faster                                                       |
| gc_traversal               | 4.01 ms                                                | 3.86 ms: 1.04x faster                                                      |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                                      |
| pprint_safe_repr           | 747 ms                                                 | 722 ms: 1.04x faster                                                       |
| tornado_http               | 98.1 ms                                                | 95.6 ms: 1.03x faster                                                      |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                                      |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                     |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.01x faster                                                       |
| unpickle_list              | 5.21 us                                                | 5.14 us: 1.01x faster                                                      |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                       |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                       |
| deepcopy_memo              | 40.2 us                                                | 39.8 us: 1.01x faster                                                      |
| deepcopy                   | 365 us                                                 | 362 us: 1.01x faster                                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.20 us: 1.00x faster                                                      |
| regex_compile              | 141 ms                                                 | 141 ms: 1.00x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.00x slower                                                     |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.00x slower                                                       |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                                      |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 54.1 ms: 1.01x slower                                                      |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                      |
| dask                       | 365 ms                                                 | 373 ms: 1.02x slower                                                       |
| sympy_expand               | 484 ms                                                 | 496 ms: 1.02x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                      |
| bench_thread_pool          | 834 us                                                 | 863 us: 1.03x slower                                                       |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                       |
| chameleon                  | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                      |
| html5lib                   | 64.8 ms                                                | 68.1 ms: 1.05x slower                                                      |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                      |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.06x slower                                                       |
| thrift                     | 784 us                                                 | 834 us: 1.06x slower                                                       |
| xml_etree_generate         | 81.1 ms                                                | 86.8 ms: 1.07x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.08x slower                                                       |
| dulwich_log                | 64.6 ms                                                | 69.7 ms: 1.08x slower                                                      |
| pidigits                   | 194 ms                                                 | 210 ms: 1.08x slower                                                       |
| regex_v8                   | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                      |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                                      |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                      |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                      |
| django_template            | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                      |
| sqlite_synth               | 2.57 us                                                | 2.83 us: 1.10x slower                                                      |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                       |
| docutils                   | 2.66 sec                                               | 2.93 sec: 1.10x slower                                                     |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                      |
| pickle_list                | 4.59 us                                                | 5.09 us: 1.11x slower                                                      |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                      |
| mypy2                      | 686 ms                                                 | 785 ms: 1.15x slower                                                       |
| regex_effbot               | 3.51 ms                                                | 4.23 ms: 1.21x slower                                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                      |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                      |
| async_generators           | 374 ms                                                 | 470 ms: 1.26x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.66 ms: 1.27x slower                                                      |
| telco                      | 6.86 ms                                                | 8.74 ms: 1.27x slower                                                      |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                               |

Benchmark hidden because not significant (3): nqueens, bench_mp_pool, pyflate
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x