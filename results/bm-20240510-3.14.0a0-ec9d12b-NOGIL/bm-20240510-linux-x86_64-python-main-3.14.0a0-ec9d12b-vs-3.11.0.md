# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: ec9d12b
- commit date: 2024-05-10
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 264 ms                                                 | 395 ms: 1.49x slower                                  |
| chameleon      | 6.70 ms                                                | 12.8 ms: 1.91x slower                                 |
| docutils       | 2.66 sec                                               | 3.38 sec: 1.27x slower                                |
| html5lib       | 64.8 ms                                                | 96.6 ms: 1.49x slower                                 |
| tornado_http   | 98.1 ms                                                | 136 ms: 1.39x slower                                  |
| Geometric mean | (ref)                                                  | 1.50x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.29 sec                                               | 883 ms: 1.47x faster                                  |
| async_tree_io              | 1.29 sec                                               | 938 ms: 1.37x faster                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 503 ms: 1.25x faster                                  |
| async_tree_none_tg         | 491 ms                                                 | 396 ms: 1.24x faster                                  |
| async_tree_none            | 528 ms                                                 | 453 ms: 1.17x faster                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 657 ms: 1.16x faster                                  |
| async_tree_memoization     | 639 ms                                                 | 559 ms: 1.14x faster                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 715 ms: 1.05x faster                                  |
| Geometric mean             | (ref)                                                  | 1.22x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.01x faster                                  |
| float          | 78.9 ms                                                | 133 ms: 1.68x slower                                  |
| nbody          | 96.0 ms                                                | 227 ms: 2.37x slower                                  |
| Geometric mean | (ref)                                                  | 1.58x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.56 ms: 1.02x slower                                 |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                  |
| regex_v8       | 22.9 ms                                                | 26.5 ms: 1.16x slower                                 |
| regex_compile  | 141 ms                                                 | 217 ms: 1.53x slower                                  |
| Geometric mean | (ref)                                                  | 1.18x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 164 ms                                                 | 144 ms: 1.14x faster                                  |
| json_dumps           | 13.3 ms                                                | 13.9 ms: 1.04x slower                                 |
| xml_etree_iterparse  | 108 ms                                                 | 113 ms: 1.04x slower                                  |
| unpickle_list        | 5.21 us                                                | 5.57 us: 1.07x slower                                 |
| json_loads           | 29.2 us                                                | 32.7 us: 1.12x slower                                 |
| pickle               | 11.0 us                                                | 12.4 us: 1.13x slower                                 |
| pickle_list          | 4.59 us                                                | 5.34 us: 1.16x slower                                 |
| pickle_dict          | 34.6 us                                                | 42.4 us: 1.23x slower                                 |
| unpickle             | 13.8 us                                                | 17.0 us: 1.23x slower                                 |
| xml_etree_generate   | 81.1 ms                                                | 110 ms: 1.35x slower                                  |
| tomli_loads          | 2.30 sec                                               | 3.30 sec: 1.43x slower                                |
| xml_etree_process    | 56.9 ms                                                | 89.6 ms: 1.57x slower                                 |
| unpickle_pure_python | 242 us                                                 | 398 us: 1.64x slower                                  |
| pickle_pure_python   | 320 us                                                 | 570 us: 1.78x slower                                  |
| Geometric mean       | (ref)                                                  | 1.24x slower                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 9.16 ms: 1.52x slower                                 |
| python_startup         | 8.56 ms                                                | 13.3 ms: 1.56x slower                                 |
| Geometric mean         | (ref)                                                  | 1.54x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 81.4 ms: 1.52x slower                                 |
| genshi_text     | 22.5 ms                                                | 39.4 ms: 1.75x slower                                 |
| django_template | 33.5 ms                                                | 60.1 ms: 1.79x slower                                 |
| mako            | 10.7 ms                                                | 20.7 ms: 1.94x slower                                 |
| Geometric mean  | (ref)                                                  | 1.74x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| generators                 | 74.9 ms                                                | 36.6 ms: 2.04x faster                                 |
| typing_runtime_protocols   | 520 us                                                 | 259 us: 2.01x faster                                  |
| asyncio_tcp                | 875 ms                                                 | 590 ms: 1.48x faster                                  |
| async_tree_io_tg           | 1.29 sec                                               | 883 ms: 1.47x faster                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 2.14 sec: 1.45x faster                                |
| async_tree_io              | 1.29 sec                                               | 938 ms: 1.37x faster                                  |
| gc_traversal               | 4.01 ms                                                | 3.21 ms: 1.25x faster                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 503 ms: 1.25x faster                                  |
| async_tree_none_tg         | 491 ms                                                 | 396 ms: 1.24x faster                                  |
| pylint                     | 476 ms                                                 | 398 ms: 1.20x faster                                  |
| async_tree_none            | 528 ms                                                 | 453 ms: 1.17x faster                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 657 ms: 1.16x faster                                  |
| bench_mp_pool              | 24.0 ms                                                | 21.0 ms: 1.15x faster                                 |
| async_tree_memoization     | 639 ms                                                 | 559 ms: 1.14x faster                                  |
| xml_etree_parse            | 164 ms                                                 | 144 ms: 1.14x faster                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 715 ms: 1.05x faster                                  |
| pidigits                   | 194 ms                                                 | 191 ms: 1.01x faster                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.42 ms: 1.01x faster                                 |
| regex_effbot               | 3.51 ms                                                | 3.56 ms: 1.02x slower                                 |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                  |
| json_dumps                 | 13.3 ms                                                | 13.9 ms: 1.04x slower                                 |
| xml_etree_iterparse        | 108 ms                                                 | 113 ms: 1.04x slower                                  |
| unpickle_list              | 5.21 us                                                | 5.57 us: 1.07x slower                                 |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                  |
| json_loads                 | 29.2 us                                                | 32.7 us: 1.12x slower                                 |
| pickle                     | 11.0 us                                                | 12.4 us: 1.13x slower                                 |
| pathlib                    | 18.5 ms                                                | 20.9 ms: 1.13x slower                                 |
| regex_v8                   | 22.9 ms                                                | 26.5 ms: 1.16x slower                                 |
| pickle_list                | 4.59 us                                                | 5.34 us: 1.16x slower                                 |
| json                       | 5.24 ms                                                | 6.13 ms: 1.17x slower                                 |
| comprehensions             | 23.6 us                                                | 27.7 us: 1.17x slower                                 |
| pickle_dict                | 34.6 us                                                | 42.4 us: 1.23x slower                                 |
| unpickle                   | 13.8 us                                                | 17.0 us: 1.23x slower                                 |
| mdp                        | 2.77 sec                                               | 3.42 sec: 1.23x slower                                |
| coroutines                 | 27.0 ms                                                | 33.5 ms: 1.24x slower                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.24 ms: 1.24x slower                                 |
| sqlite_synth               | 2.57 us                                                | 3.21 us: 1.25x slower                                 |
| docutils                   | 2.66 sec                                               | 3.38 sec: 1.27x slower                                |
| pycparser                  | 1.19 sec                                               | 1.56 sec: 1.32x slower                                |
| meteor_contest             | 109 ms                                                 | 145 ms: 1.33x slower                                  |
| scimark_fft                | 345 ms                                                 | 461 ms: 1.33x slower                                  |
| nqueens                    | 87.9 ms                                                | 118 ms: 1.34x slower                                  |
| sympy_integrate            | 21.5 ms                                                | 29.0 ms: 1.35x slower                                 |
| xml_etree_generate         | 81.1 ms                                                | 110 ms: 1.35x slower                                  |
| dulwich_log                | 64.6 ms                                                | 87.8 ms: 1.36x slower                                 |
| tornado_http               | 98.1 ms                                                | 136 ms: 1.39x slower                                  |
| tomli_loads                | 2.30 sec                                               | 3.30 sec: 1.43x slower                                |
| sympy_str                  | 297 ms                                                 | 430 ms: 1.45x slower                                  |
| async_generators           | 374 ms                                                 | 553 ms: 1.48x slower                                  |
| fannkuch                   | 405 ms                                                 | 600 ms: 1.48x slower                                  |
| html5lib                   | 64.8 ms                                                | 96.6 ms: 1.49x slower                                 |
| 2to3                       | 264 ms                                                 | 395 ms: 1.49x slower                                  |
| crypto_pyaes               | 76.7 ms                                                | 115 ms: 1.50x slower                                  |
| richards_super             | 61.9 ms                                                | 93.3 ms: 1.51x slower                                 |
| genshi_xml                 | 53.4 ms                                                | 81.4 ms: 1.52x slower                                 |
| python_startup_no_site     | 6.01 ms                                                | 9.16 ms: 1.52x slower                                 |
| sympy_sum                  | 169 ms                                                 | 258 ms: 1.53x slower                                  |
| regex_compile              | 141 ms                                                 | 217 ms: 1.53x slower                                  |
| sqlglot_normalize          | 113 ms                                                 | 174 ms: 1.54x slower                                  |
| python_startup             | 8.56 ms                                                | 13.3 ms: 1.56x slower                                 |
| richards                   | 49.8 ms                                                | 77.8 ms: 1.56x slower                                 |
| sympy_expand               | 484 ms                                                 | 758 ms: 1.57x slower                                  |
| xml_etree_process          | 56.9 ms                                                | 89.6 ms: 1.57x slower                                 |
| deepcopy                   | 365 us                                                 | 578 us: 1.58x slower                                  |
| sqlglot_optimize           | 55.3 ms                                                | 87.6 ms: 1.58x slower                                 |
| deepcopy_reduce            | 3.22 us                                                | 5.22 us: 1.62x slower                                 |
| deepcopy_memo              | 40.2 us                                                | 65.1 us: 1.62x slower                                 |
| unpickle_pure_python       | 242 us                                                 | 398 us: 1.64x slower                                  |
| float                      | 78.9 ms                                                | 133 ms: 1.68x slower                                  |
| logging_simple             | 6.22 us                                                | 10.5 us: 1.69x slower                                 |
| sqlglot_transpile          | 1.75 ms                                                | 2.99 ms: 1.71x slower                                 |
| chaos                      | 71.9 ms                                                | 124 ms: 1.72x slower                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 122 ms: 1.73x slower                                  |
| pyflate                    | 434 ms                                                 | 749 ms: 1.73x slower                                  |
| logging_format             | 6.81 us                                                | 11.8 us: 1.73x slower                                 |
| spectral_norm              | 108 ms                                                 | 188 ms: 1.74x slower                                  |
| pprint_pformat             | 1.55 sec                                               | 2.70 sec: 1.74x slower                                |
| genshi_text                | 22.5 ms                                                | 39.4 ms: 1.75x slower                                 |
| pprint_safe_repr           | 747 ms                                                 | 1.31 sec: 1.75x slower                                |
| logging_silent             | 111 ns                                                 | 195 ns: 1.76x slower                                  |
| sqlglot_parse              | 1.43 ms                                                | 2.52 ms: 1.76x slower                                 |
| pickle_pure_python         | 320 us                                                 | 570 us: 1.78x slower                                  |
| hexiom                     | 6.89 ms                                                | 12.3 ms: 1.79x slower                                 |
| django_template            | 33.5 ms                                                | 60.1 ms: 1.79x slower                                 |
| flaskblogging              | 7.28 ms                                                | 13.4 ms: 1.84x slower                                 |
| chameleon                  | 6.70 ms                                                | 12.8 ms: 1.91x slower                                 |
| raytrace                   | 309 ms                                                 | 589 ms: 1.91x slower                                  |
| mako                       | 10.7 ms                                                | 20.7 ms: 1.94x slower                                 |
| scimark_lu                 | 116 ms                                                 | 238 ms: 2.05x slower                                  |
| go                         | 149 ms                                                 | 311 ms: 2.09x slower                                  |
| deltablue                  | 3.92 ms                                                | 8.32 ms: 2.12x slower                                 |
| scimark_sor                | 121 ms                                                 | 270 ms: 2.23x slower                                  |
| nbody                      | 96.0 ms                                                | 227 ms: 2.37x slower                                  |
| bench_thread_pool          | 834 us                                                 | 3.04 ms: 3.65x slower                                 |
| coverage                   | 78.8 ms                                                | 787 ms: 10.00x slower                                 |
| thrift                     | 784 us                                                 | 13.1 ms: 16.66x slower                                |
| telco                      | 6.86 ms                                                | 317 ms: 46.18x slower                                 |
| Geometric mean             | (ref)                                                  | 1.44x slower                                          |
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x