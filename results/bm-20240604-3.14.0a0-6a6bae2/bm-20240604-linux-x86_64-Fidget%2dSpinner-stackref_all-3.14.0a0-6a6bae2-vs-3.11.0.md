# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: stackref_all
- machine: linux-x86_64
- commit hash: 6a6bae2
- commit date: 2024-06-04
- overall geometric mean: 1.07x faster
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                    |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                  |
| html5lib       | 64.8 ms                                                | 67.1 ms: 1.03x slower                                                   |
| tornado_http   | 98.1 ms                                                | 94.0 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 902 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                    |
| async_tree_none            | 528 ms                                                 | 373 ms: 1.41x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 946 ms: 1.36x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 470 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 621 ms: 1.21x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                   |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| float          | 78.9 ms                                                | 77.8 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.04x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                   |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                    |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.09x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                    |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.6 us: 1.03x slower                                                   |
| unpickle_list        | 5.21 us                                                | 5.42 us: 1.04x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 85.8 ms: 1.06x slower                                                   |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                   |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.06 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.13 ms: 1.19x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.0 ms: 1.03x faster                                                   |
| genshi_text     | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                   |
| django_template | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                   |
| mako            | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-6a6bae2 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                    |
| generators                 | 74.9 ms                                                | 29.5 ms: 2.54x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 501 ms: 1.75x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                  |
| pylint                     | 476 ms                                                 | 315 ms: 1.51x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 902 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                    |
| async_tree_none            | 528 ms                                                 | 373 ms: 1.41x faster                                                    |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.40x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 946 ms: 1.36x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 470 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 621 ms: 1.21x faster                                                    |
| deltablue                  | 3.92 ms                                                | 3.25 ms: 1.21x faster                                                   |
| chaos                      | 71.9 ms                                                | 59.7 ms: 1.20x faster                                                   |
| raytrace                   | 309 ms                                                 | 263 ms: 1.17x faster                                                    |
| coroutines                 | 27.0 ms                                                | 23.4 ms: 1.15x faster                                                   |
| richards_super             | 61.9 ms                                                | 54.0 ms: 1.15x faster                                                   |
| pathlib                    | 18.5 ms                                                | 16.3 ms: 1.14x faster                                                   |
| logging_silent             | 111 ns                                                 | 99.6 ns: 1.11x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                   |
| nqueens                    | 87.9 ms                                                | 80.2 ms: 1.10x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.29 ms: 1.09x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.09x faster                                                    |
| logging_simple             | 6.22 us                                                | 5.69 us: 1.09x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                    |
| nbody                      | 96.0 ms                                                | 88.1 ms: 1.09x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.61 ms: 1.08x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                  |
| logging_format             | 6.81 us                                                | 6.36 us: 1.07x faster                                                   |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                    |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.81 ms: 1.05x faster                                                   |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                                    |
| regex_compile              | 141 ms                                                 | 135 ms: 1.04x faster                                                    |
| tornado_http               | 98.1 ms                                                | 94.0 ms: 1.04x faster                                                   |
| richards                   | 49.8 ms                                                | 47.7 ms: 1.04x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 73.7 ms: 1.04x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 68.5 ms: 1.03x faster                                                   |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                    |
| genshi_xml                 | 53.4 ms                                                | 52.0 ms: 1.03x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                   |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.94 ms: 1.02x faster                                                   |
| float                      | 78.9 ms                                                | 77.8 ms: 1.02x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.73 sec: 1.02x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                  |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                                   |
| fannkuch                   | 405 ms                                                 | 403 ms: 1.00x faster                                                    |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                    |
| deepcopy                   | 365 us                                                 | 367 us: 1.00x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 65.0 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 747 ms                                                 | 753 ms: 1.01x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                  |
| json                       | 5.24 ms                                                | 5.35 ms: 1.02x slower                                                   |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                    |
| thrift                     | 784 us                                                 | 805 us: 1.03x slower                                                    |
| pickle_dict                | 34.6 us                                                | 35.6 us: 1.03x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.32 us: 1.03x slower                                                   |
| genshi_text                | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                    |
| html5lib                   | 64.8 ms                                                | 67.1 ms: 1.03x slower                                                   |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.04x slower                                                    |
| django_template            | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                   |
| unpickle_list              | 5.21 us                                                | 5.42 us: 1.04x slower                                                   |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                                    |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 85.8 ms: 1.06x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                   |
| mako                       | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                   |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                   |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                   |
| scimark_fft                | 345 ms                                                 | 379 ms: 1.10x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.06 us: 1.10x slower                                                   |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.15x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.97 us: 1.15x slower                                                   |
| coverage                   | 78.8 ms                                                | 92.5 ms: 1.17x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.13 ms: 1.19x slower                                                   |
| async_generators           | 374 ms                                                 | 447 ms: 1.20x slower                                                    |
| telco                      | 6.86 ms                                                | 8.36 ms: 1.22x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (5): bench_mp_pool, xml_etree_iterparse, bench_thread_pool, scimark_lu, dask
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.69% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x