# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 330 ms                                                                 | 316 ms: 1.04x faster                                              |
| chameleon      | 8.02 ms                                                                | 7.81 ms: 1.03x faster                                             |
| docutils       | 3.24 sec                                                               | 3.13 sec: 1.04x faster                                            |
| html5lib       | 74.0 ms                                                                | 72.2 ms: 1.02x faster                                             |
| tornado_http   | 102 ms                                                                 | 104 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_memoization     | 530 ms                                                                 | 487 ms: 1.09x faster                                              |
| async_tree_cpu_io_mixed    | 653 ms                                                                 | 632 ms: 1.03x faster                                              |
| async_tree_cpu_io_mixed_tg | 630 ms                                                                 | 612 ms: 1.03x faster                                              |
| async_tree_none_tg         | 378 ms                                                                 | 369 ms: 1.02x faster                                              |
| async_tree_none            | 396 ms                                                                 | 421 ms: 1.06x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 199 ms                                                                 | 130 ms: 1.53x faster                                              |
| float          | 136 ms                                                                 | 99.2 ms: 1.37x faster                                             |
| pidigits       | 195 ms                                                                 | 192 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                                  | 1.28x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 226 ms                                                                 | 196 ms: 1.16x faster                                              |
| regex_effbot   | 3.60 ms                                                                | 3.63 ms: 1.01x slower                                             |
| regex_dna      | 221 ms                                                                 | 226 ms: 1.02x slower                                              |
| regex_v8       | 25.2 ms                                                                | 26.5 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 408 us                                                                 | 316 us: 1.29x faster                                              |
| tomli_loads          | 3.51 sec                                                               | 2.77 sec: 1.26x faster                                            |
| xml_etree_iterparse  | 133 ms                                                                 | 116 ms: 1.15x faster                                              |
| xml_etree_process    | 71.8 ms                                                                | 66.3 ms: 1.08x faster                                             |
| xml_etree_generate   | 106 ms                                                                 | 98.8 ms: 1.07x faster                                             |
| unpickle             | 16.0 us                                                                | 15.6 us: 1.02x faster                                             |
| pickle_pure_python   | 319 us                                                                 | 322 us: 1.01x slower                                              |
| json_loads           | 28.4 us                                                                | 28.9 us: 1.02x slower                                             |
| unpickle_list        | 5.27 us                                                                | 5.39 us: 1.02x slower                                             |
| pickle_dict          | 34.3 us                                                                | 35.1 us: 1.03x slower                                             |
| pickle               | 11.7 us                                                                | 12.0 us: 1.03x slower                                             |
| pickle_list          | 5.07 us                                                                | 5.23 us: 1.03x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.05x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                             |
| python_startup_no_site | 9.08 ms                                                                | 9.17 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 20.5 ms                                                                | 13.8 ms: 1.48x faster                                             |
| django_template | 43.2 ms                                                                | 42.2 ms: 1.02x faster                                             |
| genshi_text     | 26.8 ms                                                                | 27.4 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                      |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| spectral_norm              | 242 ms                                                                 | 151 ms: 1.61x faster                                              |
| nbody                      | 199 ms                                                                 | 130 ms: 1.53x faster                                              |
| mako                       | 20.5 ms                                                                | 13.8 ms: 1.48x faster                                             |
| fannkuch                   | 758 ms                                                                 | 513 ms: 1.48x faster                                              |
| scimark_sparse_mat_mult    | 8.86 ms                                                                | 6.04 ms: 1.47x faster                                             |
| scimark_monte_carlo        | 137 ms                                                                 | 94.1 ms: 1.45x faster                                             |
| hexiom                     | 15.1 ms                                                                | 10.4 ms: 1.45x faster                                             |
| comprehensions             | 35.8 us                                                                | 24.7 us: 1.45x faster                                             |
| float                      | 136 ms                                                                 | 99.2 ms: 1.37x faster                                             |
| scimark_fft                | 624 ms                                                                 | 457 ms: 1.37x faster                                              |
| crypto_pyaes               | 124 ms                                                                 | 94.4 ms: 1.32x faster                                             |
| pyflate                    | 880 ms                                                                 | 670 ms: 1.31x faster                                              |
| unpickle_pure_python       | 408 us                                                                 | 316 us: 1.29x faster                                              |
| tomli_loads                | 3.51 sec                                                               | 2.77 sec: 1.26x faster                                            |
| unpack_sequence            | 86.5 ns                                                                | 68.8 ns: 1.26x faster                                             |
| scimark_lu                 | 208 ms                                                                 | 167 ms: 1.24x faster                                              |
| chaos                      | 100 ms                                                                 | 82.5 ms: 1.21x faster                                             |
| nqueens                    | 150 ms                                                                 | 124 ms: 1.21x faster                                              |
| go                         | 231 ms                                                                 | 193 ms: 1.20x faster                                              |
| richards                   | 77.9 ms                                                                | 67.1 ms: 1.16x faster                                             |
| regex_compile              | 226 ms                                                                 | 196 ms: 1.16x faster                                              |
| pprint_safe_repr           | 1.18 sec                                                               | 1.03 sec: 1.15x faster                                            |
| xml_etree_iterparse        | 133 ms                                                                 | 116 ms: 1.15x faster                                              |
| pprint_pformat             | 2.48 sec                                                               | 2.17 sec: 1.14x faster                                            |
| richards_super             | 84.7 ms                                                                | 74.4 ms: 1.14x faster                                             |
| raytrace                   | 444 ms                                                                 | 391 ms: 1.14x faster                                              |
| meteor_contest             | 144 ms                                                                 | 128 ms: 1.12x faster                                              |
| async_tree_memoization     | 530 ms                                                                 | 487 ms: 1.09x faster                                              |
| xml_etree_process          | 71.8 ms                                                                | 66.3 ms: 1.08x faster                                             |
| xml_etree_generate         | 106 ms                                                                 | 98.8 ms: 1.07x faster                                             |
| mdp                        | 3.21 sec                                                               | 3.02 sec: 1.06x faster                                            |
| sympy_integrate            | 25.3 ms                                                                | 24.0 ms: 1.05x faster                                             |
| 2to3                       | 330 ms                                                                 | 316 ms: 1.04x faster                                              |
| scimark_sor                | 180 ms                                                                 | 173 ms: 1.04x faster                                              |
| sqlglot_optimize           | 69.6 ms                                                                | 66.9 ms: 1.04x faster                                             |
| sympy_sum                  | 189 ms                                                                 | 182 ms: 1.04x faster                                              |
| sqlglot_parse              | 1.62 ms                                                                | 1.56 ms: 1.04x faster                                             |
| sqlglot_transpile          | 1.96 ms                                                                | 1.89 ms: 1.04x faster                                             |
| docutils                   | 3.24 sec                                                               | 3.13 sec: 1.04x faster                                            |
| async_generators           | 499 ms                                                                 | 483 ms: 1.03x faster                                              |
| async_tree_cpu_io_mixed    | 653 ms                                                                 | 632 ms: 1.03x faster                                              |
| gc_traversal               | 3.86 ms                                                                | 3.74 ms: 1.03x faster                                             |
| sympy_str                  | 345 ms                                                                 | 335 ms: 1.03x faster                                              |
| deepcopy_memo              | 50.9 us                                                                | 49.5 us: 1.03x faster                                             |
| async_tree_cpu_io_mixed_tg | 630 ms                                                                 | 612 ms: 1.03x faster                                              |
| pathlib                    | 21.3 ms                                                                | 20.7 ms: 1.03x faster                                             |
| chameleon                  | 8.02 ms                                                                | 7.81 ms: 1.03x faster                                             |
| html5lib                   | 74.0 ms                                                                | 72.2 ms: 1.02x faster                                             |
| django_template            | 43.2 ms                                                                | 42.2 ms: 1.02x faster                                             |
| async_tree_none_tg         | 378 ms                                                                 | 369 ms: 1.02x faster                                              |
| unpickle                   | 16.0 us                                                                | 15.6 us: 1.02x faster                                             |
| bench_thread_pool          | 929 us                                                                 | 910 us: 1.02x faster                                              |
| deepcopy_reduce            | 3.38 us                                                                | 3.31 us: 1.02x faster                                             |
| deltablue                  | 4.74 ms                                                                | 4.66 ms: 1.02x faster                                             |
| sqlglot_normalize          | 133 ms                                                                 | 130 ms: 1.02x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                             |
| telco                      | 9.83 ms                                                                | 9.69 ms: 1.01x faster                                             |
| pidigits                   | 195 ms                                                                 | 192 ms: 1.01x faster                                              |
| logging_format             | 7.45 us                                                                | 7.36 us: 1.01x faster                                             |
| sqlite_synth               | 3.12 us                                                                | 3.09 us: 1.01x faster                                             |
| dulwich_log                | 75.9 ms                                                                | 75.5 ms: 1.01x faster                                             |
| deepcopy                   | 394 us                                                                 | 392 us: 1.00x faster                                              |
| asyncio_tcp_ssl            | 1.87 sec                                                               | 1.86 sec: 1.00x faster                                            |
| asyncio_tcp                | 509 ms                                                                 | 510 ms: 1.00x slower                                              |
| logging_simple             | 6.70 us                                                                | 6.75 us: 1.01x slower                                             |
| regex_effbot               | 3.60 ms                                                                | 3.63 ms: 1.01x slower                                             |
| python_startup             | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                             |
| python_startup_no_site     | 9.08 ms                                                                | 9.17 ms: 1.01x slower                                             |
| pickle_pure_python         | 319 us                                                                 | 322 us: 1.01x slower                                              |
| tornado_http               | 102 ms                                                                 | 104 ms: 1.01x slower                                              |
| typing_runtime_protocols   | 125 us                                                                 | 127 us: 1.01x slower                                              |
| json_loads                 | 28.4 us                                                                | 28.9 us: 1.02x slower                                             |
| generators                 | 30.3 ms                                                                | 30.9 ms: 1.02x slower                                             |
| genshi_text                | 26.8 ms                                                                | 27.4 ms: 1.02x slower                                             |
| regex_dna                  | 221 ms                                                                 | 226 ms: 1.02x slower                                              |
| unpickle_list              | 5.27 us                                                                | 5.39 us: 1.02x slower                                             |
| pickle_dict                | 34.3 us                                                                | 35.1 us: 1.03x slower                                             |
| pickle                     | 11.7 us                                                                | 12.0 us: 1.03x slower                                             |
| logging_silent             | 109 ns                                                                 | 112 ns: 1.03x slower                                              |
| pickle_list                | 5.07 us                                                                | 5.23 us: 1.03x slower                                             |
| regex_v8                   | 25.2 ms                                                                | 26.5 ms: 1.05x slower                                             |
| async_tree_none            | 396 ms                                                                 | 421 ms: 1.06x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                      |

Benchmark hidden because not significant (20): pylint, mypy2, xml_etree_parse, thrift, dask, gunicorn, create_gc_cycles, genshi_xml, djangocms, asyncio_websockets, bench_mp_pool, json_dumps, async_tree_io_tg, sympy_expand, aiohttp, coverage, pycparser, json, async_tree_io, async_tree_memoization_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x