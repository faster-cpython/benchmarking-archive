# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.05x faster
- HPT reliability: 91.31%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.05x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.05 ms: 1.05x slower                                                |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                               |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                |
| tornado_http   | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.49x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 907 ms: 1.43x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 450 ms: 1.42x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 929 ms: 1.38x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 599 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.0 ms: 1.10x faster                                                |
| float          | 78.9 ms                                                | 72.8 ms: 1.08x faster                                                |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 143 ms: 1.01x slower                                                 |
| regex_effbot   | 3.51 ms                                                | 3.63 ms: 1.03x slower                                                |
| regex_dna      | 205 ms                                                 | 219 ms: 1.07x slower                                                 |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.02 sec: 1.14x faster                                               |
| unpickle_pure_python | 242 us                                                 | 229 us: 1.06x faster                                                 |
| pickle_pure_python   | 320 us                                                 | 308 us: 1.04x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                 |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                                |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                |
| pickle               | 11.0 us                                                | 11.8 us: 1.08x slower                                                |
| pickle_list          | 4.59 us                                                | 4.97 us: 1.08x slower                                                |
| unpickle             | 13.8 us                                                | 15.2 us: 1.09x slower                                                |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                |
| python_startup_no_site | 6.01 ms                                                | 9.49 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.96 ms: 1.07x faster                                                |
| genshi_xml      | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                |
| django_template | 33.5 ms                                                | 36.4 ms: 1.08x slower                                                |
| genshi_text     | 22.5 ms                                                | 24.9 ms: 1.10x slower                                                |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.57x faster                                                 |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.71x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                               |
| pylint                     | 476 ms                                                 | 299 ms: 1.59x faster                                                 |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.49x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 907 ms: 1.43x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 450 ms: 1.42x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 929 ms: 1.38x faster                                                 |
| comprehensions             | 23.6 us                                                | 17.4 us: 1.35x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 599 ms: 1.27x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.21x faster                                                |
| richards_super             | 61.9 ms                                                | 51.7 ms: 1.20x faster                                                |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.33 ms: 1.16x faster                                                |
| tomli_loads                | 2.30 sec                                               | 2.02 sec: 1.14x faster                                               |
| deltablue                  | 3.92 ms                                                | 3.48 ms: 1.13x faster                                                |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                 |
| fannkuch                   | 405 ms                                                 | 367 ms: 1.10x faster                                                 |
| nbody                      | 96.0 ms                                                | 87.0 ms: 1.10x faster                                                |
| crypto_pyaes               | 76.7 ms                                                | 70.1 ms: 1.09x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 64.9 ms: 1.09x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.69 ms: 1.09x faster                                                |
| float                      | 78.9 ms                                                | 72.8 ms: 1.08x faster                                                |
| richards                   | 49.8 ms                                                | 46.0 ms: 1.08x faster                                                |
| scimark_fft                | 345 ms                                                 | 319 ms: 1.08x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                |
| spectral_norm              | 108 ms                                                 | 101 ms: 1.07x faster                                                 |
| djangocms                  | 33.5 us                                                | 31.3 us: 1.07x faster                                                |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                 |
| mako                       | 10.7 ms                                                | 9.96 ms: 1.07x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 229 us: 1.06x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.64 sec: 1.05x faster                                               |
| logging_simple             | 6.22 us                                                | 5.94 us: 1.05x faster                                                |
| pickle_pure_python         | 320 us                                                 | 308 us: 1.04x faster                                                 |
| logging_format             | 6.81 us                                                | 6.57 us: 1.04x faster                                                |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                               |
| sympy_sum                  | 169 ms                                                 | 164 ms: 1.03x faster                                                 |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                 |
| sympy_str                  | 297 ms                                                 | 291 ms: 1.02x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                 |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                |
| pprint_safe_repr           | 747 ms                                                 | 738 ms: 1.01x faster                                                 |
| tornado_http               | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                |
| deepcopy                   | 365 us                                                 | 363 us: 1.01x faster                                                 |
| regex_compile              | 141 ms                                                 | 143 ms: 1.01x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 21.7 ms: 1.01x slower                                                |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                 |
| sympy_expand               | 484 ms                                                 | 497 ms: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 858 us: 1.03x slower                                                 |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                                |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                 |
| regex_effbot               | 3.51 ms                                                | 3.63 ms: 1.03x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                |
| nqueens                    | 87.9 ms                                                | 91.2 ms: 1.04x slower                                                |
| pyflate                    | 434 ms                                                 | 451 ms: 1.04x slower                                                 |
| 2to3                       | 264 ms                                                 | 276 ms: 1.05x slower                                                 |
| thrift                     | 784 us                                                 | 821 us: 1.05x slower                                                 |
| json                       | 5.24 ms                                                | 5.50 ms: 1.05x slower                                                |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.05 ms: 1.05x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 58.7 ms: 1.06x slower                                                |
| go                         | 149 ms                                                 | 158 ms: 1.06x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                |
| regex_dna                  | 205 ms                                                 | 219 ms: 1.07x slower                                                 |
| pickle                     | 11.0 us                                                | 11.8 us: 1.08x slower                                                |
| pickle_list                | 4.59 us                                                | 4.97 us: 1.08x slower                                                |
| django_template            | 33.5 ms                                                | 36.4 ms: 1.08x slower                                                |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                               |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.09x slower                                                |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                                |
| genshi_text                | 22.5 ms                                                | 24.9 ms: 1.10x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.11x slower                                                |
| dulwich_log                | 64.6 ms                                                | 71.6 ms: 1.11x slower                                                |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                                 |
| scimark_lu                 | 116 ms                                                 | 130 ms: 1.12x slower                                                 |
| mypy2                      | 686 ms                                                 | 794 ms: 1.16x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.66 ms: 1.16x slower                                                |
| coverage                   | 78.8 ms                                                | 96.9 ms: 1.23x slower                                                |
| telco                      | 6.86 ms                                                | 8.55 ms: 1.25x slower                                                |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                 |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 9.49 ms: 1.58x slower                                                |
| unpack_sequence            | 43.5 ns                                                | 115 ns: 2.64x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (7): deepcopy_memo, hexiom, bench_mp_pool, meteor_contest, unpickle_list, deepcopy_reduce, pycparser
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 91.31% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x