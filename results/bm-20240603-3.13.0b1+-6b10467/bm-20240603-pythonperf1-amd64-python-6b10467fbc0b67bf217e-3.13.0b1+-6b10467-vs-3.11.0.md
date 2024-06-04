# Results vs. 3.11.0

- fork: python
- ref: 6b10467fbc0b67bf217e
- machine: windows-amd64
- commit hash: 6b10467
- commit date: 2024-06-03
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 207 ms: 1.03x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.70 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.3 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 263 ms: 1.54x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                        |
| async_tree_io              | 808 ms                                                      | 580 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 388 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 607 ms: 1.37x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.6 ms: 1.07x faster                                                       |
| nbody          | 70.3 ms                                                     | 67.2 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.0 ms: 1.18x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                       |
| regex_dna      | 116 ms                                                      | 118 ms: 1.01x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.55 ms: 1.46x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 123 us: 1.28x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 175 us: 1.19x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.3 ms: 1.07x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.8 ms: 1.06x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.3 ms: 1.01x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.68 us: 1.04x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.06x slower                                                       |
| pickle               | 6.64 us                                                     | 7.19 us: 1.08x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.44 us: 1.11x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.03 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.5 ms: 1.02x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.4 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 33.1 ms: 1.21x faster                                                       |
| mako            | 7.58 ms                                                     | 6.36 ms: 1.19x faster                                                       |
| django_template | 24.4 ms                                                     | 21.6 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.19x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1-amd64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 102 us: 3.21x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.4 ms: 1.75x faster                                                       |
| pylint                     | 323 ms                                                      | 204 ms: 1.59x faster                                                        |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 263 ms: 1.54x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 472 ms: 1.54x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.52x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.4 us: 1.51x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.55 ms: 1.46x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.89 ms: 1.43x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.44 sec: 1.41x faster                                                      |
| async_tree_io              | 808 ms                                                      | 580 ms: 1.39x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 52.4 ns: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 388 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 607 ms: 1.37x faster                                                        |
| raytrace                   | 213 ms                                                      | 159 ms: 1.34x faster                                                        |
| richards_super             | 38.7 ms                                                     | 29.3 ms: 1.32x faster                                                       |
| chaos                      | 48.4 ms                                                     | 37.6 ms: 1.29x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 123 us: 1.28x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 768 us: 1.24x faster                                                        |
| go                         | 101 ms                                                      | 82.0 ms: 1.23x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.70 ms: 1.23x faster                                                       |
| richards                   | 31.4 ms                                                     | 25.7 ms: 1.22x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 33.1 ms: 1.21x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 56.7 ms: 1.21x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 38.5 ms: 1.20x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.71 us: 1.20x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 971 us: 1.20x faster                                                        |
| mako                       | 7.58 ms                                                     | 6.36 ms: 1.19x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 175 us: 1.19x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.34 sec: 1.19x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 84.6 ms: 1.18x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 77.0 ms: 1.18x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.13 us: 1.17x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.3 us: 1.17x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 54.1 ms: 1.16x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.4 ms: 1.15x faster                                                       |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.15x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                       |
| deepcopy                   | 246 us                                                      | 218 us: 1.13x faster                                                        |
| django_template            | 24.4 ms                                                     | 21.6 ms: 1.13x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.70 ms: 1.12x faster                                                       |
| pyflate                    | 312 ms                                                      | 279 ms: 1.12x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 987 ms: 1.10x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.3 ms: 1.10x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 794 us: 1.10x faster                                                        |
| mypy2                      | 459 ms                                                      | 419 ms: 1.10x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 483 ms: 1.10x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 62.4 ms: 1.10x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 44.6 ms: 1.10x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 174 ms: 1.09x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| sympy_expand               | 299 ms                                                      | 276 ms: 1.08x faster                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.39 ms: 1.08x faster                                                       |
| float                      | 54.4 ms                                                     | 50.6 ms: 1.07x faster                                                       |
| scimark_fft                | 179 ms                                                      | 167 ms: 1.07x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 91.3 ms: 1.07x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.8 ms: 1.06x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 74.1 ms: 1.05x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.0 ms: 1.05x faster                                                       |
| nbody                      | 70.3 ms                                                     | 67.2 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.0 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.98 us: 1.04x faster                                                       |
| 2to3                       | 214 ms                                                      | 207 ms: 1.03x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 16.5 ms: 1.02x faster                                                       |
| fannkuch                   | 253 ms                                                      | 250 ms: 1.01x faster                                                        |
| regex_v8                   | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                       |
| coverage                   | 43.4 ms                                                     | 43.2 ms: 1.00x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| aiohttp                    | 883 us                                                      | 891 us: 1.01x slower                                                        |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.01x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 53.3 ms: 1.01x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 65.1 ms: 1.03x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.4 ms: 1.03x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.68 us: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 74.8 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.06x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.19 us: 1.08x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.44 us: 1.11x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.03 us: 1.12x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.60 ms: 1.13x slower                                                       |
| async_generators           | 177 ms                                                      | 223 ms: 1.26x slower                                                        |
| create_gc_cycles           | 713 us                                                      | 906 us: 1.27x slower                                                        |
| thrift                     | 494 us                                                      | 8.10 ms: 16.40x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (4): pycparser, pickle_dict, json, pidigits
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown