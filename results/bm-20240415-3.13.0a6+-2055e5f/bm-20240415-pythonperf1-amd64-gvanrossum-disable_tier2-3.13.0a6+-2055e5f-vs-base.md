# Results vs. base

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 210 ms                                                                      | 211 ms: 1.01x slower                                                     |
| chameleon      | 4.77 ms                                                                     | 4.87 ms: 1.02x slower                                                    |
| html5lib       | 35.9 ms                                                                     | 36.8 ms: 1.02x slower                                                    |
| tornado_http   | 81.5 ms                                                                     | 82.6 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|---------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 615 ms                                                                      | 627 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed   | 389 ms                                                                      | 399 ms: 1.02x slower                                                     |
| async_tree_memoization    | 269 ms                                                                      | 278 ms: 1.03x slower                                                     |
| async_tree_memoization_tg | 264 ms                                                                      | 274 ms: 1.04x slower                                                     |
| async_tree_none           | 220 ms                                                                      | 229 ms: 1.04x slower                                                     |
| Geometric mean            | (ref)                                                                       | 1.03x slower                                                             |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 68.5 ms                                                                     | 69.8 ms: 1.02x slower                                                    |
| float          | 51.1 ms                                                                     | 53.0 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.02x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.60 ms                                                                     | 1.57 ms: 1.02x faster                                                    |
| regex_dna      | 120 ms                                                                      | 120 ms: 1.00x faster                                                     |
| regex_compile  | 78.6 ms                                                                     | 80.8 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list        | 2.93 us                                                                     | 2.74 us: 1.07x faster                                                    |
| json_loads           | 13.7 us                                                                     | 13.6 us: 1.01x faster                                                    |
| xml_etree_parse      | 91.6 ms                                                                     | 92.3 ms: 1.01x slower                                                    |
| pickle_dict          | 19.6 us                                                                     | 19.8 us: 1.01x slower                                                    |
| xml_etree_iterparse  | 63.2 ms                                                                     | 63.8 ms: 1.01x slower                                                    |
| xml_etree_process    | 37.7 ms                                                                     | 38.5 ms: 1.02x slower                                                    |
| tomli_loads          | 1.40 sec                                                                    | 1.43 sec: 1.02x slower                                                   |
| xml_etree_generate   | 54.7 ms                                                                     | 56.6 ms: 1.04x slower                                                    |
| pickle_pure_python   | 176 us                                                                      | 183 us: 1.04x slower                                                     |
| unpickle_pure_python | 127 us                                                                      | 133 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (4): unpickle, pickle, json_dumps, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                                     | 20.3 ms: 1.03x slower                                                    |
| python_startup_no_site | 16.1 ms                                                                     | 16.8 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                                       | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 15.7 ms                                                                     | 16.1 ms: 1.03x slower                                                    |
| django_template | 22.4 ms                                                                     | 23.3 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                                       | 1.02x slower                                                             |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                 | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|---------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list             | 2.93 us                                                                     | 2.74 us: 1.07x faster                                                    |
| typing_runtime_protocols  | 74.5 us                                                                     | 72.8 us: 1.02x faster                                                    |
| regex_effbot              | 1.60 ms                                                                     | 1.57 ms: 1.02x faster                                                    |
| async_generators          | 236 ms                                                                      | 234 ms: 1.01x faster                                                     |
| json_loads                | 13.7 us                                                                     | 13.6 us: 1.01x faster                                                    |
| crypto_pyaes              | 45.5 ms                                                                     | 45.2 ms: 1.01x faster                                                    |
| regex_dna                 | 120 ms                                                                      | 120 ms: 1.00x faster                                                     |
| mdp                       | 1.37 sec                                                                    | 1.37 sec: 1.00x slower                                                   |
| scimark_lu                | 56.0 ms                                                                     | 56.1 ms: 1.00x slower                                                    |
| gc_traversal              | 1.54 ms                                                                     | 1.55 ms: 1.01x slower                                                    |
| generators                | 20.7 ms                                                                     | 20.8 ms: 1.01x slower                                                    |
| deepcopy                  | 221 us                                                                      | 222 us: 1.01x slower                                                     |
| pathlib                   | 75.6 ms                                                                     | 76.1 ms: 1.01x slower                                                    |
| sqlite_synth              | 1.65 us                                                                     | 1.67 us: 1.01x slower                                                    |
| deepcopy_memo             | 21.8 us                                                                     | 21.9 us: 1.01x slower                                                    |
| 2to3                      | 210 ms                                                                      | 211 ms: 1.01x slower                                                     |
| xml_etree_parse           | 91.6 ms                                                                     | 92.3 ms: 1.01x slower                                                    |
| pickle_dict               | 19.6 us                                                                     | 19.8 us: 1.01x slower                                                    |
| chaos                     | 38.5 ms                                                                     | 38.8 ms: 1.01x slower                                                    |
| sqlglot_transpile         | 980 us                                                                      | 989 us: 1.01x slower                                                     |
| coroutines                | 13.3 ms                                                                     | 13.4 ms: 1.01x slower                                                    |
| xml_etree_iterparse       | 63.2 ms                                                                     | 63.8 ms: 1.01x slower                                                    |
| deepcopy_reduce           | 2.01 us                                                                     | 2.03 us: 1.01x slower                                                    |
| sympy_sum                 | 83.9 ms                                                                     | 84.8 ms: 1.01x slower                                                    |
| comprehensions            | 10.6 us                                                                     | 10.7 us: 1.01x slower                                                    |
| mypy2                     | 419 ms                                                                      | 424 ms: 1.01x slower                                                     |
| pyflate                   | 286 ms                                                                      | 289 ms: 1.01x slower                                                     |
| tornado_http              | 81.5 ms                                                                     | 82.6 ms: 1.01x slower                                                    |
| pprint_pformat            | 981 ms                                                                      | 996 ms: 1.01x slower                                                     |
| sympy_str                 | 160 ms                                                                      | 162 ms: 1.02x slower                                                     |
| sympy_integrate           | 12.4 ms                                                                     | 12.6 ms: 1.02x slower                                                    |
| meteor_contest            | 72.4 ms                                                                     | 73.6 ms: 1.02x slower                                                    |
| bench_mp_pool             | 63.5 ms                                                                     | 64.7 ms: 1.02x slower                                                    |
| nbody                     | 68.5 ms                                                                     | 69.8 ms: 1.02x slower                                                    |
| pprint_safe_repr          | 480 ms                                                                      | 489 ms: 1.02x slower                                                     |
| async_tree_io_tg          | 615 ms                                                                      | 627 ms: 1.02x slower                                                     |
| nqueens                   | 58.8 ms                                                                     | 60.0 ms: 1.02x slower                                                    |
| chameleon                 | 4.77 ms                                                                     | 4.87 ms: 1.02x slower                                                    |
| xml_etree_process         | 37.7 ms                                                                     | 38.5 ms: 1.02x slower                                                    |
| scimark_monte_carlo       | 40.9 ms                                                                     | 41.7 ms: 1.02x slower                                                    |
| tomli_loads               | 1.40 sec                                                                    | 1.43 sec: 1.02x slower                                                   |
| sqlglot_parse             | 772 us                                                                      | 790 us: 1.02x slower                                                     |
| sqlglot_normalize         | 178 ms                                                                      | 182 ms: 1.02x slower                                                     |
| sqlglot_optimize          | 33.5 ms                                                                     | 34.3 ms: 1.02x slower                                                    |
| thrift                    | 7.92 ms                                                                     | 8.10 ms: 1.02x slower                                                    |
| html5lib                  | 35.9 ms                                                                     | 36.8 ms: 1.02x slower                                                    |
| scimark_sor               | 74.4 ms                                                                     | 76.2 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed   | 389 ms                                                                      | 399 ms: 1.02x slower                                                     |
| genshi_text               | 15.7 ms                                                                     | 16.1 ms: 1.03x slower                                                    |
| fannkuch                  | 246 ms                                                                      | 253 ms: 1.03x slower                                                     |
| python_startup            | 19.8 ms                                                                     | 20.3 ms: 1.03x slower                                                    |
| logging_simple            | 5.87 us                                                                     | 6.03 us: 1.03x slower                                                    |
| deltablue                 | 1.99 ms                                                                     | 2.05 ms: 1.03x slower                                                    |
| regex_compile             | 78.6 ms                                                                     | 80.8 ms: 1.03x slower                                                    |
| async_tree_memoization    | 269 ms                                                                      | 278 ms: 1.03x slower                                                     |
| xml_etree_generate        | 54.7 ms                                                                     | 56.6 ms: 1.04x slower                                                    |
| float                     | 51.1 ms                                                                     | 53.0 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult   | 2.60 ms                                                                     | 2.70 ms: 1.04x slower                                                    |
| logging_format            | 6.28 us                                                                     | 6.52 us: 1.04x slower                                                    |
| pickle_pure_python        | 176 us                                                                      | 183 us: 1.04x slower                                                     |
| python_startup_no_site    | 16.1 ms                                                                     | 16.8 ms: 1.04x slower                                                    |
| async_tree_memoization_tg | 264 ms                                                                      | 274 ms: 1.04x slower                                                     |
| dulwich_log               | 39.0 ms                                                                     | 40.6 ms: 1.04x slower                                                    |
| async_tree_none           | 220 ms                                                                      | 229 ms: 1.04x slower                                                     |
| django_template           | 22.4 ms                                                                     | 23.3 ms: 1.04x slower                                                    |
| coverage                  | 45.3 ms                                                                     | 47.3 ms: 1.04x slower                                                    |
| hexiom                    | 3.72 ms                                                                     | 3.89 ms: 1.05x slower                                                    |
| scimark_fft               | 180 ms                                                                      | 188 ms: 1.05x slower                                                     |
| unpickle_pure_python      | 127 us                                                                      | 133 us: 1.05x slower                                                     |
| go                        | 86.8 ms                                                                     | 91.0 ms: 1.05x slower                                                    |
| logging_silent            | 53.8 ns                                                                     | 56.6 ns: 1.05x slower                                                    |
| spectral_norm             | 61.6 ms                                                                     | 65.8 ms: 1.07x slower                                                    |
| raytrace                  | 157 ms                                                                      | 168 ms: 1.07x slower                                                     |
| pycparser                 | 689 ms                                                                      | 739 ms: 1.07x slower                                                     |
| richards_super            | 30.4 ms                                                                     | 33.7 ms: 1.11x slower                                                    |
| richards                  | 26.8 ms                                                                     | 29.9 ms: 1.12x slower                                                    |
| Geometric mean            | (ref)                                                                       | 1.02x slower                                                             |

Benchmark hidden because not significant (21): asyncio_tcp_ssl, create_gc_cycles, genshi_xml, unpickle, aiohttp, pidigits, telco, pylint, sympy_expand, pickle, json_dumps, mako, docutils, bench_thread_pool, pickle_list, async_tree_cpu_io_mixed_tg, async_tree_io, json, asyncio_tcp, async_tree_none_tg, regex_v8

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown