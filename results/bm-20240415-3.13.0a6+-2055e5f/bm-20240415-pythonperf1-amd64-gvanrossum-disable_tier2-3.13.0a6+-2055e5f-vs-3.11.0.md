# Results vs. 3.11.0

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 211 ms: 1.01x faster                                                     |
| chameleon      | 5.26 ms                                                     | 4.87 ms: 1.08x faster                                                    |
| html5lib       | 38.9 ms                                                     | 36.8 ms: 1.06x faster                                                    |
| tornado_http   | 92.8 ms                                                     | 82.6 ms: 1.12x faster                                                    |
| Geometric mean | (ref)                                                       | 1.05x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 274 ms: 1.47x faster                                                     |
| async_tree_none            | 332 ms                                                      | 229 ms: 1.45x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 225 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.35x faster                                                     |
| async_tree_io              | 808 ms                                                      | 606 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 399 ms: 1.33x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 627 ms: 1.32x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 53.0 ms: 1.03x faster                                                    |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| nbody          | 70.3 ms                                                     | 69.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                       | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 80.8 ms: 1.13x faster                                                    |
| regex_dna      | 116 ms                                                      | 120 ms: 1.03x slower                                                     |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                    |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                       | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.71 ms: 1.42x faster                                                    |
| unpickle_pure_python | 157 us                                                      | 133 us: 1.18x faster                                                     |
| pickle_pure_python   | 208 us                                                      | 183 us: 1.14x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.8 ms: 1.03x faster                                                    |
| tomli_loads          | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                   |
| xml_etree_process    | 37.2 ms                                                     | 38.5 ms: 1.03x slower                                                    |
| json_loads           | 13.0 us                                                     | 13.6 us: 1.05x slower                                                    |
| unpickle_list        | 2.59 us                                                     | 2.74 us: 1.06x slower                                                    |
| pickle_dict          | 18.5 us                                                     | 19.8 us: 1.07x slower                                                    |
| xml_etree_generate   | 52.5 ms                                                     | 56.6 ms: 1.08x slower                                                    |
| unpickle             | 7.57 us                                                     | 8.32 us: 1.10x slower                                                    |
| pickle               | 6.64 us                                                     | 7.45 us: 1.12x slower                                                    |
| pickle_list          | 2.70 us                                                     | 3.18 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.36 ms: 1.19x faster                                                    |
| genshi_xml      | 39.9 ms                                                     | 34.4 ms: 1.16x faster                                                    |
| genshi_text     | 18.4 ms                                                     | 16.1 ms: 1.14x faster                                                    |
| django_template | 24.4 ms                                                     | 23.3 ms: 1.05x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.14x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 72.8 us: 4.48x faster                                                    |
| generators                 | 34.0 ms                                                     | 20.8 ms: 1.63x faster                                                    |
| pylint                     | 323 ms                                                      | 209 ms: 1.55x faster                                                     |
| asyncio_tcp                | 726 ms                                                      | 481 ms: 1.51x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 274 ms: 1.47x faster                                                     |
| comprehensions             | 15.6 us                                                     | 10.7 us: 1.46x faster                                                    |
| async_tree_none            | 332 ms                                                      | 229 ms: 1.45x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.71 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 309 ms                                                      | 225 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.35x faster                                                     |
| async_tree_io              | 808 ms                                                      | 606 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 399 ms: 1.33x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 627 ms: 1.32x faster                                                     |
| deltablue                  | 2.70 ms                                                     | 2.05 ms: 1.32x faster                                                    |
| raytrace                   | 213 ms                                                      | 168 ms: 1.27x faster                                                     |
| logging_silent             | 71.8 ns                                                     | 56.6 ns: 1.27x faster                                                    |
| chaos                      | 48.4 ms                                                     | 38.8 ms: 1.25x faster                                                    |
| sqlglot_parse              | 953 us                                                      | 790 us: 1.21x faster                                                     |
| mako                       | 7.58 ms                                                     | 6.36 ms: 1.19x faster                                                    |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.71 sec: 1.19x faster                                                   |
| deepcopy_memo              | 26.0 us                                                     | 21.9 us: 1.19x faster                                                    |
| sympy_sum                  | 100 ms                                                      | 84.8 ms: 1.18x faster                                                    |
| unpickle_pure_python       | 157 us                                                      | 133 us: 1.18x faster                                                     |
| sqlglot_transpile          | 1.16 ms                                                     | 989 us: 1.18x faster                                                     |
| hexiom                     | 4.55 ms                                                     | 3.89 ms: 1.17x faster                                                    |
| mdp                        | 1.59 sec                                                    | 1.37 sec: 1.16x faster                                                   |
| genshi_xml                 | 39.9 ms                                                     | 34.4 ms: 1.16x faster                                                    |
| richards_super             | 38.7 ms                                                     | 33.7 ms: 1.15x faster                                                    |
| genshi_text                | 18.4 ms                                                     | 16.1 ms: 1.14x faster                                                    |
| dulwich_log                | 46.4 ms                                                     | 40.6 ms: 1.14x faster                                                    |
| pickle_pure_python         | 208 us                                                      | 183 us: 1.14x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 60.0 ms: 1.14x faster                                                    |
| sympy_str                  | 185 ms                                                      | 162 ms: 1.14x faster                                                     |
| logging_simple             | 6.86 us                                                     | 6.03 us: 1.14x faster                                                    |
| regex_compile              | 91.0 ms                                                     | 80.8 ms: 1.13x faster                                                    |
| tornado_http               | 92.8 ms                                                     | 82.6 ms: 1.12x faster                                                    |
| scimark_lu                 | 62.8 ms                                                     | 56.1 ms: 1.12x faster                                                    |
| coroutines                 | 15.0 ms                                                     | 13.4 ms: 1.12x faster                                                    |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.11x faster                                                    |
| go                         | 101 ms                                                      | 91.0 ms: 1.11x faster                                                    |
| deepcopy                   | 246 us                                                      | 222 us: 1.11x faster                                                     |
| logging_format             | 7.16 us                                                     | 6.52 us: 1.10x faster                                                    |
| pprint_pformat             | 1.09 sec                                                    | 996 ms: 1.09x faster                                                     |
| bench_thread_pool          | 872 us                                                      | 803 us: 1.09x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.7 ms: 1.09x faster                                                    |
| sympy_expand               | 299 ms                                                      | 276 ms: 1.08x faster                                                     |
| mypy2                      | 459 ms                                                      | 424 ms: 1.08x faster                                                     |
| chameleon                  | 5.26 ms                                                     | 4.87 ms: 1.08x faster                                                    |
| pprint_safe_repr           | 529 ms                                                      | 489 ms: 1.08x faster                                                     |
| crypto_pyaes               | 48.9 ms                                                     | 45.2 ms: 1.08x faster                                                    |
| pyflate                    | 312 ms                                                      | 289 ms: 1.08x faster                                                     |
| sqlite_synth               | 1.77 us                                                     | 1.67 us: 1.06x faster                                                    |
| xml_etree_parse            | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                    |
| html5lib                   | 38.9 ms                                                     | 36.8 ms: 1.06x faster                                                    |
| richards                   | 31.4 ms                                                     | 29.9 ms: 1.05x faster                                                    |
| django_template            | 24.4 ms                                                     | 23.3 ms: 1.05x faster                                                    |
| sqlglot_normalize          | 190 ms                                                      | 182 ms: 1.04x faster                                                     |
| spectral_norm              | 68.3 ms                                                     | 65.8 ms: 1.04x faster                                                    |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.8 ms: 1.03x faster                                                    |
| float                      | 54.4 ms                                                     | 53.0 ms: 1.03x faster                                                    |
| scimark_sor                | 78.1 ms                                                     | 76.2 ms: 1.02x faster                                                    |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| meteor_contest             | 75.2 ms                                                     | 73.6 ms: 1.02x faster                                                    |
| tomli_loads                | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                   |
| deepcopy_reduce            | 2.06 us                                                     | 2.03 us: 1.01x faster                                                    |
| 2to3                       | 214 ms                                                      | 211 ms: 1.01x faster                                                     |
| nbody                      | 70.3 ms                                                     | 69.8 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 34.3 ms: 1.01x faster                                                    |
| bench_mp_pool              | 63.2 ms                                                     | 64.7 ms: 1.02x slower                                                    |
| python_startup             | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                                    |
| regex_dna                  | 116 ms                                                      | 120 ms: 1.03x slower                                                     |
| xml_etree_process          | 37.2 ms                                                     | 38.5 ms: 1.03x slower                                                    |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                    |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.70 ms: 1.05x slower                                                    |
| json_loads                 | 13.0 us                                                     | 13.6 us: 1.05x slower                                                    |
| scimark_fft                | 179 ms                                                      | 188 ms: 1.05x slower                                                     |
| unpickle_list              | 2.59 us                                                     | 2.74 us: 1.06x slower                                                    |
| pickle_dict                | 18.5 us                                                     | 19.8 us: 1.07x slower                                                    |
| pathlib                    | 70.9 ms                                                     | 76.1 ms: 1.07x slower                                                    |
| xml_etree_generate         | 52.5 ms                                                     | 56.6 ms: 1.08x slower                                                    |
| coverage                   | 43.4 ms                                                     | 47.3 ms: 1.09x slower                                                    |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                    |
| unpickle                   | 7.57 us                                                     | 8.32 us: 1.10x slower                                                    |
| pickle                     | 6.64 us                                                     | 7.45 us: 1.12x slower                                                    |
| pickle_list                | 2.70 us                                                     | 3.18 us: 1.18x slower                                                    |
| telco                      | 4.06 ms                                                     | 5.05 ms: 1.24x slower                                                    |
| create_gc_cycles           | 713 us                                                      | 888 us: 1.24x slower                                                     |
| async_generators           | 177 ms                                                      | 234 ms: 1.32x slower                                                     |
| thrift                     | 494 us                                                      | 8.10 ms: 16.40x slower                                                   |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                             |

Benchmark hidden because not significant (6): python_startup_no_site, aiohttp, fannkuch, docutils, pycparser, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown