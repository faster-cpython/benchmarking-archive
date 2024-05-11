# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a2
- machine: linux-x86_64
- commit hash: 9c4347e
- commit date: 2023-11-22
- overall geometric mean: 1.17x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.60x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 294 ms: 1.11x slower                                       |
| chameleon      | 6.70 ms                                                | 7.76 ms: 1.16x slower                                      |
| docutils       | 2.66 sec                                               | 2.89 sec: 1.08x slower                                     |
| html5lib       | 64.8 ms                                                | 71.7 ms: 1.11x slower                                      |
| tornado_http   | 98.1 ms                                                | 108 ms: 1.10x slower                                       |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 509 ms: 1.04x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 657 ms: 1.03x slower                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 804 ms: 1.07x slower                                       |
| async_tree_io              | 1.29 sec                                               | 1.39 sec: 1.08x slower                                     |
| async_tree_none_tg         | 491 ms                                                 | 540 ms: 1.10x slower                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 692 ms: 1.10x slower                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 850 ms: 1.12x slower                                       |
| async_tree_io_tg           | 1.29 sec                                               | 1.45 sec: 1.12x slower                                     |
| Geometric mean             | (ref)                                                  | 1.07x slower                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                       |
| nbody          | 96.0 ms                                                | 110 ms: 1.14x slower                                       |
| float          | 78.9 ms                                                | 95.5 ms: 1.21x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 149 ms: 1.06x slower                                       |
| regex_dna      | 205 ms                                                 | 222 ms: 1.09x slower                                       |
| regex_effbot   | 3.51 ms                                                | 3.83 ms: 1.09x slower                                      |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                      |
| Geometric mean | (ref)                                                  | 1.09x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 11.3 ms: 1.18x faster                                      |
| pickle_dict          | 34.6 us                                                | 32.7 us: 1.06x faster                                      |
| unpickle_list        | 5.21 us                                                | 5.26 us: 1.01x slower                                      |
| unpickle_pure_python | 242 us                                                 | 246 us: 1.02x slower                                       |
| pickle_list          | 4.59 us                                                | 4.71 us: 1.03x slower                                      |
| tomli_loads          | 2.30 sec                                               | 2.37 sec: 1.03x slower                                     |
| pickle               | 11.0 us                                                | 11.4 us: 1.04x slower                                      |
| pickle_pure_python   | 320 us                                                 | 335 us: 1.05x slower                                       |
| xml_etree_iterparse  | 108 ms                                                 | 114 ms: 1.06x slower                                       |
| json_loads           | 29.2 us                                                | 30.9 us: 1.06x slower                                      |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                      |
| xml_etree_parse      | 164 ms                                                 | 472 ms: 2.88x slower                                       |
| xml_etree_process    | 56.9 ms                                                | 1.03 sec: 18.07x slower                                    |
| xml_etree_generate   | 81.1 ms                                                | 1.58 sec: 19.51x slower                                    |
| Geometric mean       | (ref)                                                  | 1.66x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 9.60 ms: 1.60x slower                                      |
| Geometric mean         | (ref)                                                  | 1.44x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 56.2 ms: 1.05x slower                                      |
| genshi_text     | 22.5 ms                                                | 24.9 ms: 1.10x slower                                      |
| django_template | 33.5 ms                                                | 38.3 ms: 1.14x slower                                      |
| mako            | 10.7 ms                                                | 12.9 ms: 1.21x slower                                      |
| Geometric mean  | (ref)                                                  | 1.13x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 127 us: 4.09x faster                                       |
| generators                 | 74.9 ms                                                | 31.2 ms: 2.40x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 511 ms: 1.71x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                     |
| pylint                     | 476 ms                                                 | 341 ms: 1.40x faster                                       |
| comprehensions             | 23.6 us                                                | 18.5 us: 1.28x faster                                      |
| json_dumps                 | 13.3 ms                                                | 11.3 ms: 1.18x faster                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.22 ms: 1.18x faster                                      |
| gc_traversal               | 4.01 ms                                                | 3.64 ms: 1.10x faster                                      |
| coroutines                 | 27.0 ms                                                | 24.8 ms: 1.09x faster                                      |
| bench_mp_pool              | 24.0 ms                                                | 22.6 ms: 1.06x faster                                      |
| pickle_dict                | 34.6 us                                                | 32.7 us: 1.06x faster                                      |
| richards_super             | 61.9 ms                                                | 59.1 ms: 1.05x faster                                      |
| chaos                      | 71.9 ms                                                | 68.7 ms: 1.05x faster                                      |
| async_tree_none            | 528 ms                                                 | 509 ms: 1.04x faster                                       |
| hexiom                     | 6.89 ms                                                | 6.86 ms: 1.00x faster                                      |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.44 ms: 1.00x slower                                      |
| nqueens                    | 87.9 ms                                                | 88.6 ms: 1.01x slower                                      |
| unpickle_list              | 5.21 us                                                | 5.26 us: 1.01x slower                                      |
| unpickle_pure_python       | 242 us                                                 | 246 us: 1.02x slower                                       |
| raytrace                   | 309 ms                                                 | 314 ms: 1.02x slower                                       |
| deltablue                  | 3.92 ms                                                | 3.99 ms: 1.02x slower                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.79 ms: 1.02x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                       |
| pickle_list                | 4.59 us                                                | 4.71 us: 1.03x slower                                      |
| tomli_loads                | 2.30 sec                                               | 2.37 sec: 1.03x slower                                     |
| async_tree_memoization     | 639 ms                                                 | 657 ms: 1.03x slower                                       |
| pickle                     | 11.0 us                                                | 11.4 us: 1.04x slower                                      |
| logging_simple             | 6.22 us                                                | 6.44 us: 1.04x slower                                      |
| logging_format             | 6.81 us                                                | 7.09 us: 1.04x slower                                      |
| mdp                        | 2.77 sec                                               | 2.89 sec: 1.04x slower                                     |
| richards                   | 49.8 ms                                                | 51.9 ms: 1.04x slower                                      |
| logging_silent             | 111 ns                                                 | 116 ns: 1.04x slower                                       |
| crypto_pyaes               | 76.7 ms                                                | 80.1 ms: 1.04x slower                                      |
| sqlglot_normalize          | 113 ms                                                 | 118 ms: 1.05x slower                                       |
| pickle_pure_python         | 320 us                                                 | 335 us: 1.05x slower                                       |
| genshi_xml                 | 53.4 ms                                                | 56.2 ms: 1.05x slower                                      |
| go                         | 149 ms                                                 | 157 ms: 1.06x slower                                       |
| regex_compile              | 141 ms                                                 | 149 ms: 1.06x slower                                       |
| xml_etree_iterparse        | 108 ms                                                 | 114 ms: 1.06x slower                                       |
| json_loads                 | 29.2 us                                                | 30.9 us: 1.06x slower                                      |
| pprint_pformat             | 1.55 sec                                               | 1.66 sec: 1.07x slower                                     |
| pathlib                    | 18.5 ms                                                | 19.8 ms: 1.07x slower                                      |
| sympy_integrate            | 21.5 ms                                                | 22.9 ms: 1.07x slower                                      |
| deepcopy_memo              | 40.2 us                                                | 43.0 us: 1.07x slower                                      |
| deepcopy                   | 365 us                                                 | 392 us: 1.07x slower                                       |
| meteor_contest             | 109 ms                                                 | 117 ms: 1.07x slower                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 804 ms: 1.07x slower                                       |
| sqlglot_optimize           | 55.3 ms                                                | 59.4 ms: 1.07x slower                                      |
| pycparser                  | 1.19 sec                                               | 1.27 sec: 1.08x slower                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 76.1 ms: 1.08x slower                                      |
| async_tree_io              | 1.29 sec                                               | 1.39 sec: 1.08x slower                                     |
| json                       | 5.24 ms                                                | 5.68 ms: 1.08x slower                                      |
| docutils                   | 2.66 sec                                               | 2.89 sec: 1.08x slower                                     |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.09x slower                                       |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.09x slower                                       |
| pprint_safe_repr           | 747 ms                                                 | 812 ms: 1.09x slower                                       |
| regex_effbot               | 3.51 ms                                                | 3.83 ms: 1.09x slower                                      |
| dulwich_log                | 64.6 ms                                                | 70.8 ms: 1.10x slower                                      |
| tornado_http               | 98.1 ms                                                | 108 ms: 1.10x slower                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.53 us: 1.10x slower                                      |
| async_tree_none_tg         | 491 ms                                                 | 540 ms: 1.10x slower                                       |
| genshi_text                | 22.5 ms                                                | 24.9 ms: 1.10x slower                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 692 ms: 1.10x slower                                       |
| html5lib                   | 64.8 ms                                                | 71.7 ms: 1.11x slower                                      |
| 2to3                       | 264 ms                                                 | 294 ms: 1.11x slower                                       |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                      |
| fannkuch                   | 405 ms                                                 | 451 ms: 1.11x slower                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.61 ms: 1.12x slower                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 850 ms: 1.12x slower                                       |
| sympy_str                  | 297 ms                                                 | 332 ms: 1.12x slower                                       |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.12x slower                                      |
| async_tree_io_tg           | 1.29 sec                                               | 1.45 sec: 1.12x slower                                     |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.12x slower                                      |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                      |
| nbody                      | 96.0 ms                                                | 110 ms: 1.14x slower                                       |
| django_template            | 33.5 ms                                                | 38.3 ms: 1.14x slower                                      |
| scimark_sor                | 121 ms                                                 | 140 ms: 1.15x slower                                       |
| chameleon                  | 6.70 ms                                                | 7.76 ms: 1.16x slower                                      |
| scimark_fft                | 345 ms                                                 | 405 ms: 1.17x slower                                       |
| pyflate                    | 434 ms                                                 | 510 ms: 1.17x slower                                       |
| spectral_norm              | 108 ms                                                 | 130 ms: 1.20x slower                                       |
| float                      | 78.9 ms                                                | 95.5 ms: 1.21x slower                                      |
| mako                       | 10.7 ms                                                | 12.9 ms: 1.21x slower                                      |
| sympy_sum                  | 169 ms                                                 | 211 ms: 1.25x slower                                       |
| sqlite_synth               | 2.57 us                                                | 3.23 us: 1.25x slower                                      |
| sympy_expand               | 484 ms                                                 | 613 ms: 1.27x slower                                       |
| bench_thread_pool          | 834 us                                                 | 1.09 ms: 1.30x slower                                      |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                      |
| async_generators           | 374 ms                                                 | 500 ms: 1.34x slower                                       |
| flaskblogging              | 7.28 ms                                                | 10.2 ms: 1.40x slower                                      |
| telco                      | 6.86 ms                                                | 9.60 ms: 1.40x slower                                      |
| python_startup_no_site     | 6.01 ms                                                | 9.60 ms: 1.60x slower                                      |
| mypy2                      | 686 ms                                                 | 1.15 sec: 1.68x slower                                     |
| xml_etree_parse            | 164 ms                                                 | 472 ms: 2.88x slower                                       |
| coverage                   | 78.8 ms                                                | 725 ms: 9.21x slower                                       |
| thrift                     | 784 us                                                 | 9.50 ms: 12.12x slower                                     |
| xml_etree_process          | 56.9 ms                                                | 1.03 sec: 18.07x slower                                    |
| xml_etree_generate         | 81.1 ms                                                | 1.58 sec: 19.51x slower                                    |
| Geometric mean             | (ref)                                                  | 1.17x slower                                               |
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, djangocms, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.60x