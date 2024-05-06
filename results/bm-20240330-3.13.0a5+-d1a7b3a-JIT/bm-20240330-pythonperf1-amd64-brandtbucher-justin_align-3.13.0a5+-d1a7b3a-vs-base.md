# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 221 ms                                                                      | 217 ms: 1.02x faster                                                      |
| docutils       | 1.69 sec                                                                    | 1.68 sec: 1.01x faster                                                    |
| html5lib       | 36.2 ms                                                                     | 35.5 ms: 1.02x faster                                                     |
| tornado_http   | 84.2 ms                                                                     | 83.5 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization | 268 ms                                                                      | 265 ms: 1.01x faster                                                      |
| Geometric mean         | (ref)                                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (7): async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 59.4 ms                                                                     | 57.7 ms: 1.03x faster                                                     |
| float          | 47.7 ms                                                                     | 47.3 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 16.4 ms                                                                     | 14.7 ms: 1.11x faster                                                     |
| regex_compile  | 83.0 ms                                                                     | 83.3 ms: 1.00x slower                                                     |
| regex_dna      | 117 ms                                                                      | 119 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_dict          | 18.7 us                                                                     | 18.3 us: 1.03x faster                                                     |
| json_dumps           | 5.64 ms                                                                     | 5.51 ms: 1.02x faster                                                     |
| xml_etree_iterparse  | 62.4 ms                                                                     | 61.4 ms: 1.02x faster                                                     |
| xml_etree_process    | 36.8 ms                                                                     | 36.3 ms: 1.01x faster                                                     |
| unpickle_pure_python | 130 us                                                                      | 129 us: 1.01x faster                                                      |
| tomli_loads          | 1.22 sec                                                                    | 1.20 sec: 1.01x faster                                                    |
| unpickle_list        | 2.77 us                                                                     | 2.74 us: 1.01x faster                                                     |
| xml_etree_generate   | 53.7 ms                                                                     | 53.3 ms: 1.01x faster                                                     |
| pickle_pure_python   | 175 us                                                                      | 174 us: 1.00x faster                                                      |
| xml_etree_parse      | 90.2 ms                                                                     | 91.5 ms: 1.01x slower                                                     |
| json_loads           | 13.8 us                                                                     | 14.4 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                                       | 1.00x faster                                                              |

Benchmark hidden because not significant (3): unpickle, pickle_list, pickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 15.5 ms                                                                     | 15.0 ms: 1.03x faster                                                     |
| django_template | 23.0 ms                                                                     | 22.5 ms: 1.03x faster                                                     |
| genshi_xml      | 33.8 ms                                                                     | 33.0 ms: 1.02x faster                                                     |
| mako            | 5.63 ms                                                                     | 5.75 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                       | 1.01x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json                     | 3.48 ms                                                                     | 2.97 ms: 1.17x faster                                                     |
| regex_v8                 | 16.4 ms                                                                     | 14.7 ms: 1.11x faster                                                     |
| mdp                      | 1.47 sec                                                                    | 1.38 sec: 1.06x faster                                                    |
| generators               | 20.4 ms                                                                     | 19.3 ms: 1.05x faster                                                     |
| richards                 | 30.2 ms                                                                     | 28.7 ms: 1.05x faster                                                     |
| bench_mp_pool            | 70.6 ms                                                                     | 67.3 ms: 1.05x faster                                                     |
| deepcopy_reduce          | 1.99 us                                                                     | 1.90 us: 1.05x faster                                                     |
| deepcopy                 | 226 us                                                                      | 217 us: 1.04x faster                                                      |
| richards_super           | 33.5 ms                                                                     | 32.2 ms: 1.04x faster                                                     |
| raytrace                 | 182 ms                                                                      | 176 ms: 1.04x faster                                                      |
| unpack_sequence          | 47.2 ns                                                                     | 45.6 ns: 1.03x faster                                                     |
| scimark_sparse_mat_mult  | 2.29 ms                                                                     | 2.22 ms: 1.03x faster                                                     |
| nbody                    | 59.4 ms                                                                     | 57.7 ms: 1.03x faster                                                     |
| typing_runtime_protocols | 71.1 us                                                                     | 69.0 us: 1.03x faster                                                     |
| genshi_text              | 15.5 ms                                                                     | 15.0 ms: 1.03x faster                                                     |
| sqlglot_normalize        | 185 ms                                                                      | 181 ms: 1.03x faster                                                      |
| django_template          | 23.0 ms                                                                     | 22.5 ms: 1.03x faster                                                     |
| pickle_dict              | 18.7 us                                                                     | 18.3 us: 1.03x faster                                                     |
| coroutines               | 13.1 ms                                                                     | 12.8 ms: 1.02x faster                                                     |
| genshi_xml               | 33.8 ms                                                                     | 33.0 ms: 1.02x faster                                                     |
| json_dumps               | 5.64 ms                                                                     | 5.51 ms: 1.02x faster                                                     |
| pyflate                  | 284 ms                                                                      | 278 ms: 1.02x faster                                                      |
| deltablue                | 2.06 ms                                                                     | 2.02 ms: 1.02x faster                                                     |
| 2to3                     | 221 ms                                                                      | 217 ms: 1.02x faster                                                      |
| go                       | 94.1 ms                                                                     | 92.2 ms: 1.02x faster                                                     |
| sqlglot_optimize         | 35.6 ms                                                                     | 34.9 ms: 1.02x faster                                                     |
| html5lib                 | 36.2 ms                                                                     | 35.5 ms: 1.02x faster                                                     |
| thrift                   | 8.97 ms                                                                     | 8.83 ms: 1.02x faster                                                     |
| xml_etree_iterparse      | 62.4 ms                                                                     | 61.4 ms: 1.02x faster                                                     |
| async_generators         | 244 ms                                                                      | 241 ms: 1.02x faster                                                      |
| telco                    | 4.72 ms                                                                     | 4.65 ms: 1.01x faster                                                     |
| logging_silent           | 53.5 ns                                                                     | 52.8 ns: 1.01x faster                                                     |
| xml_etree_process        | 36.8 ms                                                                     | 36.3 ms: 1.01x faster                                                     |
| unpickle_pure_python     | 130 us                                                                      | 129 us: 1.01x faster                                                      |
| tomli_loads              | 1.22 sec                                                                    | 1.20 sec: 1.01x faster                                                    |
| logging_format           | 6.31 us                                                                     | 6.23 us: 1.01x faster                                                     |
| async_tree_memoization   | 268 ms                                                                      | 265 ms: 1.01x faster                                                      |
| deepcopy_memo            | 21.6 us                                                                     | 21.3 us: 1.01x faster                                                     |
| sqlglot_transpile        | 1.00 ms                                                                     | 990 us: 1.01x faster                                                      |
| unpickle_list            | 2.77 us                                                                     | 2.74 us: 1.01x faster                                                     |
| float                    | 47.7 ms                                                                     | 47.3 ms: 1.01x faster                                                     |
| xml_etree_generate       | 53.7 ms                                                                     | 53.3 ms: 1.01x faster                                                     |
| tornado_http             | 84.2 ms                                                                     | 83.5 ms: 1.01x faster                                                     |
| sqlglot_parse            | 778 us                                                                      | 772 us: 1.01x faster                                                      |
| spectral_norm            | 51.4 ms                                                                     | 51.1 ms: 1.01x faster                                                     |
| logging_simple           | 5.84 us                                                                     | 5.80 us: 1.01x faster                                                     |
| mypy2                    | 448 ms                                                                      | 446 ms: 1.01x faster                                                      |
| nqueens                  | 60.1 ms                                                                     | 59.8 ms: 1.01x faster                                                     |
| sympy_expand             | 285 ms                                                                      | 284 ms: 1.01x faster                                                      |
| docutils                 | 1.69 sec                                                                    | 1.68 sec: 1.01x faster                                                    |
| pickle_pure_python       | 175 us                                                                      | 174 us: 1.00x faster                                                      |
| regex_compile            | 83.0 ms                                                                     | 83.3 ms: 1.00x slower                                                     |
| dulwich_log              | 41.0 ms                                                                     | 41.2 ms: 1.00x slower                                                     |
| sympy_sum                | 87.6 ms                                                                     | 88.1 ms: 1.01x slower                                                     |
| meteor_contest           | 71.7 ms                                                                     | 72.3 ms: 1.01x slower                                                     |
| xml_etree_parse          | 90.2 ms                                                                     | 91.5 ms: 1.01x slower                                                     |
| scimark_monte_carlo      | 39.5 ms                                                                     | 40.3 ms: 1.02x slower                                                     |
| mako                     | 5.63 ms                                                                     | 5.75 ms: 1.02x slower                                                     |
| fannkuch                 | 224 ms                                                                      | 229 ms: 1.02x slower                                                      |
| regex_dna                | 117 ms                                                                      | 119 ms: 1.02x slower                                                      |
| scimark_sor              | 81.5 ms                                                                     | 83.8 ms: 1.03x slower                                                     |
| json_loads               | 13.8 us                                                                     | 14.4 us: 1.04x slower                                                     |
| scimark_lu               | 75.7 ms                                                                     | 79.9 ms: 1.06x slower                                                     |
| pycparser                | 685 ms                                                                      | 727 ms: 1.06x slower                                                      |
| Geometric mean           | (ref)                                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (34): bench_thread_pool, async_tree_io, asyncio_tcp_ssl, asyncio_tcp, aiohttp, async_tree_io_tg, async_tree_none, async_tree_memoization_tg, pprint_safe_repr, async_tree_none_tg, create_gc_cycles, async_tree_cpu_io_mixed, gc_traversal, python_startup_no_site, python_startup, pathlib, chameleon, sympy_integrate, coverage, regex_effbot, hexiom, sympy_str, pylint, sqlite_synth, scimark_fft, comprehensions, async_tree_cpu_io_mixed_tg, pprint_pformat, pidigits, chaos, unpickle, pickle_list, crypto_pyaes, pickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown