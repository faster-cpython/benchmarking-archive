# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 19f3205
- commit date: 2024-04-26
- overall geometric mean: 1.07x faster
- HPT reliability: 98.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.04x slower                                                       |
| chameleon      | 6.70 ms                                                | 6.99 ms: 1.04x slower                                                      |
| docutils       | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                     |
| html5lib       | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                      |
| tornado_http   | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 77.8 ms: 1.23x faster                                                      |
| float          | 78.9 ms                                                | 72.7 ms: 1.09x faster                                                      |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                  | 1.11x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.02x faster                                                       |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                      |
| regex_v8       | 22.9 ms                                                | 25.3 ms: 1.11x slower                                                      |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                  | 1.07x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                      |
| tomli_loads          | 2.30 sec                                               | 1.92 sec: 1.20x faster                                                     |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                       |
| unpickle_pure_python | 242 us                                                 | 226 us: 1.07x faster                                                       |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                      |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                                       |
| unpickle_list        | 5.21 us                                                | 5.26 us: 1.01x slower                                                      |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                                      |
| xml_etree_process    | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                      |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.6 ms: 1.08x slower                                                      |
| unpickle             | 13.8 us                                                | 15.0 us: 1.08x slower                                                      |
| pickle_list          | 4.59 us                                                | 5.12 us: 1.12x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.69 ms: 1.28x slower                                                      |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                      |
| genshi_xml      | 53.4 ms                                                | 53.9 ms: 1.01x slower                                                      |
| django_template | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                      |
| genshi_text     | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.44x faster                                                       |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                      |
| asyncio_tcp                | 875 ms                                                 | 516 ms: 1.70x faster                                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                     |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                       |
| pylint                     | 476 ms                                                 | 334 ms: 1.43x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                                       |
| comprehensions             | 23.6 us                                                | 17.2 us: 1.38x faster                                                      |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                                       |
| richards_super             | 61.9 ms                                                | 48.4 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                                       |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                      |
| nbody                      | 96.0 ms                                                | 77.8 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 1.92 sec: 1.20x faster                                                     |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                      |
| richards                   | 49.8 ms                                                | 41.9 ms: 1.19x faster                                                      |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.33 ms: 1.16x faster                                                      |
| fannkuch                   | 405 ms                                                 | 353 ms: 1.15x faster                                                       |
| scimark_fft                | 345 ms                                                 | 303 ms: 1.14x faster                                                       |
| raytrace                   | 309 ms                                                 | 273 ms: 1.13x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 68.3 ms: 1.12x faster                                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 63.6 ms: 1.11x faster                                                      |
| spectral_norm              | 108 ms                                                 | 97.9 ms: 1.10x faster                                                      |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                       |
| float                      | 78.9 ms                                                | 72.7 ms: 1.09x faster                                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                                      |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                       |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                      |
| unpickle_pure_python       | 242 us                                                 | 226 us: 1.07x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.67 ms: 1.07x faster                                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                      |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                      |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                      |
| pprint_pformat             | 1.55 sec                                               | 1.47 sec: 1.06x faster                                                     |
| hexiom                     | 6.89 ms                                                | 6.53 ms: 1.05x faster                                                      |
| logging_format             | 6.81 us                                                | 6.47 us: 1.05x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                                       |
| pathlib                    | 18.5 ms                                                | 17.7 ms: 1.05x faster                                                      |
| json                       | 5.24 ms                                                | 5.04 ms: 1.04x faster                                                      |
| gc_traversal               | 4.01 ms                                                | 3.87 ms: 1.04x faster                                                      |
| djangocms                  | 33.5 us                                                | 32.6 us: 1.03x faster                                                      |
| pprint_safe_repr           | 747 ms                                                 | 728 ms: 1.03x faster                                                       |
| deepcopy_memo              | 40.2 us                                                | 39.1 us: 1.03x faster                                                      |
| nqueens                    | 87.9 ms                                                | 85.7 ms: 1.03x faster                                                      |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                       |
| tornado_http               | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                      |
| regex_compile              | 141 ms                                                 | 139 ms: 1.02x faster                                                       |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                                     |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                       |
| deepcopy                   | 365 us                                                 | 362 us: 1.01x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.77 sec: 1.00x faster                                                     |
| go                         | 149 ms                                                 | 149 ms: 1.00x slower                                                       |
| bench_mp_pool              | 24.0 ms                                                | 24.1 ms: 1.00x slower                                                      |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.01x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 53.9 ms: 1.01x slower                                                      |
| unpickle_list              | 5.21 us                                                | 5.26 us: 1.01x slower                                                      |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                       |
| dask                       | 365 ms                                                 | 374 ms: 1.02x slower                                                       |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                                      |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                       |
| sympy_integrate            | 21.5 ms                                                | 22.0 ms: 1.03x slower                                                      |
| sympy_expand               | 484 ms                                                 | 497 ms: 1.03x slower                                                       |
| pyflate                    | 434 ms                                                 | 448 ms: 1.03x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                      |
| bench_thread_pool          | 834 us                                                 | 866 us: 1.04x slower                                                       |
| chameleon                  | 6.70 ms                                                | 6.99 ms: 1.04x slower                                                      |
| 2to3                       | 264 ms                                                 | 276 ms: 1.04x slower                                                       |
| thrift                     | 784 us                                                 | 825 us: 1.05x slower                                                       |
| html5lib                   | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                      |
| xml_etree_process          | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                      |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                      |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                      |
| django_template            | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                      |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.07x slower                                                       |
| dulwich_log                | 64.6 ms                                                | 69.2 ms: 1.07x slower                                                      |
| xml_etree_generate         | 81.1 ms                                                | 87.6 ms: 1.08x slower                                                      |
| genshi_text                | 22.5 ms                                                | 24.4 ms: 1.08x slower                                                      |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.08x slower                                                      |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                                      |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 127 ms: 1.09x slower                                                       |
| docutils                   | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                     |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                      |
| regex_v8                   | 22.9 ms                                                | 25.3 ms: 1.11x slower                                                      |
| pickle_list                | 4.59 us                                                | 5.12 us: 1.12x slower                                                      |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                       |
| mypy2                      | 686 ms                                                 | 787 ms: 1.15x slower                                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.23x slower                                                      |
| coverage                   | 78.8 ms                                                | 97.4 ms: 1.24x slower                                                      |
| async_generators           | 374 ms                                                 | 467 ms: 1.25x slower                                                       |
| telco                      | 6.86 ms                                                | 8.63 ms: 1.26x slower                                                      |
| python_startup_no_site     | 6.01 ms                                                | 7.69 ms: 1.28x slower                                                      |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                               |

Benchmark hidden because not significant (1): deepcopy_reduce
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.25% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x