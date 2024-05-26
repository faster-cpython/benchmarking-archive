# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: windows-amd64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 244 ms: 1.14x slower                                                       |
| chameleon      | 5.26 ms                                                     | 5.14 ms: 1.02x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                     |
| html5lib       | 38.9 ms                                                     | 37.5 ms: 1.04x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 85.3 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.46x faster                                                       |
| async_tree_none            | 332 ms                                                      | 228 ms: 1.46x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 281 ms: 1.42x faster                                                       |
| async_tree_io              | 808 ms                                                      | 603 ms: 1.34x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 393 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 401 ms: 1.32x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 51.2 ms: 1.37x faster                                                      |
| float          | 54.4 ms                                                     | 43.4 ms: 1.25x faster                                                      |
| Geometric mean | (ref)                                                       | 1.20x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.5 ms: 1.04x faster                                                      |
| regex_dna      | 116 ms                                                      | 117 ms: 1.01x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                       | 1.02x slower                                                               |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.75 ms: 1.41x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 170 us: 1.23x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.23 sec: 1.19x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.1 ms: 1.07x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 17.5 us: 1.06x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.0 ms: 1.03x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 50.9 ms: 1.03x faster                                                      |
| pickle_list          | 2.70 us                                                     | 2.87 us: 1.06x slower                                                      |
| pickle               | 6.64 us                                                     | 7.08 us: 1.07x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.09x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.92 us: 1.13x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.96 us: 1.18x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.8 ms: 1.12x slower                                                      |
| python_startup         | 19.8 ms                                                     | 22.8 ms: 1.15x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 4.90 ms: 1.55x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 18.2 ms: 1.02x faster                                                      |
| django_template | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                      |
| genshi_xml      | 39.9 ms                                                     | 44.8 ms: 1.12x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.08x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 115 us: 2.83x faster                                                       |
| generators                 | 34.0 ms                                                     | 21.2 ms: 1.60x faster                                                      |
| mako                       | 7.58 ms                                                     | 4.90 ms: 1.55x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 487 ms: 1.49x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.37 sec: 1.48x faster                                                     |
| spectral_norm              | 68.3 ms                                                     | 46.1 ms: 1.48x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.46x faster                                                       |
| async_tree_none            | 332 ms                                                      | 228 ms: 1.46x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 281 ms: 1.42x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.75 ms: 1.41x faster                                                      |
| nbody                      | 70.3 ms                                                     | 51.2 ms: 1.37x faster                                                      |
| pylint                     | 323 ms                                                      | 236 ms: 1.37x faster                                                       |
| async_tree_io              | 808 ms                                                      | 603 ms: 1.34x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 393 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 401 ms: 1.32x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 54.5 ns: 1.32x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 20.7 us: 1.26x faster                                                      |
| float                      | 54.4 ms                                                     | 43.4 ms: 1.25x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 170 us: 1.23x faster                                                       |
| pyflate                    | 312 ms                                                      | 256 ms: 1.22x faster                                                       |
| raytrace                   | 213 ms                                                      | 175 ms: 1.22x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.21x faster                                                      |
| chaos                      | 48.4 ms                                                     | 40.3 ms: 1.20x faster                                                      |
| scimark_fft                | 179 ms                                                      | 149 ms: 1.20x faster                                                       |
| richards_super             | 38.7 ms                                                     | 32.3 ms: 1.20x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.76 us: 1.19x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.23 sec: 1.19x faster                                                     |
| sqlglot_parse              | 953 us                                                      | 805 us: 1.18x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.3 ms: 1.18x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 41.4 ms: 1.18x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.15 us: 1.16x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 935 ms: 1.16x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.35 ms: 1.15x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 461 ms: 1.15x faster                                                       |
| fannkuch                   | 253 ms                                                      | 221 ms: 1.15x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.45 sec: 1.10x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 62.0 ms: 1.10x faster                                                      |
| richards                   | 31.4 ms                                                     | 28.7 ms: 1.10x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 85.3 ms: 1.09x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 92.4 ms: 1.08x faster                                                      |
| go                         | 101 ms                                                      | 93.7 ms: 1.08x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.1 ms: 1.07x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 826 us: 1.06x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 17.5 us: 1.06x faster                                                      |
| sympy_str                  | 185 ms                                                      | 177 ms: 1.04x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 87.5 ms: 1.04x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 37.5 ms: 1.04x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.0 ms: 1.03x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 50.9 ms: 1.03x faster                                                      |
| deepcopy                   | 246 us                                                      | 240 us: 1.03x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 73.2 ms: 1.03x faster                                                      |
| chameleon                  | 5.26 ms                                                     | 5.14 ms: 1.02x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 18.2 ms: 1.02x faster                                                      |
| sympy_integrate            | 14.0 ms                                                     | 13.9 ms: 1.01x faster                                                      |
| regex_dna                  | 116 ms                                                      | 117 ms: 1.01x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 4.67 ms: 1.03x slower                                                      |
| sympy_expand               | 299 ms                                                      | 309 ms: 1.03x slower                                                       |
| thrift                     | 494 us                                                      | 513 us: 1.04x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 81.5 ms: 1.04x slower                                                      |
| coverage                   | 43.4 ms                                                     | 45.3 ms: 1.04x slower                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 2.15 us: 1.04x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| django_template            | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                      |
| pickle_list                | 2.70 us                                                     | 2.87 us: 1.06x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 36.8 ms: 1.07x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.08 us: 1.07x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 67.7 ms: 1.08x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                     |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.09x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 78.8 ms: 1.11x slower                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 18.8 ms: 1.12x slower                                                      |
| genshi_xml                 | 39.9 ms                                                     | 44.8 ms: 1.12x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.92 us: 1.13x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.62 ms: 1.14x slower                                                      |
| 2to3                       | 214 ms                                                      | 244 ms: 1.14x slower                                                       |
| python_startup             | 19.8 ms                                                     | 22.8 ms: 1.15x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 73.8 ms: 1.17x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.96 us: 1.18x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 911 us: 1.28x slower                                                       |
| async_generators           | 177 ms                                                      | 253 ms: 1.43x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                               |

Benchmark hidden because not significant (5): json, pidigits, flaskblogging, pycparser, regex_v8
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown