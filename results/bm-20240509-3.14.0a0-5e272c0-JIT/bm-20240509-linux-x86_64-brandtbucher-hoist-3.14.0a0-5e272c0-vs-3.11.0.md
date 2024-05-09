# Results vs. 3.11.0

- fork: brandtbucher
- ref: hoist
- machine: linux-x86_64
- commit hash: 5e272c0
- commit date: 2024-05-09
- overall geometric mean: 1.02x faster
- HPT reliability: 88.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                         |
| chameleon      | 6.70 ms                                                | 7.17 ms: 1.07x slower                                        |
| docutils       | 2.66 sec                                               | 2.97 sec: 1.12x slower                                       |
| html5lib       | 64.8 ms                                                | 69.2 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                  | 1.06x slower                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 368 ms: 1.43x faster                                         |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 455 ms: 1.38x faster                                         |
| async_tree_io              | 1.29 sec                                               | 936 ms: 1.37x faster                                         |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                         |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 623 ms: 1.20x faster                                         |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.0 ms: 1.19x faster                                        |
| float          | 78.9 ms                                                | 71.3 ms: 1.11x faster                                        |
| pidigits       | 194 ms                                                 | 197 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                  | 1.09x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.01x faster                                         |
| regex_dna      | 205 ms                                                 | 220 ms: 1.08x slower                                         |
| regex_effbot   | 3.51 ms                                                | 3.82 ms: 1.09x slower                                        |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                        |
| Geometric mean | (ref)                                                  | 1.06x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.29x faster                                        |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                       |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                         |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.09x faster                                         |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                         |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                         |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                        |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                        |
| unpickle_list        | 5.21 us                                                | 5.25 us: 1.01x slower                                        |
| xml_etree_process    | 56.9 ms                                                | 58.4 ms: 1.03x slower                                        |
| xml_etree_generate   | 81.1 ms                                                | 83.4 ms: 1.03x slower                                        |
| pickle               | 11.0 us                                                | 12.2 us: 1.11x slower                                        |
| unpickle             | 13.8 us                                                | 16.0 us: 1.15x slower                                        |
| pickle_list          | 4.59 us                                                | 5.47 us: 1.19x slower                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.65 ms: 1.27x slower                                        |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                        |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.53 ms: 1.12x faster                                        |
| genshi_xml      | 53.4 ms                                                | 57.4 ms: 1.07x slower                                        |
| django_template | 33.5 ms                                                | 36.6 ms: 1.09x slower                                        |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                        |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 176 us: 2.96x faster                                         |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.50x faster                                        |
| asyncio_tcp                | 875 ms                                                 | 521 ms: 1.68x faster                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                       |
| async_tree_none            | 528 ms                                                 | 368 ms: 1.43x faster                                         |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                        |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 455 ms: 1.38x faster                                         |
| async_tree_io              | 1.29 sec                                               | 936 ms: 1.37x faster                                         |
| pylint                     | 476 ms                                                 | 357 ms: 1.33x faster                                         |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                         |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.29x faster                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                         |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                       |
| richards_super             | 61.9 ms                                                | 48.7 ms: 1.27x faster                                        |
| chaos                      | 71.9 ms                                                | 58.4 ms: 1.23x faster                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 623 ms: 1.20x faster                                         |
| nbody                      | 96.0 ms                                                | 81.0 ms: 1.19x faster                                        |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                       |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                        |
| richards                   | 49.8 ms                                                | 42.6 ms: 1.17x faster                                        |
| raytrace                   | 309 ms                                                 | 274 ms: 1.13x faster                                         |
| mako                       | 10.7 ms                                                | 9.53 ms: 1.12x faster                                        |
| fannkuch                   | 405 ms                                                 | 365 ms: 1.11x faster                                         |
| float                      | 78.9 ms                                                | 71.3 ms: 1.11x faster                                        |
| crypto_pyaes               | 76.7 ms                                                | 69.4 ms: 1.11x faster                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.56 ms: 1.10x faster                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 64.5 ms: 1.10x faster                                        |
| spectral_norm              | 108 ms                                                 | 99.0 ms: 1.09x faster                                        |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                        |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.09x faster                                         |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                        |
| deepcopy_memo              | 40.2 us                                                | 37.5 us: 1.07x faster                                        |
| scimark_fft                | 345 ms                                                 | 323 ms: 1.07x faster                                         |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                        |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                         |
| logging_format             | 6.81 us                                                | 6.48 us: 1.05x faster                                        |
| deltablue                  | 3.92 ms                                                | 3.74 ms: 1.05x faster                                        |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                         |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                        |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                       |
| pprint_safe_repr           | 747 ms                                                 | 730 ms: 1.02x faster                                         |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                         |
| regex_compile              | 141 ms                                                 | 139 ms: 1.01x faster                                         |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                        |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                        |
| hexiom                     | 6.89 ms                                                | 6.85 ms: 1.01x faster                                        |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                         |
| unpickle_list              | 5.21 us                                                | 5.25 us: 1.01x slower                                        |
| deepcopy                   | 365 us                                                 | 369 us: 1.01x slower                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.26 us: 1.01x slower                                        |
| mdp                        | 2.77 sec                                               | 2.81 sec: 1.01x slower                                       |
| pidigits                   | 194 ms                                                 | 197 ms: 1.01x slower                                         |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.02x slower                                         |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.02x slower                                       |
| sympy_str                  | 297 ms                                                 | 304 ms: 1.02x slower                                         |
| pyflate                    | 434 ms                                                 | 444 ms: 1.02x slower                                         |
| xml_etree_process          | 56.9 ms                                                | 58.4 ms: 1.03x slower                                        |
| xml_etree_generate         | 81.1 ms                                                | 83.4 ms: 1.03x slower                                        |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                         |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                        |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                         |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                         |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                         |
| bench_thread_pool          | 834 us                                                 | 869 us: 1.04x slower                                         |
| sympy_expand               | 484 ms                                                 | 507 ms: 1.05x slower                                         |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                         |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                         |
| sympy_integrate            | 21.5 ms                                                | 22.8 ms: 1.06x slower                                        |
| html5lib                   | 64.8 ms                                                | 69.2 ms: 1.07x slower                                        |
| chameleon                  | 6.70 ms                                                | 7.17 ms: 1.07x slower                                        |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.07x slower                                         |
| genshi_xml                 | 53.4 ms                                                | 57.4 ms: 1.07x slower                                        |
| regex_dna                  | 205 ms                                                 | 220 ms: 1.08x slower                                         |
| regex_effbot               | 3.51 ms                                                | 3.82 ms: 1.09x slower                                        |
| django_template            | 33.5 ms                                                | 36.6 ms: 1.09x slower                                        |
| dulwich_log                | 64.6 ms                                                | 70.5 ms: 1.09x slower                                        |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                        |
| coverage                   | 78.8 ms                                                | 87.1 ms: 1.11x slower                                        |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                        |
| pickle                     | 11.0 us                                                | 12.2 us: 1.11x slower                                        |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                        |
| docutils                   | 2.66 sec                                               | 2.97 sec: 1.12x slower                                       |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.13x slower                                        |
| gunicorn                   | 1.20 ms                                                | 1.36 ms: 1.13x slower                                        |
| unpickle                   | 13.8 us                                                | 16.0 us: 1.15x slower                                        |
| pickle_list                | 4.59 us                                                | 5.47 us: 1.19x slower                                        |
| async_generators           | 374 ms                                                 | 472 ms: 1.26x slower                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                        |
| python_startup_no_site     | 6.01 ms                                                | 7.65 ms: 1.27x slower                                        |
| flaskblogging              | 7.28 ms                                                | 9.32 ms: 1.28x slower                                        |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                        |
| telco                      | 6.86 ms                                                | 173 ms: 25.19x slower                                        |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (5): nqueens, tornado_http, bench_mp_pool, gc_traversal, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: djangocms, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 88.09% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x