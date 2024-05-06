# Results vs. 3.12.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: b64de3d
- commit date: 2024-05-03
- overall geometric mean: 1.01x slower
- HPT reliability: 90.37%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 291 ms: 1.02x slower                                                                   |
| chameleon      | 7.23 ms                                                      | 7.52 ms: 1.04x slower                                                                  |
| docutils       | 2.87 sec                                                     | 3.02 sec: 1.05x slower                                                                 |
| tornado_http   | 121 ms                                                       | 119 ms: 1.02x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 347 ms: 1.24x faster                                                                   |
| async_tree_memoization_tg  | 540 ms                                                       | 445 ms: 1.21x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 376 ms: 1.20x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 588 ms: 1.19x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 913 ms: 1.15x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 475 ms: 1.15x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 622 ms: 1.12x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.18x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 255 ms: 1.04x faster                                                                   |
| nbody          | 88.0 ms                                                      | 91.0 ms: 1.03x slower                                                                  |
| float          | 76.6 ms                                                      | 80.9 ms: 1.06x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.52 ms: 1.01x faster                                                                  |
| regex_dna      | 239 ms                                                       | 237 ms: 1.01x faster                                                                   |
| regex_compile  | 144 ms                                                       | 143 ms: 1.01x faster                                                                   |
| regex_v8       | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 84.7 ms: 1.02x faster                                                                  |
| unpickle_list        | 4.66 us                                                      | 4.68 us: 1.01x slower                                                                  |
| xml_etree_iterparse  | 103 ms                                                       | 104 ms: 1.01x slower                                                                   |
| xml_etree_parse      | 144 ms                                                       | 145 ms: 1.01x slower                                                                   |
| json_loads           | 24.4 us                                                      | 24.6 us: 1.01x slower                                                                  |
| pickle_dict          | 32.5 us                                                      | 32.9 us: 1.01x slower                                                                  |
| xml_etree_process    | 58.4 ms                                                      | 59.1 ms: 1.01x slower                                                                  |
| pickle_list          | 4.43 us                                                      | 4.49 us: 1.01x slower                                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                                   |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                                                  |
| pickle_pure_python   | 318 us                                                       | 326 us: 1.02x slower                                                                   |
| pickle               | 10.5 us                                                      | 10.9 us: 1.03x slower                                                                  |
| json_dumps           | 10.2 ms                                                      | 11.1 ms: 1.08x slower                                                                  |
| tomli_loads          | 2.16 sec                                                     | 2.38 sec: 1.10x slower                                                                 |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.80 ms: 1.02x slower                                                                  |
| python_startup         | 11.6 ms                                                      | 12.8 ms: 1.11x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 39.6 ms: 1.04x slower                                                                  |
| mako            | 10.0 ms                                                      | 10.4 ms: 1.04x slower                                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| comprehensions             | 21.9 us                                                      | 17.1 us: 1.28x faster                                                                  |
| async_tree_none_tg         | 431 ms                                                       | 347 ms: 1.24x faster                                                                   |
| async_tree_memoization_tg  | 540 ms                                                       | 445 ms: 1.21x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 376 ms: 1.20x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 588 ms: 1.19x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 913 ms: 1.15x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 475 ms: 1.15x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 622 ms: 1.12x faster                                                                   |
| go                         | 150 ms                                                       | 134 ms: 1.11x faster                                                                   |
| generators                 | 37.4 ms                                                      | 33.6 ms: 1.11x faster                                                                  |
| raytrace                   | 298 ms                                                       | 270 ms: 1.10x faster                                                                   |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                                  |
| coroutines                 | 23.0 ms                                                      | 21.5 ms: 1.07x faster                                                                  |
| mypy2                      | 830 ms                                                       | 778 ms: 1.07x faster                                                                   |
| async_generators           | 390 ms                                                       | 368 ms: 1.06x faster                                                                   |
| bench_thread_pool          | 950 us                                                       | 897 us: 1.06x faster                                                                   |
| sympy_sum                  | 162 ms                                                       | 154 ms: 1.05x faster                                                                   |
| pidigits                   | 265 ms                                                       | 255 ms: 1.04x faster                                                                   |
| chaos                      | 64.0 ms                                                      | 62.1 ms: 1.03x faster                                                                  |
| mdp                        | 2.57 sec                                                     | 2.50 sec: 1.03x faster                                                                 |
| sympy_integrate            | 23.9 ms                                                      | 23.4 ms: 1.02x faster                                                                  |
| xml_etree_generate         | 86.1 ms                                                      | 84.7 ms: 1.02x faster                                                                  |
| tornado_http               | 121 ms                                                       | 119 ms: 1.02x faster                                                                   |
| regex_effbot               | 3.57 ms                                                      | 3.52 ms: 1.01x faster                                                                  |
| sympy_str                  | 302 ms                                                       | 298 ms: 1.01x faster                                                                   |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                                   |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                                 |
| regex_dna                  | 239 ms                                                       | 237 ms: 1.01x faster                                                                   |
| regex_compile              | 144 ms                                                       | 143 ms: 1.01x faster                                                                   |
| nqueens                    | 89.9 ms                                                      | 90.2 ms: 1.00x slower                                                                  |
| pprint_pformat             | 1.65 sec                                                     | 1.66 sec: 1.00x slower                                                                 |
| unpickle_list              | 4.66 us                                                      | 4.68 us: 1.01x slower                                                                  |
| xml_etree_iterparse        | 103 ms                                                       | 104 ms: 1.01x slower                                                                   |
| scimark_lu                 | 98.8 ms                                                      | 99.5 ms: 1.01x slower                                                                  |
| pprint_safe_repr           | 807 ms                                                       | 814 ms: 1.01x slower                                                                   |
| xml_etree_parse            | 144 ms                                                       | 145 ms: 1.01x slower                                                                   |
| json_loads                 | 24.4 us                                                      | 24.6 us: 1.01x slower                                                                  |
| pickle_dict                | 32.5 us                                                      | 32.9 us: 1.01x slower                                                                  |
| xml_etree_process          | 58.4 ms                                                      | 59.1 ms: 1.01x slower                                                                  |
| sqlglot_parse              | 1.38 ms                                                      | 1.39 ms: 1.01x slower                                                                  |
| dulwich_log                | 65.4 ms                                                      | 66.2 ms: 1.01x slower                                                                  |
| pickle_list                | 4.43 us                                                      | 4.49 us: 1.01x slower                                                                  |
| logging_simple             | 6.71 us                                                      | 6.81 us: 1.01x slower                                                                  |
| deepcopy_reduce            | 3.37 us                                                      | 3.43 us: 1.02x slower                                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                                   |
| sqlite_synth               | 2.77 us                                                      | 2.82 us: 1.02x slower                                                                  |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                                 |
| python_startup_no_site     | 8.64 ms                                                      | 8.80 ms: 1.02x slower                                                                  |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.29 ms: 1.02x slower                                                                  |
| 2to3                       | 285 ms                                                       | 291 ms: 1.02x slower                                                                   |
| deepcopy_memo              | 36.8 us                                                      | 37.5 us: 1.02x slower                                                                  |
| meteor_contest             | 128 ms                                                       | 131 ms: 1.02x slower                                                                   |
| crypto_pyaes               | 80.3 ms                                                      | 82.0 ms: 1.02x slower                                                                  |
| asyncio_websockets         | 387 ms                                                       | 395 ms: 1.02x slower                                                                   |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                                                  |
| pickle_pure_python         | 318 us                                                       | 326 us: 1.02x slower                                                                   |
| deepcopy                   | 368 us                                                       | 378 us: 1.03x slower                                                                   |
| logging_format             | 7.48 us                                                      | 7.67 us: 1.03x slower                                                                  |
| pickle                     | 10.5 us                                                      | 10.9 us: 1.03x slower                                                                  |
| nbody                      | 88.0 ms                                                      | 91.0 ms: 1.03x slower                                                                  |
| fannkuch                   | 350 ms                                                       | 362 ms: 1.03x slower                                                                   |
| django_template            | 38.2 ms                                                      | 39.6 ms: 1.04x slower                                                                  |
| logging_silent             | 94.4 ns                                                      | 98.0 ns: 1.04x slower                                                                  |
| chameleon                  | 7.23 ms                                                      | 7.52 ms: 1.04x slower                                                                  |
| mako                       | 10.0 ms                                                      | 10.4 ms: 1.04x slower                                                                  |
| sqlglot_optimize           | 57.5 ms                                                      | 60.1 ms: 1.05x slower                                                                  |
| sympy_expand               | 484 ms                                                       | 506 ms: 1.05x slower                                                                   |
| gunicorn                   | 1.00 ms                                                      | 1.05 ms: 1.05x slower                                                                  |
| json                       | 5.12 ms                                                      | 5.38 ms: 1.05x slower                                                                  |
| sqlglot_normalize          | 116 ms                                                       | 122 ms: 1.05x slower                                                                   |
| scimark_fft                | 301 ms                                                       | 317 ms: 1.05x slower                                                                   |
| docutils                   | 2.87 sec                                                     | 3.02 sec: 1.05x slower                                                                 |
| float                      | 76.6 ms                                                      | 80.9 ms: 1.06x slower                                                                  |
| deltablue                  | 3.24 ms                                                      | 3.46 ms: 1.07x slower                                                                  |
| hexiom                     | 5.96 ms                                                      | 6.38 ms: 1.07x slower                                                                  |
| scimark_monte_carlo        | 69.0 ms                                                      | 73.8 ms: 1.07x slower                                                                  |
| aiohttp                    | 1.02 ms                                                      | 1.09 ms: 1.07x slower                                                                  |
| pyflate                    | 439 ms                                                       | 474 ms: 1.08x slower                                                                   |
| regex_v8                   | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                                  |
| json_dumps                 | 10.2 ms                                                      | 11.1 ms: 1.08x slower                                                                  |
| spectral_norm              | 91.6 ms                                                      | 101 ms: 1.10x slower                                                                   |
| tomli_loads                | 2.16 sec                                                     | 2.38 sec: 1.10x slower                                                                 |
| python_startup             | 11.6 ms                                                      | 12.8 ms: 1.11x slower                                                                  |
| richards                   | 45.7 ms                                                      | 51.2 ms: 1.12x slower                                                                  |
| richards_super             | 51.3 ms                                                      | 58.8 ms: 1.14x slower                                                                  |
| typing_runtime_protocols   | 152 us                                                       | 175 us: 1.15x slower                                                                   |
| coverage                   | 66.7 ms                                                      | 77.4 ms: 1.16x slower                                                                  |
| telco                      | 6.96 ms                                                      | 8.27 ms: 1.19x slower                                                                  |
| scimark_sor                | 109 ms                                                       | 130 ms: 1.19x slower                                                                   |
| create_gc_cycles           | 1.59 ms                                                      | 2.01 ms: 1.26x slower                                                                  |
| gc_traversal               | 3.48 ms                                                      | 4.82 ms: 1.38x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (3): bench_mp_pool, dask, sqlglot_transpile
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240503-3.13.0a6+-b64de3d/bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d.json: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 90.37% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.91x