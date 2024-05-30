# Results vs. 3.11.0

- fork: faster-cpython
- ref: deferred_rc_overhead
- machine: linux-x86_64
- commit hash: e12729e
- commit date: 2024-05-30
- overall geometric mean: 1.05x faster
- HPT reliability: 79.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 274 ms: 1.04x slower                                                            |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                          |
| html5lib       | 64.8 ms                                                | 66.7 ms: 1.03x slower                                                           |
| tornado_http   | 98.1 ms                                                | 94.3 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 356 ms: 1.38x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                            |
| async_tree_none            | 528 ms                                                 | 389 ms: 1.36x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 951 ms: 1.35x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 973 ms: 1.33x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 622 ms: 1.20x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.4 ms: 1.04x faster                                                           |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| float          | 78.9 ms                                                | 79.6 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                            |
| regex_v8       | 22.9 ms                                                | 24.6 ms: 1.08x slower                                                           |
| regex_effbot   | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                           |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 225 us: 1.08x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.22 sec: 1.04x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 313 us: 1.02x faster                                                            |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                           |
| pickle_dict          | 34.6 us                                                | 35.3 us: 1.02x slower                                                           |
| unpickle_list        | 5.21 us                                                | 5.43 us: 1.04x slower                                                           |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 61.3 ms: 1.08x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                           |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.14 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.6 ms: 1.02x faster                                                           |
| genshi_text     | 22.5 ms                                                | 24.0 ms: 1.06x slower                                                           |
| mako            | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                           |
| django_template | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240530-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-e12729e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 172 us: 3.03x faster                                                            |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.51x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                          |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                            |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.39x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 356 ms: 1.38x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 457 ms: 1.37x faster                                                            |
| async_tree_none            | 528 ms                                                 | 389 ms: 1.36x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 951 ms: 1.35x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 973 ms: 1.33x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 593 ms: 1.28x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 622 ms: 1.20x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.33 ms: 1.18x faster                                                           |
| chaos                      | 71.9 ms                                                | 62.6 ms: 1.15x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.2 ms: 1.14x faster                                                           |
| coroutines                 | 27.0 ms                                                | 23.7 ms: 1.14x faster                                                           |
| raytrace                   | 309 ms                                                 | 274 ms: 1.12x faster                                                            |
| richards_super             | 61.9 ms                                                | 56.2 ms: 1.10x faster                                                           |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.72 ms: 1.08x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 225 us: 1.08x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                           |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                          |
| hexiom                     | 6.89 ms                                                | 6.43 ms: 1.07x faster                                                           |
| sqlglot_parse              | 1.43 ms                                                | 1.35 ms: 1.06x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                           |
| nqueens                    | 87.9 ms                                                | 83.2 ms: 1.06x faster                                                           |
| logging_format             | 6.81 us                                                | 6.47 us: 1.05x faster                                                           |
| sympy_str                  | 297 ms                                                 | 284 ms: 1.05x faster                                                            |
| tornado_http               | 98.1 ms                                                | 94.3 ms: 1.04x faster                                                           |
| nbody                      | 96.0 ms                                                | 92.4 ms: 1.04x faster                                                           |
| sympy_integrate            | 21.5 ms                                                | 20.7 ms: 1.04x faster                                                           |
| tomli_loads                | 2.30 sec                                               | 2.22 sec: 1.04x faster                                                          |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                            |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 313 us: 1.02x faster                                                            |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                          |
| genshi_xml                 | 53.4 ms                                                | 52.6 ms: 1.02x faster                                                           |
| sympy_expand               | 484 ms                                                 | 477 ms: 1.02x faster                                                            |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                           |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                           |
| bench_thread_pool          | 834 us                                                 | 836 us: 1.00x slower                                                            |
| float                      | 78.9 ms                                                | 79.6 ms: 1.01x slower                                                           |
| pprint_pformat             | 1.55 sec                                               | 1.57 sec: 1.01x slower                                                          |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 71.9 ms: 1.02x slower                                                           |
| crypto_pyaes               | 76.7 ms                                                | 78.0 ms: 1.02x slower                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 56.3 ms: 1.02x slower                                                           |
| pickle_dict                | 34.6 us                                                | 35.3 us: 1.02x slower                                                           |
| deepcopy                   | 365 us                                                 | 374 us: 1.02x slower                                                            |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                            |
| html5lib                   | 64.8 ms                                                | 66.7 ms: 1.03x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 66.6 ms: 1.03x slower                                                           |
| scimark_lu                 | 116 ms                                                 | 120 ms: 1.03x slower                                                            |
| deepcopy_memo              | 40.2 us                                                | 41.5 us: 1.03x slower                                                           |
| 2to3                       | 264 ms                                                 | 274 ms: 1.04x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 774 ms: 1.04x slower                                                            |
| thrift                     | 784 us                                                 | 815 us: 1.04x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.43 us: 1.04x slower                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.35 us: 1.04x slower                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.25 ms: 1.04x slower                                                           |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                          |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                           |
| genshi_text                | 22.5 ms                                                | 24.0 ms: 1.06x slower                                                           |
| mako                       | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                           |
| django_template            | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 24.6 ms: 1.08x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 61.3 ms: 1.08x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                           |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                           |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                           |
| scimark_fft                | 345 ms                                                 | 384 ms: 1.11x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.14 us: 1.12x slower                                                           |
| pyflate                    | 434 ms                                                 | 488 ms: 1.13x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.98 us: 1.16x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.08 ms: 1.18x slower                                                           |
| coverage                   | 78.8 ms                                                | 93.6 ms: 1.19x slower                                                           |
| async_generators           | 374 ms                                                 | 452 ms: 1.21x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                           |
| telco                      | 6.86 ms                                                | 8.60 ms: 1.25x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                                    |

Benchmark hidden because not significant (4): xml_etree_iterparse, richards, fannkuch, json
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 79.35% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x