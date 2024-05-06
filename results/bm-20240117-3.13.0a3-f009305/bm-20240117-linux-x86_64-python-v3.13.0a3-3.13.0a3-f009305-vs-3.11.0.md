# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: linux-x86_64
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.05x faster
- HPT reliability: 99.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                       |
| chameleon      | 6.70 ms                                                | 6.87 ms: 1.03x slower                                      |
| docutils       | 2.66 sec                                               | 2.68 sec: 1.01x slower                                     |
| html5lib       | 64.8 ms                                                | 67.9 ms: 1.05x slower                                      |
| tornado_http   | 98.1 ms                                                | 96.8 ms: 1.01x faster                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 446 ms: 1.18x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 574 ms: 1.11x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 447 ms: 1.10x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 586 ms: 1.07x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 1.21 sec: 1.07x faster                                     |
| async_tree_io              | 1.29 sec                                               | 1.21 sec: 1.06x faster                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 734 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 724 ms: 1.03x faster                                       |
| Geometric mean             | (ref)                                                  | 1.08x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.5 ms: 1.07x faster                                      |
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                       |
| float          | 78.9 ms                                                | 82.0 ms: 1.04x slower                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 131 ms: 1.08x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                      |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                      |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                       |
| Geometric mean | (ref)                                                  | 1.05x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.28x faster                                      |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                     |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                       |
| pickle_dict          | 34.6 us                                                | 33.8 us: 1.02x faster                                      |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                       |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                       |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                      |
| unpickle_list        | 5.21 us                                                | 5.25 us: 1.01x slower                                      |
| pickle               | 11.0 us                                                | 11.5 us: 1.05x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.4 ms: 1.08x slower                                      |
| pickle_list          | 4.59 us                                                | 4.98 us: 1.09x slower                                      |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.21x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 8.92 ms: 1.48x slower                                      |
| Geometric mean         | (ref)                                                  | 1.34x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                      |
| genshi_text     | 22.5 ms                                                | 23.2 ms: 1.03x slower                                      |
| django_template | 33.5 ms                                                | 34.7 ms: 1.03x slower                                      |
| mako            | 10.7 ms                                                | 11.3 ms: 1.06x slower                                      |
| Geometric mean  | (ref)                                                  | 1.02x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 110 us: 4.72x faster                                       |
| generators                 | 74.9 ms                                                | 29.2 ms: 2.57x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 493 ms: 1.78x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.83 sec: 1.70x faster                                     |
| pylint                     | 476 ms                                                 | 313 ms: 1.52x faster                                       |
| comprehensions             | 23.6 us                                                | 16.3 us: 1.45x faster                                      |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                      |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                      |
| coroutines                 | 27.0 ms                                                | 22.3 ms: 1.21x faster                                      |
| chaos                      | 71.9 ms                                                | 59.9 ms: 1.20x faster                                      |
| async_tree_none            | 528 ms                                                 | 446 ms: 1.18x faster                                       |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                       |
| hexiom                     | 6.89 ms                                                | 6.10 ms: 1.13x faster                                      |
| richards_super             | 61.9 ms                                                | 55.1 ms: 1.12x faster                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.28 ms: 1.12x faster                                      |
| async_tree_memoization     | 639 ms                                                 | 574 ms: 1.11x faster                                       |
| sympy_sum                  | 169 ms                                                 | 152 ms: 1.11x faster                                       |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 447 ms: 1.10x faster                                       |
| nqueens                    | 87.9 ms                                                | 80.7 ms: 1.09x faster                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.61 ms: 1.09x faster                                      |
| sympy_str                  | 297 ms                                                 | 275 ms: 1.08x faster                                       |
| regex_compile              | 141 ms                                                 | 131 ms: 1.08x faster                                       |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.08x faster                                     |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.08x faster                                      |
| nbody                      | 96.0 ms                                                | 89.5 ms: 1.07x faster                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 586 ms: 1.07x faster                                       |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                     |
| async_tree_io_tg           | 1.29 sec                                               | 1.21 sec: 1.07x faster                                     |
| async_tree_io              | 1.29 sec                                               | 1.21 sec: 1.06x faster                                     |
| go                         | 149 ms                                                 | 140 ms: 1.06x faster                                       |
| crypto_pyaes               | 76.7 ms                                                | 72.3 ms: 1.06x faster                                      |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                      |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                       |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                      |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                       |
| logging_simple             | 6.22 us                                                | 5.89 us: 1.06x faster                                      |
| deepcopy_memo              | 40.2 us                                                | 38.4 us: 1.05x faster                                      |
| logging_format             | 6.81 us                                                | 6.53 us: 1.04x faster                                      |
| deepcopy                   | 365 us                                                 | 350 us: 1.04x faster                                       |
| sympy_expand               | 484 ms                                                 | 466 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 734 ms: 1.04x faster                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.11 us: 1.04x faster                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 724 ms: 1.03x faster                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 68.6 ms: 1.03x faster                                      |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                       |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                      |
| pickle_dict                | 34.6 us                                                | 33.8 us: 1.02x faster                                      |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                       |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                       |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                       |
| richards                   | 49.8 ms                                                | 48.9 ms: 1.02x faster                                      |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                       |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                      |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.01x faster                                     |
| tornado_http               | 98.1 ms                                                | 96.8 ms: 1.01x faster                                      |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                      |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                      |
| fannkuch                   | 405 ms                                                 | 402 ms: 1.01x faster                                       |
| docutils                   | 2.66 sec                                               | 2.68 sec: 1.01x slower                                     |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                       |
| unpickle_list              | 5.21 us                                                | 5.25 us: 1.01x slower                                      |
| bench_thread_pool          | 834 us                                                 | 842 us: 1.01x slower                                       |
| thrift                     | 784 us                                                 | 796 us: 1.01x slower                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.10 ms: 1.02x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                       |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                       |
| chameleon                  | 6.70 ms                                                | 6.87 ms: 1.03x slower                                      |
| spectral_norm              | 108 ms                                                 | 111 ms: 1.03x slower                                       |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                      |
| genshi_text                | 22.5 ms                                                | 23.2 ms: 1.03x slower                                      |
| django_template            | 33.5 ms                                                | 34.7 ms: 1.03x slower                                      |
| dulwich_log                | 64.6 ms                                                | 66.8 ms: 1.03x slower                                      |
| float                      | 78.9 ms                                                | 82.0 ms: 1.04x slower                                      |
| pickle                     | 11.0 us                                                | 11.5 us: 1.05x slower                                      |
| html5lib                   | 64.8 ms                                                | 67.9 ms: 1.05x slower                                      |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                      |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.51 ms: 1.05x slower                                      |
| mako                       | 10.7 ms                                                | 11.3 ms: 1.06x slower                                      |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                      |
| scimark_fft                | 345 ms                                                 | 366 ms: 1.06x slower                                       |
| xml_etree_generate         | 81.1 ms                                                | 87.4 ms: 1.08x slower                                      |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                       |
| pyflate                    | 434 ms                                                 | 471 ms: 1.09x slower                                       |
| pickle_list                | 4.59 us                                                | 4.98 us: 1.09x slower                                      |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                      |
| sqlite_synth               | 2.57 us                                                | 2.88 us: 1.12x slower                                      |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                       |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                      |
| flaskblogging              | 7.28 ms                                                | 8.79 ms: 1.21x slower                                      |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.21x slower                                      |
| async_generators           | 374 ms                                                 | 454 ms: 1.21x slower                                       |
| coverage                   | 78.8 ms                                                | 95.8 ms: 1.22x slower                                      |
| telco                      | 6.86 ms                                                | 8.55 ms: 1.25x slower                                      |
| mypy2                      | 686 ms                                                 | 865 ms: 1.26x slower                                       |
| python_startup_no_site     | 6.01 ms                                                | 8.92 ms: 1.48x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (3): pprint_safe_repr, pathlib, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.09% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x