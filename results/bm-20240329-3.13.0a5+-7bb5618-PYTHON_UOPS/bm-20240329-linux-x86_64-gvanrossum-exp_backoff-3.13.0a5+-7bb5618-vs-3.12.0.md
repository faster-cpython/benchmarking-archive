# Results vs. 3.12.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 316 ms: 1.15x slower                                              |
| chameleon      | 7.41 ms                                                | 7.81 ms: 1.05x slower                                             |
| docutils       | 2.77 sec                                               | 3.13 sec: 1.13x slower                                            |
| Geometric mean | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 369 ms: 1.22x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 984 ms: 1.20x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 482 ms: 1.19x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 487 ms: 1.19x faster                                              |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.18x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 632 ms: 1.15x faster                                              |
| async_tree_io              | 1.16 sec                                               | 1.01 sec: 1.15x faster                                            |
| async_tree_none            | 472 ms                                                 | 421 ms: 1.12x faster                                              |
| Geometric mean             | (ref)                                                  | 1.17x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 192 ms: 1.03x slower                                              |
| float          | 84.7 ms                                                | 99.2 ms: 1.17x slower                                             |
| nbody          | 97.0 ms                                                | 130 ms: 1.34x slower                                              |
| Geometric mean | (ref)                                                  | 1.17x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.63 ms: 1.00x slower                                             |
| regex_dna      | 212 ms                                                 | 226 ms: 1.06x slower                                              |
| regex_v8       | 23.1 ms                                                | 26.5 ms: 1.15x slower                                             |
| regex_compile  | 148 ms                                                 | 196 ms: 1.32x slower                                              |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle             | 15.9 us                                                | 15.6 us: 1.01x faster                                             |
| pickle_dict          | 35.5 us                                                | 35.1 us: 1.01x faster                                             |
| json_loads           | 28.5 us                                                | 28.9 us: 1.01x slower                                             |
| unpickle_list        | 5.29 us                                                | 5.39 us: 1.02x slower                                             |
| xml_etree_parse      | 159 ms                                                 | 163 ms: 1.02x slower                                              |
| pickle_list          | 5.08 us                                                | 5.23 us: 1.03x slower                                             |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                             |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                             |
| xml_etree_process    | 61.7 ms                                                | 66.3 ms: 1.07x slower                                             |
| xml_etree_iterparse  | 107 ms                                                 | 116 ms: 1.08x slower                                              |
| xml_etree_generate   | 89.2 ms                                                | 98.8 ms: 1.11x slower                                             |
| tomli_loads          | 2.33 sec                                               | 2.77 sec: 1.19x slower                                            |
| unpickle_pure_python | 230 us                                                 | 316 us: 1.37x slower                                              |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                      |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.8 ms: 1.13x slower                                             |
| python_startup_no_site | 6.94 ms                                                | 9.17 ms: 1.32x slower                                             |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.8 ms: 1.16x slower                                             |
| django_template | 34.6 ms                                                | 42.2 ms: 1.22x slower                                             |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 127 us: 1.24x faster                                              |
| async_tree_none_tg         | 450 ms                                                 | 369 ms: 1.22x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 984 ms: 1.20x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 482 ms: 1.19x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 487 ms: 1.19x faster                                              |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.18x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 632 ms: 1.15x faster                                              |
| async_tree_io              | 1.16 sec                                               | 1.01 sec: 1.15x faster                                            |
| async_tree_none            | 472 ms                                                 | 421 ms: 1.12x faster                                              |
| unpickle                   | 15.9 us                                                | 15.6 us: 1.01x faster                                             |
| gc_traversal               | 3.79 ms                                                | 3.74 ms: 1.01x faster                                             |
| generators                 | 31.2 ms                                                | 30.9 ms: 1.01x faster                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.31 us: 1.01x faster                                             |
| pickle_dict                | 35.5 us                                                | 35.1 us: 1.01x faster                                             |
| coroutines                 | 23.2 ms                                                | 23.0 ms: 1.01x faster                                             |
| regex_effbot               | 3.61 ms                                                | 3.63 ms: 1.00x slower                                             |
| json_loads                 | 28.5 us                                                | 28.9 us: 1.01x slower                                             |
| logging_format             | 7.23 us                                                | 7.36 us: 1.02x slower                                             |
| unpickle_list              | 5.29 us                                                | 5.39 us: 1.02x slower                                             |
| xml_etree_parse            | 159 ms                                                 | 163 ms: 1.02x slower                                              |
| pidigits                   | 187 ms                                                 | 192 ms: 1.03x slower                                              |
| pickle_list                | 5.08 us                                                | 5.23 us: 1.03x slower                                             |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                              |
| dask                       | 372 ms                                                 | 386 ms: 1.04x slower                                              |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                             |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                              |
| async_generators           | 463 ms                                                 | 483 ms: 1.04x slower                                              |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                            |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                             |
| json                       | 5.26 ms                                                | 5.49 ms: 1.04x slower                                             |
| logging_simple             | 6.46 us                                                | 6.75 us: 1.04x slower                                             |
| chameleon                  | 7.41 ms                                                | 7.81 ms: 1.05x slower                                             |
| deepcopy                   | 371 us                                                 | 392 us: 1.06x slower                                              |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.06x slower                                              |
| pathlib                    | 19.3 ms                                                | 20.7 ms: 1.07x slower                                             |
| logging_silent             | 104 ns                                                 | 112 ns: 1.07x slower                                              |
| xml_etree_process          | 61.7 ms                                                | 66.3 ms: 1.07x slower                                             |
| sympy_sum                  | 169 ms                                                 | 182 ms: 1.08x slower                                              |
| bench_thread_pool          | 842 us                                                 | 910 us: 1.08x slower                                              |
| xml_etree_iterparse        | 107 ms                                                 | 116 ms: 1.08x slower                                              |
| sqlite_synth               | 2.83 us                                                | 3.09 us: 1.09x slower                                             |
| aiohttp                    | 1.15 ms                                                | 1.26 ms: 1.10x slower                                             |
| gunicorn                   | 1.24 ms                                                | 1.37 ms: 1.10x slower                                             |
| dulwich_log                | 68.5 ms                                                | 75.5 ms: 1.10x slower                                             |
| xml_etree_generate         | 89.2 ms                                                | 98.8 ms: 1.11x slower                                             |
| sympy_str                  | 300 ms                                                 | 335 ms: 1.12x slower                                              |
| sympy_integrate            | 21.4 ms                                                | 24.0 ms: 1.12x slower                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.89 ms: 1.12x slower                                             |
| python_startup             | 9.55 ms                                                | 10.8 ms: 1.13x slower                                             |
| docutils                   | 2.77 sec                                               | 3.13 sec: 1.13x slower                                            |
| comprehensions             | 21.8 us                                                | 24.7 us: 1.14x slower                                             |
| meteor_contest             | 112 ms                                                 | 128 ms: 1.14x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.56 ms: 1.14x slower                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.69 ms: 1.14x slower                                             |
| regex_v8                   | 23.1 ms                                                | 26.5 ms: 1.15x slower                                             |
| mdp                        | 2.63 sec                                               | 3.02 sec: 1.15x slower                                            |
| 2to3                       | 274 ms                                                 | 316 ms: 1.15x slower                                              |
| crypto_pyaes               | 81.9 ms                                                | 94.4 ms: 1.15x slower                                             |
| mako                       | 11.9 ms                                                | 13.8 ms: 1.16x slower                                             |
| sympy_expand               | 478 ms                                                 | 556 ms: 1.16x slower                                              |
| float                      | 84.7 ms                                                | 99.2 ms: 1.17x slower                                             |
| sqlglot_normalize          | 110 ms                                                 | 130 ms: 1.18x slower                                              |
| tomli_loads                | 2.33 sec                                               | 2.77 sec: 1.19x slower                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.04 ms: 1.19x slower                                             |
| scimark_fft                | 382 ms                                                 | 457 ms: 1.20x slower                                              |
| pycparser                  | 1.18 sec                                               | 1.43 sec: 1.21x slower                                            |
| deepcopy_memo              | 40.7 us                                                | 49.5 us: 1.22x slower                                             |
| django_template            | 34.6 ms                                                | 42.2 ms: 1.22x slower                                             |
| sqlglot_optimize           | 54.8 ms                                                | 66.9 ms: 1.22x slower                                             |
| fannkuch                   | 417 ms                                                 | 513 ms: 1.23x slower                                              |
| chaos                      | 67.0 ms                                                | 82.5 ms: 1.23x slower                                             |
| raytrace                   | 312 ms                                                 | 391 ms: 1.25x slower                                              |
| scimark_monte_carlo        | 75.1 ms                                                | 94.1 ms: 1.25x slower                                             |
| deltablue                  | 3.72 ms                                                | 4.66 ms: 1.25x slower                                             |
| unpack_sequence            | 54.0 ns                                                | 68.8 ns: 1.28x slower                                             |
| spectral_norm              | 115 ms                                                 | 151 ms: 1.31x slower                                              |
| regex_compile              | 148 ms                                                 | 196 ms: 1.32x slower                                              |
| python_startup_no_site     | 6.94 ms                                                | 9.17 ms: 1.32x slower                                             |
| pprint_safe_repr           | 776 ms                                                 | 1.03 sec: 1.33x slower                                            |
| scimark_sor                | 129 ms                                                 | 173 ms: 1.34x slower                                              |
| nbody                      | 97.0 ms                                                | 130 ms: 1.34x slower                                              |
| coverage                   | 72.7 ms                                                | 98.5 ms: 1.36x slower                                             |
| telco                      | 7.10 ms                                                | 9.69 ms: 1.36x slower                                             |
| unpickle_pure_python       | 230 us                                                 | 316 us: 1.37x slower                                              |
| go                         | 139 ms                                                 | 193 ms: 1.38x slower                                              |
| pprint_pformat             | 1.57 sec                                               | 2.17 sec: 1.39x slower                                            |
| pyflate                    | 482 ms                                                 | 670 ms: 1.39x slower                                              |
| scimark_lu                 | 118 ms                                                 | 167 ms: 1.42x slower                                              |
| richards_super             | 51.5 ms                                                | 74.4 ms: 1.44x slower                                             |
| richards                   | 45.8 ms                                                | 67.1 ms: 1.46x slower                                             |
| nqueens                    | 83.3 ms                                                | 124 ms: 1.49x slower                                              |
| hexiom                     | 6.41 ms                                                | 10.4 ms: 1.62x slower                                             |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                      |

Benchmark hidden because not significant (4): pickle_pure_python, mypy2, bench_mp_pool, tornado_http
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240329-3.13.0a5+-7bb5618-PYTHON_UOPS/bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.96x