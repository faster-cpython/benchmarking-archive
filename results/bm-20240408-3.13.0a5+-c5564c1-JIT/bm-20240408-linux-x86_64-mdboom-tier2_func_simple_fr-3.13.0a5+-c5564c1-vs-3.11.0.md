# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.04x faster
- HPT reliability: 75.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                                   |
| chameleon      | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                  |
| docutils       | 2.66 sec                                               | 2.94 sec: 1.10x slower                                                 |
| html5lib       | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                  |
| tornado_http   | 98.1 ms                                                | 96.7 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 949 ms: 1.36x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 956 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.9 ms: 1.06x faster                                                  |
| float          | 78.9 ms                                                | 78.4 ms: 1.01x faster                                                  |
| pidigits       | 194 ms                                                 | 211 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 145 ms: 1.03x slower                                                   |
| regex_effbot   | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                  |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                   |
| regex_v8       | 22.9 ms                                                | 26.0 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                  |
| tomli_loads          | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 309 us: 1.04x faster                                                   |
| json_loads           | 29.2 us                                                | 28.2 us: 1.04x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 240 us: 1.01x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.32 us: 1.02x slower                                                  |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                  |
| pickle               | 11.0 us                                                | 11.8 us: 1.08x slower                                                  |
| unpickle             | 13.8 us                                                | 15.0 us: 1.08x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 87.7 ms: 1.08x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.28 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| python_startup_no_site | 6.01 ms                                                | 9.51 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 10.8 ms: 1.02x slower                                                  |
| genshi_text    | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.59x faster                                                   |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.52x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 501 ms: 1.75x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                 |
| pylint                     | 476 ms                                                 | 296 ms: 1.61x faster                                                   |
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 949 ms: 1.36x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 956 ms: 1.35x faster                                                   |
| comprehensions             | 23.6 us                                                | 17.9 us: 1.32x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                   |
| richards_super             | 61.9 ms                                                | 49.8 ms: 1.24x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.1 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                   |
| chaos                      | 71.9 ms                                                | 62.2 ms: 1.16x faster                                                  |
| richards                   | 49.8 ms                                                | 44.1 ms: 1.13x faster                                                  |
| raytrace                   | 309 ms                                                 | 274 ms: 1.13x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.11x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                  |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.68 ms: 1.07x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.84 us: 1.07x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                  |
| nbody                      | 96.0 ms                                                | 90.9 ms: 1.06x faster                                                  |
| logging_format             | 6.81 us                                                | 6.51 us: 1.05x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 309 us: 1.04x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.2 us: 1.04x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.88 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 68.9 ms: 1.03x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                   |
| fannkuch                   | 405 ms                                                 | 397 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.93 ms: 1.02x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 75.6 ms: 1.02x faster                                                  |
| tornado_http               | 98.1 ms                                                | 96.7 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| deepcopy                   | 365 us                                                 | 362 us: 1.01x faster                                                   |
| float                      | 78.9 ms                                                | 78.4 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 240 us: 1.01x faster                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.25 us: 1.01x slower                                                  |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                   |
| scimark_fft                | 345 ms                                                 | 349 ms: 1.01x slower                                                   |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.02x slower                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.58 sec: 1.02x slower                                                 |
| pprint_safe_repr           | 747 ms                                                 | 762 ms: 1.02x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.32 us: 1.02x slower                                                  |
| mdp                        | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                 |
| hexiom                     | 6.89 ms                                                | 7.04 ms: 1.02x slower                                                  |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                                  |
| regex_compile              | 141 ms                                                 | 145 ms: 1.03x slower                                                   |
| bench_thread_pool          | 834 us                                                 | 856 us: 1.03x slower                                                   |
| sympy_expand               | 484 ms                                                 | 498 ms: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                   |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                   |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                                  |
| meteor_contest             | 109 ms                                                 | 113 ms: 1.03x slower                                                   |
| nqueens                    | 87.9 ms                                                | 90.9 ms: 1.03x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 22.2 ms: 1.03x slower                                                  |
| pycparser                  | 1.19 sec                                               | 1.23 sec: 1.04x slower                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 57.4 ms: 1.04x slower                                                  |
| thrift                     | 784 us                                                 | 820 us: 1.05x slower                                                   |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                                   |
| go                         | 149 ms                                                 | 157 ms: 1.05x slower                                                   |
| html5lib                   | 64.8 ms                                                | 68.5 ms: 1.06x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                  |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.06x slower                                                   |
| chameleon                  | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                  |
| pickle                     | 11.0 us                                                | 11.8 us: 1.08x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.08x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 87.7 ms: 1.08x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                  |
| pyflate                    | 434 ms                                                 | 471 ms: 1.09x slower                                                   |
| pidigits                   | 194 ms                                                 | 211 ms: 1.09x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 70.2 ms: 1.09x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.94 sec: 1.10x slower                                                 |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                   |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                                  |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 26.0 ms: 1.14x slower                                                  |
| mypy2                      | 686 ms                                                 | 786 ms: 1.15x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 134 ms: 1.15x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.28 us: 1.15x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.22x slower                                                  |
| async_generators           | 374 ms                                                 | 459 ms: 1.23x slower                                                   |
| coverage                   | 78.8 ms                                                | 98.3 ms: 1.25x slower                                                  |
| telco                      | 6.86 ms                                                | 8.68 ms: 1.27x slower                                                  |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 9.51 ms: 1.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (5): sympy_sum, bench_mp_pool, sympy_str, genshi_xml, json
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 75.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x