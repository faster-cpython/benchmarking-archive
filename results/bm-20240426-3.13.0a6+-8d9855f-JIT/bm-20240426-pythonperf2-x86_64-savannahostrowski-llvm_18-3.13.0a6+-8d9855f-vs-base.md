# Results vs. base

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 304 ms                                                                       | 302 ms: 1.01x faster                                                       |
| chameleon      | 7.58 ms                                                                      | 7.46 ms: 1.02x faster                                                      |
| docutils       | 3.10 sec                                                                     | 3.09 sec: 1.00x faster                                                     |
| html5lib       | 74.0 ms                                                                      | 74.6 ms: 1.01x slower                                                      |
| tornado_http   | 124 ms                                                                       | 122 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg | 881 ms                                                                       | 852 ms: 1.03x faster                                                       |
| async_tree_io    | 909 ms                                                                       | 883 ms: 1.03x faster                                                       |
| Geometric mean   | (ref)                                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 261 ms                                                                       | 261 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                               |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 240 ms                                                                       | 238 ms: 1.01x faster                                                       |
| regex_effbot   | 3.44 ms                                                                      | 3.51 ms: 1.02x slower                                                      |
| regex_v8       | 24.9 ms                                                                      | 26.1 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 223 us                                                                       | 214 us: 1.04x faster                                                       |
| tomli_loads          | 2.12 sec                                                                     | 2.09 sec: 1.02x faster                                                     |
| xml_etree_process    | 58.6 ms                                                                      | 57.6 ms: 1.02x faster                                                      |
| xml_etree_iterparse  | 101 ms                                                                       | 100 ms: 1.01x faster                                                       |
| json_loads           | 24.9 us                                                                      | 24.6 us: 1.01x faster                                                      |
| pickle_dict          | 30.8 us                                                                      | 30.5 us: 1.01x faster                                                      |
| xml_etree_generate   | 83.6 ms                                                                      | 83.0 ms: 1.01x faster                                                      |
| xml_etree_parse      | 143 ms                                                                       | 142 ms: 1.01x faster                                                       |
| pickle               | 10.3 us                                                                      | 10.3 us: 1.00x slower                                                      |
| json_dumps           | 10.6 ms                                                                      | 10.7 ms: 1.01x slower                                                      |
| pickle_pure_python   | 312 us                                                                       | 317 us: 1.02x slower                                                       |
| unpickle_list        | 4.64 us                                                                      | 4.73 us: 1.02x slower                                                      |
| unpickle             | 15.1 us                                                                      | 15.6 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                                        | 1.00x faster                                                               |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 13.5 ms                                                                      | 13.4 ms: 1.00x faster                                                      |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 41.4 ms                                                                      | 40.4 ms: 1.03x faster                                                      |
| genshi_text     | 29.7 ms                                                                      | 29.1 ms: 1.02x faster                                                      |
| mako            | 9.84 ms                                                                      | 9.65 ms: 1.02x faster                                                      |
| genshi_xml      | 63.1 ms                                                                      | 62.3 ms: 1.01x faster                                                      |
| Geometric mean  | (ref)                                                                        | 1.02x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| thrift                   | 918 us                                                                       | 877 us: 1.05x faster                                                       |
| unpickle_pure_python     | 223 us                                                                       | 214 us: 1.04x faster                                                       |
| hexiom                   | 7.31 ms                                                                      | 7.02 ms: 1.04x faster                                                      |
| sqlglot_normalize        | 128 ms                                                                       | 123 ms: 1.04x faster                                                       |
| deepcopy                 | 408 us                                                                       | 393 us: 1.04x faster                                                       |
| sympy_expand             | 531 ms                                                                       | 513 ms: 1.04x faster                                                       |
| async_tree_io_tg         | 881 ms                                                                       | 852 ms: 1.03x faster                                                       |
| deepcopy_memo            | 38.6 us                                                                      | 37.4 us: 1.03x faster                                                      |
| richards_super           | 52.8 ms                                                                      | 51.2 ms: 1.03x faster                                                      |
| async_tree_io            | 909 ms                                                                       | 883 ms: 1.03x faster                                                       |
| sqlglot_optimize         | 64.7 ms                                                                      | 63.1 ms: 1.03x faster                                                      |
| django_template          | 41.4 ms                                                                      | 40.4 ms: 1.03x faster                                                      |
| genshi_text              | 29.7 ms                                                                      | 29.1 ms: 1.02x faster                                                      |
| spectral_norm            | 92.8 ms                                                                      | 90.9 ms: 1.02x faster                                                      |
| crypto_pyaes             | 77.8 ms                                                                      | 76.3 ms: 1.02x faster                                                      |
| scimark_monte_carlo      | 70.5 ms                                                                      | 69.1 ms: 1.02x faster                                                      |
| mako                     | 9.84 ms                                                                      | 9.65 ms: 1.02x faster                                                      |
| richards                 | 46.6 ms                                                                      | 45.8 ms: 1.02x faster                                                      |
| sympy_str                | 313 ms                                                                       | 308 ms: 1.02x faster                                                       |
| tomli_loads              | 2.12 sec                                                                     | 2.09 sec: 1.02x faster                                                     |
| tornado_http             | 124 ms                                                                       | 122 ms: 1.02x faster                                                       |
| xml_etree_process        | 58.6 ms                                                                      | 57.6 ms: 1.02x faster                                                      |
| chameleon                | 7.58 ms                                                                      | 7.46 ms: 1.02x faster                                                      |
| mypy2                    | 855 ms                                                                       | 843 ms: 1.01x faster                                                       |
| pprint_pformat           | 1.70 sec                                                                     | 1.68 sec: 1.01x faster                                                     |
| xml_etree_iterparse      | 101 ms                                                                       | 100 ms: 1.01x faster                                                       |
| genshi_xml               | 63.1 ms                                                                      | 62.3 ms: 1.01x faster                                                      |
| json_loads               | 24.9 us                                                                      | 24.6 us: 1.01x faster                                                      |
| comprehensions           | 19.6 us                                                                      | 19.3 us: 1.01x faster                                                      |
| deepcopy_reduce          | 3.48 us                                                                      | 3.44 us: 1.01x faster                                                      |
| dask                     | 406 ms                                                                       | 402 ms: 1.01x faster                                                       |
| gunicorn                 | 1.11 ms                                                                      | 1.10 ms: 1.01x faster                                                      |
| coroutines               | 21.9 ms                                                                      | 21.6 ms: 1.01x faster                                                      |
| regex_dna                | 240 ms                                                                       | 238 ms: 1.01x faster                                                       |
| json                     | 5.36 ms                                                                      | 5.31 ms: 1.01x faster                                                      |
| pickle_dict              | 30.8 us                                                                      | 30.5 us: 1.01x faster                                                      |
| typing_runtime_protocols | 186 us                                                                       | 185 us: 1.01x faster                                                       |
| xml_etree_generate       | 83.6 ms                                                                      | 83.0 ms: 1.01x faster                                                      |
| 2to3                     | 304 ms                                                                       | 302 ms: 1.01x faster                                                       |
| go                       | 174 ms                                                                       | 173 ms: 1.01x faster                                                       |
| create_gc_cycles         | 1.90 ms                                                                      | 1.89 ms: 1.01x faster                                                      |
| xml_etree_parse          | 143 ms                                                                       | 142 ms: 1.01x faster                                                       |
| sympy_sum                | 165 ms                                                                       | 165 ms: 1.00x faster                                                       |
| mdp                      | 2.58 sec                                                                     | 2.57 sec: 1.00x faster                                                     |
| docutils                 | 3.10 sec                                                                     | 3.09 sec: 1.00x faster                                                     |
| fannkuch                 | 377 ms                                                                       | 376 ms: 1.00x faster                                                       |
| nqueens                  | 101 ms                                                                       | 100 ms: 1.00x faster                                                       |
| asyncio_tcp              | 376 ms                                                                       | 374 ms: 1.00x faster                                                       |
| python_startup           | 13.5 ms                                                                      | 13.4 ms: 1.00x faster                                                      |
| asyncio_tcp_ssl          | 1.58 sec                                                                     | 1.58 sec: 1.00x faster                                                     |
| scimark_sparse_mat_mult  | 4.08 ms                                                                      | 4.06 ms: 1.00x faster                                                      |
| sympy_integrate          | 25.7 ms                                                                      | 25.6 ms: 1.00x faster                                                      |
| pidigits                 | 261 ms                                                                       | 261 ms: 1.00x faster                                                       |
| pickle                   | 10.3 us                                                                      | 10.3 us: 1.00x slower                                                      |
| dulwich_log              | 67.0 ms                                                                      | 67.4 ms: 1.01x slower                                                      |
| logging_silent           | 94.8 ns                                                                      | 95.4 ns: 1.01x slower                                                      |
| html5lib                 | 74.0 ms                                                                      | 74.6 ms: 1.01x slower                                                      |
| json_dumps               | 10.6 ms                                                                      | 10.7 ms: 1.01x slower                                                      |
| meteor_contest           | 134 ms                                                                       | 135 ms: 1.01x slower                                                       |
| pycparser                | 1.28 sec                                                                     | 1.29 sec: 1.01x slower                                                     |
| logging_simple           | 6.42 us                                                                      | 6.52 us: 1.01x slower                                                      |
| pickle_pure_python       | 312 us                                                                       | 317 us: 1.02x slower                                                       |
| sqlite_synth             | 2.67 us                                                                      | 2.71 us: 1.02x slower                                                      |
| async_generators         | 382 ms                                                                       | 389 ms: 1.02x slower                                                       |
| unpickle_list            | 4.64 us                                                                      | 4.73 us: 1.02x slower                                                      |
| coverage                 | 78.0 ms                                                                      | 79.6 ms: 1.02x slower                                                      |
| gc_traversal             | 4.34 ms                                                                      | 4.43 ms: 1.02x slower                                                      |
| logging_format           | 7.00 us                                                                      | 7.15 us: 1.02x slower                                                      |
| regex_effbot             | 3.44 ms                                                                      | 3.51 ms: 1.02x slower                                                      |
| raytrace                 | 275 ms                                                                       | 281 ms: 1.02x slower                                                       |
| scimark_fft              | 309 ms                                                                       | 318 ms: 1.03x slower                                                       |
| pyflate                  | 479 ms                                                                       | 494 ms: 1.03x slower                                                       |
| unpickle                 | 15.1 us                                                                      | 15.6 us: 1.04x slower                                                      |
| regex_v8                 | 24.9 ms                                                                      | 26.1 ms: 1.05x slower                                                      |
| scimark_lu               | 113 ms                                                                       | 119 ms: 1.06x slower                                                       |
| Geometric mean           | (ref)                                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (25): asyncio_websockets, bench_mp_pool, async_tree_memoization, bench_thread_pool, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, pylint, deltablue, aiohttp, float, nbody, sqlglot_transpile, python_startup_no_site, scimark_sor, pickle_list, pathlib, generators, sqlglot_parse, chaos, regex_compile, telco, pprint_safe_repr

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x