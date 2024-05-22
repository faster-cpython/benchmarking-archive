# Results vs. 3.11.0

- fork: brandtbucher
- ref: unbox_floats
- machine: linux-x86_64
- commit hash: 994a9dc
- commit date: 2024-05-22
- overall geometric mean: 1.06x faster
- HPT reliability: 93.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                |
| chameleon      | 6.70 ms                                                | 7.13 ms: 1.06x slower                                               |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                              |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                               |
| tornado_http   | 98.1 ms                                                | 96.8 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.41x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                |
| async_tree_io              | 1.29 sec                                               | 977 ms: 1.32x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 619 ms: 1.21x faster                                                |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 78.9 ms                                                | 76.0 ms: 1.04x faster                                               |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                |
| nbody          | 96.0 ms                                                | 110 ms: 1.14x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.02x faster                                                |
| regex_effbot   | 3.51 ms                                                | 3.80 ms: 1.08x slower                                               |
| regex_v8       | 22.9 ms                                                | 25.3 ms: 1.10x slower                                               |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                |
| Geometric mean | (ref)                                                  | 1.07x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                               |
| tomli_loads          | 2.30 sec                                               | 1.93 sec: 1.19x faster                                              |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                |
| pickle_pure_python   | 320 us                                                 | 298 us: 1.07x faster                                                |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                |
| unpickle_list        | 5.21 us                                                | 5.18 us: 1.01x faster                                               |
| json_loads           | 29.2 us                                                | 29.1 us: 1.00x faster                                               |
| pickle_dict          | 34.6 us                                                | 35.0 us: 1.01x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 83.1 ms: 1.03x slower                                               |
| xml_etree_process    | 56.9 ms                                                | 58.4 ms: 1.03x slower                                               |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                               |
| pickle_list          | 4.59 us                                                | 5.23 us: 1.14x slower                                               |
| unpickle             | 13.8 us                                                | 15.8 us: 1.14x slower                                               |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.61 ms: 1.27x slower                                               |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.28x slower                                               |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.92 ms: 1.07x faster                                               |
| genshi_xml      | 53.4 ms                                                | 57.8 ms: 1.08x slower                                               |
| django_template | 33.5 ms                                                | 36.4 ms: 1.08x slower                                               |
| genshi_text     | 22.5 ms                                                | 25.2 ms: 1.12x slower                                               |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-unbox_floats-3.14.0a0-994a9dc |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 174 us: 2.99x faster                                                |
| generators                 | 74.9 ms                                                | 30.8 ms: 2.43x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 520 ms: 1.68x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                               |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.41x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                |
| pylint                     | 476 ms                                                 | 354 ms: 1.34x faster                                                |
| async_tree_io              | 1.29 sec                                               | 977 ms: 1.32x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                |
| richards_super             | 61.9 ms                                                | 48.2 ms: 1.28x faster                                               |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 619 ms: 1.21x faster                                                |
| tomli_loads                | 2.30 sec                                               | 1.93 sec: 1.19x faster                                              |
| richards                   | 49.8 ms                                                | 42.0 ms: 1.18x faster                                               |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                               |
| fannkuch                   | 405 ms                                                 | 351 ms: 1.16x faster                                                |
| chaos                      | 71.9 ms                                                | 63.2 ms: 1.14x faster                                               |
| crypto_pyaes               | 76.7 ms                                                | 68.0 ms: 1.13x faster                                               |
| pathlib                    | 18.5 ms                                                | 16.7 ms: 1.11x faster                                               |
| scimark_monte_carlo        | 70.7 ms                                                | 63.7 ms: 1.11x faster                                               |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                               |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                |
| raytrace                   | 309 ms                                                 | 284 ms: 1.08x faster                                                |
| logging_simple             | 6.22 us                                                | 5.78 us: 1.08x faster                                               |
| mako                       | 10.7 ms                                                | 9.92 ms: 1.07x faster                                               |
| pickle_pure_python         | 320 us                                                 | 298 us: 1.07x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                |
| logging_format             | 6.81 us                                                | 6.36 us: 1.07x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                               |
| mdp                        | 2.77 sec                                               | 2.60 sec: 1.07x faster                                              |
| deepcopy_memo              | 40.2 us                                                | 37.8 us: 1.06x faster                                               |
| pprint_pformat             | 1.55 sec                                               | 1.47 sec: 1.06x faster                                              |
| deltablue                  | 3.92 ms                                                | 3.72 ms: 1.05x faster                                               |
| pprint_safe_repr           | 747 ms                                                 | 714 ms: 1.05x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.80 ms: 1.05x faster                                               |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                |
| hexiom                     | 6.89 ms                                                | 6.62 ms: 1.04x faster                                               |
| float                      | 78.9 ms                                                | 76.0 ms: 1.04x faster                                               |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                |
| spectral_norm              | 108 ms                                                 | 106 ms: 1.02x faster                                                |
| regex_compile              | 141 ms                                                 | 139 ms: 1.02x faster                                                |
| tornado_http               | 98.1 ms                                                | 96.8 ms: 1.01x faster                                               |
| nqueens                    | 87.9 ms                                                | 87.0 ms: 1.01x faster                                               |
| unpickle_list              | 5.21 us                                                | 5.18 us: 1.01x faster                                               |
| json_loads                 | 29.2 us                                                | 29.1 us: 1.00x faster                                               |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                |
| go                         | 149 ms                                                 | 149 ms: 1.01x slower                                                |
| deepcopy                   | 365 us                                                 | 369 us: 1.01x slower                                                |
| pickle_dict                | 34.6 us                                                | 35.0 us: 1.01x slower                                               |
| pyflate                    | 434 ms                                                 | 439 ms: 1.01x slower                                                |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.01x slower                                              |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.01x slower                                                |
| gc_traversal               | 4.01 ms                                                | 4.08 ms: 1.02x slower                                               |
| sympy_sum                  | 169 ms                                                 | 173 ms: 1.02x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 56.7 ms: 1.03x slower                                               |
| xml_etree_generate         | 81.1 ms                                                | 83.1 ms: 1.03x slower                                               |
| xml_etree_process          | 56.9 ms                                                | 58.4 ms: 1.03x slower                                               |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                               |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                |
| dask                       | 365 ms                                                 | 378 ms: 1.04x slower                                                |
| bench_thread_pool          | 834 us                                                 | 866 us: 1.04x slower                                                |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                               |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                               |
| sympy_expand               | 484 ms                                                 | 511 ms: 1.05x slower                                                |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.13 ms: 1.06x slower                                               |
| dulwich_log                | 64.6 ms                                                | 68.9 ms: 1.07x slower                                               |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.08x slower                                                |
| genshi_xml                 | 53.4 ms                                                | 57.8 ms: 1.08x slower                                               |
| regex_effbot               | 3.51 ms                                                | 3.80 ms: 1.08x slower                                               |
| django_template            | 33.5 ms                                                | 36.4 ms: 1.08x slower                                               |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                               |
| regex_v8                   | 22.9 ms                                                | 25.3 ms: 1.10x slower                                               |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                              |
| genshi_text                | 22.5 ms                                                | 25.2 ms: 1.12x slower                                               |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.91 us: 1.13x slower                                               |
| pickle_list                | 4.59 us                                                | 5.23 us: 1.14x slower                                               |
| unpickle                   | 13.8 us                                                | 15.8 us: 1.14x slower                                               |
| nbody                      | 96.0 ms                                                | 110 ms: 1.14x slower                                                |
| telco                      | 6.86 ms                                                | 8.23 ms: 1.20x slower                                               |
| coverage                   | 78.8 ms                                                | 94.8 ms: 1.20x slower                                               |
| async_generators           | 374 ms                                                 | 467 ms: 1.25x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                               |
| python_startup_no_site     | 6.01 ms                                                | 7.61 ms: 1.27x slower                                               |
| flaskblogging              | 7.28 ms                                                | 9.28 ms: 1.27x slower                                               |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.28x slower                                               |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                        |

Benchmark hidden because not significant (3): sqlglot_normalize, scimark_fft, bench_mp_pool
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, json, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, thrift, unpack_sequence

# HPT report

- Reliability score: 93.15% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x