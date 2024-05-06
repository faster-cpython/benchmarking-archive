# Results vs. 3.11.0

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: ced0ca9
- commit date: 2024-04-16
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 210 ms: 1.02x faster                                                     |
| chameleon      | 5.26 ms                                                     | 4.80 ms: 1.10x faster                                                    |
| html5lib       | 38.9 ms                                                     | 35.8 ms: 1.09x faster                                                    |
| tornado_http   | 92.8 ms                                                     | 80.8 ms: 1.15x faster                                                    |
| Geometric mean | (ref)                                                       | 1.07x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                     |
| async_tree_none            | 332 ms                                                      | 222 ms: 1.49x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 270 ms: 1.48x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 217 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                     |
| async_tree_io              | 808 ms                                                      | 595 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 391 ms: 1.36x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 617 ms: 1.34x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.41x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.7 ms: 1.07x faster                                                    |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| nbody          | 70.3 ms                                                     | 70.8 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                       | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 79.8 ms: 1.14x faster                                                    |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                                    |
| regex_v8       | 14.2 ms                                                     | 18.3 ms: 1.29x slower                                                    |
| Geometric mean | (ref)                                                       | 1.04x slower                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.64 ms: 1.43x faster                                                    |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                     |
| pickle_pure_python   | 208 us                                                      | 176 us: 1.19x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 92.8 ms: 1.05x faster                                                    |
| tomli_loads          | 1.46 sec                                                    | 1.41 sec: 1.03x faster                                                   |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.1 ms: 1.02x faster                                                    |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.01x slower                                                    |
| xml_etree_generate   | 52.5 ms                                                     | 54.5 ms: 1.04x slower                                                    |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                    |
| pickle               | 6.64 us                                                     | 7.13 us: 1.07x slower                                                    |
| unpickle             | 7.57 us                                                     | 8.25 us: 1.09x slower                                                    |
| unpickle_list        | 2.59 us                                                     | 2.83 us: 1.09x slower                                                    |
| pickle_list          | 2.70 us                                                     | 3.16 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.0 ms: 1.05x faster                                                    |
| Geometric mean         | (ref)                                                       | 1.03x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.33 ms: 1.20x faster                                                    |
| genshi_xml      | 39.9 ms                                                     | 33.5 ms: 1.19x faster                                                    |
| genshi_text     | 18.4 ms                                                     | 15.9 ms: 1.16x faster                                                    |
| django_template | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.16x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 73.9 us: 4.41x faster                                                    |
| generators                 | 34.0 ms                                                     | 21.4 ms: 1.59x faster                                                    |
| pylint                     | 323 ms                                                      | 208 ms: 1.55x faster                                                     |
| asyncio_tcp                | 726 ms                                                      | 475 ms: 1.53x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                     |
| async_tree_none            | 332 ms                                                      | 222 ms: 1.49x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 270 ms: 1.48x faster                                                     |
| comprehensions             | 15.6 us                                                     | 10.7 us: 1.47x faster                                                    |
| json_dumps                 | 8.09 ms                                                     | 5.64 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 309 ms                                                      | 217 ms: 1.42x faster                                                     |
| deltablue                  | 2.70 ms                                                     | 1.95 ms: 1.38x faster                                                    |
| raytrace                   | 213 ms                                                      | 156 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                     |
| async_tree_io              | 808 ms                                                      | 595 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 391 ms: 1.36x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 617 ms: 1.34x faster                                                     |
| logging_silent             | 71.8 ns                                                     | 54.1 ns: 1.33x faster                                                    |
| richards_super             | 38.7 ms                                                     | 30.2 ms: 1.28x faster                                                    |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                                    |
| sqlglot_parse              | 953 us                                                      | 760 us: 1.25x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                     |
| hexiom                     | 4.55 ms                                                     | 3.77 ms: 1.21x faster                                                    |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.69 sec: 1.20x faster                                                   |
| sqlglot_transpile          | 1.16 ms                                                     | 971 us: 1.20x faster                                                     |
| mako                       | 7.58 ms                                                     | 6.33 ms: 1.20x faster                                                    |
| genshi_xml                 | 39.9 ms                                                     | 33.5 ms: 1.19x faster                                                    |
| deepcopy_memo              | 26.0 us                                                     | 21.8 us: 1.19x faster                                                    |
| go                         | 101 ms                                                      | 85.1 ms: 1.19x faster                                                    |
| pickle_pure_python         | 208 us                                                      | 176 us: 1.19x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 84.5 ms: 1.19x faster                                                    |
| richards                   | 31.4 ms                                                     | 26.5 ms: 1.18x faster                                                    |
| dulwich_log                | 46.4 ms                                                     | 39.5 ms: 1.17x faster                                                    |
| genshi_text                | 18.4 ms                                                     | 15.9 ms: 1.16x faster                                                    |
| logging_simple             | 6.86 us                                                     | 5.96 us: 1.15x faster                                                    |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                     |
| tornado_http               | 92.8 ms                                                     | 80.8 ms: 1.15x faster                                                    |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.15x faster                                                    |
| mdp                        | 1.59 sec                                                    | 1.39 sec: 1.14x faster                                                   |
| nqueens                    | 68.3 ms                                                     | 59.7 ms: 1.14x faster                                                    |
| regex_compile              | 91.0 ms                                                     | 79.8 ms: 1.14x faster                                                    |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.8 ms: 1.14x faster                                                    |
| logging_format             | 7.16 us                                                     | 6.38 us: 1.12x faster                                                    |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.12x faster                                                    |
| deepcopy                   | 246 us                                                      | 221 us: 1.12x faster                                                     |
| sympy_expand               | 299 ms                                                      | 272 ms: 1.10x faster                                                     |
| chameleon                  | 5.26 ms                                                     | 4.80 ms: 1.10x faster                                                    |
| mypy2                      | 459 ms                                                      | 419 ms: 1.10x faster                                                     |
| pprint_pformat             | 1.09 sec                                                    | 993 ms: 1.10x faster                                                     |
| spectral_norm              | 68.3 ms                                                     | 62.5 ms: 1.09x faster                                                    |
| django_template            | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                                    |
| html5lib                   | 38.9 ms                                                     | 35.8 ms: 1.09x faster                                                    |
| scimark_lu                 | 62.8 ms                                                     | 57.9 ms: 1.08x faster                                                    |
| pprint_safe_repr           | 529 ms                                                      | 489 ms: 1.08x faster                                                     |
| pyflate                    | 312 ms                                                      | 290 ms: 1.08x faster                                                     |
| bench_thread_pool          | 872 us                                                      | 809 us: 1.08x faster                                                     |
| sqlglot_normalize          | 190 ms                                                      | 177 ms: 1.08x faster                                                     |
| float                      | 54.4 ms                                                     | 50.7 ms: 1.07x faster                                                    |
| sqlite_synth               | 1.77 us                                                     | 1.65 us: 1.07x faster                                                    |
| python_startup_no_site     | 16.8 ms                                                     | 16.0 ms: 1.05x faster                                                    |
| xml_etree_parse            | 97.6 ms                                                     | 92.8 ms: 1.05x faster                                                    |
| crypto_pyaes               | 48.9 ms                                                     | 46.6 ms: 1.05x faster                                                    |
| pycparser                  | 720 ms                                                      | 689 ms: 1.04x faster                                                     |
| meteor_contest             | 75.2 ms                                                     | 72.7 ms: 1.04x faster                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 33.4 ms: 1.03x faster                                                    |
| tomli_loads                | 1.46 sec                                                    | 1.41 sec: 1.03x faster                                                   |
| deepcopy_reduce            | 2.06 us                                                     | 2.01 us: 1.02x faster                                                    |
| scimark_sor                | 78.1 ms                                                     | 76.3 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.1 ms: 1.02x faster                                                    |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| 2to3                       | 214 ms                                                      | 210 ms: 1.02x faster                                                     |
| aiohttp                    | 883 us                                                      | 875 us: 1.01x faster                                                     |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.01x slower                                                    |
| nbody                      | 70.3 ms                                                     | 70.8 ms: 1.01x slower                                                    |
| bench_mp_pool              | 63.2 ms                                                     | 63.8 ms: 1.01x slower                                                    |
| fannkuch                   | 253 ms                                                      | 257 ms: 1.02x slower                                                     |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                    |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                                    |
| xml_etree_generate         | 52.5 ms                                                     | 54.5 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.68 ms: 1.04x slower                                                    |
| scimark_fft                | 179 ms                                                      | 190 ms: 1.06x slower                                                     |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                    |
| coverage                   | 43.4 ms                                                     | 46.4 ms: 1.07x slower                                                    |
| pickle                     | 6.64 us                                                     | 7.13 us: 1.07x slower                                                    |
| pathlib                    | 70.9 ms                                                     | 76.1 ms: 1.07x slower                                                    |
| unpickle                   | 7.57 us                                                     | 8.25 us: 1.09x slower                                                    |
| unpickle_list              | 2.59 us                                                     | 2.83 us: 1.09x slower                                                    |
| pickle_list                | 2.70 us                                                     | 3.16 us: 1.17x slower                                                    |
| telco                      | 4.06 ms                                                     | 5.09 ms: 1.25x slower                                                    |
| create_gc_cycles           | 713 us                                                      | 899 us: 1.26x slower                                                     |
| regex_v8                   | 14.2 ms                                                     | 18.3 ms: 1.29x slower                                                    |
| async_generators           | 177 ms                                                      | 229 ms: 1.29x slower                                                     |
| thrift                     | 494 us                                                      | 7.91 ms: 16.02x slower                                                   |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                             |

Benchmark hidden because not significant (5): python_startup, xml_etree_process, regex_dna, docutils, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown