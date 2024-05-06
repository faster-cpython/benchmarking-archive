# Results vs. base

- fork: faster-cpython
- ref: convert_deopts_to_ex
- machine: linux-x86_64
- commit hash: 458d82f
- commit date: 2024-04-19
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 305 ms: 1.01x slower                                                             |
| docutils       | 3.08 sec                                                               | 3.14 sec: 1.02x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): chameleon, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 121 ms                                                                 | 122 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 222 ms                                                                 | 224 ms: 1.01x slower                                                             |
| regex_compile  | 179 ms                                                                 | 181 ms: 1.01x slower                                                             |
| regex_effbot   | 3.54 ms                                                                | 3.73 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.37 us                                                                | 4.83 us: 1.11x faster                                                            |
| pickle_dict          | 36.1 us                                                                | 32.8 us: 1.10x faster                                                            |
| unpickle_pure_python | 286 us                                                                 | 282 us: 1.02x faster                                                             |
| xml_etree_generate   | 93.0 ms                                                                | 93.5 ms: 1.01x slower                                                            |
| xml_etree_process    | 63.9 ms                                                                | 65.1 ms: 1.02x slower                                                            |
| json_loads           | 27.3 us                                                                | 27.8 us: 1.02x slower                                                            |
| unpickle_list        | 5.10 us                                                                | 5.33 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): xml_etree_iterparse, pickle, tomli_loads, xml_etree_parse, pickle_pure_python, json_dumps, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.12 ms                                                                | 7.11 ms: 1.00x faster                                                            |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 13.5 ms                                                                | 13.6 ms: 1.00x slower                                                            |
| django_template | 40.8 ms                                                                | 41.3 ms: 1.01x slower                                                            |
| genshi_xml      | 59.7 ms                                                                | 64.7 ms: 1.08x slower                                                            |
| genshi_text     | 26.2 ms                                                                | 28.7 ms: 1.09x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list              | 5.37 us                                                                | 4.83 us: 1.11x faster                                                            |
| pickle_dict              | 36.1 us                                                                | 32.8 us: 1.10x faster                                                            |
| deepcopy_memo            | 45.5 us                                                                | 42.9 us: 1.06x faster                                                            |
| mdp                      | 2.99 sec                                                               | 2.84 sec: 1.05x faster                                                           |
| sqlglot_parse            | 1.50 ms                                                                | 1.48 ms: 1.02x faster                                                            |
| unpickle_pure_python     | 286 us                                                                 | 282 us: 1.02x faster                                                             |
| sqlite_synth             | 3.05 us                                                                | 3.01 us: 1.02x faster                                                            |
| create_gc_cycles         | 1.78 ms                                                                | 1.76 ms: 1.01x faster                                                            |
| telco                    | 9.19 ms                                                                | 9.11 ms: 1.01x faster                                                            |
| generators               | 30.0 ms                                                                | 29.8 ms: 1.01x faster                                                            |
| sqlglot_transpile        | 1.82 ms                                                                | 1.81 ms: 1.01x faster                                                            |
| logging_silent           | 107 ns                                                                 | 106 ns: 1.01x faster                                                             |
| asyncio_tcp_ssl          | 1.87 sec                                                               | 1.86 sec: 1.01x faster                                                           |
| scimark_monte_carlo      | 88.8 ms                                                                | 88.3 ms: 1.01x faster                                                            |
| deepcopy_reduce          | 3.35 us                                                                | 3.34 us: 1.00x faster                                                            |
| python_startup_no_site   | 7.12 ms                                                                | 7.11 ms: 1.00x faster                                                            |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| mako                     | 13.5 ms                                                                | 13.6 ms: 1.00x slower                                                            |
| xml_etree_generate       | 93.0 ms                                                                | 93.5 ms: 1.01x slower                                                            |
| bench_mp_pool            | 23.9 ms                                                                | 24.0 ms: 1.01x slower                                                            |
| sympy_sum                | 177 ms                                                                 | 178 ms: 1.01x slower                                                             |
| pprint_safe_repr         | 966 ms                                                                 | 974 ms: 1.01x slower                                                             |
| richards                 | 55.9 ms                                                                | 56.3 ms: 1.01x slower                                                            |
| richards_super           | 62.4 ms                                                                | 62.9 ms: 1.01x slower                                                            |
| pprint_pformat           | 2.01 sec                                                               | 2.02 sec: 1.01x slower                                                           |
| nbody                    | 121 ms                                                                 | 122 ms: 1.01x slower                                                             |
| hexiom                   | 9.55 ms                                                                | 9.65 ms: 1.01x slower                                                            |
| regex_dna                | 222 ms                                                                 | 224 ms: 1.01x slower                                                             |
| gunicorn                 | 1.32 ms                                                                | 1.33 ms: 1.01x slower                                                            |
| thrift                   | 838 us                                                                 | 847 us: 1.01x slower                                                             |
| sympy_str                | 322 ms                                                                 | 325 ms: 1.01x slower                                                             |
| gc_traversal             | 3.76 ms                                                                | 3.80 ms: 1.01x slower                                                            |
| deepcopy                 | 380 us                                                                 | 384 us: 1.01x slower                                                             |
| django_template          | 40.8 ms                                                                | 41.3 ms: 1.01x slower                                                            |
| raytrace                 | 322 ms                                                                 | 326 ms: 1.01x slower                                                             |
| regex_compile            | 179 ms                                                                 | 181 ms: 1.01x slower                                                             |
| 2to3                     | 301 ms                                                                 | 305 ms: 1.01x slower                                                             |
| nqueens                  | 107 ms                                                                 | 109 ms: 1.01x slower                                                             |
| sympy_expand             | 536 ms                                                                 | 544 ms: 1.01x slower                                                             |
| sympy_integrate          | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                            |
| comprehensions           | 23.5 us                                                                | 23.9 us: 1.02x slower                                                            |
| sqlglot_optimize         | 63.2 ms                                                                | 64.2 ms: 1.02x slower                                                            |
| xml_etree_process        | 63.9 ms                                                                | 65.1 ms: 1.02x slower                                                            |
| dask                     | 381 ms                                                                 | 389 ms: 1.02x slower                                                             |
| docutils                 | 3.08 sec                                                               | 3.14 sec: 1.02x slower                                                           |
| json_loads               | 27.3 us                                                                | 27.8 us: 1.02x slower                                                            |
| dulwich_log              | 73.4 ms                                                                | 75.1 ms: 1.02x slower                                                            |
| sqlglot_normalize        | 123 ms                                                                 | 126 ms: 1.02x slower                                                             |
| scimark_fft              | 445 ms                                                                 | 457 ms: 1.03x slower                                                             |
| pathlib                  | 18.2 ms                                                                | 18.7 ms: 1.03x slower                                                            |
| crypto_pyaes             | 91.6 ms                                                                | 94.1 ms: 1.03x slower                                                            |
| mypy2                    | 806 ms                                                                 | 829 ms: 1.03x slower                                                             |
| go                       | 185 ms                                                                 | 191 ms: 1.03x slower                                                             |
| chaos                    | 78.5 ms                                                                | 80.9 ms: 1.03x slower                                                            |
| djangocms                | 32.4 us                                                                | 33.4 us: 1.03x slower                                                            |
| asyncio_tcp              | 516 ms                                                                 | 533 ms: 1.03x slower                                                             |
| scimark_sparse_mat_mult  | 5.98 ms                                                                | 6.20 ms: 1.04x slower                                                            |
| scimark_lu               | 166 ms                                                                 | 173 ms: 1.04x slower                                                             |
| meteor_contest           | 120 ms                                                                 | 125 ms: 1.04x slower                                                             |
| typing_runtime_protocols | 119 us                                                                 | 124 us: 1.04x slower                                                             |
| unpickle_list            | 5.10 us                                                                | 5.33 us: 1.05x slower                                                            |
| regex_effbot             | 3.54 ms                                                                | 3.73 ms: 1.05x slower                                                            |
| scimark_sor              | 151 ms                                                                 | 159 ms: 1.05x slower                                                             |
| logging_simple           | 6.41 us                                                                | 6.76 us: 1.05x slower                                                            |
| deltablue                | 4.10 ms                                                                | 4.37 ms: 1.06x slower                                                            |
| coroutines               | 22.8 ms                                                                | 24.3 ms: 1.07x slower                                                            |
| logging_format           | 7.05 us                                                                | 7.54 us: 1.07x slower                                                            |
| genshi_xml               | 59.7 ms                                                                | 64.7 ms: 1.08x slower                                                            |
| genshi_text              | 26.2 ms                                                                | 28.7 ms: 1.09x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (32): async_tree_io_tg, async_tree_none, xml_etree_iterparse, pickle, async_tree_memoization, pycparser, async_tree_io, async_tree_cpu_io_mixed, fannkuch, tornado_http, coverage, float, spectral_norm, tomli_loads, async_generators, pyflate, xml_etree_parse, regex_v8, pidigits, pickle_pure_python, json_dumps, asyncio_websockets, bench_thread_pool, json, chameleon, html5lib, aiohttp, async_tree_cpu_io_mixed_tg, unpickle, async_tree_memoization_tg, async_tree_none_tg, pylint

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x