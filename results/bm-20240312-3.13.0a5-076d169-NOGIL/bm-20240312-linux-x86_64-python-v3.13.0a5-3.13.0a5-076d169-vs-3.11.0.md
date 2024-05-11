# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: linux-x86_64
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 377 ms: 1.43x slower                                       |
| chameleon      | 6.70 ms                                                | 12.3 ms: 1.83x slower                                      |
| docutils       | 2.66 sec                                               | 3.28 sec: 1.23x slower                                     |
| html5lib       | 64.8 ms                                                | 91.5 ms: 1.41x slower                                      |
| tornado_http   | 98.1 ms                                                | 137 ms: 1.40x slower                                       |
| Geometric mean | (ref)                                                  | 1.45x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 1.29 sec                                               | 839 ms: 1.54x faster                                       |
| async_tree_io              | 1.29 sec                                               | 877 ms: 1.47x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 369 ms: 1.33x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 472 ms: 1.33x faster                                       |
| async_tree_none            | 528 ms                                                 | 412 ms: 1.28x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 518 ms: 1.23x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 623 ms: 1.22x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 668 ms: 1.12x faster                                       |
| Geometric mean             | (ref)                                                  | 1.31x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 192 ms: 1.01x faster                                       |
| float          | 78.9 ms                                                | 127 ms: 1.60x slower                                       |
| nbody          | 96.0 ms                                                | 215 ms: 2.24x slower                                       |
| Geometric mean | (ref)                                                  | 1.52x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.56 ms: 1.02x slower                                      |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                       |
| regex_v8       | 22.9 ms                                                | 26.9 ms: 1.18x slower                                      |
| regex_compile  | 141 ms                                                 | 204 ms: 1.45x slower                                       |
| Geometric mean | (ref)                                                  | 1.18x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 164 ms                                                 | 156 ms: 1.05x faster                                       |
| json_dumps           | 13.3 ms                                                | 13.7 ms: 1.03x slower                                      |
| pickle_list          | 4.59 us                                                | 4.97 us: 1.08x slower                                      |
| xml_etree_iterparse  | 108 ms                                                 | 117 ms: 1.09x slower                                       |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                      |
| unpickle_list        | 5.21 us                                                | 5.75 us: 1.10x slower                                      |
| json_loads           | 29.2 us                                                | 34.8 us: 1.19x slower                                      |
| pickle_dict          | 34.6 us                                                | 41.4 us: 1.20x slower                                      |
| unpickle             | 13.8 us                                                | 18.1 us: 1.31x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 108 ms: 1.33x slower                                       |
| tomli_loads          | 2.30 sec                                               | 3.11 sec: 1.35x slower                                     |
| unpickle_pure_python | 242 us                                                 | 367 us: 1.52x slower                                       |
| xml_etree_process    | 56.9 ms                                                | 86.4 ms: 1.52x slower                                      |
| pickle_pure_python   | 320 us                                                 | 528 us: 1.65x slower                                       |
| Geometric mean       | (ref)                                                  | 1.23x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 13.6 ms: 1.59x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 11.6 ms: 1.93x slower                                      |
| Geometric mean         | (ref)                                                  | 1.75x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 78.4 ms: 1.47x slower                                      |
| django_template | 33.5 ms                                                | 57.7 ms: 1.72x slower                                      |
| genshi_text     | 22.5 ms                                                | 38.9 ms: 1.73x slower                                      |
| mako            | 10.7 ms                                                | 21.0 ms: 1.97x slower                                      |
| Geometric mean  | (ref)                                                  | 1.71x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-linux-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 167 us: 3.11x faster                                       |
| generators                 | 74.9 ms                                                | 36.2 ms: 2.07x faster                                      |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.99 sec: 1.56x faster                                     |
| gc_traversal               | 4.01 ms                                                | 2.57 ms: 1.56x faster                                      |
| async_tree_io_tg           | 1.29 sec                                               | 839 ms: 1.54x faster                                       |
| asyncio_tcp                | 875 ms                                                 | 584 ms: 1.50x faster                                       |
| async_tree_io              | 1.29 sec                                               | 877 ms: 1.47x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 369 ms: 1.33x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 472 ms: 1.33x faster                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.08 ms: 1.32x faster                                      |
| async_tree_none            | 528 ms                                                 | 412 ms: 1.28x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 518 ms: 1.23x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 623 ms: 1.22x faster                                       |
| pylint                     | 476 ms                                                 | 390 ms: 1.22x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 668 ms: 1.12x faster                                       |
| xml_etree_parse            | 164 ms                                                 | 156 ms: 1.05x faster                                       |
| pidigits                   | 194 ms                                                 | 192 ms: 1.01x faster                                       |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                      |
| regex_effbot               | 3.51 ms                                                | 3.56 ms: 1.02x slower                                      |
| json_dumps                 | 13.3 ms                                                | 13.7 ms: 1.03x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                       |
| coroutines                 | 27.0 ms                                                | 29.3 ms: 1.08x slower                                      |
| pickle_list                | 4.59 us                                                | 4.97 us: 1.08x slower                                      |
| xml_etree_iterparse        | 108 ms                                                 | 117 ms: 1.09x slower                                       |
| comprehensions             | 23.6 us                                                | 25.7 us: 1.09x slower                                      |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                      |
| unpickle_list              | 5.21 us                                                | 5.75 us: 1.10x slower                                      |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                       |
| regex_v8                   | 22.9 ms                                                | 26.9 ms: 1.18x slower                                      |
| mdp                        | 2.77 sec                                               | 3.30 sec: 1.19x slower                                     |
| json                       | 5.24 ms                                                | 6.24 ms: 1.19x slower                                      |
| json_loads                 | 29.2 us                                                | 34.8 us: 1.19x slower                                      |
| pickle_dict                | 34.6 us                                                | 41.4 us: 1.20x slower                                      |
| docutils                   | 2.66 sec                                               | 3.28 sec: 1.23x slower                                     |
| meteor_contest             | 109 ms                                                 | 136 ms: 1.24x slower                                       |
| nqueens                    | 87.9 ms                                                | 111 ms: 1.27x slower                                       |
| unpickle                   | 13.8 us                                                | 18.1 us: 1.31x slower                                      |
| sympy_integrate            | 21.5 ms                                                | 28.4 ms: 1.32x slower                                      |
| xml_etree_generate         | 81.1 ms                                                | 108 ms: 1.33x slower                                       |
| pycparser                  | 1.19 sec                                               | 1.57 sec: 1.33x slower                                     |
| richards_super             | 61.9 ms                                                | 82.3 ms: 1.33x slower                                      |
| tomli_loads                | 2.30 sec                                               | 3.11 sec: 1.35x slower                                     |
| richards                   | 49.8 ms                                                | 68.0 ms: 1.37x slower                                      |
| async_generators           | 374 ms                                                 | 511 ms: 1.37x slower                                       |
| fannkuch                   | 405 ms                                                 | 559 ms: 1.38x slower                                       |
| dulwich_log                | 64.6 ms                                                | 89.2 ms: 1.38x slower                                      |
| scimark_fft                | 345 ms                                                 | 481 ms: 1.39x slower                                       |
| pathlib                    | 18.5 ms                                                | 25.9 ms: 1.40x slower                                      |
| tornado_http               | 98.1 ms                                                | 137 ms: 1.40x slower                                       |
| crypto_pyaes               | 76.7 ms                                                | 108 ms: 1.41x slower                                       |
| html5lib                   | 64.8 ms                                                | 91.5 ms: 1.41x slower                                      |
| sympy_str                  | 297 ms                                                 | 421 ms: 1.42x slower                                       |
| gunicorn                   | 1.20 ms                                                | 1.71 ms: 1.43x slower                                      |
| 2to3                       | 264 ms                                                 | 377 ms: 1.43x slower                                       |
| aiohttp                    | 1.12 ms                                                | 1.59 ms: 1.43x slower                                      |
| deepcopy                   | 365 us                                                 | 527 us: 1.44x slower                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 7.26 ms: 1.44x slower                                      |
| regex_compile              | 141 ms                                                 | 204 ms: 1.45x slower                                       |
| genshi_xml                 | 53.4 ms                                                | 78.4 ms: 1.47x slower                                      |
| deepcopy_reduce            | 3.22 us                                                | 4.74 us: 1.47x slower                                      |
| sqlite_synth               | 2.57 us                                                | 3.84 us: 1.49x slower                                      |
| sympy_sum                  | 169 ms                                                 | 254 ms: 1.50x slower                                       |
| deepcopy_memo              | 40.2 us                                                | 60.8 us: 1.51x slower                                      |
| unpickle_pure_python       | 242 us                                                 | 367 us: 1.52x slower                                       |
| xml_etree_process          | 56.9 ms                                                | 86.4 ms: 1.52x slower                                      |
| sympy_expand               | 484 ms                                                 | 740 ms: 1.53x slower                                       |
| mypy2                      | 686 ms                                                 | 1.07 sec: 1.57x slower                                     |
| sqlglot_normalize          | 113 ms                                                 | 177 ms: 1.57x slower                                       |
| logging_silent             | 111 ns                                                 | 176 ns: 1.58x slower                                       |
| python_startup             | 8.56 ms                                                | 13.6 ms: 1.59x slower                                      |
| hexiom                     | 6.89 ms                                                | 11.0 ms: 1.60x slower                                      |
| float                      | 78.9 ms                                                | 127 ms: 1.60x slower                                       |
| pprint_pformat             | 1.55 sec                                               | 2.49 sec: 1.60x slower                                     |
| chaos                      | 71.9 ms                                                | 115 ms: 1.60x slower                                       |
| sqlglot_optimize           | 55.3 ms                                                | 88.8 ms: 1.61x slower                                      |
| pprint_safe_repr           | 747 ms                                                 | 1.20 sec: 1.61x slower                                     |
| sqlglot_transpile          | 1.75 ms                                                | 2.84 ms: 1.63x slower                                      |
| logging_simple             | 6.22 us                                                | 10.2 us: 1.63x slower                                      |
| logging_format             | 6.81 us                                                | 11.2 us: 1.65x slower                                      |
| pickle_pure_python         | 320 us                                                 | 528 us: 1.65x slower                                       |
| sqlglot_parse              | 1.43 ms                                                | 2.37 ms: 1.65x slower                                      |
| spectral_norm              | 108 ms                                                 | 181 ms: 1.67x slower                                       |
| pyflate                    | 434 ms                                                 | 728 ms: 1.68x slower                                       |
| raytrace                   | 309 ms                                                 | 518 ms: 1.68x slower                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 119 ms: 1.69x slower                                       |
| telco                      | 6.86 ms                                                | 11.7 ms: 1.70x slower                                      |
| django_template            | 33.5 ms                                                | 57.7 ms: 1.72x slower                                      |
| genshi_text                | 22.5 ms                                                | 38.9 ms: 1.73x slower                                      |
| chameleon                  | 6.70 ms                                                | 12.3 ms: 1.83x slower                                      |
| go                         | 149 ms                                                 | 273 ms: 1.84x slower                                       |
| deltablue                  | 3.92 ms                                                | 7.43 ms: 1.89x slower                                      |
| python_startup_no_site     | 6.01 ms                                                | 11.6 ms: 1.93x slower                                      |
| flaskblogging              | 7.28 ms                                                | 14.3 ms: 1.97x slower                                      |
| mako                       | 10.7 ms                                                | 21.0 ms: 1.97x slower                                      |
| scimark_sor                | 121 ms                                                 | 241 ms: 1.99x slower                                       |
| scimark_lu                 | 116 ms                                                 | 250 ms: 2.15x slower                                       |
| nbody                      | 96.0 ms                                                | 215 ms: 2.24x slower                                       |
| bench_thread_pool          | 834 us                                                 | 3.01 ms: 3.61x slower                                      |
| coverage                   | 78.8 ms                                                | 891 ms: 11.31x slower                                      |
| thrift                     | 784 us                                                 | 12.4 ms: 15.80x slower                                     |
| Geometric mean             | (ref)                                                  | 1.35x slower                                               |
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, djangocms, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.13x