# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.04x faster
- HPT reliability: 51.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 282 ms: 1.07x slower                                                     |
| chameleon      | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                    |
| docutils       | 2.66 sec                                               | 2.94 sec: 1.10x slower                                                   |
| html5lib       | 64.8 ms                                                | 67.6 ms: 1.04x slower                                                    |
| tornado_http   | 98.1 ms                                                | 96.5 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 907 ms: 1.43x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 348 ms: 1.41x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 458 ms: 1.40x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 597 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.4 ms: 1.04x faster                                                    |
| float          | 78.9 ms                                                | 77.0 ms: 1.03x faster                                                    |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 149 ms: 1.06x slower                                                     |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                    |
| regex_v8       | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                    |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.06 sec: 1.12x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 308 us: 1.04x faster                                                     |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                     |
| unpickle_pure_python | 242 us                                                 | 238 us: 1.02x faster                                                     |
| pickle_dict          | 34.6 us                                                | 34.1 us: 1.02x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                    |
| unpickle_list        | 5.21 us                                                | 5.19 us: 1.00x faster                                                    |
| xml_etree_process    | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                    |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                    |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                    |
| pickle_list          | 4.59 us                                                | 4.96 us: 1.08x slower                                                    |
| unpickle             | 13.8 us                                                | 15.0 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                    |
| python_startup_no_site | 6.01 ms                                                | 9.51 ms: 1.58x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                    |
| genshi_xml      | 53.4 ms                                                | 55.7 ms: 1.04x slower                                                    |
| genshi_text     | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                    |
| django_template | 33.5 ms                                                | 37.1 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.58x faster                                                     |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                                    |
| asyncio_tcp                | 875 ms                                                 | 518 ms: 1.69x faster                                                     |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                   |
| pylint                     | 476 ms                                                 | 306 ms: 1.56x faster                                                     |
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 907 ms: 1.43x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 348 ms: 1.41x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 458 ms: 1.40x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 597 ms: 1.28x faster                                                     |
| comprehensions             | 23.6 us                                                | 18.5 us: 1.27x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                     |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.18x faster                                                    |
| richards_super             | 61.9 ms                                                | 53.0 ms: 1.17x faster                                                    |
| deltablue                  | 3.92 ms                                                | 3.48 ms: 1.13x faster                                                    |
| chaos                      | 71.9 ms                                                | 64.1 ms: 1.12x faster                                                    |
| tomli_loads                | 2.30 sec                                               | 2.06 sec: 1.12x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                    |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                     |
| richards                   | 49.8 ms                                                | 46.4 ms: 1.07x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                    |
| logging_simple             | 6.22 us                                                | 5.84 us: 1.07x faster                                                    |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                                    |
| raytrace                   | 309 ms                                                 | 296 ms: 1.04x faster                                                     |
| fannkuch                   | 405 ms                                                 | 390 ms: 1.04x faster                                                     |
| pickle_pure_python         | 320 us                                                 | 308 us: 1.04x faster                                                     |
| nbody                      | 96.0 ms                                                | 92.4 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.87 ms: 1.03x faster                                                    |
| djangocms                  | 33.5 us                                                | 32.5 us: 1.03x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                     |
| float                      | 78.9 ms                                                | 77.0 ms: 1.03x faster                                                    |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                     |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                    |
| crypto_pyaes               | 76.7 ms                                                | 75.3 ms: 1.02x faster                                                    |
| unpickle_pure_python       | 242 us                                                 | 238 us: 1.02x faster                                                     |
| tornado_http               | 98.1 ms                                                | 96.5 ms: 1.02x faster                                                    |
| deepcopy                   | 365 us                                                 | 359 us: 1.02x faster                                                     |
| pickle_dict                | 34.6 us                                                | 34.1 us: 1.02x faster                                                    |
| deepcopy_reduce            | 3.22 us                                                | 3.18 us: 1.01x faster                                                    |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                     |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                    |
| scimark_fft                | 345 ms                                                 | 343 ms: 1.01x faster                                                     |
| unpickle_list              | 5.21 us                                                | 5.19 us: 1.00x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 3.99 ms: 1.00x faster                                                    |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                     |
| mdp                        | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                   |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                     |
| pprint_safe_repr           | 747 ms                                                 | 766 ms: 1.03x slower                                                     |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                    |
| bench_thread_pool          | 834 us                                                 | 859 us: 1.03x slower                                                     |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                     |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                                    |
| sympy_expand               | 484 ms                                                 | 501 ms: 1.03x slower                                                     |
| dask                       | 365 ms                                                 | 378 ms: 1.03x slower                                                     |
| sympy_integrate            | 21.5 ms                                                | 22.3 ms: 1.04x slower                                                    |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                                     |
| genshi_xml                 | 53.4 ms                                                | 55.7 ms: 1.04x slower                                                    |
| html5lib                   | 64.8 ms                                                | 67.6 ms: 1.04x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 58.0 ms: 1.05x slower                                                    |
| xml_etree_process          | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                    |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.05x slower                                                     |
| chameleon                  | 6.70 ms                                                | 7.06 ms: 1.05x slower                                                    |
| regex_compile              | 141 ms                                                 | 149 ms: 1.06x slower                                                     |
| json                       | 5.24 ms                                                | 5.54 ms: 1.06x slower                                                    |
| nqueens                    | 87.9 ms                                                | 93.5 ms: 1.06x slower                                                    |
| hexiom                     | 6.89 ms                                                | 7.33 ms: 1.06x slower                                                    |
| go                         | 149 ms                                                 | 158 ms: 1.06x slower                                                     |
| 2to3                       | 264 ms                                                 | 282 ms: 1.07x slower                                                     |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                    |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                    |
| pickle_list                | 4.59 us                                                | 4.96 us: 1.08x slower                                                    |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                     |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.09x slower                                                    |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                    |
| genshi_text                | 22.5 ms                                                | 24.8 ms: 1.10x slower                                                    |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                                    |
| docutils                   | 2.66 sec                                               | 2.94 sec: 1.10x slower                                                   |
| django_template            | 33.5 ms                                                | 37.1 ms: 1.11x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 71.4 ms: 1.11x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                    |
| scimark_lu                 | 116 ms                                                 | 130 ms: 1.12x slower                                                     |
| pyflate                    | 434 ms                                                 | 491 ms: 1.13x slower                                                     |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.14x slower                                                     |
| create_gc_cycles           | 1.43 ms                                                | 1.68 ms: 1.17x slower                                                    |
| mypy2                      | 686 ms                                                 | 812 ms: 1.18x slower                                                     |
| coverage                   | 78.8 ms                                                | 95.8 ms: 1.22x slower                                                    |
| async_generators           | 374 ms                                                 | 458 ms: 1.23x slower                                                     |
| telco                      | 6.86 ms                                                | 8.71 ms: 1.27x slower                                                    |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 9.51 ms: 1.58x slower                                                    |
| unpack_sequence            | 43.5 ns                                                | 85.6 ns: 1.97x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (4): pprint_pformat, pycparser, bench_mp_pool, scimark_monte_carlo
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 51.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x