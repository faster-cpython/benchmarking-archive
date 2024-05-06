# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-amd64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 97.32%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 221 ms                                                                      | 218 ms: 1.01x faster                                                      |
| chameleon      | 4.87 ms                                                                     | 4.79 ms: 1.02x faster                                                     |
| html5lib       | 36.2 ms                                                                     | 36.5 ms: 1.01x slower                                                     |
| tornado_http   | 84.2 ms                                                                     | 85.5 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                              |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization | 268 ms                                                                      | 267 ms: 1.00x faster                                                      |
| Geometric mean         | (ref)                                                                       | 1.00x faster                                                              |

Benchmark hidden because not significant (7): async_tree_io, async_tree_cpu_io_mixed, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 47.7 ms                                                                     | 46.0 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 16.4 ms                                                                     | 14.6 ms: 1.12x faster                                                     |
| regex_effbot   | 1.57 ms                                                                     | 1.55 ms: 1.01x faster                                                     |
| regex_dna      | 117 ms                                                                      | 116 ms: 1.01x faster                                                      |
| regex_compile  | 83.0 ms                                                                     | 83.8 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                       | 1.03x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.22 sec                                                                    | 1.17 sec: 1.04x faster                                                    |
| unpickle_pure_python | 130 us                                                                      | 125 us: 1.04x faster                                                      |
| xml_etree_iterparse  | 62.4 ms                                                                     | 60.7 ms: 1.03x faster                                                     |
| unpickle             | 8.68 us                                                                     | 8.50 us: 1.02x faster                                                     |
| pickle_list          | 2.90 us                                                                     | 2.86 us: 1.02x faster                                                     |
| json_dumps           | 5.64 ms                                                                     | 5.55 ms: 1.02x faster                                                     |
| xml_etree_generate   | 53.7 ms                                                                     | 53.0 ms: 1.01x faster                                                     |
| pickle_dict          | 18.7 us                                                                     | 18.5 us: 1.01x faster                                                     |
| pickle_pure_python   | 175 us                                                                      | 173 us: 1.01x faster                                                      |
| pickle               | 7.34 us                                                                     | 7.26 us: 1.01x faster                                                     |
| xml_etree_process    | 36.8 ms                                                                     | 37.1 ms: 1.01x slower                                                     |
| json_loads           | 13.8 us                                                                     | 14.0 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 20.4 ms                                                                     | 19.6 ms: 1.04x faster                                                     |
| python_startup         | 22.4 ms                                                                     | 22.0 ms: 1.02x faster                                                     |
| Geometric mean         | (ref)                                                                       | 1.03x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 5.63 ms                                                                     | 5.22 ms: 1.08x faster                                                     |
| genshi_text     | 15.5 ms                                                                     | 15.1 ms: 1.03x faster                                                     |
| django_template | 23.0 ms                                                                     | 23.3 ms: 1.01x slower                                                     |
| Geometric mean  | (ref)                                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json                     | 3.48 ms                                                                     | 3.01 ms: 1.16x faster                                                     |
| regex_v8                 | 16.4 ms                                                                     | 14.6 ms: 1.12x faster                                                     |
| spectral_norm            | 51.4 ms                                                                     | 46.1 ms: 1.12x faster                                                     |
| scimark_fft              | 170 ms                                                                      | 153 ms: 1.11x faster                                                      |
| scimark_monte_carlo      | 39.5 ms                                                                     | 36.1 ms: 1.09x faster                                                     |
| mako                     | 5.63 ms                                                                     | 5.22 ms: 1.08x faster                                                     |
| pyflate                  | 284 ms                                                                      | 264 ms: 1.08x faster                                                      |
| scimark_lu               | 75.7 ms                                                                     | 71.8 ms: 1.05x faster                                                     |
| bench_mp_pool            | 70.6 ms                                                                     | 67.4 ms: 1.05x faster                                                     |
| crypto_pyaes             | 43.9 ms                                                                     | 41.9 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult  | 2.29 ms                                                                     | 2.19 ms: 1.05x faster                                                     |
| comprehensions           | 11.3 us                                                                     | 10.8 us: 1.04x faster                                                     |
| tomli_loads              | 1.22 sec                                                                    | 1.17 sec: 1.04x faster                                                    |
| unpickle_pure_python     | 130 us                                                                      | 125 us: 1.04x faster                                                      |
| python_startup_no_site   | 20.4 ms                                                                     | 19.6 ms: 1.04x faster                                                     |
| float                    | 47.7 ms                                                                     | 46.0 ms: 1.04x faster                                                     |
| raytrace                 | 182 ms                                                                      | 176 ms: 1.03x faster                                                      |
| chaos                    | 39.0 ms                                                                     | 37.9 ms: 1.03x faster                                                     |
| xml_etree_iterparse      | 62.4 ms                                                                     | 60.7 ms: 1.03x faster                                                     |
| scimark_sor              | 81.5 ms                                                                     | 79.3 ms: 1.03x faster                                                     |
| genshi_text              | 15.5 ms                                                                     | 15.1 ms: 1.03x faster                                                     |
| richards                 | 30.2 ms                                                                     | 29.5 ms: 1.02x faster                                                     |
| richards_super           | 33.5 ms                                                                     | 32.7 ms: 1.02x faster                                                     |
| python_startup           | 22.4 ms                                                                     | 22.0 ms: 1.02x faster                                                     |
| unpickle                 | 8.68 us                                                                     | 8.50 us: 1.02x faster                                                     |
| fannkuch                 | 224 ms                                                                      | 220 ms: 1.02x faster                                                      |
| chameleon                | 4.87 ms                                                                     | 4.79 ms: 1.02x faster                                                     |
| generators               | 20.4 ms                                                                     | 20.0 ms: 1.02x faster                                                     |
| hexiom                   | 4.54 ms                                                                     | 4.47 ms: 1.02x faster                                                     |
| pickle_list              | 2.90 us                                                                     | 2.86 us: 1.02x faster                                                     |
| json_dumps               | 5.64 ms                                                                     | 5.55 ms: 1.02x faster                                                     |
| 2to3                     | 221 ms                                                                      | 218 ms: 1.01x faster                                                      |
| sqlite_synth             | 1.59 us                                                                     | 1.57 us: 1.01x faster                                                     |
| xml_etree_generate       | 53.7 ms                                                                     | 53.0 ms: 1.01x faster                                                     |
| regex_effbot             | 1.57 ms                                                                     | 1.55 ms: 1.01x faster                                                     |
| pickle_dict              | 18.7 us                                                                     | 18.5 us: 1.01x faster                                                     |
| typing_runtime_protocols | 71.1 us                                                                     | 70.2 us: 1.01x faster                                                     |
| pickle_pure_python       | 175 us                                                                      | 173 us: 1.01x faster                                                      |
| pickle                   | 7.34 us                                                                     | 7.26 us: 1.01x faster                                                     |
| pprint_safe_repr         | 470 ms                                                                      | 466 ms: 1.01x faster                                                      |
| logging_silent           | 53.5 ns                                                                     | 53.1 ns: 1.01x faster                                                     |
| regex_dna                | 117 ms                                                                      | 116 ms: 1.01x faster                                                      |
| logging_format           | 6.31 us                                                                     | 6.27 us: 1.01x faster                                                     |
| telco                    | 4.72 ms                                                                     | 4.69 ms: 1.01x faster                                                     |
| sqlglot_transpile        | 1.00 ms                                                                     | 995 us: 1.01x faster                                                      |
| deepcopy                 | 226 us                                                                      | 225 us: 1.01x faster                                                      |
| async_tree_memoization   | 268 ms                                                                      | 267 ms: 1.00x faster                                                      |
| meteor_contest           | 71.7 ms                                                                     | 72.0 ms: 1.00x slower                                                     |
| logging_simple           | 5.84 us                                                                     | 5.86 us: 1.00x slower                                                     |
| nqueens                  | 60.1 ms                                                                     | 60.4 ms: 1.01x slower                                                     |
| xml_etree_process        | 36.8 ms                                                                     | 37.1 ms: 1.01x slower                                                     |
| sqlglot_optimize         | 35.6 ms                                                                     | 35.8 ms: 1.01x slower                                                     |
| sympy_str                | 166 ms                                                                      | 167 ms: 1.01x slower                                                      |
| async_generators         | 244 ms                                                                      | 247 ms: 1.01x slower                                                      |
| regex_compile            | 83.0 ms                                                                     | 83.8 ms: 1.01x slower                                                     |
| sympy_expand             | 285 ms                                                                      | 288 ms: 1.01x slower                                                      |
| mypy2                    | 448 ms                                                                      | 453 ms: 1.01x slower                                                      |
| html5lib                 | 36.2 ms                                                                     | 36.5 ms: 1.01x slower                                                     |
| dulwich_log              | 41.0 ms                                                                     | 41.5 ms: 1.01x slower                                                     |
| django_template          | 23.0 ms                                                                     | 23.3 ms: 1.01x slower                                                     |
| go                       | 94.1 ms                                                                     | 95.3 ms: 1.01x slower                                                     |
| json_loads               | 13.8 us                                                                     | 14.0 us: 1.01x slower                                                     |
| tornado_http             | 84.2 ms                                                                     | 85.5 ms: 1.01x slower                                                     |
| deepcopy_memo            | 21.6 us                                                                     | 22.1 us: 1.02x slower                                                     |
| thrift                   | 8.97 ms                                                                     | 9.19 ms: 1.03x slower                                                     |
| mdp                      | 1.47 sec                                                                    | 1.51 sec: 1.03x slower                                                    |
| pycparser                | 685 ms                                                                      | 728 ms: 1.06x slower                                                      |
| unpack_sequence          | 47.2 ns                                                                     | 60.8 ns: 1.29x slower                                                     |
| Geometric mean           | (ref)                                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (30): asyncio_tcp_ssl, nbody, async_tree_io, bench_thread_pool, create_gc_cycles, async_tree_cpu_io_mixed, async_tree_none, pathlib, deepcopy_reduce, sympy_integrate, async_tree_cpu_io_mixed_tg, deltablue, pprint_pformat, xml_etree_parse, unpickle_list, gc_traversal, sqlglot_normalize, pidigits, coverage, sqlglot_parse, docutils, pylint, async_tree_memoization_tg, async_tree_none_tg, sympy_sum, aiohttp, asyncio_tcp, genshi_xml, async_tree_io_tg, coroutines

# HPT report

- Reliability score: 97.32% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown