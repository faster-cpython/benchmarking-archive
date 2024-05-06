# Results vs. base

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: e83be54
- commit date: 2024-04-15
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 210 ms                                                                      | 211 ms: 1.01x slower                                                     |
| chameleon      | 4.77 ms                                                                     | 4.83 ms: 1.01x slower                                                    |
| html5lib       | 35.9 ms                                                                     | 37.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg        | 615 ms                                                                      | 626 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed | 389 ms                                                                      | 397 ms: 1.02x slower                                                     |
| async_tree_none         | 220 ms                                                                      | 227 ms: 1.03x slower                                                     |
| Geometric mean          | (ref)                                                                       | 1.02x slower                                                             |

Benchmark hidden because not significant (5): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                      | 147 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                             |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 120 ms                                                                      | 117 ms: 1.03x faster                                                     |
| regex_effbot   | 1.60 ms                                                                     | 1.56 ms: 1.03x faster                                                    |
| regex_compile  | 78.6 ms                                                                     | 78.9 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_dict          | 19.6 us                                                                     | 18.4 us: 1.07x faster                                                    |
| unpickle_list        | 2.93 us                                                                     | 2.83 us: 1.04x faster                                                    |
| json_loads           | 13.7 us                                                                     | 13.5 us: 1.02x faster                                                    |
| pickle               | 7.44 us                                                                     | 7.37 us: 1.01x faster                                                    |
| json_dumps           | 5.70 ms                                                                     | 5.65 ms: 1.01x faster                                                    |
| xml_etree_generate   | 54.7 ms                                                                     | 54.8 ms: 1.00x slower                                                    |
| xml_etree_iterparse  | 63.2 ms                                                                     | 63.6 ms: 1.01x slower                                                    |
| unpickle             | 8.33 us                                                                     | 8.40 us: 1.01x slower                                                    |
| unpickle_pure_python | 127 us                                                                      | 128 us: 1.01x slower                                                     |
| xml_etree_parse      | 91.6 ms                                                                     | 92.8 ms: 1.01x slower                                                    |
| pickle_pure_python   | 176 us                                                                      | 180 us: 1.02x slower                                                     |
| tomli_loads          | 1.40 sec                                                                    | 1.43 sec: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (2): pickle_list, xml_etree_process

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 22.4 ms                                                                     | 23.6 ms: 1.05x slower                                                    |
| genshi_text     | 15.7 ms                                                                     | 16.8 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                                       | 1.03x slower                                                             |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|--------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_dict              | 19.6 us                                                                     | 18.4 us: 1.07x faster                                                    |
| scimark_lu               | 56.0 ms                                                                     | 53.8 ms: 1.04x faster                                                    |
| unpickle_list            | 2.93 us                                                                     | 2.83 us: 1.04x faster                                                    |
| scimark_sor              | 74.4 ms                                                                     | 72.0 ms: 1.03x faster                                                    |
| regex_dna                | 120 ms                                                                      | 117 ms: 1.03x faster                                                     |
| regex_effbot             | 1.60 ms                                                                     | 1.56 ms: 1.03x faster                                                    |
| scimark_monte_carlo      | 40.9 ms                                                                     | 39.9 ms: 1.02x faster                                                    |
| crypto_pyaes             | 45.5 ms                                                                     | 44.5 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult  | 2.60 ms                                                                     | 2.55 ms: 1.02x faster                                                    |
| json_loads               | 13.7 us                                                                     | 13.5 us: 1.02x faster                                                    |
| spectral_norm            | 61.6 ms                                                                     | 60.9 ms: 1.01x faster                                                    |
| sqlglot_parse            | 772 us                                                                      | 764 us: 1.01x faster                                                     |
| chaos                    | 38.5 ms                                                                     | 38.1 ms: 1.01x faster                                                    |
| pickle                   | 7.44 us                                                                     | 7.37 us: 1.01x faster                                                    |
| thrift                   | 7.92 ms                                                                     | 7.84 ms: 1.01x faster                                                    |
| json_dumps               | 5.70 ms                                                                     | 5.65 ms: 1.01x faster                                                    |
| pyflate                  | 286 ms                                                                      | 286 ms: 1.00x slower                                                     |
| xml_etree_generate       | 54.7 ms                                                                     | 54.8 ms: 1.00x slower                                                    |
| pidigits                 | 147 ms                                                                      | 147 ms: 1.00x slower                                                     |
| regex_compile            | 78.6 ms                                                                     | 78.9 ms: 1.00x slower                                                    |
| gc_traversal             | 1.54 ms                                                                     | 1.55 ms: 1.01x slower                                                    |
| xml_etree_iterparse      | 63.2 ms                                                                     | 63.6 ms: 1.01x slower                                                    |
| sympy_sum                | 83.9 ms                                                                     | 84.5 ms: 1.01x slower                                                    |
| sympy_integrate          | 12.4 ms                                                                     | 12.5 ms: 1.01x slower                                                    |
| pathlib                  | 75.6 ms                                                                     | 76.2 ms: 1.01x slower                                                    |
| unpickle                 | 8.33 us                                                                     | 8.40 us: 1.01x slower                                                    |
| 2to3                     | 210 ms                                                                      | 211 ms: 1.01x slower                                                     |
| telco                    | 5.05 ms                                                                     | 5.10 ms: 1.01x slower                                                    |
| scimark_fft              | 180 ms                                                                      | 182 ms: 1.01x slower                                                     |
| sympy_str                | 160 ms                                                                      | 161 ms: 1.01x slower                                                     |
| unpickle_pure_python     | 127 us                                                                      | 128 us: 1.01x slower                                                     |
| generators               | 20.7 ms                                                                     | 20.9 ms: 1.01x slower                                                    |
| mypy2                    | 419 ms                                                                      | 424 ms: 1.01x slower                                                     |
| xml_etree_parse          | 91.6 ms                                                                     | 92.8 ms: 1.01x slower                                                    |
| typing_runtime_protocols | 74.5 us                                                                     | 75.5 us: 1.01x slower                                                    |
| chameleon                | 4.77 ms                                                                     | 4.83 ms: 1.01x slower                                                    |
| pprint_pformat           | 981 ms                                                                      | 996 ms: 1.01x slower                                                     |
| coverage                 | 45.3 ms                                                                     | 46.0 ms: 1.02x slower                                                    |
| mdp                      | 1.37 sec                                                                    | 1.39 sec: 1.02x slower                                                   |
| pprint_safe_repr         | 480 ms                                                                      | 489 ms: 1.02x slower                                                     |
| logging_simple           | 5.87 us                                                                     | 5.98 us: 1.02x slower                                                    |
| async_tree_io_tg         | 615 ms                                                                      | 626 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed  | 389 ms                                                                      | 397 ms: 1.02x slower                                                     |
| hexiom                   | 3.72 ms                                                                     | 3.79 ms: 1.02x slower                                                    |
| pickle_pure_python       | 176 us                                                                      | 180 us: 1.02x slower                                                     |
| tomli_loads              | 1.40 sec                                                                    | 1.43 sec: 1.02x slower                                                   |
| deepcopy                 | 221 us                                                                      | 226 us: 1.02x slower                                                     |
| dulwich_log              | 39.0 ms                                                                     | 39.9 ms: 1.02x slower                                                    |
| meteor_contest           | 72.4 ms                                                                     | 74.2 ms: 1.02x slower                                                    |
| logging_format           | 6.28 us                                                                     | 6.46 us: 1.03x slower                                                    |
| async_tree_none          | 220 ms                                                                      | 227 ms: 1.03x slower                                                     |
| deltablue                | 1.99 ms                                                                     | 2.06 ms: 1.03x slower                                                    |
| sqlglot_normalize        | 178 ms                                                                      | 185 ms: 1.03x slower                                                     |
| sqlglot_optimize         | 33.5 ms                                                                     | 34.7 ms: 1.04x slower                                                    |
| html5lib                 | 35.9 ms                                                                     | 37.4 ms: 1.04x slower                                                    |
| raytrace                 | 157 ms                                                                      | 164 ms: 1.05x slower                                                     |
| go                       | 86.8 ms                                                                     | 90.8 ms: 1.05x slower                                                    |
| django_template          | 22.4 ms                                                                     | 23.6 ms: 1.05x slower                                                    |
| logging_silent           | 53.8 ns                                                                     | 56.8 ns: 1.06x slower                                                    |
| genshi_text              | 15.7 ms                                                                     | 16.8 ms: 1.07x slower                                                    |
| richards                 | 26.8 ms                                                                     | 29.3 ms: 1.09x slower                                                    |
| pycparser                | 689 ms                                                                      | 753 ms: 1.09x slower                                                     |
| richards_super           | 30.4 ms                                                                     | 33.3 ms: 1.09x slower                                                    |
| Geometric mean           | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (34): pickle_list, async_generators, float, sympy_expand, genshi_xml, xml_etree_process, mako, deepcopy_memo, sqlglot_transpile, nbody, create_gc_cycles, nqueens, comprehensions, python_startup, sqlite_synth, fannkuch, pylint, bench_mp_pool, docutils, coroutines, deepcopy_reduce, aiohttp, tornado_http, python_startup_no_site, bench_thread_pool, asyncio_tcp, async_tree_io, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, async_tree_memoization, regex_v8, async_tree_memoization_tg, async_tree_none_tg, json

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown