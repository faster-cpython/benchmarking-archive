# Results vs. base

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: ced0ca9
- commit date: 2024-04-16
- overall geometric mean: 1.00x slower
- HPT reliability: 95.09%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tornado_http   | 81.5 ms                                                                     | 80.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                             |

Benchmark hidden because not significant (4): 2to3, chameleon, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                      | 147 ms: 1.00x slower                                                     |
| nbody          | 68.5 ms                                                                     | 70.8 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 120 ms                                                                      | 116 ms: 1.03x faster                                                     |
| regex_effbot   | 1.60 ms                                                                     | 1.55 ms: 1.03x faster                                                    |
| regex_compile  | 78.6 ms                                                                     | 79.8 ms: 1.02x slower                                                    |
| regex_v8       | 14.9 ms                                                                     | 18.3 ms: 1.23x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_dict          | 19.6 us                                                                     | 18.6 us: 1.06x faster                                                    |
| pickle               | 7.44 us                                                                     | 7.13 us: 1.04x faster                                                    |
| unpickle_list        | 2.93 us                                                                     | 2.83 us: 1.04x faster                                                    |
| xml_etree_process    | 37.7 ms                                                                     | 37.2 ms: 1.01x faster                                                    |
| unpickle_pure_python | 127 us                                                                      | 125 us: 1.01x faster                                                     |
| json_dumps           | 5.70 ms                                                                     | 5.64 ms: 1.01x faster                                                    |
| unpickle             | 8.33 us                                                                     | 8.25 us: 1.01x faster                                                    |
| xml_etree_generate   | 54.7 ms                                                                     | 54.5 ms: 1.00x faster                                                    |
| json_loads           | 13.7 us                                                                     | 13.9 us: 1.01x slower                                                    |
| tomli_loads          | 1.40 sec                                                                    | 1.41 sec: 1.01x slower                                                   |
| xml_etree_parse      | 91.6 ms                                                                     | 92.8 ms: 1.01x slower                                                    |
| xml_etree_iterparse  | 63.2 ms                                                                     | 64.1 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (2): pickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.1 ms                                                                     | 16.0 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|-----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 34.5 ms                                                                     | 33.5 ms: 1.03x faster                                                    |
| django_template | 22.4 ms                                                                     | 22.5 ms: 1.00x slower                                                    |
| genshi_text     | 15.7 ms                                                                     | 15.9 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                       | 1.00x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|--------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_dict              | 19.6 us                                                                     | 18.6 us: 1.06x faster                                                    |
| pickle                   | 7.44 us                                                                     | 7.13 us: 1.04x faster                                                    |
| unpickle_list            | 2.93 us                                                                     | 2.83 us: 1.04x faster                                                    |
| regex_dna                | 120 ms                                                                      | 116 ms: 1.03x faster                                                     |
| regex_effbot             | 1.60 ms                                                                     | 1.55 ms: 1.03x faster                                                    |
| async_generators         | 236 ms                                                                      | 229 ms: 1.03x faster                                                     |
| genshi_xml               | 34.5 ms                                                                     | 33.5 ms: 1.03x faster                                                    |
| scimark_monte_carlo      | 40.9 ms                                                                     | 39.8 ms: 1.03x faster                                                    |
| deltablue                | 1.99 ms                                                                     | 1.95 ms: 1.02x faster                                                    |
| go                       | 86.8 ms                                                                     | 85.1 ms: 1.02x faster                                                    |
| sqlglot_parse            | 772 us                                                                      | 760 us: 1.02x faster                                                     |
| coroutines               | 13.3 ms                                                                     | 13.1 ms: 1.02x faster                                                    |
| xml_etree_process        | 37.7 ms                                                                     | 37.2 ms: 1.01x faster                                                    |
| sympy_expand             | 275 ms                                                                      | 272 ms: 1.01x faster                                                     |
| python_startup_no_site   | 16.1 ms                                                                     | 16.0 ms: 1.01x faster                                                    |
| richards                 | 26.8 ms                                                                     | 26.5 ms: 1.01x faster                                                    |
| unpickle_pure_python     | 127 us                                                                      | 125 us: 1.01x faster                                                     |
| json_dumps               | 5.70 ms                                                                     | 5.64 ms: 1.01x faster                                                    |
| sqlglot_normalize        | 178 ms                                                                      | 177 ms: 1.01x faster                                                     |
| typing_runtime_protocols | 74.5 us                                                                     | 73.9 us: 1.01x faster                                                    |
| tornado_http             | 81.5 ms                                                                     | 80.8 ms: 1.01x faster                                                    |
| unpickle                 | 8.33 us                                                                     | 8.25 us: 1.01x faster                                                    |
| sqlglot_transpile        | 980 us                                                                      | 971 us: 1.01x faster                                                     |
| richards_super           | 30.4 ms                                                                     | 30.2 ms: 1.01x faster                                                    |
| raytrace                 | 157 ms                                                                      | 156 ms: 1.01x faster                                                     |
| xml_etree_generate       | 54.7 ms                                                                     | 54.5 ms: 1.00x faster                                                    |
| sqlite_synth             | 1.65 us                                                                     | 1.65 us: 1.00x faster                                                    |
| meteor_contest           | 72.4 ms                                                                     | 72.7 ms: 1.00x slower                                                    |
| pidigits                 | 147 ms                                                                      | 147 ms: 1.00x slower                                                     |
| logging_silent           | 53.8 ns                                                                     | 54.1 ns: 1.00x slower                                                    |
| django_template          | 22.4 ms                                                                     | 22.5 ms: 1.00x slower                                                    |
| bench_mp_pool            | 63.5 ms                                                                     | 63.8 ms: 1.01x slower                                                    |
| sympy_sum                | 83.9 ms                                                                     | 84.5 ms: 1.01x slower                                                    |
| telco                    | 5.05 ms                                                                     | 5.09 ms: 1.01x slower                                                    |
| pathlib                  | 75.6 ms                                                                     | 76.1 ms: 1.01x slower                                                    |
| sympy_str                | 160 ms                                                                      | 161 ms: 1.01x slower                                                     |
| json_loads               | 13.7 us                                                                     | 13.9 us: 1.01x slower                                                    |
| comprehensions           | 10.6 us                                                                     | 10.7 us: 1.01x slower                                                    |
| genshi_text              | 15.7 ms                                                                     | 15.9 ms: 1.01x slower                                                    |
| pprint_pformat           | 981 ms                                                                      | 993 ms: 1.01x slower                                                     |
| tomli_loads              | 1.40 sec                                                                    | 1.41 sec: 1.01x slower                                                   |
| dulwich_log              | 39.0 ms                                                                     | 39.5 ms: 1.01x slower                                                    |
| xml_etree_parse          | 91.6 ms                                                                     | 92.8 ms: 1.01x slower                                                    |
| sympy_integrate          | 12.4 ms                                                                     | 12.6 ms: 1.01x slower                                                    |
| pyflate                  | 286 ms                                                                      | 290 ms: 1.01x slower                                                     |
| spectral_norm            | 61.6 ms                                                                     | 62.5 ms: 1.01x slower                                                    |
| xml_etree_iterparse      | 63.2 ms                                                                     | 64.1 ms: 1.01x slower                                                    |
| hexiom                   | 3.72 ms                                                                     | 3.77 ms: 1.01x slower                                                    |
| regex_compile            | 78.6 ms                                                                     | 79.8 ms: 1.02x slower                                                    |
| logging_format           | 6.28 us                                                                     | 6.38 us: 1.02x slower                                                    |
| logging_simple           | 5.87 us                                                                     | 5.96 us: 1.02x slower                                                    |
| nqueens                  | 58.8 ms                                                                     | 59.7 ms: 1.02x slower                                                    |
| mdp                      | 1.37 sec                                                                    | 1.39 sec: 1.02x slower                                                   |
| pprint_safe_repr         | 480 ms                                                                      | 489 ms: 1.02x slower                                                     |
| crypto_pyaes             | 45.5 ms                                                                     | 46.6 ms: 1.02x slower                                                    |
| coverage                 | 45.3 ms                                                                     | 46.4 ms: 1.02x slower                                                    |
| scimark_sor              | 74.4 ms                                                                     | 76.3 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult  | 2.60 ms                                                                     | 2.68 ms: 1.03x slower                                                    |
| generators               | 20.7 ms                                                                     | 21.4 ms: 1.03x slower                                                    |
| nbody                    | 68.5 ms                                                                     | 70.8 ms: 1.03x slower                                                    |
| scimark_lu               | 56.0 ms                                                                     | 57.9 ms: 1.03x slower                                                    |
| fannkuch                 | 246 ms                                                                      | 257 ms: 1.05x slower                                                     |
| scimark_fft              | 180 ms                                                                      | 190 ms: 1.05x slower                                                     |
| regex_v8                 | 14.9 ms                                                                     | 18.3 ms: 1.23x slower                                                    |
| Geometric mean           | (ref)                                                                       | 1.00x slower                                                             |

Benchmark hidden because not significant (33): asyncio_tcp_ssl, float, aiohttp, python_startup, pylint, chaos, pickle_list, html5lib, mako, sqlglot_optimize, mypy2, thrift, pickle_pure_python, deepcopy, deepcopy_reduce, pycparser, docutils, async_tree_io, 2to3, json, deepcopy_memo, async_tree_cpu_io_mixed_tg, gc_traversal, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, create_gc_cycles, chameleon, async_tree_memoization_tg, async_tree_none, asyncio_tcp, bench_thread_pool

# HPT report

- Reliability score: 95.09% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown