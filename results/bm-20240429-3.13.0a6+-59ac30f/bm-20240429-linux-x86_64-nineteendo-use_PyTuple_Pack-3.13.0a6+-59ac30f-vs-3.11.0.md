# Results vs. 3.11.0

- fork: nineteendo
- ref: use_PyTuple_Pack
- machine: linux-x86_64
- commit hash: 59ac30f
- commit date: 2024-04-29
- overall geometric mean: 1.07x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 267 ms: 1.01x slower                                                   |
| chameleon      | 6.70 ms                                                | 6.98 ms: 1.04x slower                                                  |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                 |
| html5lib       | 64.8 ms                                                | 67.4 ms: 1.04x slower                                                  |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 349 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 332 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 436 ms: 1.44x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 898 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 933 ms: 1.39x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                  |
| float          | 78.9 ms                                                | 77.7 ms: 1.02x faster                                                  |
| pidigits       | 194 ms                                                 | 212 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                  |
| regex_dna      | 205 ms                                                 | 218 ms: 1.06x slower                                                   |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 215 us: 1.13x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                   |
| json_loads           | 29.2 us                                                | 27.4 us: 1.06x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.38 us: 1.03x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                  |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.02 us: 1.09x slower                                                  |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.1 ms: 1.05x faster                                                  |
| mako            | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                  |
| django_template | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                  |
| genshi_text     | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                   |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                 |
| async_tree_none            | 528 ms                                                 | 349 ms: 1.51x faster                                                   |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 332 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 436 ms: 1.44x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 898 ms: 1.43x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 933 ms: 1.39x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.19 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                   |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.21x faster                                                  |
| chaos                      | 71.9 ms                                                | 60.1 ms: 1.20x faster                                                  |
| raytrace                   | 309 ms                                                 | 259 ms: 1.19x faster                                                   |
| richards_super             | 61.9 ms                                                | 53.1 ms: 1.16x faster                                                  |
| logging_silent             | 111 ns                                                 | 97.2 ns: 1.14x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.27 ms: 1.13x faster                                                  |
| unpickle_pure_python       | 242 us                                                 | 215 us: 1.13x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.15 ms: 1.12x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.57 ms: 1.11x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                   |
| nbody                      | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                  |
| nqueens                    | 87.9 ms                                                | 80.7 ms: 1.09x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 37.2 us: 1.08x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.57 sec: 1.08x faster                                                 |
| sympy_str                  | 297 ms                                                 | 277 ms: 1.07x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                 |
| richards                   | 49.8 ms                                                | 46.6 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.84 us: 1.07x faster                                                  |
| json_loads                 | 29.2 us                                                | 27.4 us: 1.06x faster                                                  |
| djangocms                  | 33.5 us                                                | 31.5 us: 1.06x faster                                                  |
| sympy_integrate            | 21.5 ms                                                | 20.2 ms: 1.06x faster                                                  |
| pathlib                    | 18.5 ms                                                | 17.5 ms: 1.06x faster                                                  |
| go                         | 149 ms                                                 | 141 ms: 1.06x faster                                                   |
| logging_format             | 6.81 us                                                | 6.46 us: 1.05x faster                                                  |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                   |
| genshi_xml                 | 53.4 ms                                                | 51.1 ms: 1.05x faster                                                  |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.14 sec: 1.04x faster                                                 |
| fannkuch                   | 405 ms                                                 | 390 ms: 1.04x faster                                                   |
| sympy_expand               | 484 ms                                                 | 467 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.50 sec: 1.04x faster                                                 |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.04x faster                                                   |
| deepcopy                   | 365 us                                                 | 353 us: 1.04x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 69.4 ms: 1.02x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 75.4 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 54.4 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 735 ms: 1.02x faster                                                   |
| float                      | 78.9 ms                                                | 77.7 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.17 us: 1.01x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                   |
| json                       | 5.24 ms                                                | 5.18 ms: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| bench_thread_pool          | 834 us                                                 | 831 us: 1.00x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 4.02 ms: 1.00x slower                                                  |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                  |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.00x slower                                                   |
| 2to3                       | 264 ms                                                 | 267 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.12 ms: 1.02x slower                                                  |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 66.3 ms: 1.03x slower                                                  |
| django_template            | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                  |
| unpickle_list              | 5.21 us                                                | 5.38 us: 1.03x slower                                                  |
| html5lib                   | 64.8 ms                                                | 67.4 ms: 1.04x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.98 ms: 1.04x slower                                                  |
| genshi_text                | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                  |
| thrift                     | 784 us                                                 | 821 us: 1.05x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                 |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                  |
| scimark_fft                | 345 ms                                                 | 365 ms: 1.06x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                  |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                  |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.06x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                  |
| mypy2                      | 686 ms                                                 | 733 ms: 1.07x slower                                                   |
| pyflate                    | 434 ms                                                 | 466 ms: 1.08x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                  |
| pidigits                   | 194 ms                                                 | 212 ms: 1.09x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.09x slower                                                  |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                  |
| coverage                   | 78.8 ms                                                | 91.6 ms: 1.16x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                  |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                  |
| telco                      | 6.86 ms                                                | 8.45 ms: 1.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (4): scimark_lu, pickle_dict, spectral_norm, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x