# Results vs. 3.12.0

- fork: python
- ref: c7e7bfc4ca26bf90e0d4
- machine: linux-x86_64
- commit hash: c7e7bfc
- commit date: 2024-04-29
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 267 ms: 1.03x faster                                                   |
| chameleon      | 7.41 ms                                                | 6.95 ms: 1.07x faster                                                  |
| docutils       | 2.77 sec                                               | 2.81 sec: 1.01x slower                                                 |
| tornado_http   | 103 ms                                                 | 93.6 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 331 ms: 1.36x faster                                                   |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 436 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 935 ms: 1.26x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 927 ms: 1.25x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.19x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.1 ms: 1.10x faster                                                  |
| float          | 84.7 ms                                                | 78.0 ms: 1.09x faster                                                  |
| pidigits       | 187 ms                                                 | 212 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.65 ms: 1.01x slower                                                  |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                   |
| regex_v8       | 23.1 ms                                                | 24.9 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.14 sec: 1.09x faster                                                 |
| unpickle_pure_python | 230 us                                                 | 212 us: 1.08x faster                                                   |
| pickle_pure_python   | 324 us                                                 | 301 us: 1.08x faster                                                   |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                  |
| json_loads           | 28.5 us                                                | 27.3 us: 1.04x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 59.4 ms: 1.04x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 86.3 ms: 1.03x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.17 us: 1.02x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                                  |
| pickle_dict          | 35.5 us                                                | 35.4 us: 1.00x faster                                                  |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.03x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                  |
| django_template | 34.6 ms                                                | 35.0 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 331 ms: 1.36x faster                                                   |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 436 ms: 1.32x faster                                                   |
| comprehensions             | 21.8 us                                                | 16.9 us: 1.29x faster                                                  |
| async_tree_io_tg           | 1.18 sec                                               | 935 ms: 1.26x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 927 ms: 1.25x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                   |
| raytrace                   | 312 ms                                                 | 261 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.19x faster                                                   |
| deltablue                  | 3.72 ms                                                | 3.21 ms: 1.16x faster                                                  |
| logging_format             | 7.23 us                                                | 6.33 us: 1.14x faster                                                  |
| mypy2                      | 830 ms                                                 | 732 ms: 1.13x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.73 us: 1.13x faster                                                  |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                   |
| chaos                      | 67.0 ms                                                | 60.4 ms: 1.11x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 153 ms: 1.10x faster                                                   |
| nbody                      | 97.0 ms                                                | 88.1 ms: 1.10x faster                                                  |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                  |
| tornado_http               | 103 ms                                                 | 93.6 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 68.6 ms: 1.10x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 74.7 ms: 1.10x faster                                                  |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                  |
| tomli_loads                | 2.33 sec                                               | 2.14 sec: 1.09x faster                                                 |
| float                      | 84.7 ms                                                | 78.0 ms: 1.09x faster                                                  |
| unpickle_pure_python       | 230 us                                                 | 212 us: 1.08x faster                                                   |
| fannkuch                   | 417 ms                                                 | 385 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 37.6 us: 1.08x faster                                                  |
| sympy_str                  | 300 ms                                                 | 277 ms: 1.08x faster                                                   |
| pickle_pure_python         | 324 us                                                 | 301 us: 1.08x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.07x faster                                                  |
| chameleon                  | 7.41 ms                                                | 6.95 ms: 1.07x faster                                                  |
| sympy_integrate            | 21.4 ms                                                | 20.1 ms: 1.06x faster                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                  |
| scimark_sor                | 129 ms                                                 | 122 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 776 ms                                                 | 732 ms: 1.06x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                  |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                                   |
| hexiom                     | 6.41 ms                                                | 6.13 ms: 1.05x faster                                                  |
| pyflate                    | 482 ms                                                 | 461 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                  |
| json_loads                 | 28.5 us                                                | 27.3 us: 1.04x faster                                                  |
| generators                 | 31.2 ms                                                | 29.9 ms: 1.04x faster                                                  |
| scimark_fft                | 382 ms                                                 | 366 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                 |
| xml_etree_process          | 61.7 ms                                                | 59.4 ms: 1.04x faster                                                  |
| async_generators           | 463 ms                                                 | 446 ms: 1.04x faster                                                   |
| dulwich_log                | 68.5 ms                                                | 66.1 ms: 1.04x faster                                                  |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.04x faster                                                  |
| spectral_norm              | 115 ms                                                 | 111 ms: 1.03x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 86.3 ms: 1.03x faster                                                  |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                   |
| sympy_expand               | 478 ms                                                 | 464 ms: 1.03x faster                                                   |
| scimark_lu                 | 118 ms                                                 | 115 ms: 1.03x faster                                                   |
| json                       | 5.26 ms                                                | 5.13 ms: 1.03x faster                                                  |
| 2to3                       | 274 ms                                                 | 267 ms: 1.03x faster                                                   |
| pycparser                  | 1.18 sec                                               | 1.15 sec: 1.02x faster                                                 |
| gc_traversal               | 3.79 ms                                                | 3.70 ms: 1.02x faster                                                  |
| unpickle_list              | 5.29 us                                                | 5.17 us: 1.02x faster                                                  |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                                   |
| dask                       | 372 ms                                                 | 365 ms: 1.02x faster                                                   |
| bench_thread_pool          | 842 us                                                 | 827 us: 1.02x faster                                                   |
| pickle_list                | 5.08 us                                                | 5.00 us: 1.02x faster                                                  |
| nqueens                    | 83.3 ms                                                | 81.9 ms: 1.02x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.6 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 54.6 ms: 1.00x faster                                                  |
| pickle_dict                | 35.5 us                                                | 35.4 us: 1.00x faster                                                  |
| aiohttp                    | 1.15 ms                                                | 1.16 ms: 1.01x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.65 ms: 1.01x slower                                                  |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| django_template            | 34.6 ms                                                | 35.0 ms: 1.01x slower                                                  |
| docutils                   | 2.77 sec                                               | 2.81 sec: 1.01x slower                                                 |
| go                         | 139 ms                                                 | 142 ms: 1.01x slower                                                   |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.02x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 2.92 us: 1.03x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                 |
| richards                   | 45.8 ms                                                | 47.3 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.22 ms: 1.03x slower                                                  |
| typing_runtime_protocols   | 158 us                                                 | 164 us: 1.04x slower                                                   |
| richards_super             | 51.5 ms                                                | 53.7 ms: 1.04x slower                                                  |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 24.9 ms: 1.08x slower                                                  |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| pidigits                   | 187 ms                                                 | 212 ms: 1.13x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                | 1.74 ms: 1.18x slower                                                  |
| telco                      | 7.10 ms                                                | 8.62 ms: 1.21x slower                                                  |
| coverage                   | 72.7 ms                                                | 91.0 ms: 1.25x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, mdp
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240429-3.13.0a6+-c7e7bfc/bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x