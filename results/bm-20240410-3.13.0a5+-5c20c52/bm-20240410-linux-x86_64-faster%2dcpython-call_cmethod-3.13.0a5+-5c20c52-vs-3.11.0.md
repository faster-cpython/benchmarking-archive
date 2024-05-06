# Results vs. 3.11.0

- fork: faster-cpython
- ref: call_cmethod
- machine: linux-x86_64
- commit hash: 5c20c52
- commit date: 2024-04-10
- overall geometric mean: 1.07x faster
- HPT reliability: 99.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.02x slower                                                     |
| chameleon      | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                    |
| docutils       | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                   |
| html5lib       | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                    |
| tornado_http   | 98.1 ms                                                | 94.8 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                  | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 346 ms: 1.52x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 920 ms: 1.41x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 601 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 606 ms: 1.24x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.5 ms: 1.09x faster                                                    |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.04x faster                                                     |
| regex_effbot   | 3.51 ms                                                | 3.70 ms: 1.06x slower                                                    |
| regex_v8       | 22.9 ms                                                | 24.2 ms: 1.06x slower                                                    |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                  | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                    |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                     |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                     |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                     |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| unpickle_list        | 5.21 us                                                | 5.25 us: 1.01x slower                                                    |
| pickle_dict          | 34.6 us                                                | 34.9 us: 1.01x slower                                                    |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                    |
| xml_etree_process    | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                    |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                    |
| xml_etree_generate   | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                    |
| pickle_list          | 4.59 us                                                | 5.07 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                    |
| python_startup_no_site | 6.01 ms                                                | 8.95 ms: 1.49x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 52.9 ms: 1.01x faster                                                    |
| mako           | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                    |
| genshi_text    | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.45x faster                                                     |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                    |
| asyncio_tcp                | 875 ms                                                 | 498 ms: 1.76x faster                                                     |
| pylint                     | 476 ms                                                 | 279 ms: 1.71x faster                                                     |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                   |
| async_tree_none            | 528 ms                                                 | 346 ms: 1.52x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                     |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 920 ms: 1.41x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                     |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 601 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 606 ms: 1.24x faster                                                     |
| deltablue                  | 3.92 ms                                                | 3.19 ms: 1.23x faster                                                    |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                    |
| chaos                      | 71.9 ms                                                | 60.6 ms: 1.19x faster                                                    |
| raytrace                   | 309 ms                                                 | 262 ms: 1.18x faster                                                     |
| richards_super             | 61.9 ms                                                | 52.9 ms: 1.17x faster                                                    |
| hexiom                     | 6.89 ms                                                | 6.18 ms: 1.11x faster                                                    |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                    |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                     |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                    |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                     |
| nqueens                    | 87.9 ms                                                | 80.9 ms: 1.09x faster                                                    |
| nbody                      | 96.0 ms                                                | 88.5 ms: 1.09x faster                                                    |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                     |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                   |
| logging_format             | 6.81 us                                                | 6.39 us: 1.07x faster                                                    |
| go                         | 149 ms                                                 | 140 ms: 1.06x faster                                                     |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                     |
| logging_simple             | 6.22 us                                                | 5.85 us: 1.06x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                     |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 3.79 ms: 1.06x faster                                                    |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 67.4 ms: 1.05x faster                                                    |
| regex_compile              | 141 ms                                                 | 135 ms: 1.04x faster                                                     |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                    |
| fannkuch                   | 405 ms                                                 | 389 ms: 1.04x faster                                                     |
| tornado_http               | 98.1 ms                                                | 94.8 ms: 1.03x faster                                                    |
| scimark_lu                 | 116 ms                                                 | 113 ms: 1.03x faster                                                     |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                                    |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.03x faster                                                     |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                     |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                     |
| deepcopy                   | 365 us                                                 | 359 us: 1.02x faster                                                     |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                     |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.01x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| genshi_xml                 | 53.4 ms                                                | 52.9 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 55.2 ms: 1.00x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.77 sec: 1.00x faster                                                   |
| unpickle_list              | 5.21 us                                                | 5.25 us: 1.01x slower                                                    |
| pickle_dict                | 34.6 us                                                | 34.9 us: 1.01x slower                                                    |
| dask                       | 365 ms                                                 | 369 ms: 1.01x slower                                                     |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                    |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                                     |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                                     |
| json                       | 5.24 ms                                                | 5.36 ms: 1.02x slower                                                    |
| 2to3                       | 264 ms                                                 | 271 ms: 1.02x slower                                                     |
| pathlib                    | 18.5 ms                                                | 19.0 ms: 1.03x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                     |
| dulwich_log                | 64.6 ms                                                | 66.9 ms: 1.03x slower                                                    |
| thrift                     | 784 us                                                 | 815 us: 1.04x slower                                                     |
| scimark_fft                | 345 ms                                                 | 360 ms: 1.04x slower                                                     |
| html5lib                   | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                    |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                    |
| chameleon                  | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.30 ms: 1.05x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.70 ms: 1.06x slower                                                    |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 24.2 ms: 1.06x slower                                                    |
| genshi_text                | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                    |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                    |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                                     |
| docutils                   | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                   |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                     |
| xml_etree_process          | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                    |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                     |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                    |
| pyflate                    | 434 ms                                                 | 476 ms: 1.10x slower                                                     |
| pickle_list                | 4.59 us                                                | 5.07 us: 1.11x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                    |
| async_generators           | 374 ms                                                 | 445 ms: 1.19x slower                                                     |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                    |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                    |
| coverage                   | 78.8 ms                                                | 96.8 ms: 1.23x slower                                                    |
| telco                      | 6.86 ms                                                | 8.70 ms: 1.27x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 8.95 ms: 1.49x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                             |

Benchmark hidden because not significant (4): float, bench_thread_pool, crypto_pyaes, pprint_safe_repr
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x