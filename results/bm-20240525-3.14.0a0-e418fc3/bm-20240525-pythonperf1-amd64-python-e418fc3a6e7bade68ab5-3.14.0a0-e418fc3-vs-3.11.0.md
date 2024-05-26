# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: windows-amd64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.13x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 210 ms: 1.02x faster                                                       |
| chameleon      | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.62 sec: 1.01x faster                                                     |
| html5lib       | 38.9 ms                                                     | 35.2 ms: 1.10x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 81.6 ms: 1.14x faster                                                      |
| Geometric mean | (ref)                                                       | 1.07x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 259 ms: 1.56x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 204 ms: 1.51x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 269 ms: 1.48x faster                                                       |
| async_tree_none            | 332 ms                                                      | 225 ms: 1.48x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 607 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 393 ms: 1.35x faster                                                       |
| async_tree_io              | 808 ms                                                      | 600 ms: 1.35x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.43x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.5 ms: 1.08x faster                                                      |
| nbody          | 70.3 ms                                                     | 68.7 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                       | 1.03x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 76.7 ms: 1.19x faster                                                      |
| regex_dna      | 116 ms                                                      | 117 ms: 1.01x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 14.5 ms: 1.02x slower                                                      |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                       | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.77 ms: 1.40x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 126 us: 1.24x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 177 us: 1.18x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.36 sec: 1.07x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 91.8 ms: 1.06x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.3 ms: 1.04x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.3 us: 1.01x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 53.7 ms: 1.02x slower                                                      |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                      |
| pickle               | 6.64 us                                                     | 7.23 us: 1.09x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.85 us: 1.10x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.73 us: 1.15x slower                                                      |
| pickle_list          | 2.70 us                                                     | 3.26 us: 1.21x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.6 ms: 1.02x faster                                                      |
| python_startup         | 19.8 ms                                                     | 21.0 ms: 1.06x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.02x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 31.5 ms: 1.27x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 14.6 ms: 1.26x faster                                                      |
| mako            | 7.58 ms                                                     | 6.41 ms: 1.18x faster                                                      |
| django_template | 24.4 ms                                                     | 21.9 ms: 1.12x faster                                                      |
| Geometric mean  | (ref)                                                       | 1.21x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 99.8 us: 3.26x faster                                                      |
| generators                 | 34.0 ms                                                     | 19.7 ms: 1.72x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 259 ms: 1.56x faster                                                       |
| pylint                     | 323 ms                                                      | 208 ms: 1.55x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 470 ms: 1.54x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 204 ms: 1.51x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.5 us: 1.49x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 269 ms: 1.48x faster                                                       |
| async_tree_none            | 332 ms                                                      | 225 ms: 1.48x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.90 ms: 1.42x faster                                                      |
| json_dumps                 | 8.09 ms                                                     | 5.77 ms: 1.40x faster                                                      |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.45 sec: 1.40x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 607 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                       |
| raytrace                   | 213 ms                                                      | 157 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 393 ms: 1.35x faster                                                       |
| async_tree_io              | 808 ms                                                      | 600 ms: 1.35x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 54.1 ns: 1.33x faster                                                      |
| genshi_xml                 | 39.9 ms                                                     | 31.5 ms: 1.27x faster                                                      |
| richards_super             | 38.7 ms                                                     | 30.6 ms: 1.27x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 14.6 ms: 1.26x faster                                                      |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 762 us: 1.25x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 126 us: 1.24x faster                                                       |
| go                         | 101 ms                                                      | 83.5 ms: 1.21x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 966 us: 1.21x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 83.6 ms: 1.20x faster                                                      |
| hexiom                     | 4.55 ms                                                     | 3.81 ms: 1.20x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 57.4 ms: 1.19x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 76.7 ms: 1.19x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.80 us: 1.18x faster                                                      |
| mako                       | 7.58 ms                                                     | 6.41 ms: 1.18x faster                                                      |
| pickle_pure_python         | 208 us                                                      | 177 us: 1.18x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                                      |
| richards                   | 31.4 ms                                                     | 27.0 ms: 1.16x faster                                                      |
| sympy_str                  | 185 ms                                                      | 160 ms: 1.16x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.5 us: 1.15x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.26 us: 1.14x faster                                                      |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.14x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 81.6 ms: 1.14x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.41 sec: 1.13x faster                                                     |
| deepcopy                   | 246 us                                                      | 220 us: 1.12x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.9 ms: 1.12x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 35.2 ms: 1.10x faster                                                      |
| sympy_expand               | 299 ms                                                      | 272 ms: 1.10x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.2 ms: 1.10x faster                                                      |
| pyflate                    | 312 ms                                                      | 284 ms: 1.10x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 997 ms: 1.09x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 175 ms: 1.09x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 802 us: 1.09x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 58.1 ms: 1.08x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 492 ms: 1.08x faster                                                       |
| float                      | 54.4 ms                                                     | 50.5 ms: 1.08x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.36 sec: 1.07x faster                                                     |
| crypto_pyaes               | 48.9 ms                                                     | 45.9 ms: 1.06x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 91.8 ms: 1.06x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 64.7 ms: 1.06x faster                                                      |
| pycparser                  | 720 ms                                                      | 684 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 71.5 ms: 1.05x faster                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 33.3 ms: 1.04x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.3 ms: 1.04x faster                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 2.00 us: 1.03x faster                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.51 ms: 1.03x faster                                                      |
| nbody                      | 70.3 ms                                                     | 68.7 ms: 1.02x faster                                                      |
| fannkuch                   | 253 ms                                                      | 249 ms: 1.02x faster                                                       |
| 2to3                       | 214 ms                                                      | 210 ms: 1.02x faster                                                       |
| xml_etree_process          | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 16.6 ms: 1.02x faster                                                      |
| docutils                   | 1.64 sec                                                    | 1.62 sec: 1.01x faster                                                     |
| pickle_dict                | 18.5 us                                                     | 18.3 us: 1.01x faster                                                      |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                     |
| regex_dna                  | 116 ms                                                      | 117 ms: 1.01x slower                                                       |
| scimark_fft                | 179 ms                                                      | 181 ms: 1.01x slower                                                       |
| thrift                     | 494 us                                                      | 501 us: 1.01x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.5 ms: 1.02x slower                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 53.7 ms: 1.02x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 66.2 ms: 1.05x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| python_startup             | 19.8 ms                                                     | 21.0 ms: 1.06x slower                                                      |
| coverage                   | 43.4 ms                                                     | 46.3 ms: 1.07x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.23 us: 1.09x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.85 us: 1.10x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 78.7 ms: 1.11x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.73 us: 1.15x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.70 ms: 1.16x slower                                                      |
| pickle_list                | 2.70 us                                                     | 3.26 us: 1.21x slower                                                      |
| async_generators           | 177 ms                                                      | 223 ms: 1.26x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 916 us: 1.28x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.13x faster                                                               |

Benchmark hidden because not significant (3): json, pidigits, scimark_sor
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown