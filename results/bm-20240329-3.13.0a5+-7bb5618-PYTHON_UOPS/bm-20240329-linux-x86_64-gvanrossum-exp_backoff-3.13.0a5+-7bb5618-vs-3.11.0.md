# Results vs. 3.11.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 316 ms: 1.20x slower                                              |
| chameleon      | 6.70 ms                                                | 7.81 ms: 1.17x slower                                             |
| docutils       | 2.66 sec                                               | 3.13 sec: 1.17x slower                                            |
| html5lib       | 64.8 ms                                                | 72.2 ms: 1.11x slower                                             |
| tornado_http   | 98.1 ms                                                | 104 ms: 1.06x slower                                              |
| Geometric mean | (ref)                                                  | 1.14x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 369 ms: 1.33x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 984 ms: 1.31x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 487 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 482 ms: 1.30x faster                                              |
| async_tree_io              | 1.29 sec                                               | 1.01 sec: 1.28x faster                                            |
| async_tree_none            | 528 ms                                                 | 421 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.19x faster                                              |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 192 ms: 1.01x faster                                              |
| float          | 78.9 ms                                                | 99.2 ms: 1.26x slower                                             |
| nbody          | 96.0 ms                                                | 130 ms: 1.36x slower                                              |
| Geometric mean | (ref)                                                  | 1.19x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.63 ms: 1.03x slower                                             |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                              |
| regex_v8       | 22.9 ms                                                | 26.5 ms: 1.16x slower                                             |
| regex_compile  | 141 ms                                                 | 196 ms: 1.38x slower                                              |
| Geometric mean | (ref)                                                  | 1.16x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.23x faster                                             |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                             |
| pickle_pure_python   | 320 us                                                 | 322 us: 1.01x slower                                              |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.02x slower                                             |
| unpickle_list        | 5.21 us                                                | 5.39 us: 1.03x slower                                             |
| xml_etree_iterparse  | 108 ms                                                 | 116 ms: 1.07x slower                                              |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                             |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                             |
| pickle_list          | 4.59 us                                                | 5.23 us: 1.14x slower                                             |
| xml_etree_process    | 56.9 ms                                                | 66.3 ms: 1.17x slower                                             |
| tomli_loads          | 2.30 sec                                               | 2.77 sec: 1.20x slower                                            |
| xml_etree_generate   | 81.1 ms                                                | 98.8 ms: 1.22x slower                                             |
| unpickle_pure_python | 242 us                                                 | 316 us: 1.30x slower                                              |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.8 ms: 1.26x slower                                             |
| python_startup_no_site | 6.01 ms                                                | 9.17 ms: 1.53x slower                                             |
| Geometric mean         | (ref)                                                  | 1.39x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 64.2 ms: 1.20x slower                                             |
| genshi_text     | 22.5 ms                                                | 27.4 ms: 1.21x slower                                             |
| django_template | 33.5 ms                                                | 42.2 ms: 1.26x slower                                             |
| mako            | 10.7 ms                                                | 13.8 ms: 1.30x slower                                             |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 127 us: 4.09x faster                                              |
| generators                 | 74.9 ms                                                | 30.9 ms: 2.43x faster                                             |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                              |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                            |
| pylint                     | 476 ms                                                 | 354 ms: 1.34x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 369 ms: 1.33x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 984 ms: 1.31x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 487 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 482 ms: 1.30x faster                                              |
| async_tree_io              | 1.29 sec                                               | 1.01 sec: 1.28x faster                                            |
| async_tree_none            | 528 ms                                                 | 421 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                              |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.23x faster                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.19x faster                                              |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.18x faster                                             |
| gc_traversal               | 4.01 ms                                                | 3.74 ms: 1.07x faster                                             |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                             |
| pidigits                   | 194 ms                                                 | 192 ms: 1.01x faster                                              |
| pickle_pure_python         | 320 us                                                 | 322 us: 1.01x slower                                              |
| logging_silent             | 111 ns                                                 | 112 ns: 1.01x slower                                              |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.02x slower                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                             |
| unpickle_list              | 5.21 us                                                | 5.39 us: 1.03x slower                                             |
| regex_effbot               | 3.51 ms                                                | 3.63 ms: 1.03x slower                                             |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                              |
| json                       | 5.24 ms                                                | 5.49 ms: 1.05x slower                                             |
| comprehensions             | 23.6 us                                                | 24.7 us: 1.05x slower                                             |
| dask                       | 365 ms                                                 | 386 ms: 1.06x slower                                              |
| tornado_http               | 98.1 ms                                                | 104 ms: 1.06x slower                                              |
| thrift                     | 784 us                                                 | 834 us: 1.06x slower                                              |
| xml_etree_iterparse        | 108 ms                                                 | 116 ms: 1.07x slower                                              |
| deepcopy                   | 365 us                                                 | 392 us: 1.07x slower                                              |
| sqlglot_transpile          | 1.75 ms                                                | 1.89 ms: 1.08x slower                                             |
| sympy_sum                  | 169 ms                                                 | 182 ms: 1.08x slower                                              |
| logging_format             | 6.81 us                                                | 7.36 us: 1.08x slower                                             |
| logging_simple             | 6.22 us                                                | 6.75 us: 1.08x slower                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.56 ms: 1.09x slower                                             |
| mdp                        | 2.77 sec                                               | 3.02 sec: 1.09x slower                                            |
| bench_thread_pool          | 834 us                                                 | 910 us: 1.09x slower                                              |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                             |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                              |
| html5lib                   | 64.8 ms                                                | 72.2 ms: 1.11x slower                                             |
| sympy_integrate            | 21.5 ms                                                | 24.0 ms: 1.12x slower                                             |
| pathlib                    | 18.5 ms                                                | 20.7 ms: 1.12x slower                                             |
| sympy_str                  | 297 ms                                                 | 335 ms: 1.13x slower                                              |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                             |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                             |
| gunicorn                   | 1.20 ms                                                | 1.37 ms: 1.14x slower                                             |
| pickle_list                | 4.59 us                                                | 5.23 us: 1.14x slower                                             |
| sympy_expand               | 484 ms                                                 | 556 ms: 1.15x slower                                              |
| chaos                      | 71.9 ms                                                | 82.5 ms: 1.15x slower                                             |
| sqlglot_normalize          | 113 ms                                                 | 130 ms: 1.16x slower                                              |
| regex_v8                   | 22.9 ms                                                | 26.5 ms: 1.16x slower                                             |
| xml_etree_process          | 56.9 ms                                                | 66.3 ms: 1.17x slower                                             |
| chameleon                  | 6.70 ms                                                | 7.81 ms: 1.17x slower                                             |
| dulwich_log                | 64.6 ms                                                | 75.5 ms: 1.17x slower                                             |
| meteor_contest             | 109 ms                                                 | 128 ms: 1.17x slower                                              |
| docutils                   | 2.66 sec                                               | 3.13 sec: 1.17x slower                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.69 ms: 1.18x slower                                             |
| deltablue                  | 3.92 ms                                                | 4.66 ms: 1.19x slower                                             |
| 2to3                       | 264 ms                                                 | 316 ms: 1.20x slower                                              |
| genshi_xml                 | 53.4 ms                                                | 64.2 ms: 1.20x slower                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.04 ms: 1.20x slower                                             |
| richards_super             | 61.9 ms                                                | 74.4 ms: 1.20x slower                                             |
| sqlite_synth               | 2.57 us                                                | 3.09 us: 1.20x slower                                             |
| tomli_loads                | 2.30 sec                                               | 2.77 sec: 1.20x slower                                            |
| pycparser                  | 1.19 sec                                               | 1.43 sec: 1.21x slower                                            |
| sqlglot_optimize           | 55.3 ms                                                | 66.9 ms: 1.21x slower                                             |
| mypy2                      | 686 ms                                                 | 830 ms: 1.21x slower                                              |
| genshi_text                | 22.5 ms                                                | 27.4 ms: 1.21x slower                                             |
| xml_etree_generate         | 81.1 ms                                                | 98.8 ms: 1.22x slower                                             |
| crypto_pyaes               | 76.7 ms                                                | 94.4 ms: 1.23x slower                                             |
| deepcopy_memo              | 40.2 us                                                | 49.5 us: 1.23x slower                                             |
| coverage                   | 78.8 ms                                                | 98.5 ms: 1.25x slower                                             |
| float                      | 78.9 ms                                                | 99.2 ms: 1.26x slower                                             |
| django_template            | 33.5 ms                                                | 42.2 ms: 1.26x slower                                             |
| python_startup             | 8.56 ms                                                | 10.8 ms: 1.26x slower                                             |
| fannkuch                   | 405 ms                                                 | 513 ms: 1.26x slower                                              |
| raytrace                   | 309 ms                                                 | 391 ms: 1.27x slower                                              |
| async_generators           | 374 ms                                                 | 483 ms: 1.29x slower                                              |
| mako                       | 10.7 ms                                                | 13.8 ms: 1.30x slower                                             |
| go                         | 149 ms                                                 | 193 ms: 1.30x slower                                              |
| unpickle_pure_python       | 242 us                                                 | 316 us: 1.30x slower                                              |
| scimark_fft                | 345 ms                                                 | 457 ms: 1.32x slower                                              |
| scimark_monte_carlo        | 70.7 ms                                                | 94.1 ms: 1.33x slower                                             |
| richards                   | 49.8 ms                                                | 67.1 ms: 1.35x slower                                             |
| nbody                      | 96.0 ms                                                | 130 ms: 1.36x slower                                              |
| pprint_safe_repr           | 747 ms                                                 | 1.03 sec: 1.38x slower                                            |
| regex_compile              | 141 ms                                                 | 196 ms: 1.38x slower                                              |
| spectral_norm              | 108 ms                                                 | 151 ms: 1.39x slower                                              |
| pprint_pformat             | 1.55 sec                                               | 2.17 sec: 1.40x slower                                            |
| telco                      | 6.86 ms                                                | 9.69 ms: 1.41x slower                                             |
| nqueens                    | 87.9 ms                                                | 124 ms: 1.41x slower                                              |
| scimark_sor                | 121 ms                                                 | 173 ms: 1.42x slower                                              |
| scimark_lu                 | 116 ms                                                 | 167 ms: 1.44x slower                                              |
| hexiom                     | 6.89 ms                                                | 10.4 ms: 1.51x slower                                             |
| python_startup_no_site     | 6.01 ms                                                | 9.17 ms: 1.53x slower                                             |
| pyflate                    | 434 ms                                                 | 670 ms: 1.54x slower                                              |
| unpack_sequence            | 43.5 ns                                                | 68.8 ns: 1.58x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (3): djangocms, xml_etree_parse, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.02x