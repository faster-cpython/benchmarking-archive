# Results vs. 3.11.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.03x faster
- HPT reliability: 54.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.06x slower                                              |
| chameleon      | 6.70 ms                                                | 7.19 ms: 1.07x slower                                             |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                            |
| html5lib       | 64.8 ms                                                | 66.8 ms: 1.03x slower                                             |
| tornado_http   | 98.1 ms                                                | 97.1 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                              |
| async_tree_none            | 528 ms                                                 | 391 ms: 1.35x faster                                              |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.35x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 601 ms: 1.25x faster                                              |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.6 ms: 1.06x faster                                             |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                              |
| float          | 78.9 ms                                                | 77.1 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 146 ms: 1.03x slower                                              |
| regex_effbot   | 3.51 ms                                                | 3.84 ms: 1.10x slower                                             |
| regex_dna      | 205 ms                                                 | 230 ms: 1.13x slower                                              |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                             |
| tomli_loads          | 2.30 sec                                               | 2.07 sec: 1.11x faster                                            |
| pickle_pure_python   | 320 us                                                 | 308 us: 1.04x faster                                              |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                             |
| unpickle_pure_python | 242 us                                                 | 245 us: 1.01x slower                                              |
| unpickle_list        | 5.21 us                                                | 5.38 us: 1.03x slower                                             |
| pickle_list          | 4.59 us                                                | 4.93 us: 1.07x slower                                             |
| xml_etree_process    | 56.9 ms                                                | 61.7 ms: 1.08x slower                                             |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                             |
| xml_etree_generate   | 81.1 ms                                                | 89.7 ms: 1.11x slower                                             |
| unpickle             | 13.8 us                                                | 15.7 us: 1.13x slower                                             |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                             |
| python_startup_no_site | 6.01 ms                                                | 9.49 ms: 1.58x slower                                             |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.7 ms: 1.00x slower                                             |
| genshi_xml      | 53.4 ms                                                | 56.4 ms: 1.06x slower                                             |
| django_template | 33.5 ms                                                | 36.5 ms: 1.09x slower                                             |
| genshi_text     | 22.5 ms                                                | 25.4 ms: 1.13x slower                                             |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.45x faster                                              |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                             |
| asyncio_tcp                | 875 ms                                                 | 511 ms: 1.71x faster                                              |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                            |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                              |
| pylint                     | 476 ms                                                 | 338 ms: 1.41x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 454 ms: 1.38x faster                                              |
| async_tree_none            | 528 ms                                                 | 391 ms: 1.35x faster                                              |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.35x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                              |
| comprehensions             | 23.6 us                                                | 18.3 us: 1.29x faster                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 601 ms: 1.25x faster                                              |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.20x faster                                             |
| richards_super             | 61.9 ms                                                | 53.9 ms: 1.15x faster                                             |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.11x faster                                            |
| chaos                      | 71.9 ms                                                | 65.8 ms: 1.09x faster                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.35 ms: 1.06x faster                                             |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                             |
| nbody                      | 96.0 ms                                                | 90.6 ms: 1.06x faster                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.06x faster                                             |
| richards                   | 49.8 ms                                                | 47.3 ms: 1.05x faster                                             |
| djangocms                  | 33.5 us                                                | 32.0 us: 1.05x faster                                             |
| logging_simple             | 6.22 us                                                | 5.98 us: 1.04x faster                                             |
| mdp                        | 2.77 sec                                               | 2.67 sec: 1.04x faster                                            |
| raytrace                   | 309 ms                                                 | 297 ms: 1.04x faster                                              |
| pickle_pure_python         | 320 us                                                 | 308 us: 1.04x faster                                              |
| logging_format             | 6.81 us                                                | 6.61 us: 1.03x faster                                             |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                              |
| crypto_pyaes               | 76.7 ms                                                | 74.6 ms: 1.03x faster                                             |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                              |
| float                      | 78.9 ms                                                | 77.1 ms: 1.02x faster                                             |
| fannkuch                   | 405 ms                                                 | 396 ms: 1.02x faster                                              |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                             |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                              |
| sympy_str                  | 297 ms                                                 | 292 ms: 1.02x faster                                              |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.96 ms: 1.01x faster                                             |
| deepcopy_memo              | 40.2 us                                                | 39.7 us: 1.01x faster                                             |
| deepcopy                   | 365 us                                                 | 361 us: 1.01x faster                                              |
| tornado_http               | 98.1 ms                                                | 97.1 ms: 1.01x faster                                             |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                             |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                              |
| unpickle_pure_python       | 242 us                                                 | 245 us: 1.01x slower                                              |
| pprint_safe_repr           | 747 ms                                                 | 759 ms: 1.02x slower                                              |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                             |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                              |
| json                       | 5.24 ms                                                | 5.36 ms: 1.02x slower                                             |
| bench_thread_pool          | 834 us                                                 | 856 us: 1.03x slower                                              |
| sympy_expand               | 484 ms                                                 | 498 ms: 1.03x slower                                              |
| html5lib                   | 64.8 ms                                                | 66.8 ms: 1.03x slower                                             |
| unpickle_list              | 5.21 us                                                | 5.38 us: 1.03x slower                                             |
| go                         | 149 ms                                                 | 153 ms: 1.03x slower                                              |
| nqueens                    | 87.9 ms                                                | 90.7 ms: 1.03x slower                                             |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                              |
| regex_compile              | 141 ms                                                 | 146 ms: 1.03x slower                                              |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                             |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                              |
| dask                       | 365 ms                                                 | 378 ms: 1.04x slower                                              |
| hexiom                     | 6.89 ms                                                | 7.15 ms: 1.04x slower                                             |
| pycparser                  | 1.19 sec                                               | 1.23 sec: 1.04x slower                                            |
| sqlglot_optimize           | 55.3 ms                                                | 58.0 ms: 1.05x slower                                             |
| genshi_xml                 | 53.4 ms                                                | 56.4 ms: 1.06x slower                                             |
| 2to3                       | 264 ms                                                 | 281 ms: 1.06x slower                                              |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                              |
| chameleon                  | 6.70 ms                                                | 7.19 ms: 1.07x slower                                             |
| pickle_list                | 4.59 us                                                | 4.93 us: 1.07x slower                                             |
| xml_etree_process          | 56.9 ms                                                | 61.7 ms: 1.08x slower                                             |
| django_template            | 33.5 ms                                                | 36.5 ms: 1.09x slower                                             |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                             |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                             |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                             |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.09x slower                                              |
| dulwich_log                | 64.6 ms                                                | 70.7 ms: 1.09x slower                                             |
| regex_effbot               | 3.51 ms                                                | 3.84 ms: 1.10x slower                                             |
| xml_etree_generate         | 81.1 ms                                                | 89.7 ms: 1.11x slower                                             |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                             |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.13x slower                                              |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                             |
| genshi_text                | 22.5 ms                                                | 25.4 ms: 1.13x slower                                             |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.13x slower                                             |
| pyflate                    | 434 ms                                                 | 492 ms: 1.13x slower                                              |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.14x slower                                              |
| mypy2                      | 686 ms                                                 | 791 ms: 1.15x slower                                              |
| create_gc_cycles           | 1.43 ms                                                | 1.69 ms: 1.18x slower                                             |
| async_generators           | 374 ms                                                 | 466 ms: 1.25x slower                                              |
| coverage                   | 78.8 ms                                                | 99.8 ms: 1.27x slower                                             |
| telco                      | 6.86 ms                                                | 8.71 ms: 1.27x slower                                             |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                             |
| python_startup_no_site     | 6.01 ms                                                | 9.49 ms: 1.58x slower                                             |
| unpack_sequence            | 43.5 ns                                                | 86.2 ns: 1.98x slower                                             |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (9): xml_etree_parse, pprint_pformat, xml_etree_iterparse, deepcopy_reduce, bench_mp_pool, scimark_fft, pickle_dict, deltablue, scimark_monte_carlo
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 54.05% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x