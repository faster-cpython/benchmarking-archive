# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 281 ms: 1.02x slower                                              |
| chameleon      | 7.05 ms                                                                | 7.19 ms: 1.02x slower                                             |
| docutils       | 2.87 sec                                                               | 2.90 sec: 1.01x slower                                            |
| html5lib       | 67.3 ms                                                                | 66.8 ms: 1.01x faster                                             |
| tornado_http   | 96.6 ms                                                                | 97.1 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg       | 904 ms                                                                 | 934 ms: 1.03x slower                                              |
| async_tree_io          | 922 ms                                                                 | 957 ms: 1.04x slower                                              |
| async_tree_memoization | 439 ms                                                                 | 462 ms: 1.05x slower                                              |
| async_tree_none        | 352 ms                                                                 | 391 ms: 1.11x slower                                              |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                      |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 93.3 ms                                                                | 90.6 ms: 1.03x faster                                             |
| pidigits       | 189 ms                                                                 | 189 ms: 1.00x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                | 25.8 ms: 1.01x faster                                             |
| regex_dna      | 226 ms                                                                 | 230 ms: 1.02x slower                                              |
| regex_effbot   | 3.73 ms                                                                | 3.84 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_list          | 5.02 us                                                                | 4.93 us: 1.02x faster                                             |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                             |
| xml_etree_iterparse  | 107 ms                                                                 | 108 ms: 1.00x slower                                              |
| pickle_pure_python   | 307 us                                                                 | 308 us: 1.00x slower                                              |
| pickle_dict          | 34.4 us                                                                | 34.6 us: 1.01x slower                                             |
| pickle               | 11.8 us                                                                | 12.0 us: 1.01x slower                                             |
| tomli_loads          | 2.04 sec                                                               | 2.07 sec: 1.01x slower                                            |
| unpickle_pure_python | 240 us                                                                 | 245 us: 1.02x slower                                              |
| unpickle_list        | 5.25 us                                                                | 5.38 us: 1.02x slower                                             |
| xml_etree_process    | 60.0 ms                                                                | 61.7 ms: 1.03x slower                                             |
| xml_etree_generate   | 86.8 ms                                                                | 89.7 ms: 1.03x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (3): json_loads, xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                             |
| python_startup_no_site | 9.51 ms                                                                | 9.49 ms: 1.00x faster                                             |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.7 ms: 1.00x faster                                             |
| django_template | 35.9 ms                                                                | 36.5 ms: 1.02x slower                                             |
| genshi_text     | 24.9 ms                                                                | 25.4 ms: 1.02x slower                                             |
| genshi_xml      | 54.8 ms                                                                | 56.4 ms: 1.03x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                      |

All benchmarks:
===============

| Benchmark                | bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5+-94c9742 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody                    | 93.3 ms                                                                | 90.6 ms: 1.03x faster                                             |
| unpack_sequence          | 88.4 ns                                                                | 86.2 ns: 1.03x faster                                             |
| coroutines               | 22.8 ms                                                                | 22.4 ms: 1.02x faster                                             |
| pickle_list              | 5.02 us                                                                | 4.93 us: 1.02x faster                                             |
| mdp                      | 2.70 sec                                                               | 2.67 sec: 1.01x faster                                            |
| go                       | 155 ms                                                                 | 153 ms: 1.01x faster                                              |
| thrift                   | 817 us                                                                 | 810 us: 1.01x faster                                              |
| pathlib                  | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                             |
| html5lib                 | 67.3 ms                                                                | 66.8 ms: 1.01x faster                                             |
| regex_v8                 | 26.0 ms                                                                | 25.8 ms: 1.01x faster                                             |
| hexiom                   | 7.20 ms                                                                | 7.15 ms: 1.01x faster                                             |
| json_dumps               | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                             |
| python_startup           | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                             |
| mako                     | 10.7 ms                                                                | 10.7 ms: 1.00x faster                                             |
| python_startup_no_site   | 9.51 ms                                                                | 9.49 ms: 1.00x faster                                             |
| pidigits                 | 189 ms                                                                 | 189 ms: 1.00x slower                                              |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.85 sec: 1.00x slower                                            |
| deepcopy                 | 360 us                                                                 | 361 us: 1.00x slower                                              |
| xml_etree_iterparse      | 107 ms                                                                 | 108 ms: 1.00x slower                                              |
| gc_traversal             | 3.77 ms                                                                | 3.78 ms: 1.00x slower                                             |
| meteor_contest           | 111 ms                                                                 | 111 ms: 1.00x slower                                              |
| tornado_http             | 96.6 ms                                                                | 97.1 ms: 1.00x slower                                             |
| sympy_integrate          | 21.8 ms                                                                | 21.9 ms: 1.00x slower                                             |
| pickle_pure_python       | 307 us                                                                 | 308 us: 1.00x slower                                              |
| deepcopy_memo            | 39.5 us                                                                | 39.7 us: 1.01x slower                                             |
| sympy_str                | 291 ms                                                                 | 292 ms: 1.01x slower                                              |
| pickle_dict              | 34.4 us                                                                | 34.6 us: 1.01x slower                                             |
| scimark_sor              | 132 ms                                                                 | 133 ms: 1.01x slower                                              |
| sqlglot_optimize         | 57.5 ms                                                                | 58.0 ms: 1.01x slower                                             |
| raytrace                 | 294 ms                                                                 | 297 ms: 1.01x slower                                              |
| sympy_sum                | 164 ms                                                                 | 166 ms: 1.01x slower                                              |
| docutils                 | 2.87 sec                                                               | 2.90 sec: 1.01x slower                                            |
| sqlite_synth             | 2.86 us                                                                | 2.89 us: 1.01x slower                                             |
| scimark_fft              | 342 ms                                                                 | 346 ms: 1.01x slower                                              |
| create_gc_cycles         | 1.67 ms                                                                | 1.69 ms: 1.01x slower                                             |
| fannkuch                 | 392 ms                                                                 | 396 ms: 1.01x slower                                              |
| sympy_expand             | 492 ms                                                                 | 498 ms: 1.01x slower                                              |
| pickle                   | 11.8 us                                                                | 12.0 us: 1.01x slower                                             |
| tomli_loads              | 2.04 sec                                                               | 2.07 sec: 1.01x slower                                            |
| sqlglot_transpile        | 1.64 ms                                                                | 1.66 ms: 1.01x slower                                             |
| spectral_norm            | 114 ms                                                                 | 116 ms: 1.01x slower                                              |
| async_generators         | 460 ms                                                                 | 466 ms: 1.01x slower                                              |
| pyflate                  | 486 ms                                                                 | 492 ms: 1.01x slower                                              |
| sqlglot_parse            | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                             |
| 2to3                     | 277 ms                                                                 | 281 ms: 1.02x slower                                              |
| sqlglot_normalize        | 112 ms                                                                 | 114 ms: 1.02x slower                                              |
| generators               | 29.6 ms                                                                | 30.1 ms: 1.02x slower                                             |
| django_template          | 35.9 ms                                                                | 36.5 ms: 1.02x slower                                             |
| scimark_sparse_mat_mult  | 4.88 ms                                                                | 4.96 ms: 1.02x slower                                             |
| chameleon                | 7.05 ms                                                                | 7.19 ms: 1.02x slower                                             |
| genshi_text              | 24.9 ms                                                                | 25.4 ms: 1.02x slower                                             |
| unpickle_pure_python     | 240 us                                                                 | 245 us: 1.02x slower                                              |
| pprint_safe_repr         | 743 ms                                                                 | 759 ms: 1.02x slower                                              |
| regex_dna                | 226 ms                                                                 | 230 ms: 1.02x slower                                              |
| logging_format           | 6.47 us                                                                | 6.61 us: 1.02x slower                                             |
| unpickle_list            | 5.25 us                                                                | 5.38 us: 1.02x slower                                             |
| richards                 | 46.2 ms                                                                | 47.3 ms: 1.02x slower                                             |
| logging_simple           | 5.84 us                                                                | 5.98 us: 1.02x slower                                             |
| coverage                 | 97.4 ms                                                                | 99.8 ms: 1.02x slower                                             |
| richards_super           | 52.6 ms                                                                | 53.9 ms: 1.03x slower                                             |
| xml_etree_process        | 60.0 ms                                                                | 61.7 ms: 1.03x slower                                             |
| asyncio_tcp              | 497 ms                                                                 | 511 ms: 1.03x slower                                              |
| telco                    | 8.45 ms                                                                | 8.71 ms: 1.03x slower                                             |
| genshi_xml               | 54.8 ms                                                                | 56.4 ms: 1.03x slower                                             |
| regex_effbot             | 3.73 ms                                                                | 3.84 ms: 1.03x slower                                             |
| async_tree_io_tg         | 904 ms                                                                 | 934 ms: 1.03x slower                                              |
| xml_etree_generate       | 86.8 ms                                                                | 89.7 ms: 1.03x slower                                             |
| typing_runtime_protocols | 112 us                                                                 | 117 us: 1.04x slower                                              |
| async_tree_io            | 922 ms                                                                 | 957 ms: 1.04x slower                                              |
| chaos                    | 63.4 ms                                                                | 65.8 ms: 1.04x slower                                             |
| async_tree_memoization   | 439 ms                                                                 | 462 ms: 1.05x slower                                              |
| logging_silent           | 101 ns                                                                 | 108 ns: 1.07x slower                                              |
| async_tree_none          | 352 ms                                                                 | 391 ms: 1.11x slower                                              |
| deltablue                | 3.46 ms                                                                | 3.93 ms: 1.14x slower                                             |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (28): djangocms, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, json_loads, json, dulwich_log, crypto_pyaes, nqueens, aiohttp, asyncio_websockets, regex_compile, bench_mp_pool, float, comprehensions, gunicorn, bench_thread_pool, deepcopy_reduce, pycparser, scimark_lu, pprint_pformat, scimark_monte_carlo, dask, mypy2, xml_etree_parse, pylint, async_tree_memoization_tg, unpickle

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x