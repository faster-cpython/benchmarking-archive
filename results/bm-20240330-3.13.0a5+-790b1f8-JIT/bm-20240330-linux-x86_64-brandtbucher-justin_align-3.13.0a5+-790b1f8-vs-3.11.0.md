# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.02x faster
- HPT reliability: 83.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.06x slower                                                 |
| chameleon      | 6.70 ms                                                | 7.22 ms: 1.08x slower                                                |
| docutils       | 2.66 sec                                               | 2.91 sec: 1.09x slower                                               |
| html5lib       | 64.8 ms                                                | 66.7 ms: 1.03x slower                                                |
| tornado_http   | 98.1 ms                                                | 97.5 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 345 ms: 1.42x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 922 ms: 1.40x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 952 ms: 1.35x faster                                                 |
| async_tree_none            | 528 ms                                                 | 394 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 603 ms: 1.24x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 93.6 ms: 1.03x faster                                                |
| pidigits       | 194 ms                                                 | 189 ms: 1.02x faster                                                 |
| float          | 78.9 ms                                                | 78.4 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 153 ms: 1.08x slower                                                 |
| regex_effbot   | 3.51 ms                                                | 3.82 ms: 1.09x slower                                                |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                                 |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.09x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                               |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.04x faster                                                 |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                 |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                |
| pickle_dict          | 34.6 us                                                | 34.1 us: 1.01x faster                                                |
| unpickle_pure_python | 242 us                                                 | 251 us: 1.04x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                |
| pickle               | 11.0 us                                                | 11.8 us: 1.08x slower                                                |
| pickle_list          | 4.59 us                                                | 4.96 us: 1.08x slower                                                |
| xml_etree_generate   | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                |
| unpickle             | 13.8 us                                                | 15.2 us: 1.09x slower                                                |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                |
| python_startup_no_site | 6.01 ms                                                | 9.51 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                |
| mako            | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                |
| django_template | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                |
| genshi_text     | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.57x faster                                                 |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.48x faster                                                |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                                 |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                               |
| pylint                     | 476 ms                                                 | 300 ms: 1.58x faster                                                 |
| async_tree_none_tg         | 491 ms                                                 | 345 ms: 1.42x faster                                                 |
| async_tree_io_tg           | 1.29 sec                                               | 922 ms: 1.40x faster                                                 |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                                 |
| async_tree_io              | 1.29 sec                                               | 952 ms: 1.35x faster                                                 |
| async_tree_none            | 528 ms                                                 | 394 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 603 ms: 1.24x faster                                                 |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                |
| comprehensions             | 23.6 us                                                | 19.3 us: 1.23x faster                                                |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                |
| richards_super             | 61.9 ms                                                | 54.6 ms: 1.13x faster                                                |
| deltablue                  | 3.92 ms                                                | 3.50 ms: 1.12x faster                                                |
| logging_silent             | 111 ns                                                 | 99.6 ns: 1.12x faster                                                |
| chaos                      | 71.9 ms                                                | 64.4 ms: 1.12x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.71 ms: 1.08x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.07x faster                                                |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.06x faster                                                |
| djangocms                  | 33.5 us                                                | 31.8 us: 1.05x faster                                                |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.04x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                               |
| raytrace                   | 309 ms                                                 | 296 ms: 1.04x faster                                                 |
| logging_simple             | 6.22 us                                                | 5.98 us: 1.04x faster                                                |
| logging_format             | 6.81 us                                                | 6.55 us: 1.04x faster                                                |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                 |
| nbody                      | 96.0 ms                                                | 93.6 ms: 1.03x faster                                                |
| pidigits                   | 194 ms                                                 | 189 ms: 1.02x faster                                                 |
| richards                   | 49.8 ms                                                | 48.7 ms: 1.02x faster                                                |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                |
| pickle_dict                | 34.6 us                                                | 34.1 us: 1.01x faster                                                |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                 |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                 |
| float                      | 78.9 ms                                                | 78.4 ms: 1.01x faster                                                |
| tornado_http               | 98.1 ms                                                | 97.5 ms: 1.01x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 40.0 us: 1.00x faster                                                |
| deepcopy                   | 365 us                                                 | 364 us: 1.00x faster                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.23 us: 1.00x slower                                                |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.09 ms: 1.01x slower                                                |
| fannkuch                   | 405 ms                                                 | 411 ms: 1.01x slower                                                 |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                |
| json                       | 5.24 ms                                                | 5.36 ms: 1.02x slower                                                |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 857 us: 1.03x slower                                                 |
| html5lib                   | 64.8 ms                                                | 66.7 ms: 1.03x slower                                                |
| sympy_expand               | 484 ms                                                 | 499 ms: 1.03x slower                                                 |
| dask                       | 365 ms                                                 | 377 ms: 1.03x slower                                                 |
| scimark_fft                | 345 ms                                                 | 357 ms: 1.03x slower                                                 |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                 |
| pathlib                    | 18.5 ms                                                | 19.2 ms: 1.04x slower                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 73.3 ms: 1.04x slower                                                |
| unpickle_pure_python       | 242 us                                                 | 251 us: 1.04x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 55.4 ms: 1.04x slower                                                |
| pprint_pformat             | 1.55 sec                                               | 1.61 sec: 1.04x slower                                               |
| sqlglot_optimize           | 55.3 ms                                                | 57.8 ms: 1.05x slower                                                |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                                 |
| 2to3                       | 264 ms                                                 | 281 ms: 1.06x slower                                                 |
| nqueens                    | 87.9 ms                                                | 93.4 ms: 1.06x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                |
| mako                       | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                |
| pprint_safe_repr           | 747 ms                                                 | 798 ms: 1.07x slower                                                 |
| go                         | 149 ms                                                 | 159 ms: 1.07x slower                                                 |
| django_template            | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                |
| pickle                     | 11.0 us                                                | 11.8 us: 1.08x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.22 ms: 1.08x slower                                                |
| pickle_list                | 4.59 us                                                | 4.96 us: 1.08x slower                                                |
| regex_compile              | 141 ms                                                 | 153 ms: 1.08x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                |
| regex_effbot               | 3.51 ms                                                | 3.82 ms: 1.09x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                |
| docutils                   | 2.66 sec                                               | 2.91 sec: 1.09x slower                                               |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.09x slower                                                |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                                 |
| hexiom                     | 6.89 ms                                                | 7.56 ms: 1.10x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                 |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                                |
| dulwich_log                | 64.6 ms                                                | 71.4 ms: 1.11x slower                                                |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                |
| spectral_norm              | 108 ms                                                 | 121 ms: 1.12x slower                                                 |
| scimark_lu                 | 116 ms                                                 | 134 ms: 1.15x slower                                                 |
| mypy2                      | 686 ms                                                 | 792 ms: 1.16x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.66 ms: 1.16x slower                                                |
| pyflate                    | 434 ms                                                 | 505 ms: 1.16x slower                                                 |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                 |
| coverage                   | 78.8 ms                                                | 97.8 ms: 1.24x slower                                                |
| telco                      | 6.86 ms                                                | 8.68 ms: 1.27x slower                                                |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 9.51 ms: 1.58x slower                                                |
| unpack_sequence            | 43.5 ns                                                | 125 ns: 2.87x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (5): unpickle_list, xml_etree_iterparse, pycparser, bench_mp_pool, crypto_pyaes
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 83.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x