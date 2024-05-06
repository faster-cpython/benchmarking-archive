# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.01x slower
- HPT reliability: 99.35%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                                      | 220 ms: 1.01x slower                                                      |
| chameleon      | 4.78 ms                                                                     | 4.74 ms: 1.01x faster                                                     |
| html5lib       | 35.8 ms                                                                     | 36.5 ms: 1.02x slower                                                     |
| tornado_http   | 84.8 ms                                                                     | 83.9 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                              |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                      | 147 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                              |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 16.4 ms                                                                     | 14.2 ms: 1.16x faster                                                     |
| regex_effbot   | 1.57 ms                                                                     | 1.56 ms: 1.01x faster                                                     |
| regex_dna      | 116 ms                                                                      | 118 ms: 1.01x slower                                                      |
| regex_compile  | 84.6 ms                                                                     | 89.1 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                       | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_list        | 2.80 us                                                                     | 2.74 us: 1.02x faster                                                     |
| xml_etree_parse      | 91.6 ms                                                                     | 89.6 ms: 1.02x faster                                                     |
| pickle               | 7.32 us                                                                     | 7.16 us: 1.02x faster                                                     |
| unpickle             | 8.72 us                                                                     | 8.56 us: 1.02x faster                                                     |
| pickle_pure_python   | 175 us                                                                      | 172 us: 1.01x faster                                                      |
| xml_etree_generate   | 53.4 ms                                                                     | 53.0 ms: 1.01x faster                                                     |
| pickle_dict          | 18.6 us                                                                     | 18.5 us: 1.01x faster                                                     |
| json_dumps           | 5.61 ms                                                                     | 5.57 ms: 1.01x faster                                                     |
| xml_etree_process    | 36.4 ms                                                                     | 37.0 ms: 1.02x slower                                                     |
| json_loads           | 13.8 us                                                                     | 14.5 us: 1.05x slower                                                     |
| unpickle_pure_python | 128 us                                                                      | 136 us: 1.06x slower                                                      |
| tomli_loads          | 1.21 sec                                                                    | 1.32 sec: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                                       | 1.01x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 20.2 ms                                                                     | 19.6 ms: 1.03x faster                                                     |
| python_startup         | 22.6 ms                                                                     | 21.9 ms: 1.03x faster                                                     |
| Geometric mean         | (ref)                                                                       | 1.03x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 34.2 ms                                                                     | 33.3 ms: 1.03x faster                                                     |
| django_template | 22.8 ms                                                                     | 22.5 ms: 1.01x faster                                                     |
| genshi_text     | 15.1 ms                                                                     | 15.0 ms: 1.01x faster                                                     |
| mako            | 5.84 ms                                                                     | 6.08 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                                       | 1.00x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json                     | 4.10 ms                                                                     | 3.19 ms: 1.29x faster                                                     |
| regex_v8                 | 16.4 ms                                                                     | 14.2 ms: 1.16x faster                                                     |
| coverage                 | 47.4 ms                                                                     | 44.7 ms: 1.06x faster                                                     |
| python_startup_no_site   | 20.2 ms                                                                     | 19.6 ms: 1.03x faster                                                     |
| genshi_xml               | 34.2 ms                                                                     | 33.3 ms: 1.03x faster                                                     |
| python_startup           | 22.6 ms                                                                     | 21.9 ms: 1.03x faster                                                     |
| deltablue                | 2.06 ms                                                                     | 2.02 ms: 1.02x faster                                                     |
| unpickle_list            | 2.80 us                                                                     | 2.74 us: 1.02x faster                                                     |
| xml_etree_parse          | 91.6 ms                                                                     | 89.6 ms: 1.02x faster                                                     |
| pickle                   | 7.32 us                                                                     | 7.16 us: 1.02x faster                                                     |
| unpickle                 | 8.72 us                                                                     | 8.56 us: 1.02x faster                                                     |
| gc_traversal             | 1.55 ms                                                                     | 1.52 ms: 1.02x faster                                                     |
| deepcopy                 | 223 us                                                                      | 219 us: 1.02x faster                                                      |
| pickle_pure_python       | 175 us                                                                      | 172 us: 1.01x faster                                                      |
| async_generators         | 247 ms                                                                      | 244 ms: 1.01x faster                                                      |
| django_template          | 22.8 ms                                                                     | 22.5 ms: 1.01x faster                                                     |
| sqlglot_normalize        | 184 ms                                                                      | 182 ms: 1.01x faster                                                      |
| tornado_http             | 84.8 ms                                                                     | 83.9 ms: 1.01x faster                                                     |
| logging_silent           | 53.6 ns                                                                     | 53.1 ns: 1.01x faster                                                     |
| genshi_text              | 15.1 ms                                                                     | 15.0 ms: 1.01x faster                                                     |
| chameleon                | 4.78 ms                                                                     | 4.74 ms: 1.01x faster                                                     |
| raytrace                 | 180 ms                                                                      | 178 ms: 1.01x faster                                                      |
| xml_etree_generate       | 53.4 ms                                                                     | 53.0 ms: 1.01x faster                                                     |
| regex_effbot             | 1.57 ms                                                                     | 1.56 ms: 1.01x faster                                                     |
| pickle_dict              | 18.6 us                                                                     | 18.5 us: 1.01x faster                                                     |
| json_dumps               | 5.61 ms                                                                     | 5.57 ms: 1.01x faster                                                     |
| meteor_contest           | 73.1 ms                                                                     | 73.4 ms: 1.00x slower                                                     |
| sympy_str                | 168 ms                                                                      | 168 ms: 1.00x slower                                                      |
| sympy_integrate          | 13.3 ms                                                                     | 13.4 ms: 1.00x slower                                                     |
| deepcopy_reduce          | 1.93 us                                                                     | 1.94 us: 1.00x slower                                                     |
| pidigits                 | 147 ms                                                                      | 147 ms: 1.01x slower                                                      |
| 2to3                     | 218 ms                                                                      | 220 ms: 1.01x slower                                                      |
| typing_runtime_protocols | 70.1 us                                                                     | 70.6 us: 1.01x slower                                                     |
| sympy_expand             | 287 ms                                                                      | 290 ms: 1.01x slower                                                      |
| regex_dna                | 116 ms                                                                      | 118 ms: 1.01x slower                                                      |
| generators               | 20.1 ms                                                                     | 20.3 ms: 1.01x slower                                                     |
| coroutines               | 12.9 ms                                                                     | 13.1 ms: 1.01x slower                                                     |
| sqlite_synth             | 1.58 us                                                                     | 1.60 us: 1.01x slower                                                     |
| sqlglot_transpile        | 1000 us                                                                     | 1.01 ms: 1.01x slower                                                     |
| logging_simple           | 5.96 us                                                                     | 6.05 us: 1.02x slower                                                     |
| deepcopy_memo            | 21.9 us                                                                     | 22.3 us: 1.02x slower                                                     |
| xml_etree_process        | 36.4 ms                                                                     | 37.0 ms: 1.02x slower                                                     |
| html5lib                 | 35.8 ms                                                                     | 36.5 ms: 1.02x slower                                                     |
| logging_format           | 6.37 us                                                                     | 6.51 us: 1.02x slower                                                     |
| sqlglot_parse            | 778 us                                                                      | 796 us: 1.02x slower                                                      |
| crypto_pyaes             | 43.9 ms                                                                     | 44.9 ms: 1.02x slower                                                     |
| thrift                   | 9.06 ms                                                                     | 9.29 ms: 1.03x slower                                                     |
| chaos                    | 39.1 ms                                                                     | 40.1 ms: 1.03x slower                                                     |
| pylint                   | 190 ms                                                                      | 195 ms: 1.03x slower                                                      |
| go                       | 93.5 ms                                                                     | 96.7 ms: 1.03x slower                                                     |
| scimark_sor              | 81.3 ms                                                                     | 84.1 ms: 1.03x slower                                                     |
| pprint_safe_repr         | 479 ms                                                                      | 496 ms: 1.04x slower                                                      |
| mako                     | 5.84 ms                                                                     | 6.08 ms: 1.04x slower                                                     |
| scimark_fft              | 171 ms                                                                      | 178 ms: 1.04x slower                                                      |
| nqueens                  | 60.9 ms                                                                     | 63.6 ms: 1.04x slower                                                     |
| telco                    | 4.69 ms                                                                     | 4.91 ms: 1.05x slower                                                     |
| pprint_pformat           | 985 ms                                                                      | 1.03 sec: 1.05x slower                                                    |
| regex_compile            | 84.6 ms                                                                     | 89.1 ms: 1.05x slower                                                     |
| json_loads               | 13.8 us                                                                     | 14.5 us: 1.05x slower                                                     |
| pyflate                  | 281 ms                                                                      | 296 ms: 1.05x slower                                                      |
| scimark_sparse_mat_mult  | 2.26 ms                                                                     | 2.38 ms: 1.05x slower                                                     |
| unpickle_pure_python     | 128 us                                                                      | 136 us: 1.06x slower                                                      |
| scimark_lu               | 70.9 ms                                                                     | 75.5 ms: 1.06x slower                                                     |
| scimark_monte_carlo      | 39.7 ms                                                                     | 42.3 ms: 1.06x slower                                                     |
| mdp                      | 1.41 sec                                                                    | 1.54 sec: 1.09x slower                                                    |
| spectral_norm            | 51.1 ms                                                                     | 55.6 ms: 1.09x slower                                                     |
| richards_super           | 31.6 ms                                                                     | 34.4 ms: 1.09x slower                                                     |
| tomli_loads              | 1.21 sec                                                                    | 1.32 sec: 1.09x slower                                                    |
| comprehensions           | 10.9 us                                                                     | 12.0 us: 1.10x slower                                                     |
| richards                 | 28.2 ms                                                                     | 31.0 ms: 1.10x slower                                                     |
| asyncio_tcp_ssl          | 1.47 sec                                                                    | 1.63 sec: 1.11x slower                                                    |
| hexiom                   | 4.57 ms                                                                     | 5.22 ms: 1.14x slower                                                     |
| fannkuch                 | 228 ms                                                                      | 263 ms: 1.15x slower                                                      |
| unpack_sequence          | 46.5 ns                                                                     | 57.5 ns: 1.24x slower                                                     |
| Geometric mean           | (ref)                                                                       | 1.01x slower                                                              |

Benchmark hidden because not significant (24): bench_thread_pool, async_tree_cpu_io_mixed_tg, async_tree_io, create_gc_cycles, pathlib, async_tree_io_tg, async_tree_cpu_io_mixed, sqlglot_optimize, bench_mp_pool, aiohttp, docutils, dulwich_log, async_tree_none_tg, async_tree_memoization, mypy2, async_tree_none, xml_etree_iterparse, pickle_list, nbody, sympy_sum, float, async_tree_memoization_tg, asyncio_tcp, pycparser

# HPT report

- Reliability score: 99.35% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown