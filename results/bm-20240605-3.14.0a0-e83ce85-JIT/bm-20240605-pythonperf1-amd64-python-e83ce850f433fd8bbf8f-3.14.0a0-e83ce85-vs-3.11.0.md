# Results vs. 3.11.0

- fork: python
- ref: e83ce850f433fd8bbf8f
- machine: windows-amd64
- commit hash: e83ce85
- commit date: 2024-06-05
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 230 ms: 1.07x slower                                                       |
| docutils       | 1.64 sec                                                    | 1.78 sec: 1.08x slower                                                     |
| html5lib       | 38.9 ms                                                     | 36.8 ms: 1.06x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 86.2 ms: 1.08x faster                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 266 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 210 ms: 1.47x faster                                                       |
| async_tree_none            | 332 ms                                                      | 229 ms: 1.45x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 277 ms: 1.44x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 617 ms: 1.34x faster                                                       |
| async_tree_io              | 808 ms                                                      | 603 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.33x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 53.1 ms: 1.32x faster                                                      |
| float          | 54.4 ms                                                     | 44.2 ms: 1.23x faster                                                      |
| pidigits       | 150 ms                                                      | 149 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                       | 1.18x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.3 ms: 1.03x faster                                                      |
| regex_dna      | 116 ms                                                      | 118 ms: 1.01x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 14.5 ms: 1.02x slower                                                      |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.75 ms: 1.41x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.22x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 91.5 ms: 1.07x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 17.8 us: 1.04x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 51.2 ms: 1.03x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.3 ms: 1.02x faster                                                      |
| pickle_list          | 2.70 us                                                     | 2.73 us: 1.01x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.08x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.82 us: 1.09x slower                                                      |
| pickle               | 6.64 us                                                     | 7.29 us: 1.10x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.77 us: 1.16x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                      |
| python_startup         | 19.8 ms                                                     | 21.8 ms: 1.10x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.08x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.24 ms: 1.45x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 18.1 ms: 1.02x faster                                                      |
| django_template | 24.4 ms                                                     | 25.2 ms: 1.03x slower                                                      |
| genshi_xml      | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.06x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 112 us: 2.90x faster                                                       |
| generators                 | 34.0 ms                                                     | 21.6 ms: 1.57x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 470 ms: 1.55x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 44.2 ms: 1.54x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.53x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 266 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 210 ms: 1.47x faster                                                       |
| async_tree_none            | 332 ms                                                      | 229 ms: 1.45x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.24 ms: 1.45x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 277 ms: 1.44x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.41 sec: 1.44x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.75 ms: 1.41x faster                                                      |
| pylint                     | 323 ms                                                      | 235 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 617 ms: 1.34x faster                                                       |
| async_tree_io              | 808 ms                                                      | 603 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.33x faster                                                       |
| nbody                      | 70.3 ms                                                     | 53.1 ms: 1.32x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 55.4 ns: 1.29x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 20.9 us: 1.24x faster                                                      |
| float                      | 54.4 ms                                                     | 44.2 ms: 1.23x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.22x faster                                                       |
| pyflate                    | 312 ms                                                      | 257 ms: 1.22x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                       |
| chaos                      | 48.4 ms                                                     | 40.1 ms: 1.21x faster                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.20x faster                                                      |
| raytrace                   | 213 ms                                                      | 178 ms: 1.20x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 37.7 ms: 1.20x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                     |
| scimark_fft                | 179 ms                                                      | 150 ms: 1.20x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 808 us: 1.18x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 41.6 ms: 1.18x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.84 us: 1.18x faster                                                      |
| fannkuch                   | 253 ms                                                      | 217 ms: 1.16x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 457 ms: 1.16x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.35 ms: 1.15x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 949 ms: 1.15x faster                                                       |
| richards_super             | 38.7 ms                                                     | 33.8 ms: 1.14x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.27 us: 1.14x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 60.5 ms: 1.13x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.12x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 809 us: 1.08x faster                                                       |
| go                         | 101 ms                                                      | 93.8 ms: 1.08x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 86.2 ms: 1.08x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.49 sec: 1.07x faster                                                     |
| xml_etree_parse            | 97.6 ms                                                     | 91.5 ms: 1.07x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 94.3 ms: 1.06x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 36.8 ms: 1.06x faster                                                      |
| richards                   | 31.4 ms                                                     | 30.1 ms: 1.04x faster                                                      |
| sympy_str                  | 185 ms                                                      | 178 ms: 1.04x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 17.8 us: 1.04x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 88.3 ms: 1.03x faster                                                      |
| deepcopy                   | 246 us                                                      | 239 us: 1.03x faster                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 51.2 ms: 1.03x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 73.3 ms: 1.03x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.3 ms: 1.02x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 18.1 ms: 1.02x faster                                                      |
| pidigits                   | 150 ms                                                      | 149 ms: 1.00x faster                                                       |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.01x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.73 us: 1.01x slower                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 2.10 us: 1.02x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 14.5 ms: 1.02x slower                                                      |
| hexiom                     | 4.55 ms                                                     | 4.67 ms: 1.03x slower                                                      |
| thrift                     | 494 us                                                      | 508 us: 1.03x slower                                                       |
| django_template            | 24.4 ms                                                     | 25.2 ms: 1.03x slower                                                      |
| sympy_expand               | 299 ms                                                      | 309 ms: 1.03x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                      |
| coverage                   | 43.4 ms                                                     | 45.8 ms: 1.05x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 74.9 ms: 1.06x slower                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                      |
| 2to3                       | 214 ms                                                      | 230 ms: 1.07x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 37.3 ms: 1.08x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.78 sec: 1.08x slower                                                     |
| scimark_sor                | 78.1 ms                                                     | 84.7 ms: 1.08x slower                                                      |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.08x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.82 us: 1.09x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 69.3 ms: 1.10x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.29 us: 1.10x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 69.1 ms: 1.10x slower                                                      |
| python_startup             | 19.8 ms                                                     | 21.8 ms: 1.10x slower                                                      |
| genshi_xml                 | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.55 ms: 1.12x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.77 us: 1.16x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 908 us: 1.27x slower                                                       |
| async_generators           | 177 ms                                                      | 254 ms: 1.43x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                               |

Benchmark hidden because not significant (3): json, pycparser, sympy_integrate
Ignored benchmarks (10) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown