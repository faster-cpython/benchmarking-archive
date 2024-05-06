# Results vs. base

- fork: faster-cpython
- ref: move_set_ip_to_exits
- machine: linux-x86_64
- commit hash: ed60e2e
- commit date: 2024-04-19
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 311 ms: 1.03x slower                                                             |
| chameleon      | 7.58 ms                                                                | 8.08 ms: 1.07x slower                                                            |
| docutils       | 3.08 sec                                                               | 3.15 sec: 1.02x slower                                                           |
| html5lib       | 71.9 ms                                                                | 72.9 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg | 352 ms                                                                 | 367 ms: 1.04x slower                                                             |
| Geometric mean     | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (7): async_tree_io, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                 | 200 ms: 1.04x slower                                                             |
| float          | 89.3 ms                                                                | 93.3 ms: 1.04x slower                                                            |
| nbody          | 121 ms                                                                 | 127 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 222 ms                                                                 | 227 ms: 1.02x slower                                                             |
| regex_v8       | 25.2 ms                                                                | 26.0 ms: 1.03x slower                                                            |
| regex_effbot   | 3.54 ms                                                                | 3.68 ms: 1.04x slower                                                            |
| regex_compile  | 179 ms                                                                 | 191 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.37 us                                                                | 5.11 us: 1.05x faster                                                            |
| pickle               | 12.2 us                                                                | 11.6 us: 1.05x faster                                                            |
| unpickle             | 15.5 us                                                                | 15.1 us: 1.03x faster                                                            |
| pickle_dict          | 36.1 us                                                                | 35.2 us: 1.02x faster                                                            |
| pickle_pure_python   | 316 us                                                                 | 310 us: 1.02x faster                                                             |
| xml_etree_iterparse  | 112 ms                                                                 | 110 ms: 1.02x faster                                                             |
| json_dumps           | 10.7 ms                                                                | 10.7 ms: 1.00x faster                                                            |
| json_loads           | 27.3 us                                                                | 27.7 us: 1.02x slower                                                            |
| xml_etree_process    | 63.9 ms                                                                | 65.0 ms: 1.02x slower                                                            |
| xml_etree_generate   | 93.0 ms                                                                | 96.0 ms: 1.03x slower                                                            |
| tomli_loads          | 2.55 sec                                                               | 2.69 sec: 1.05x slower                                                           |
| unpickle_pure_python | 286 us                                                                 | 303 us: 1.06x slower                                                             |
| unpickle_list        | 5.10 us                                                                | 5.46 us: 1.07x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.12 ms                                                                | 7.10 ms: 1.00x faster                                                            |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 13.5 ms                                                                | 13.7 ms: 1.01x slower                                                            |
| genshi_text     | 26.2 ms                                                                | 26.7 ms: 1.02x slower                                                            |
| django_template | 40.8 ms                                                                | 42.8 ms: 1.05x slower                                                            |
| genshi_xml      | 59.7 ms                                                                | 63.1 ms: 1.06x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list              | 5.37 us                                                                | 5.11 us: 1.05x faster                                                            |
| pickle                   | 12.2 us                                                                | 11.6 us: 1.05x faster                                                            |
| mdp                      | 2.99 sec                                                               | 2.90 sec: 1.03x faster                                                           |
| unpickle                 | 15.5 us                                                                | 15.1 us: 1.03x faster                                                            |
| pickle_dict              | 36.1 us                                                                | 35.2 us: 1.02x faster                                                            |
| spectral_norm            | 144 ms                                                                 | 141 ms: 1.02x faster                                                             |
| pickle_pure_python       | 316 us                                                                 | 310 us: 1.02x faster                                                             |
| xml_etree_iterparse      | 112 ms                                                                 | 110 ms: 1.02x faster                                                             |
| generators               | 30.0 ms                                                                | 29.9 ms: 1.00x faster                                                            |
| json_dumps               | 10.7 ms                                                                | 10.7 ms: 1.00x faster                                                            |
| asyncio_tcp              | 516 ms                                                                 | 514 ms: 1.00x faster                                                             |
| python_startup_no_site   | 7.12 ms                                                                | 7.10 ms: 1.00x faster                                                            |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl          | 1.87 sec                                                               | 1.86 sec: 1.00x faster                                                           |
| gc_traversal             | 3.76 ms                                                                | 3.78 ms: 1.00x slower                                                            |
| bench_thread_pool        | 884 us                                                                 | 889 us: 1.01x slower                                                             |
| scimark_fft              | 445 ms                                                                 | 448 ms: 1.01x slower                                                             |
| deepcopy_reduce          | 3.35 us                                                                | 3.38 us: 1.01x slower                                                            |
| logging_simple           | 6.41 us                                                                | 6.46 us: 1.01x slower                                                            |
| mako                     | 13.5 ms                                                                | 13.7 ms: 1.01x slower                                                            |
| dulwich_log              | 73.4 ms                                                                | 74.3 ms: 1.01x slower                                                            |
| html5lib                 | 71.9 ms                                                                | 72.9 ms: 1.01x slower                                                            |
| sympy_integrate          | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                            |
| djangocms                | 32.4 us                                                                | 32.9 us: 1.02x slower                                                            |
| logging_format           | 7.05 us                                                                | 7.16 us: 1.02x slower                                                            |
| deepcopy_memo            | 45.5 us                                                                | 46.3 us: 1.02x slower                                                            |
| genshi_text              | 26.2 ms                                                                | 26.7 ms: 1.02x slower                                                            |
| json_loads               | 27.3 us                                                                | 27.7 us: 1.02x slower                                                            |
| sympy_sum                | 177 ms                                                                 | 180 ms: 1.02x slower                                                             |
| pathlib                  | 18.2 ms                                                                | 18.5 ms: 1.02x slower                                                            |
| xml_etree_process        | 63.9 ms                                                                | 65.0 ms: 1.02x slower                                                            |
| sympy_expand             | 536 ms                                                                 | 546 ms: 1.02x slower                                                             |
| sympy_str                | 322 ms                                                                 | 328 ms: 1.02x slower                                                             |
| regex_dna                | 222 ms                                                                 | 227 ms: 1.02x slower                                                             |
| docutils                 | 3.08 sec                                                               | 3.15 sec: 1.02x slower                                                           |
| async_generators         | 468 ms                                                                 | 479 ms: 1.02x slower                                                             |
| fannkuch                 | 502 ms                                                                 | 515 ms: 1.02x slower                                                             |
| deepcopy                 | 380 us                                                                 | 390 us: 1.03x slower                                                             |
| richards                 | 55.9 ms                                                                | 57.3 ms: 1.03x slower                                                            |
| regex_v8                 | 25.2 ms                                                                | 26.0 ms: 1.03x slower                                                            |
| deltablue                | 4.10 ms                                                                | 4.23 ms: 1.03x slower                                                            |
| sqlite_synth             | 3.05 us                                                                | 3.14 us: 1.03x slower                                                            |
| go                       | 185 ms                                                                 | 191 ms: 1.03x slower                                                             |
| comprehensions           | 23.5 us                                                                | 24.3 us: 1.03x slower                                                            |
| sqlglot_transpile        | 1.82 ms                                                                | 1.88 ms: 1.03x slower                                                            |
| xml_etree_generate       | 93.0 ms                                                                | 96.0 ms: 1.03x slower                                                            |
| 2to3                     | 301 ms                                                                 | 311 ms: 1.03x slower                                                             |
| sqlglot_parse            | 1.50 ms                                                                | 1.55 ms: 1.03x slower                                                            |
| scimark_lu               | 166 ms                                                                 | 172 ms: 1.04x slower                                                             |
| pycparser                | 1.28 sec                                                               | 1.32 sec: 1.04x slower                                                           |
| async_tree_none_tg       | 352 ms                                                                 | 367 ms: 1.04x slower                                                             |
| regex_effbot             | 3.54 ms                                                                | 3.68 ms: 1.04x slower                                                            |
| sqlglot_normalize        | 123 ms                                                                 | 128 ms: 1.04x slower                                                             |
| richards_super           | 62.4 ms                                                                | 65.0 ms: 1.04x slower                                                            |
| sqlglot_optimize         | 63.2 ms                                                                | 65.9 ms: 1.04x slower                                                            |
| pidigits                 | 191 ms                                                                 | 200 ms: 1.04x slower                                                             |
| telco                    | 9.19 ms                                                                | 9.60 ms: 1.04x slower                                                            |
| float                    | 89.3 ms                                                                | 93.3 ms: 1.04x slower                                                            |
| coroutines               | 22.8 ms                                                                | 23.8 ms: 1.04x slower                                                            |
| django_template          | 40.8 ms                                                                | 42.8 ms: 1.05x slower                                                            |
| nbody                    | 121 ms                                                                 | 127 ms: 1.05x slower                                                             |
| tomli_loads              | 2.55 sec                                                               | 2.69 sec: 1.05x slower                                                           |
| scimark_sparse_mat_mult  | 5.98 ms                                                                | 6.30 ms: 1.05x slower                                                            |
| genshi_xml               | 59.7 ms                                                                | 63.1 ms: 1.06x slower                                                            |
| unpickle_pure_python     | 286 us                                                                 | 303 us: 1.06x slower                                                             |
| chaos                    | 78.5 ms                                                                | 83.3 ms: 1.06x slower                                                            |
| hexiom                   | 9.55 ms                                                                | 10.2 ms: 1.06x slower                                                            |
| raytrace                 | 322 ms                                                                 | 343 ms: 1.06x slower                                                             |
| chameleon                | 7.58 ms                                                                | 8.08 ms: 1.07x slower                                                            |
| regex_compile            | 179 ms                                                                 | 191 ms: 1.07x slower                                                             |
| unpickle_list            | 5.10 us                                                                | 5.46 us: 1.07x slower                                                            |
| typing_runtime_protocols | 119 us                                                                 | 129 us: 1.08x slower                                                             |
| nqueens                  | 107 ms                                                                 | 117 ms: 1.09x slower                                                             |
| meteor_contest           | 120 ms                                                                 | 131 ms: 1.09x slower                                                             |
| crypto_pyaes             | 91.6 ms                                                                | 100 ms: 1.10x slower                                                             |
| pprint_safe_repr         | 966 ms                                                                 | 1.07 sec: 1.10x slower                                                           |
| pyflate                  | 600 ms                                                                 | 672 ms: 1.12x slower                                                             |
| pprint_pformat           | 2.01 sec                                                               | 2.26 sec: 1.13x slower                                                           |
| scimark_monte_carlo      | 88.8 ms                                                                | 106 ms: 1.19x slower                                                             |
| Geometric mean           | (ref)                                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (22): async_tree_io, create_gc_cycles, logging_silent, asyncio_websockets, scimark_sor, bench_mp_pool, json, xml_etree_parse, thrift, gunicorn, dask, aiohttp, coverage, async_tree_memoization, tornado_http, pylint, async_tree_none, mypy2, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x