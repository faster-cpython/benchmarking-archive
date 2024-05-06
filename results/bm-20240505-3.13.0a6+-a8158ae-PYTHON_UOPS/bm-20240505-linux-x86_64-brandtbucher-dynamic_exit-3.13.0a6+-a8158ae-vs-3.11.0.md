# Results vs. 3.11.0

- fork: brandtbucher
- ref: dynamic_exit
- machine: linux-x86_64
- commit hash: a8158ae
- commit date: 2024-05-05
- overall geometric mean: 1.16x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 357 ms: 1.35x slower                                                 |
| chameleon      | 6.70 ms                                                | 9.02 ms: 1.35x slower                                                |
| html5lib       | 64.8 ms                                                | 83.5 ms: 1.29x slower                                                |
| tornado_http   | 98.1 ms                                                | 108 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.27x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 626 ms                                                 | 481 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 379 ms: 1.29x faster                                                 |
| async_tree_none            | 528 ms                                                 | 411 ms: 1.28x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 1.03 sec: 1.26x faster                                               |
| async_tree_io              | 1.29 sec                                               | 1.05 sec: 1.22x faster                                               |
| async_tree_memoization     | 639 ms                                                 | 532 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 639 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 666 ms: 1.12x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                 |
| float          | 78.9 ms                                                | 92.6 ms: 1.17x slower                                                |
| nbody          | 96.0 ms                                                | 123 ms: 1.28x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                 |
| regex_v8       | 22.9 ms                                                | 27.1 ms: 1.18x slower                                                |
| regex_compile  | 141 ms                                                 | 220 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                  | 1.21x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.5 ms: 1.16x faster                                                |
| xml_etree_parse      | 164 ms                                                 | 154 ms: 1.06x faster                                                 |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                                |
| unpickle_list        | 5.21 us                                                | 5.17 us: 1.01x faster                                                |
| xml_etree_iterparse  | 108 ms                                                 | 111 ms: 1.03x slower                                                 |
| pickle_dict          | 34.6 us                                                | 36.0 us: 1.04x slower                                                |
| pickle_list          | 4.59 us                                                | 5.03 us: 1.10x slower                                                |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                |
| unpickle             | 13.8 us                                                | 15.7 us: 1.14x slower                                                |
| tomli_loads          | 2.30 sec                                               | 2.81 sec: 1.22x slower                                               |
| xml_etree_process    | 56.9 ms                                                | 71.4 ms: 1.25x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 104 ms: 1.28x slower                                                 |
| unpickle_pure_python | 242 us                                                 | 331 us: 1.37x slower                                                 |
| pickle_pure_python   | 320 us                                                 | 525 us: 1.64x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.25 ms: 1.21x slower                                                |
| python_startup         | 8.56 ms                                                | 10.8 ms: 1.26x slower                                                |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 14.2 ms: 1.33x slower                                                |
| django_template | 33.5 ms                                                | 49.2 ms: 1.47x slower                                                |
| genshi_xml      | 53.4 ms                                                | 82.8 ms: 1.55x slower                                                |
| genshi_text     | 22.5 ms                                                | 39.8 ms: 1.77x slower                                                |
| Geometric mean  | (ref)                                                  | 1.52x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240505-linux-x86_64-brandtbucher-dynamic_exit-3.13.0a6+-a8158ae |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 217 us: 2.39x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 526 ms: 1.67x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                               |
| async_tree_memoization_tg  | 626 ms                                                 | 481 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 379 ms: 1.29x faster                                                 |
| async_tree_none            | 528 ms                                                 | 411 ms: 1.28x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 1.03 sec: 1.26x faster                                               |
| async_tree_io              | 1.29 sec                                               | 1.05 sec: 1.22x faster                                               |
| pylint                     | 476 ms                                                 | 396 ms: 1.20x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 532 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 639 ms: 1.19x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 11.5 ms: 1.16x faster                                                |
| generators                 | 74.9 ms                                                | 65.9 ms: 1.14x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 666 ms: 1.12x faster                                                 |
| coroutines                 | 27.0 ms                                                | 24.8 ms: 1.09x faster                                                |
| xml_etree_parse            | 164 ms                                                 | 154 ms: 1.06x faster                                                 |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.88 ms: 1.03x faster                                                |
| unpickle_list              | 5.21 us                                                | 5.17 us: 1.01x faster                                                |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                 |
| pathlib                    | 18.5 ms                                                | 19.0 ms: 1.03x slower                                                |
| xml_etree_iterparse        | 108 ms                                                 | 111 ms: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                 |
| pickle_dict                | 34.6 us                                                | 36.0 us: 1.04x slower                                                |
| mdp                        | 2.77 sec                                               | 2.91 sec: 1.05x slower                                               |
| json                       | 5.24 ms                                                | 5.53 ms: 1.05x slower                                                |
| thrift                     | 784 us                                                 | 832 us: 1.06x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                |
| dask                       | 365 ms                                                 | 395 ms: 1.08x slower                                                 |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.03 us: 1.10x slower                                                |
| tornado_http               | 98.1 ms                                                | 108 ms: 1.10x slower                                                 |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                |
| logging_simple             | 6.22 us                                                | 6.97 us: 1.12x slower                                                |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.14x slower                                                |
| comprehensions             | 23.6 us                                                | 27.1 us: 1.15x slower                                                |
| sympy_sum                  | 169 ms                                                 | 194 ms: 1.15x slower                                                 |
| logging_format             | 6.81 us                                                | 7.83 us: 1.15x slower                                                |
| raytrace                   | 309 ms                                                 | 357 ms: 1.16x slower                                                 |
| aiohttp                    | 1.12 ms                                                | 1.30 ms: 1.17x slower                                                |
| float                      | 78.9 ms                                                | 92.6 ms: 1.17x slower                                                |
| coverage                   | 78.8 ms                                                | 92.4 ms: 1.17x slower                                                |
| gunicorn                   | 1.20 ms                                                | 1.41 ms: 1.17x slower                                                |
| regex_v8                   | 22.9 ms                                                | 27.1 ms: 1.18x slower                                                |
| meteor_contest             | 109 ms                                                 | 129 ms: 1.19x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 991 us: 1.19x slower                                                 |
| deltablue                  | 3.92 ms                                                | 4.67 ms: 1.19x slower                                                |
| fannkuch                   | 405 ms                                                 | 483 ms: 1.19x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 3.10 us: 1.20x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 7.25 ms: 1.21x slower                                                |
| dulwich_log                | 64.6 ms                                                | 77.9 ms: 1.21x slower                                                |
| sympy_integrate            | 21.5 ms                                                | 25.9 ms: 1.21x slower                                                |
| tomli_loads                | 2.30 sec                                               | 2.81 sec: 1.22x slower                                               |
| chaos                      | 71.9 ms                                                | 87.6 ms: 1.22x slower                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.20 ms: 1.23x slower                                                |
| sympy_str                  | 297 ms                                                 | 366 ms: 1.23x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 71.4 ms: 1.25x slower                                                |
| python_startup             | 8.56 ms                                                | 10.8 ms: 1.26x slower                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.81 ms: 1.26x slower                                                |
| sympy_expand               | 484 ms                                                 | 614 ms: 1.27x slower                                                 |
| spectral_norm              | 108 ms                                                 | 137 ms: 1.27x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 104 ms: 1.28x slower                                                 |
| sqlglot_transpile          | 1.75 ms                                                | 2.24 ms: 1.28x slower                                                |
| nbody                      | 96.0 ms                                                | 123 ms: 1.28x slower                                                 |
| richards_super             | 61.9 ms                                                | 79.4 ms: 1.28x slower                                                |
| html5lib                   | 64.8 ms                                                | 83.5 ms: 1.29x slower                                                |
| scimark_fft                | 345 ms                                                 | 445 ms: 1.29x slower                                                 |
| mypy2                      | 686 ms                                                 | 886 ms: 1.29x slower                                                 |
| crypto_pyaes               | 76.7 ms                                                | 99.9 ms: 1.30x slower                                                |
| scimark_sor                | 121 ms                                                 | 158 ms: 1.30x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.87 ms: 1.31x slower                                                |
| flaskblogging              | 7.28 ms                                                | 9.59 ms: 1.32x slower                                                |
| mako                       | 10.7 ms                                                | 14.2 ms: 1.33x slower                                                |
| chameleon                  | 6.70 ms                                                | 9.02 ms: 1.35x slower                                                |
| async_generators           | 374 ms                                                 | 504 ms: 1.35x slower                                                 |
| 2to3                       | 264 ms                                                 | 357 ms: 1.35x slower                                                 |
| pycparser                  | 1.19 sec                                               | 1.60 sec: 1.35x slower                                               |
| sqlglot_optimize           | 55.3 ms                                                | 75.4 ms: 1.36x slower                                                |
| sqlglot_normalize          | 113 ms                                                 | 154 ms: 1.37x slower                                                 |
| unpickle_pure_python       | 242 us                                                 | 331 us: 1.37x slower                                                 |
| logging_silent             | 111 ns                                                 | 152 ns: 1.37x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 4.45 us: 1.38x slower                                                |
| go                         | 149 ms                                                 | 208 ms: 1.40x slower                                                 |
| scimark_monte_carlo        | 70.7 ms                                                | 99.5 ms: 1.41x slower                                                |
| deepcopy_memo              | 40.2 us                                                | 56.6 us: 1.41x slower                                                |
| deepcopy                   | 365 us                                                 | 518 us: 1.42x slower                                                 |
| richards                   | 49.8 ms                                                | 71.0 ms: 1.43x slower                                                |
| pyflate                    | 434 ms                                                 | 619 ms: 1.43x slower                                                 |
| django_template            | 33.5 ms                                                | 49.2 ms: 1.47x slower                                                |
| scimark_lu                 | 116 ms                                                 | 171 ms: 1.47x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 82.8 ms: 1.55x slower                                                |
| hexiom                     | 6.89 ms                                                | 10.7 ms: 1.55x slower                                                |
| regex_compile              | 141 ms                                                 | 220 ms: 1.56x slower                                                 |
| telco                      | 6.86 ms                                                | 10.7 ms: 1.56x slower                                                |
| nqueens                    | 87.9 ms                                                | 141 ms: 1.61x slower                                                 |
| pprint_safe_repr           | 747 ms                                                 | 1.21 sec: 1.62x slower                                               |
| pprint_pformat             | 1.55 sec                                               | 2.55 sec: 1.64x slower                                               |
| pickle_pure_python         | 320 us                                                 | 525 us: 1.64x slower                                                 |
| genshi_text                | 22.5 ms                                                | 39.8 ms: 1.77x slower                                                |
| Geometric mean             | (ref)                                                  | 1.16x slower                                                         |

Benchmark hidden because not significant (2): bench_mp_pool, djangocms
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.05x