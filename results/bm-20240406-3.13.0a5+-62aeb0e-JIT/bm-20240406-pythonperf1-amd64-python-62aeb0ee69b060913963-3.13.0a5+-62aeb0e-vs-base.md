# Results vs. base

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.01x faster
- HPT reliability: 96.33%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 213 ms                                                                                                                 | 221 ms: 1.04x slower                                                                                                       |
| chameleon      | 4.93 ms                                                                                                                | 4.70 ms: 1.05x faster                                                                                                      |
| docutils       | 1.64 sec                                                                                                               | 1.70 sec: 1.04x slower                                                                                                     |
| html5lib       | 37.3 ms                                                                                                                | 35.4 ms: 1.05x faster                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.00x faster                                                                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| async_tree_none  | 227 ms                                                                                                                 | 217 ms: 1.04x faster                                                                                                       |
| async_tree_io_tg | 626 ms                                                                                                                 | 605 ms: 1.03x faster                                                                                                       |
| Geometric mean   | (ref)                                                                                                                  | 1.02x faster                                                                                                               |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| nbody          | 69.8 ms                                                                                                                | 57.8 ms: 1.21x faster                                                                                                      |
| float          | 51.7 ms                                                                                                                | 46.8 ms: 1.10x faster                                                                                                      |
| pidigits       | 147 ms                                                                                                                 | 146 ms: 1.01x faster                                                                                                       |
| Geometric mean | (ref)                                                                                                                  | 1.10x faster                                                                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 16.4 ms                                                                                                                | 14.1 ms: 1.16x faster                                                                                                      |
| regex_effbot   | 1.58 ms                                                                                                                | 1.55 ms: 1.02x faster                                                                                                      |
| regex_dna      | 118 ms                                                                                                                 | 119 ms: 1.00x slower                                                                                                       |
| regex_compile  | 78.5 ms                                                                                                                | 87.0 ms: 1.11x slower                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.01x faster                                                                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 1.45 sec                                                                                                               | 1.19 sec: 1.22x faster                                                                                                     |
| xml_etree_iterparse  | 63.4 ms                                                                                                                | 60.6 ms: 1.05x faster                                                                                                      |
| xml_etree_generate   | 55.5 ms                                                                                                                | 53.1 ms: 1.05x faster                                                                                                      |
| pickle_pure_python   | 179 us                                                                                                                 | 172 us: 1.04x faster                                                                                                       |
| pickle_list          | 2.97 us                                                                                                                | 2.85 us: 1.04x faster                                                                                                      |
| unpickle_pure_python | 134 us                                                                                                                 | 129 us: 1.04x faster                                                                                                       |
| xml_etree_process    | 37.9 ms                                                                                                                | 36.6 ms: 1.04x faster                                                                                                      |
| json_dumps           | 5.73 ms                                                                                                                | 5.54 ms: 1.03x faster                                                                                                      |
| xml_etree_parse      | 93.2 ms                                                                                                                | 90.9 ms: 1.03x faster                                                                                                      |
| json_loads           | 13.9 us                                                                                                                | 13.7 us: 1.02x faster                                                                                                      |
| pickle_dict          | 18.7 us                                                                                                                | 19.0 us: 1.01x slower                                                                                                      |
| unpickle_list        | 2.83 us                                                                                                                | 2.90 us: 1.02x slower                                                                                                      |
| pickle               | 7.21 us                                                                                                                | 7.39 us: 1.03x slower                                                                                                      |
| unpickle             | 8.58 us                                                                                                                | 9.09 us: 1.06x slower                                                                                                      |
| Geometric mean       | (ref)                                                                                                                  | 1.03x faster                                                                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|------------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 18.4 ms                                                                                                                | 20.2 ms: 1.10x slower                                                                                                      |
| python_startup         | 19.8 ms                                                                                                                | 22.2 ms: 1.12x slower                                                                                                      |
| Geometric mean         | (ref)                                                                                                                  | 1.11x slower                                                                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| mako           | 6.38 ms                                                                                                                | 5.63 ms: 1.13x faster                                                                                                      |
| genshi_text    | 16.8 ms                                                                                                                | 15.6 ms: 1.07x faster                                                                                                      |
| genshi_xml     | 36.1 ms                                                                                                                | 34.8 ms: 1.04x faster                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.08x faster                                                                                                               |

All benchmarks:
===============

| Benchmark                | results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json | results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json |
|--------------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| spectral_norm            | 63.0 ms                                                                                                                | 50.4 ms: 1.25x faster                                                                                                      |
| tomli_loads              | 1.45 sec                                                                                                               | 1.19 sec: 1.22x faster                                                                                                     |
| nbody                    | 69.8 ms                                                                                                                | 57.8 ms: 1.21x faster                                                                                                      |
| regex_v8                 | 16.4 ms                                                                                                                | 14.1 ms: 1.16x faster                                                                                                      |
| mako                     | 6.38 ms                                                                                                                | 5.63 ms: 1.13x faster                                                                                                      |
| richards                 | 29.8 ms                                                                                                                | 26.5 ms: 1.13x faster                                                                                                      |
| scimark_sparse_mat_mult  | 2.54 ms                                                                                                                | 2.30 ms: 1.10x faster                                                                                                      |
| float                    | 51.7 ms                                                                                                                | 46.8 ms: 1.10x faster                                                                                                      |
| fannkuch                 | 250 ms                                                                                                                 | 231 ms: 1.08x faster                                                                                                       |
| genshi_text              | 16.8 ms                                                                                                                | 15.6 ms: 1.07x faster                                                                                                      |
| pyflate                  | 286 ms                                                                                                                 | 268 ms: 1.07x faster                                                                                                       |
| telco                    | 5.04 ms                                                                                                                | 4.74 ms: 1.07x faster                                                                                                      |
| generators               | 20.9 ms                                                                                                                | 19.6 ms: 1.06x faster                                                                                                      |
| richards_super           | 32.0 ms                                                                                                                | 30.1 ms: 1.06x faster                                                                                                      |
| logging_format           | 6.45 us                                                                                                                | 6.11 us: 1.05x faster                                                                                                      |
| html5lib                 | 37.3 ms                                                                                                                | 35.4 ms: 1.05x faster                                                                                                      |
| logging_simple           | 6.01 us                                                                                                                | 5.72 us: 1.05x faster                                                                                                      |
| chameleon                | 4.93 ms                                                                                                                | 4.70 ms: 1.05x faster                                                                                                      |
| logging_silent           | 56.1 ns                                                                                                                | 53.6 ns: 1.05x faster                                                                                                      |
| xml_etree_iterparse      | 63.4 ms                                                                                                                | 60.6 ms: 1.05x faster                                                                                                      |
| xml_etree_generate       | 55.5 ms                                                                                                                | 53.1 ms: 1.05x faster                                                                                                      |
| crypto_pyaes             | 45.5 ms                                                                                                                | 43.6 ms: 1.05x faster                                                                                                      |
| async_tree_none          | 227 ms                                                                                                                 | 217 ms: 1.04x faster                                                                                                       |
| pickle_pure_python       | 179 us                                                                                                                 | 172 us: 1.04x faster                                                                                                       |
| pickle_list              | 2.97 us                                                                                                                | 2.85 us: 1.04x faster                                                                                                      |
| scimark_fft              | 176 ms                                                                                                                 | 169 ms: 1.04x faster                                                                                                       |
| scimark_monte_carlo      | 40.3 ms                                                                                                                | 38.7 ms: 1.04x faster                                                                                                      |
| unpickle_pure_python     | 134 us                                                                                                                 | 129 us: 1.04x faster                                                                                                       |
| genshi_xml               | 36.1 ms                                                                                                                | 34.8 ms: 1.04x faster                                                                                                      |
| xml_etree_process        | 37.9 ms                                                                                                                | 36.6 ms: 1.04x faster                                                                                                      |
| async_tree_io_tg         | 626 ms                                                                                                                 | 605 ms: 1.03x faster                                                                                                       |
| json_dumps               | 5.73 ms                                                                                                                | 5.54 ms: 1.03x faster                                                                                                      |
| deepcopy_memo            | 21.6 us                                                                                                                | 21.0 us: 1.03x faster                                                                                                      |
| xml_etree_parse          | 93.2 ms                                                                                                                | 90.9 ms: 1.03x faster                                                                                                      |
| coroutines               | 13.3 ms                                                                                                                | 13.0 ms: 1.02x faster                                                                                                      |
| sqlglot_normalize        | 183 ms                                                                                                                 | 180 ms: 1.02x faster                                                                                                       |
| deepcopy_reduce          | 1.99 us                                                                                                                | 1.95 us: 1.02x faster                                                                                                      |
| meteor_contest           | 73.9 ms                                                                                                                | 72.5 ms: 1.02x faster                                                                                                      |
| json_loads               | 13.9 us                                                                                                                | 13.7 us: 1.02x faster                                                                                                      |
| bench_thread_pool        | 809 us                                                                                                                 | 795 us: 1.02x faster                                                                                                       |
| regex_effbot             | 1.58 ms                                                                                                                | 1.55 ms: 1.02x faster                                                                                                      |
| pprint_safe_repr         | 488 ms                                                                                                                 | 481 ms: 1.01x faster                                                                                                       |
| pathlib                  | 77.8 ms                                                                                                                | 76.8 ms: 1.01x faster                                                                                                      |
| json                     | 2.92 ms                                                                                                                | 2.89 ms: 1.01x faster                                                                                                      |
| pprint_pformat           | 989 ms                                                                                                                 | 979 ms: 1.01x faster                                                                                                       |
| sqlite_synth             | 1.61 us                                                                                                                | 1.59 us: 1.01x faster                                                                                                      |
| pidigits                 | 147 ms                                                                                                                 | 146 ms: 1.01x faster                                                                                                       |
| gc_traversal             | 1.55 ms                                                                                                                | 1.54 ms: 1.01x faster                                                                                                      |
| regex_dna                | 118 ms                                                                                                                 | 119 ms: 1.00x slower                                                                                                       |
| sqlglot_transpile        | 988 us                                                                                                                 | 994 us: 1.01x slower                                                                                                       |
| dulwich_log              | 40.1 ms                                                                                                                | 40.4 ms: 1.01x slower                                                                                                      |
| sympy_expand             | 282 ms                                                                                                                 | 285 ms: 1.01x slower                                                                                                       |
| sqlglot_parse            | 776 us                                                                                                                 | 785 us: 1.01x slower                                                                                                       |
| go                       | 90.9 ms                                                                                                                | 92.0 ms: 1.01x slower                                                                                                      |
| pickle_dict              | 18.7 us                                                                                                                | 19.0 us: 1.01x slower                                                                                                      |
| sqlglot_optimize         | 34.5 ms                                                                                                                | 35.0 ms: 1.01x slower                                                                                                      |
| typing_runtime_protocols | 71.4 us                                                                                                                | 72.5 us: 1.01x slower                                                                                                      |
| sympy_str                | 165 ms                                                                                                                 | 168 ms: 1.02x slower                                                                                                       |
| async_generators         | 231 ms                                                                                                                 | 235 ms: 1.02x slower                                                                                                       |
| aiohttp                  | 885 us                                                                                                                 | 900 us: 1.02x slower                                                                                                       |
| unpickle_list            | 2.83 us                                                                                                                | 2.90 us: 1.02x slower                                                                                                      |
| pickle                   | 7.21 us                                                                                                                | 7.39 us: 1.03x slower                                                                                                      |
| sympy_sum                | 85.8 ms                                                                                                                | 88.0 ms: 1.03x slower                                                                                                      |
| coverage                 | 45.7 ms                                                                                                                | 47.2 ms: 1.03x slower                                                                                                      |
| pylint                   | 187 ms                                                                                                                 | 194 ms: 1.03x slower                                                                                                       |
| deltablue                | 2.07 ms                                                                                                                | 2.15 ms: 1.04x slower                                                                                                      |
| 2to3                     | 213 ms                                                                                                                 | 221 ms: 1.04x slower                                                                                                       |
| docutils                 | 1.64 sec                                                                                                               | 1.70 sec: 1.04x slower                                                                                                     |
| mdp                      | 1.41 sec                                                                                                               | 1.47 sec: 1.04x slower                                                                                                     |
| nqueens                  | 58.8 ms                                                                                                                | 61.5 ms: 1.05x slower                                                                                                      |
| mypy2                    | 426 ms                                                                                                                 | 449 ms: 1.05x slower                                                                                                       |
| unpickle                 | 8.58 us                                                                                                                | 9.09 us: 1.06x slower                                                                                                      |
| sympy_integrate          | 12.6 ms                                                                                                                | 13.3 ms: 1.06x slower                                                                                                      |
| thrift                   | 8.04 ms                                                                                                                | 8.54 ms: 1.06x slower                                                                                                      |
| bench_mp_pool            | 64.3 ms                                                                                                                | 69.9 ms: 1.09x slower                                                                                                      |
| python_startup_no_site   | 18.4 ms                                                                                                                | 20.2 ms: 1.10x slower                                                                                                      |
| regex_compile            | 78.5 ms                                                                                                                | 87.0 ms: 1.11x slower                                                                                                      |
| python_startup           | 19.8 ms                                                                                                                | 22.2 ms: 1.12x slower                                                                                                      |
| scimark_sor              | 72.5 ms                                                                                                                | 83.4 ms: 1.15x slower                                                                                                      |
| hexiom                   | 3.79 ms                                                                                                                | 4.45 ms: 1.17x slower                                                                                                      |
| scimark_lu               | 54.1 ms                                                                                                                | 73.2 ms: 1.35x slower                                                                                                      |
| Geometric mean           | (ref)                                                                                                                  | 1.01x faster                                                                                                               |

Benchmark hidden because not significant (15): asyncio_tcp_ssl, async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed, deepcopy, comprehensions, asyncio_tcp, async_tree_cpu_io_mixed_tg, chaos, async_tree_io, tornado_http, raytrace, pycparser, create_gc_cycles

# HPT report

- Reliability score: 96.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown