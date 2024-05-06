# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 280cb86
- commit date: 2024-04-25
- overall geometric mean: 1.07x faster
- HPT reliability: 99.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                       |
| chameleon      | 6.70 ms                                                | 6.94 ms: 1.04x slower                                                      |
| docutils       | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                     |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                      |
| tornado_http   | 98.1 ms                                                | 95.3 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.49x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 937 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 947 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 75.3 ms: 1.27x faster                                                      |
| float          | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                      |
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                  | 1.12x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                       |
| regex_effbot   | 3.51 ms                                                | 3.76 ms: 1.07x slower                                                      |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                      |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                  | 1.07x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                      |
| tomli_loads          | 2.30 sec                                               | 1.90 sec: 1.21x faster                                                     |
| xml_etree_parse      | 164 ms                                                 | 148 ms: 1.11x faster                                                       |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.08x faster                                                       |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                      |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.04x faster                                                       |
| unpickle_list        | 5.21 us                                                | 5.14 us: 1.01x faster                                                      |
| pickle               | 11.0 us                                                | 11.5 us: 1.05x slower                                                      |
| xml_etree_process    | 56.9 ms                                                | 59.7 ms: 1.05x slower                                                      |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                      |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                      |
| pickle_list          | 4.59 us                                                | 5.10 us: 1.11x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.71 ms: 1.28x slower                                                      |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.0 ms: 1.06x faster                                                      |
| genshi_xml      | 53.4 ms                                                | 54.2 ms: 1.01x slower                                                      |
| django_template | 33.5 ms                                                | 35.9 ms: 1.07x slower                                                      |
| genshi_text     | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 116 us: 4.49x faster                                                       |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.51x faster                                                      |
| asyncio_tcp                | 875 ms                                                 | 516 ms: 1.70x faster                                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                     |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.49x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                       |
| pylint                     | 476 ms                                                 | 332 ms: 1.44x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                       |
| comprehensions             | 23.6 us                                                | 17.1 us: 1.38x faster                                                      |
| async_tree_io              | 1.29 sec                                               | 937 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 947 ms: 1.37x faster                                                       |
| richards_super             | 61.9 ms                                                | 48.0 ms: 1.29x faster                                                      |
| nbody                      | 96.0 ms                                                | 75.3 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                       |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 1.90 sec: 1.21x faster                                                     |
| chaos                      | 71.9 ms                                                | 59.3 ms: 1.21x faster                                                      |
| richards                   | 49.8 ms                                                | 41.9 ms: 1.19x faster                                                      |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.18x faster                                                      |
| fannkuch                   | 405 ms                                                 | 345 ms: 1.17x faster                                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.38 ms: 1.15x faster                                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 61.9 ms: 1.14x faster                                                      |
| raytrace                   | 309 ms                                                 | 271 ms: 1.14x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 67.7 ms: 1.13x faster                                                      |
| scimark_fft                | 345 ms                                                 | 308 ms: 1.12x faster                                                       |
| xml_etree_parse            | 164 ms                                                 | 148 ms: 1.11x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                      |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                       |
| float                      | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                      |
| spectral_norm              | 108 ms                                                 | 99.7 ms: 1.09x faster                                                      |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.08x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.63 ms: 1.08x faster                                                      |
| hexiom                     | 6.89 ms                                                | 6.40 ms: 1.08x faster                                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                      |
| logging_simple             | 6.22 us                                                | 5.82 us: 1.07x faster                                                      |
| mako                       | 10.7 ms                                                | 10.0 ms: 1.06x faster                                                      |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                       |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                      |
| pprint_pformat             | 1.55 sec                                               | 1.48 sec: 1.05x faster                                                     |
| djangocms                  | 33.5 us                                                | 32.0 us: 1.05x faster                                                      |
| logging_format             | 6.81 us                                                | 6.50 us: 1.05x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.04x faster                                                       |
| pprint_safe_repr           | 747 ms                                                 | 724 ms: 1.03x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.69 sec: 1.03x faster                                                     |
| tornado_http               | 98.1 ms                                                | 95.3 ms: 1.03x faster                                                      |
| deepcopy_memo              | 40.2 us                                                | 39.2 us: 1.02x faster                                                      |
| pathlib                    | 18.5 ms                                                | 18.1 ms: 1.02x faster                                                      |
| nqueens                    | 87.9 ms                                                | 86.0 ms: 1.02x faster                                                      |
| sympy_str                  | 297 ms                                                 | 291 ms: 1.02x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                       |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                     |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                      |
| unpickle_list              | 5.21 us                                                | 5.14 us: 1.01x faster                                                      |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                       |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                       |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                       |
| deepcopy                   | 365 us                                                 | 363 us: 1.01x faster                                                       |
| pyflate                    | 434 ms                                                 | 432 ms: 1.00x faster                                                       |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 54.2 ms: 1.01x slower                                                      |
| gc_traversal               | 4.01 ms                                                | 4.06 ms: 1.01x slower                                                      |
| sympy_integrate            | 21.5 ms                                                | 21.8 ms: 1.02x slower                                                      |
| sympy_expand               | 484 ms                                                 | 494 ms: 1.02x slower                                                       |
| dask                       | 365 ms                                                 | 373 ms: 1.02x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 56.7 ms: 1.03x slower                                                      |
| asyncio_websockets         | 550 ms                                                 | 565 ms: 1.03x slower                                                       |
| bench_thread_pool          | 834 us                                                 | 860 us: 1.03x slower                                                       |
| chameleon                  | 6.70 ms                                                | 6.94 ms: 1.04x slower                                                      |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                       |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                                       |
| pickle                     | 11.0 us                                                | 11.5 us: 1.05x slower                                                      |
| xml_etree_process          | 56.9 ms                                                | 59.7 ms: 1.05x slower                                                      |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                      |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                                       |
| dulwich_log                | 64.6 ms                                                | 68.8 ms: 1.07x slower                                                      |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                      |
| django_template            | 33.5 ms                                                | 35.9 ms: 1.07x slower                                                      |
| regex_effbot               | 3.51 ms                                                | 3.76 ms: 1.07x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.08x slower                                                       |
| gunicorn                   | 1.20 ms                                                | 1.29 ms: 1.08x slower                                                      |
| genshi_text                | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                      |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                      |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                      |
| sqlite_synth               | 2.57 us                                                | 2.82 us: 1.10x slower                                                      |
| docutils                   | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                     |
| pickle_list                | 4.59 us                                                | 5.10 us: 1.11x slower                                                      |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.11x slower                                                      |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                       |
| mypy2                      | 686 ms                                                 | 779 ms: 1.14x slower                                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                      |
| coverage                   | 78.8 ms                                                | 97.2 ms: 1.23x slower                                                      |
| async_generators           | 374 ms                                                 | 466 ms: 1.25x slower                                                       |
| telco                      | 6.86 ms                                                | 8.57 ms: 1.25x slower                                                      |
| python_startup_no_site     | 6.01 ms                                                | 7.71 ms: 1.28x slower                                                      |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                               |

Benchmark hidden because not significant (4): deepcopy_reduce, sqlglot_normalize, pickle_dict, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.55% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x