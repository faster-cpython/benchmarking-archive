# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: 07e95c4
- commit date: 2024-04-23
- overall geometric mean: 1.07x faster
- HPT reliability: 97.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                 |
| chameleon      | 6.70 ms                                                | 6.93 ms: 1.03x slower                                                |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                               |
| html5lib       | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                |
| tornado_http   | 98.1 ms                                                | 96.3 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 925 ms: 1.39x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.38x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 82.2 ms: 1.17x faster                                                |
| float          | 78.9 ms                                                | 73.4 ms: 1.07x faster                                                |
| pidigits       | 194 ms                                                 | 197 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                 |
| regex_effbot   | 3.51 ms                                                | 3.57 ms: 1.02x slower                                                |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.18x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                 |
| unpickle_pure_python | 242 us                                                 | 227 us: 1.07x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                 |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                 |
| unpickle_list        | 5.21 us                                                | 5.05 us: 1.03x faster                                                |
| pickle_dict          | 34.6 us                                                | 33.5 us: 1.03x faster                                                |
| pickle_list          | 4.59 us                                                | 4.75 us: 1.04x slower                                                |
| xml_etree_process    | 56.9 ms                                                | 60.1 ms: 1.06x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 87.1 ms: 1.07x slower                                                |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.57 ms: 1.26x slower                                                |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.96 ms: 1.07x faster                                                |
| genshi_xml      | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                |
| django_template | 33.5 ms                                                | 36.2 ms: 1.08x slower                                                |
| genshi_text     | 22.5 ms                                                | 24.7 ms: 1.10x slower                                                |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.56x faster                                                 |
| generators                 | 74.9 ms                                                | 30.4 ms: 2.46x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.70x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                               |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                 |
| pylint                     | 476 ms                                                 | 335 ms: 1.42x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 925 ms: 1.39x faster                                                 |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.39x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.38x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                 |
| richards_super             | 61.9 ms                                                | 48.8 ms: 1.27x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                 |
| chaos                      | 71.9 ms                                                | 60.9 ms: 1.18x faster                                                |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.18x faster                                               |
| richards                   | 49.8 ms                                                | 42.5 ms: 1.17x faster                                                |
| nbody                      | 96.0 ms                                                | 82.2 ms: 1.17x faster                                                |
| fannkuch                   | 405 ms                                                 | 353 ms: 1.15x faster                                                 |
| raytrace                   | 309 ms                                                 | 271 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 68.6 ms: 1.12x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.52 ms: 1.11x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 63.9 ms: 1.11x faster                                                |
| spectral_norm              | 108 ms                                                 | 98.9 ms: 1.09x faster                                                |
| scimark_fft                | 345 ms                                                 | 316 ms: 1.09x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                                |
| float                      | 78.9 ms                                                | 73.4 ms: 1.07x faster                                                |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                 |
| mako                       | 10.7 ms                                                | 9.96 ms: 1.07x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 227 us: 1.07x faster                                                 |
| deltablue                  | 3.92 ms                                                | 3.69 ms: 1.06x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.86 us: 1.06x faster                                                |
| hexiom                     | 6.89 ms                                                | 6.50 ms: 1.06x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.79 ms: 1.06x faster                                                |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                                |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                 |
| logging_format             | 6.81 us                                                | 6.52 us: 1.04x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                |
| unpickle_list              | 5.21 us                                                | 5.05 us: 1.03x faster                                                |
| pickle_dict                | 34.6 us                                                | 33.5 us: 1.03x faster                                                |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                                |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                                 |
| tornado_http               | 98.1 ms                                                | 96.3 ms: 1.02x faster                                                |
| nqueens                    | 87.9 ms                                                | 86.4 ms: 1.02x faster                                                |
| deepcopy_reduce            | 3.22 us                                                | 3.18 us: 1.01x faster                                                |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                 |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                 |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.76 sec: 1.00x faster                                               |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                 |
| pidigits                   | 194 ms                                                 | 197 ms: 1.01x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.57 ms: 1.02x slower                                                |
| pyflate                    | 434 ms                                                 | 442 ms: 1.02x slower                                                 |
| sympy_expand               | 484 ms                                                 | 495 ms: 1.02x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                |
| go                         | 149 ms                                                 | 153 ms: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 861 us: 1.03x slower                                                 |
| chameleon                  | 6.70 ms                                                | 6.93 ms: 1.03x slower                                                |
| dask                       | 365 ms                                                 | 378 ms: 1.03x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                |
| pickle_list                | 4.59 us                                                | 4.75 us: 1.04x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 57.4 ms: 1.04x slower                                                |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                 |
| html5lib                   | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                |
| thrift                     | 784 us                                                 | 822 us: 1.05x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 60.1 ms: 1.06x slower                                                |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 69.1 ms: 1.07x slower                                                |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.07x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 87.1 ms: 1.07x slower                                                |
| django_template            | 33.5 ms                                                | 36.2 ms: 1.08x slower                                                |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.08x slower                                                 |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                               |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                |
| genshi_text                | 22.5 ms                                                | 24.7 ms: 1.10x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.11x slower                                                |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                |
| mypy2                      | 686 ms                                                 | 790 ms: 1.15x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                |
| async_generators           | 374 ms                                                 | 469 ms: 1.25x slower                                                 |
| python_startup_no_site     | 6.01 ms                                                | 7.57 ms: 1.26x slower                                                |
| telco                      | 6.86 ms                                                | 8.69 ms: 1.27x slower                                                |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.28x slower                                                |
| coverage                   | 78.8 ms                                                | 104 ms: 1.32x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                         |

Benchmark hidden because not significant (5): pprint_pformat, pycparser, pprint_safe_repr, meteor_contest, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.19% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x