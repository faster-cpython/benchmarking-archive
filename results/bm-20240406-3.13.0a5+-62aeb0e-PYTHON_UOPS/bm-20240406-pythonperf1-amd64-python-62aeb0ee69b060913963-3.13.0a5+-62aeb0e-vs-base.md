# Results vs. base

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 213 ms                                                                                                                 | 226 ms: 1.06x slower                                                                                                               |
| chameleon      | 4.93 ms                                                                                                                | 5.06 ms: 1.03x slower                                                                                                              |
| docutils       | 1.64 sec                                                                                                               | 1.76 sec: 1.07x slower                                                                                                             |
| html5lib       | 37.3 ms                                                                                                                | 37.9 ms: 1.02x slower                                                                                                              |
| tornado_http   | 83.5 ms                                                                                                                | 86.2 ms: 1.03x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.04x slower                                                                                                                       |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none_tg, async_tree_none, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                                                                 | 148 ms: 1.00x slower                                                                                                               |
| float          | 51.7 ms                                                                                                                | 60.0 ms: 1.16x slower                                                                                                              |
| nbody          | 69.8 ms                                                                                                                | 83.2 ms: 1.19x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.12x slower                                                                                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                                                                                 | 121 ms: 1.02x slower                                                                                                               |
| regex_compile  | 78.5 ms                                                                                                                | 107 ms: 1.37x slower                                                                                                               |
| Geometric mean | (ref)                                                                                                                  | 1.07x slower                                                                                                                       |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 93.2 ms                                                                                                                | 91.1 ms: 1.02x faster                                                                                                              |
| json_dumps           | 5.73 ms                                                                                                                | 5.77 ms: 1.01x slower                                                                                                              |
| pickle_dict          | 18.7 us                                                                                                                | 19.0 us: 1.01x slower                                                                                                              |
| unpickle_list        | 2.83 us                                                                                                                | 2.88 us: 1.02x slower                                                                                                              |
| xml_etree_generate   | 55.5 ms                                                                                                                | 56.6 ms: 1.02x slower                                                                                                              |
| pickle_pure_python   | 179 us                                                                                                                 | 184 us: 1.03x slower                                                                                                               |
| xml_etree_process    | 37.9 ms                                                                                                                | 39.1 ms: 1.03x slower                                                                                                              |
| pickle               | 7.21 us                                                                                                                | 7.50 us: 1.04x slower                                                                                                              |
| tomli_loads          | 1.45 sec                                                                                                               | 1.52 sec: 1.05x slower                                                                                                             |
| xml_etree_iterparse  | 63.4 ms                                                                                                                | 67.8 ms: 1.07x slower                                                                                                              |
| unpickle_pure_python | 134 us                                                                                                                 | 169 us: 1.26x slower                                                                                                               |
| Geometric mean       | (ref)                                                                                                                  | 1.03x slower                                                                                                                       |

Benchmark hidden because not significant (3): pickle_list, json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                                                                                | 20.1 ms: 1.01x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.00x faster                                                                                                                       |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| genshi_text    | 16.8 ms                                                                                                                | 17.0 ms: 1.01x slower                                                                                                              |
| genshi_xml     | 36.1 ms                                                                                                                | 37.1 ms: 1.03x slower                                                                                                              |
| mako           | 6.38 ms                                                                                                                | 7.47 ms: 1.17x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.07x slower                                                                                                                       |

All benchmarks:
===============

| Benchmark                | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-PYTHON_UOPS/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|--------------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| richards                 | 29.8 ms                                                                                                                | 29.0 ms: 1.03x faster                                                                                                              |
| xml_etree_parse          | 93.2 ms                                                                                                                | 91.1 ms: 1.02x faster                                                                                                              |
| coroutines               | 13.3 ms                                                                                                                | 13.1 ms: 1.02x faster                                                                                                              |
| telco                    | 5.04 ms                                                                                                                | 4.96 ms: 1.02x faster                                                                                                              |
| json                     | 2.92 ms                                                                                                                | 2.88 ms: 1.01x faster                                                                                                              |
| pidigits                 | 147 ms                                                                                                                 | 148 ms: 1.00x slower                                                                                                               |
| logging_silent           | 56.1 ns                                                                                                                | 56.4 ns: 1.01x slower                                                                                                              |
| sqlite_synth             | 1.61 us                                                                                                                | 1.62 us: 1.01x slower                                                                                                              |
| coverage                 | 45.7 ms                                                                                                                | 46.0 ms: 1.01x slower                                                                                                              |
| json_dumps               | 5.73 ms                                                                                                                | 5.77 ms: 1.01x slower                                                                                                              |
| pickle_dict              | 18.7 us                                                                                                                | 19.0 us: 1.01x slower                                                                                                              |
| genshi_text              | 16.8 ms                                                                                                                | 17.0 ms: 1.01x slower                                                                                                              |
| python_startup           | 19.8 ms                                                                                                                | 20.1 ms: 1.01x slower                                                                                                              |
| html5lib                 | 37.3 ms                                                                                                                | 37.9 ms: 1.02x slower                                                                                                              |
| unpickle_list            | 2.83 us                                                                                                                | 2.88 us: 1.02x slower                                                                                                              |
| xml_etree_generate       | 55.5 ms                                                                                                                | 56.6 ms: 1.02x slower                                                                                                              |
| bench_mp_pool            | 64.3 ms                                                                                                                | 65.7 ms: 1.02x slower                                                                                                              |
| regex_dna                | 118 ms                                                                                                                 | 121 ms: 1.02x slower                                                                                                               |
| pickle_pure_python       | 179 us                                                                                                                 | 184 us: 1.03x slower                                                                                                               |
| chameleon                | 4.93 ms                                                                                                                | 5.06 ms: 1.03x slower                                                                                                              |
| genshi_xml               | 36.1 ms                                                                                                                | 37.1 ms: 1.03x slower                                                                                                              |
| bench_thread_pool        | 809 us                                                                                                                 | 835 us: 1.03x slower                                                                                                               |
| richards_super           | 32.0 ms                                                                                                                | 33.0 ms: 1.03x slower                                                                                                              |
| tornado_http             | 83.5 ms                                                                                                                | 86.2 ms: 1.03x slower                                                                                                              |
| xml_etree_process        | 37.9 ms                                                                                                                | 39.1 ms: 1.03x slower                                                                                                              |
| create_gc_cycles         | 884 us                                                                                                                 | 915 us: 1.04x slower                                                                                                               |
| aiohttp                  | 885 us                                                                                                                 | 919 us: 1.04x slower                                                                                                               |
| mdp                      | 1.41 sec                                                                                                               | 1.47 sec: 1.04x slower                                                                                                             |
| pickle                   | 7.21 us                                                                                                                | 7.50 us: 1.04x slower                                                                                                              |
| meteor_contest           | 73.9 ms                                                                                                                | 77.1 ms: 1.04x slower                                                                                                              |
| deepcopy_reduce          | 1.99 us                                                                                                                | 2.08 us: 1.04x slower                                                                                                              |
| tomli_loads              | 1.45 sec                                                                                                               | 1.52 sec: 1.05x slower                                                                                                             |
| async_generators         | 231 ms                                                                                                                 | 244 ms: 1.06x slower                                                                                                               |
| 2to3                     | 213 ms                                                                                                                 | 226 ms: 1.06x slower                                                                                                               |
| pycparser                | 677 ms                                                                                                                 | 722 ms: 1.07x slower                                                                                                               |
| deepcopy                 | 221 us                                                                                                                 | 235 us: 1.07x slower                                                                                                               |
| pylint                   | 187 ms                                                                                                                 | 200 ms: 1.07x slower                                                                                                               |
| logging_format           | 6.45 us                                                                                                                | 6.87 us: 1.07x slower                                                                                                              |
| sqlglot_transpile        | 988 us                                                                                                                 | 1.05 ms: 1.07x slower                                                                                                              |
| logging_simple           | 6.01 us                                                                                                                | 6.42 us: 1.07x slower                                                                                                              |
| xml_etree_iterparse      | 63.4 ms                                                                                                                | 67.8 ms: 1.07x slower                                                                                                              |
| sqlglot_normalize        | 183 ms                                                                                                                 | 196 ms: 1.07x slower                                                                                                               |
| docutils                 | 1.64 sec                                                                                                               | 1.76 sec: 1.07x slower                                                                                                             |
| sqlglot_parse            | 776 us                                                                                                                 | 838 us: 1.08x slower                                                                                                               |
| raytrace                 | 164 ms                                                                                                                 | 177 ms: 1.08x slower                                                                                                               |
| mypy2                    | 426 ms                                                                                                                 | 462 ms: 1.08x slower                                                                                                               |
| generators               | 20.9 ms                                                                                                                | 22.8 ms: 1.09x slower                                                                                                              |
| typing_runtime_protocols | 71.4 us                                                                                                                | 78.3 us: 1.10x slower                                                                                                              |
| sqlglot_optimize         | 34.5 ms                                                                                                                | 37.9 ms: 1.10x slower                                                                                                              |
| sympy_expand             | 282 ms                                                                                                                 | 312 ms: 1.11x slower                                                                                                               |
| sympy_sum                | 85.8 ms                                                                                                                | 95.3 ms: 1.11x slower                                                                                                              |
| dulwich_log              | 40.1 ms                                                                                                                | 45.0 ms: 1.12x slower                                                                                                              |
| sympy_str                | 165 ms                                                                                                                 | 186 ms: 1.12x slower                                                                                                               |
| sympy_integrate          | 12.6 ms                                                                                                                | 14.1 ms: 1.12x slower                                                                                                              |
| pprint_safe_repr         | 488 ms                                                                                                                 | 553 ms: 1.13x slower                                                                                                               |
| pprint_pformat           | 989 ms                                                                                                                 | 1.13 sec: 1.14x slower                                                                                                             |
| crypto_pyaes             | 45.5 ms                                                                                                                | 52.1 ms: 1.14x slower                                                                                                              |
| go                       | 90.9 ms                                                                                                                | 104 ms: 1.15x slower                                                                                                               |
| float                    | 51.7 ms                                                                                                                | 60.0 ms: 1.16x slower                                                                                                              |
| deepcopy_memo            | 21.6 us                                                                                                                | 25.1 us: 1.16x slower                                                                                                              |
| mako                     | 6.38 ms                                                                                                                | 7.47 ms: 1.17x slower                                                                                                              |
| thrift                   | 8.04 ms                                                                                                                | 9.47 ms: 1.18x slower                                                                                                              |
| fannkuch                 | 250 ms                                                                                                                 | 296 ms: 1.18x slower                                                                                                               |
| pyflate                  | 286 ms                                                                                                                 | 341 ms: 1.19x slower                                                                                                               |
| nbody                    | 69.8 ms                                                                                                                | 83.2 ms: 1.19x slower                                                                                                              |
| chaos                    | 38.5 ms                                                                                                                | 45.9 ms: 1.19x slower                                                                                                              |
| scimark_fft              | 176 ms                                                                                                                 | 212 ms: 1.20x slower                                                                                                               |
| nqueens                  | 58.8 ms                                                                                                                | 72.0 ms: 1.22x slower                                                                                                              |
| deltablue                | 2.07 ms                                                                                                                | 2.54 ms: 1.23x slower                                                                                                              |
| unpickle_pure_python     | 134 us                                                                                                                 | 169 us: 1.26x slower                                                                                                               |
| scimark_sor              | 72.5 ms                                                                                                                | 92.4 ms: 1.27x slower                                                                                                              |
| scimark_sparse_mat_mult  | 2.54 ms                                                                                                                | 3.28 ms: 1.29x slower                                                                                                              |
| scimark_monte_carlo      | 40.3 ms                                                                                                                | 52.2 ms: 1.30x slower                                                                                                              |
| comprehensions           | 10.9 us                                                                                                                | 14.6 us: 1.33x slower                                                                                                              |
| regex_compile            | 78.5 ms                                                                                                                | 107 ms: 1.37x slower                                                                                                               |
| spectral_norm            | 63.0 ms                                                                                                                | 86.6 ms: 1.37x slower                                                                                                              |
| hexiom                   | 3.79 ms                                                                                                                | 5.54 ms: 1.46x slower                                                                                                              |
| scimark_lu               | 54.1 ms                                                                                                                | 81.2 ms: 1.50x slower                                                                                                              |
| Geometric mean           | (ref)                                                                                                                  | 1.08x slower                                                                                                                       |

Benchmark hidden because not significant (18): regex_v8, asyncio_tcp_ssl, python_startup_no_site, pickle_list, json_loads, async_tree_io_tg, asyncio_tcp, unpickle, async_tree_cpu_io_mixed_tg, gc_traversal, pathlib, regex_effbot, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none_tg, async_tree_none, async_tree_io, async_tree_memoization

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: unknown