# Results vs. 3.11.0

- fork: python
- ref: ab6eda0ee59587e84cb4
- machine: linux-x86_64
- commit hash: ab6eda0
- commit date: 2024-04-29
- overall geometric mean: 1.18x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 361 ms: 1.36x slower                                                   |
| chameleon      | 6.70 ms                                                | 8.68 ms: 1.30x slower                                                  |
| docutils       | 2.66 sec                                               | 3.37 sec: 1.27x slower                                                 |
| html5lib       | 64.8 ms                                                | 79.8 ms: 1.23x slower                                                  |
| tornado_http   | 98.1 ms                                                | 105 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 393 ms: 1.34x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 366 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 476 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 999 ms: 1.30x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 526 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 636 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 651 ms: 1.15x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                   |
| float          | 78.9 ms                                                | 122 ms: 1.55x slower                                                   |
| nbody          | 96.0 ms                                                | 198 ms: 2.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                  |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                  |
| regex_compile  | 141 ms                                                 | 220 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.09x faster                                                   |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| unpickle_list        | 5.21 us                                                | 5.13 us: 1.02x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 318 us: 1.01x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.3 us: 1.02x slower                                                  |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| unpickle             | 13.8 us                                                | 15.3 us: 1.10x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.11 us: 1.11x slower                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 126 ms: 1.17x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 104 ms: 1.28x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 74.1 ms: 1.30x slower                                                  |
| tomli_loads          | 2.30 sec                                               | 3.38 sec: 1.47x slower                                                 |
| unpickle_pure_python | 242 us                                                 | 396 us: 1.64x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.19 ms: 1.20x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 47.3 ms: 1.41x slower                                                  |
| genshi_xml      | 53.4 ms                                                | 80.6 ms: 1.51x slower                                                  |
| genshi_text     | 22.5 ms                                                | 39.3 ms: 1.74x slower                                                  |
| mako            | 10.7 ms                                                | 20.3 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.63x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 217 us: 2.39x faster                                                   |
| generators                 | 74.9 ms                                                | 31.8 ms: 2.35x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.88 sec: 1.66x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 530 ms: 1.65x faster                                                   |
| async_tree_none            | 528 ms                                                 | 393 ms: 1.34x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 366 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 476 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 999 ms: 1.30x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                  |
| pylint                     | 476 ms                                                 | 387 ms: 1.23x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 526 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 636 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 651 ms: 1.15x faster                                                   |
| coroutines                 | 27.0 ms                                                | 24.5 ms: 1.10x faster                                                  |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.09x faster                                                   |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                  |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.93 ms: 1.02x faster                                                  |
| unpickle_list              | 5.21 us                                                | 5.13 us: 1.02x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 318 us: 1.01x faster                                                   |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                   |
| pickle_dict                | 34.6 us                                                | 35.3 us: 1.02x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                   |
| pathlib                    | 18.5 ms                                                | 19.2 ms: 1.03x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.34 us: 1.04x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                  |
| tornado_http               | 98.1 ms                                                | 105 ms: 1.08x slower                                                   |
| dask                       | 365 ms                                                 | 397 ms: 1.09x slower                                                   |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                  |
| thrift                     | 784 us                                                 | 854 us: 1.09x slower                                                   |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                   |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.10x slower                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.94 ms: 1.11x slower                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.59 ms: 1.11x slower                                                  |
| pickle_list                | 4.59 us                                                | 5.11 us: 1.11x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 25.6 ms: 1.12x slower                                                  |
| deepcopy                   | 365 us                                                 | 409 us: 1.12x slower                                                   |
| mdp                        | 2.77 sec                                               | 3.13 sec: 1.13x slower                                                 |
| pycparser                  | 1.19 sec                                               | 1.34 sec: 1.13x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 192 ms: 1.13x slower                                                   |
| logging_simple             | 6.22 us                                                | 7.08 us: 1.14x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.37 ms: 1.15x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.28 ms: 1.15x slower                                                  |
| logging_format             | 6.81 us                                                | 7.88 us: 1.16x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 973 us: 1.17x slower                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 126 ms: 1.17x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.19 ms: 1.20x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 77.4 ms: 1.20x slower                                                  |
| sympy_expand               | 484 ms                                                 | 585 ms: 1.21x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 3.11 us: 1.21x slower                                                  |
| sympy_str                  | 297 ms                                                 | 360 ms: 1.21x slower                                                   |
| raytrace                   | 309 ms                                                 | 376 ms: 1.22x slower                                                   |
| html5lib                   | 64.8 ms                                                | 79.8 ms: 1.23x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                  |
| deepcopy_memo              | 40.2 us                                                | 50.1 us: 1.25x slower                                                  |
| sqlglot_normalize          | 113 ms                                                 | 142 ms: 1.26x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.81 ms: 1.26x slower                                                  |
| docutils                   | 2.66 sec                                               | 3.37 sec: 1.27x slower                                                 |
| richards_super             | 61.9 ms                                                | 78.6 ms: 1.27x slower                                                  |
| mypy2                      | 686 ms                                                 | 874 ms: 1.28x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 104 ms: 1.28x slower                                                   |
| sympy_integrate            | 21.5 ms                                                | 27.7 ms: 1.29x slower                                                  |
| chameleon                  | 6.70 ms                                                | 8.68 ms: 1.30x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 74.1 ms: 1.30x slower                                                  |
| meteor_contest             | 109 ms                                                 | 143 ms: 1.31x slower                                                   |
| async_generators           | 374 ms                                                 | 496 ms: 1.33x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 73.5 ms: 1.33x slower                                                  |
| 2to3                       | 264 ms                                                 | 361 ms: 1.36x slower                                                   |
| deltablue                  | 3.92 ms                                                | 5.41 ms: 1.38x slower                                                  |
| telco                      | 6.86 ms                                                | 9.64 ms: 1.41x slower                                                  |
| django_template            | 33.5 ms                                                | 47.3 ms: 1.41x slower                                                  |
| chaos                      | 71.9 ms                                                | 103 ms: 1.44x slower                                                   |
| richards                   | 49.8 ms                                                | 71.6 ms: 1.44x slower                                                  |
| scimark_sor                | 121 ms                                                 | 178 ms: 1.46x slower                                                   |
| tomli_loads                | 2.30 sec                                               | 3.38 sec: 1.47x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 80.6 ms: 1.51x slower                                                  |
| float                      | 78.9 ms                                                | 122 ms: 1.55x slower                                                   |
| regex_compile              | 141 ms                                                 | 220 ms: 1.56x slower                                                   |
| comprehensions             | 23.6 us                                                | 37.2 us: 1.58x slower                                                  |
| crypto_pyaes               | 76.7 ms                                                | 122 ms: 1.59x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 396 us: 1.64x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 8.26 ms: 1.64x slower                                                  |
| pprint_pformat             | 1.55 sec                                               | 2.65 sec: 1.71x slower                                                 |
| fannkuch                   | 405 ms                                                 | 693 ms: 1.71x slower                                                   |
| nqueens                    | 87.9 ms                                                | 151 ms: 1.72x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 1.28 sec: 1.72x slower                                                 |
| scimark_fft                | 345 ms                                                 | 596 ms: 1.73x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 201 ms: 1.73x slower                                                   |
| genshi_text                | 22.5 ms                                                | 39.3 ms: 1.74x slower                                                  |
| go                         | 149 ms                                                 | 260 ms: 1.75x slower                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 134 ms: 1.89x slower                                                   |
| mako                       | 10.7 ms                                                | 20.3 ms: 1.91x slower                                                  |
| pyflate                    | 434 ms                                                 | 828 ms: 1.91x slower                                                   |
| spectral_norm              | 108 ms                                                 | 211 ms: 1.95x slower                                                   |
| nbody                      | 96.0 ms                                                | 198 ms: 2.07x slower                                                   |
| hexiom                     | 6.89 ms                                                | 15.0 ms: 2.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (3): djangocms, json, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.03x