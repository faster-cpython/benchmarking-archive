# Results vs. base

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 210 ms                                                                                                                 | 222 ms: 1.06x slower                                                                                                               |
| chameleon      | 5.01 ms                                                                                                                | 4.90 ms: 1.02x faster                                                                                                              |
| docutils       | 1.64 sec                                                                                                               | 1.75 sec: 1.07x slower                                                                                                             |
| html5lib       | 36.2 ms                                                                                                                | 36.9 ms: 1.02x slower                                                                                                              |
| tornado_http   | 82.2 ms                                                                                                                | 83.9 ms: 1.02x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.03x slower                                                                                                                       |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| float          | 51.6 ms                                                                                                                | 57.0 ms: 1.10x slower                                                                                                              |
| nbody          | 70.2 ms                                                                                                                | 79.3 ms: 1.13x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.08x slower                                                                                                                       |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 122 ms                                                                                                                 | 121 ms: 1.01x faster                                                                                                               |
| regex_compile  | 79.8 ms                                                                                                                | 103 ms: 1.29x slower                                                                                                               |
| Geometric mean | (ref)                                                                                                                  | 1.05x slower                                                                                                                       |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 2.94 us                                                                                                                | 2.82 us: 1.04x faster                                                                                                              |
| pickle               | 7.14 us                                                                                                                | 7.17 us: 1.00x slower                                                                                                              |
| pickle_dict          | 18.6 us                                                                                                                | 18.7 us: 1.01x slower                                                                                                              |
| xml_etree_parse      | 91.2 ms                                                                                                                | 92.1 ms: 1.01x slower                                                                                                              |
| pickle_pure_python   | 179 us                                                                                                                 | 182 us: 1.01x slower                                                                                                               |
| unpickle_list        | 2.80 us                                                                                                                | 2.88 us: 1.03x slower                                                                                                              |
| xml_etree_generate   | 55.3 ms                                                                                                                | 56.9 ms: 1.03x slower                                                                                                              |
| tomli_loads          | 1.41 sec                                                                                                               | 1.46 sec: 1.03x slower                                                                                                             |
| xml_etree_process    | 37.7 ms                                                                                                                | 39.1 ms: 1.04x slower                                                                                                              |
| xml_etree_iterparse  | 64.0 ms                                                                                                                | 66.6 ms: 1.04x slower                                                                                                              |
| unpickle             | 8.36 us                                                                                                                | 8.83 us: 1.06x slower                                                                                                              |
| unpickle_pure_python | 129 us                                                                                                                 | 155 us: 1.20x slower                                                                                                               |
| Geometric mean       | (ref)                                                                                                                  | 1.03x slower                                                                                                                       |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|------------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 17.0 ms                                                                                                                | 16.1 ms: 1.06x faster                                                                                                              |
| python_startup         | 20.3 ms                                                                                                                | 19.7 ms: 1.03x faster                                                                                                              |
| Geometric mean         | (ref)                                                                                                                  | 1.04x faster                                                                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| genshi_text    | 16.5 ms                                                                                                                | 16.7 ms: 1.01x slower                                                                                                              |
| mako           | 6.38 ms                                                                                                                | 7.07 ms: 1.11x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.04x slower                                                                                                                       |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|--------------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site   | 17.0 ms                                                                                                                | 16.1 ms: 1.06x faster                                                                                                              |
| pickle_list              | 2.94 us                                                                                                                | 2.82 us: 1.04x faster                                                                                                              |
| richards                 | 28.3 ms                                                                                                                | 27.3 ms: 1.04x faster                                                                                                              |
| richards_super           | 32.3 ms                                                                                                                | 31.2 ms: 1.03x faster                                                                                                              |
| python_startup           | 20.3 ms                                                                                                                | 19.7 ms: 1.03x faster                                                                                                              |
| chameleon                | 5.01 ms                                                                                                                | 4.90 ms: 1.02x faster                                                                                                              |
| regex_dna                | 122 ms                                                                                                                 | 121 ms: 1.01x faster                                                                                                               |
| telco                    | 5.05 ms                                                                                                                | 5.03 ms: 1.01x faster                                                                                                              |
| pickle                   | 7.14 us                                                                                                                | 7.17 us: 1.00x slower                                                                                                              |
| pickle_dict              | 18.6 us                                                                                                                | 18.7 us: 1.01x slower                                                                                                              |
| pathlib                  | 75.2 ms                                                                                                                | 75.7 ms: 1.01x slower                                                                                                              |
| gc_traversal             | 1.55 ms                                                                                                                | 1.56 ms: 1.01x slower                                                                                                              |
| xml_etree_parse          | 91.2 ms                                                                                                                | 92.1 ms: 1.01x slower                                                                                                              |
| genshi_text              | 16.5 ms                                                                                                                | 16.7 ms: 1.01x slower                                                                                                              |
| coverage                 | 46.0 ms                                                                                                                | 46.4 ms: 1.01x slower                                                                                                              |
| pickle_pure_python       | 179 us                                                                                                                 | 182 us: 1.01x slower                                                                                                               |
| create_gc_cycles         | 895 us                                                                                                                 | 909 us: 1.02x slower                                                                                                               |
| bench_mp_pool            | 64.2 ms                                                                                                                | 65.2 ms: 1.02x slower                                                                                                              |
| html5lib                 | 36.2 ms                                                                                                                | 36.9 ms: 1.02x slower                                                                                                              |
| bench_thread_pool        | 811 us                                                                                                                 | 827 us: 1.02x slower                                                                                                               |
| tornado_http             | 82.2 ms                                                                                                                | 83.9 ms: 1.02x slower                                                                                                              |
| logging_simple           | 5.98 us                                                                                                                | 6.14 us: 1.03x slower                                                                                                              |
| unpickle_list            | 2.80 us                                                                                                                | 2.88 us: 1.03x slower                                                                                                              |
| xml_etree_generate       | 55.3 ms                                                                                                                | 56.9 ms: 1.03x slower                                                                                                              |
| meteor_contest           | 72.8 ms                                                                                                                | 74.9 ms: 1.03x slower                                                                                                              |
| aiohttp                  | 885 us                                                                                                                 | 911 us: 1.03x slower                                                                                                               |
| logging_format           | 6.42 us                                                                                                                | 6.62 us: 1.03x slower                                                                                                              |
| tomli_loads              | 1.41 sec                                                                                                               | 1.46 sec: 1.03x slower                                                                                                             |
| typing_runtime_protocols | 73.8 us                                                                                                                | 76.6 us: 1.04x slower                                                                                                              |
| xml_etree_process        | 37.7 ms                                                                                                                | 39.1 ms: 1.04x slower                                                                                                              |
| async_generators         | 235 ms                                                                                                                 | 245 ms: 1.04x slower                                                                                                               |
| xml_etree_iterparse      | 64.0 ms                                                                                                                | 66.6 ms: 1.04x slower                                                                                                              |
| deepcopy                 | 222 us                                                                                                                 | 231 us: 1.04x slower                                                                                                               |
| generators               | 21.7 ms                                                                                                                | 22.6 ms: 1.04x slower                                                                                                              |
| mdp                      | 1.49 sec                                                                                                               | 1.56 sec: 1.05x slower                                                                                                             |
| sqlglot_normalize        | 179 ms                                                                                                                 | 189 ms: 1.05x slower                                                                                                               |
| pylint                   | 188 ms                                                                                                                 | 198 ms: 1.05x slower                                                                                                               |
| deepcopy_memo            | 22.3 us                                                                                                                | 23.5 us: 1.06x slower                                                                                                              |
| unpickle                 | 8.36 us                                                                                                                | 8.83 us: 1.06x slower                                                                                                              |
| 2to3                     | 210 ms                                                                                                                 | 222 ms: 1.06x slower                                                                                                               |
| raytrace                 | 165 ms                                                                                                                 | 175 ms: 1.06x slower                                                                                                               |
| fannkuch                 | 257 ms                                                                                                                 | 274 ms: 1.07x slower                                                                                                               |
| sqlglot_transpile        | 982 us                                                                                                                 | 1.05 ms: 1.07x slower                                                                                                              |
| docutils                 | 1.64 sec                                                                                                               | 1.75 sec: 1.07x slower                                                                                                             |
| sqlglot_parse            | 776 us                                                                                                                 | 829 us: 1.07x slower                                                                                                               |
| scimark_fft              | 185 ms                                                                                                                 | 199 ms: 1.08x slower                                                                                                               |
| crypto_pyaes             | 45.7 ms                                                                                                                | 49.5 ms: 1.08x slower                                                                                                              |
| pprint_safe_repr         | 491 ms                                                                                                                 | 532 ms: 1.08x slower                                                                                                               |
| sqlglot_optimize         | 34.0 ms                                                                                                                | 36.8 ms: 1.08x slower                                                                                                              |
| mypy2                    | 418 ms                                                                                                                 | 454 ms: 1.09x slower                                                                                                               |
| pprint_pformat           | 1.00 sec                                                                                                               | 1.09 sec: 1.09x slower                                                                                                             |
| sympy_integrate          | 12.6 ms                                                                                                                | 13.8 ms: 1.09x slower                                                                                                              |
| sympy_sum                | 85.4 ms                                                                                                                | 93.8 ms: 1.10x slower                                                                                                              |
| dulwich_log              | 40.3 ms                                                                                                                | 44.3 ms: 1.10x slower                                                                                                              |
| float                    | 51.6 ms                                                                                                                | 57.0 ms: 1.10x slower                                                                                                              |
| mako                     | 6.38 ms                                                                                                                | 7.07 ms: 1.11x slower                                                                                                              |
| sympy_expand             | 274 ms                                                                                                                 | 307 ms: 1.12x slower                                                                                                               |
| sympy_str                | 163 ms                                                                                                                 | 182 ms: 1.12x slower                                                                                                               |
| go                       | 90.0 ms                                                                                                                | 101 ms: 1.12x slower                                                                                                               |
| chaos                    | 39.2 ms                                                                                                                | 44.2 ms: 1.13x slower                                                                                                              |
| nbody                    | 70.2 ms                                                                                                                | 79.3 ms: 1.13x slower                                                                                                              |
| thrift                   | 8.03 ms                                                                                                                | 9.24 ms: 1.15x slower                                                                                                              |
| pyflate                  | 289 ms                                                                                                                 | 332 ms: 1.15x slower                                                                                                               |
| scimark_sparse_mat_mult  | 2.66 ms                                                                                                                | 3.08 ms: 1.16x slower                                                                                                              |
| scimark_sor              | 76.6 ms                                                                                                                | 89.4 ms: 1.17x slower                                                                                                              |
| nqueens                  | 60.8 ms                                                                                                                | 71.2 ms: 1.17x slower                                                                                                              |
| deltablue                | 2.04 ms                                                                                                                | 2.44 ms: 1.20x slower                                                                                                              |
| unpickle_pure_python     | 129 us                                                                                                                 | 155 us: 1.20x slower                                                                                                               |
| scimark_monte_carlo      | 40.6 ms                                                                                                                | 49.0 ms: 1.21x slower                                                                                                              |
| spectral_norm            | 63.3 ms                                                                                                                | 79.0 ms: 1.25x slower                                                                                                              |
| comprehensions           | 10.8 us                                                                                                                | 13.9 us: 1.29x slower                                                                                                              |
| regex_compile            | 79.8 ms                                                                                                                | 103 ms: 1.29x slower                                                                                                               |
| hexiom                   | 3.87 ms                                                                                                                | 5.19 ms: 1.34x slower                                                                                                              |
| scimark_lu               | 57.0 ms                                                                                                                | 78.6 ms: 1.38x slower                                                                                                              |
| Geometric mean           | (ref)                                                                                                                  | 1.05x slower                                                                                                                       |

Benchmark hidden because not significant (22): asyncio_tcp_ssl, regex_v8, pycparser, json, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_cpu_io_mixed, asyncio_tcp, deepcopy_reduce, async_tree_io, pidigits, coroutines, regex_effbot, json_loads, async_tree_io_tg, logging_silent, sqlite_synth, json_dumps, genshi_xml, async_tree_none, async_tree_memoization, async_tree_memoization_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown