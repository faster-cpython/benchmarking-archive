# Results vs. 3.11.0

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: e83be54
- commit date: 2024-04-15
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 211 ms: 1.01x faster                                                     |
| chameleon      | 5.26 ms                                                     | 4.83 ms: 1.09x faster                                                    |
| docutils       | 1.64 sec                                                    | 1.65 sec: 1.01x slower                                                   |
| html5lib       | 38.9 ms                                                     | 37.4 ms: 1.04x faster                                                    |
| tornado_http   | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                    |
| Geometric mean | (ref)                                                       | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                     |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 273 ms: 1.46x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 225 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.35x faster                                                     |
| async_tree_io              | 808 ms                                                      | 602 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 397 ms: 1.33x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 626 ms: 1.32x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.9 ms: 1.07x faster                                                    |
| nbody          | 70.3 ms                                                     | 68.5 ms: 1.03x faster                                                    |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                       | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.9 ms: 1.15x faster                                                    |
| regex_dna      | 116 ms                                                      | 117 ms: 1.00x slower                                                     |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                    |
| regex_v8       | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                       | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.65 ms: 1.43x faster                                                    |
| unpickle_pure_python | 157 us                                                      | 128 us: 1.22x faster                                                     |
| pickle_pure_python   | 208 us                                                      | 180 us: 1.16x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 92.8 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.6 ms: 1.03x faster                                                    |
| tomli_loads          | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                   |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.00x faster                                                    |
| xml_etree_process    | 37.2 ms                                                     | 37.6 ms: 1.01x slower                                                    |
| json_loads           | 13.0 us                                                     | 13.5 us: 1.04x slower                                                    |
| xml_etree_generate   | 52.5 ms                                                     | 54.8 ms: 1.04x slower                                                    |
| unpickle_list        | 2.59 us                                                     | 2.83 us: 1.09x slower                                                    |
| unpickle             | 7.57 us                                                     | 8.40 us: 1.11x slower                                                    |
| pickle               | 6.64 us                                                     | 7.37 us: 1.11x slower                                                    |
| pickle_list          | 2.70 us                                                     | 3.08 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                    |
| Geometric mean         | (ref)                                                       | 1.02x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.34 ms: 1.20x faster                                                    |
| genshi_xml      | 39.9 ms                                                     | 34.4 ms: 1.16x faster                                                    |
| genshi_text     | 18.4 ms                                                     | 16.8 ms: 1.10x faster                                                    |
| django_template | 24.4 ms                                                     | 23.6 ms: 1.04x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.12x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.5 us: 4.32x faster                                                    |
| generators                 | 34.0 ms                                                     | 20.9 ms: 1.62x faster                                                    |
| pylint                     | 323 ms                                                      | 210 ms: 1.54x faster                                                     |
| asyncio_tcp                | 726 ms                                                      | 476 ms: 1.52x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                     |
| comprehensions             | 15.6 us                                                     | 10.6 us: 1.48x faster                                                    |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 273 ms: 1.46x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.65 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 309 ms                                                      | 225 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.35x faster                                                     |
| async_tree_io              | 808 ms                                                      | 602 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 397 ms: 1.33x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 626 ms: 1.32x faster                                                     |
| deltablue                  | 2.70 ms                                                     | 2.06 ms: 1.31x faster                                                    |
| raytrace                   | 213 ms                                                      | 164 ms: 1.30x faster                                                     |
| chaos                      | 48.4 ms                                                     | 38.1 ms: 1.27x faster                                                    |
| logging_silent             | 71.8 ns                                                     | 56.8 ns: 1.26x faster                                                    |
| sqlglot_parse              | 953 us                                                      | 764 us: 1.25x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 128 us: 1.22x faster                                                     |
| hexiom                     | 4.55 ms                                                     | 3.79 ms: 1.20x faster                                                    |
| mako                       | 7.58 ms                                                     | 6.34 ms: 1.20x faster                                                    |
| deepcopy_memo              | 26.0 us                                                     | 21.7 us: 1.20x faster                                                    |
| sqlglot_transpile          | 1.16 ms                                                     | 979 us: 1.19x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 84.5 ms: 1.18x faster                                                    |
| scimark_lu                 | 62.8 ms                                                     | 53.8 ms: 1.17x faster                                                    |
| richards_super             | 38.7 ms                                                     | 33.3 ms: 1.16x faster                                                    |
| dulwich_log                | 46.4 ms                                                     | 39.9 ms: 1.16x faster                                                    |
| genshi_xml                 | 39.9 ms                                                     | 34.4 ms: 1.16x faster                                                    |
| pickle_pure_python         | 208 us                                                      | 180 us: 1.16x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 58.9 ms: 1.16x faster                                                    |
| regex_compile              | 91.0 ms                                                     | 78.9 ms: 1.15x faster                                                    |
| logging_simple             | 6.86 us                                                     | 5.98 us: 1.15x faster                                                    |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                     |
| mdp                        | 1.59 sec                                                    | 1.39 sec: 1.15x faster                                                   |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.9 ms: 1.14x faster                                                    |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.79 sec: 1.13x faster                                                   |
| tornado_http               | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                    |
| coroutines                 | 15.0 ms                                                     | 13.3 ms: 1.12x faster                                                    |
| sympy_integrate            | 14.0 ms                                                     | 12.5 ms: 1.12x faster                                                    |
| spectral_norm              | 68.3 ms                                                     | 60.9 ms: 1.12x faster                                                    |
| go                         | 101 ms                                                      | 90.8 ms: 1.11x faster                                                    |
| logging_format             | 7.16 us                                                     | 6.46 us: 1.11x faster                                                    |
| crypto_pyaes               | 48.9 ms                                                     | 44.5 ms: 1.10x faster                                                    |
| genshi_text                | 18.4 ms                                                     | 16.8 ms: 1.10x faster                                                    |
| deepcopy                   | 246 us                                                      | 226 us: 1.09x faster                                                     |
| pprint_pformat             | 1.09 sec                                                    | 996 ms: 1.09x faster                                                     |
| pyflate                    | 312 ms                                                      | 286 ms: 1.09x faster                                                     |
| chameleon                  | 5.26 ms                                                     | 4.83 ms: 1.09x faster                                                    |
| sympy_expand               | 299 ms                                                      | 275 ms: 1.09x faster                                                     |
| scimark_sor                | 78.1 ms                                                     | 72.0 ms: 1.09x faster                                                    |
| pprint_safe_repr           | 529 ms                                                      | 489 ms: 1.08x faster                                                     |
| mypy2                      | 459 ms                                                      | 424 ms: 1.08x faster                                                     |
| bench_thread_pool          | 872 us                                                      | 807 us: 1.08x faster                                                     |
| richards                   | 31.4 ms                                                     | 29.3 ms: 1.07x faster                                                    |
| float                      | 54.4 ms                                                     | 50.9 ms: 1.07x faster                                                    |
| sqlite_synth               | 1.77 us                                                     | 1.66 us: 1.07x faster                                                    |
| xml_etree_parse            | 97.6 ms                                                     | 92.8 ms: 1.05x faster                                                    |
| html5lib                   | 38.9 ms                                                     | 37.4 ms: 1.04x faster                                                    |
| django_template            | 24.4 ms                                                     | 23.6 ms: 1.04x faster                                                    |
| python_startup_no_site     | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                    |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.6 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 190 ms                                                      | 185 ms: 1.03x faster                                                     |
| nbody                      | 70.3 ms                                                     | 68.5 ms: 1.03x faster                                                    |
| fannkuch                   | 253 ms                                                      | 247 ms: 1.03x faster                                                     |
| tomli_loads                | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                   |
| deepcopy_reduce            | 2.06 us                                                     | 2.02 us: 1.02x faster                                                    |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| meteor_contest             | 75.2 ms                                                     | 74.2 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.55 ms: 1.01x faster                                                    |
| 2to3                       | 214 ms                                                      | 211 ms: 1.01x faster                                                     |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.00x faster                                                    |
| regex_dna                  | 116 ms                                                      | 117 ms: 1.00x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 34.7 ms: 1.01x slower                                                    |
| bench_mp_pool              | 63.2 ms                                                     | 63.7 ms: 1.01x slower                                                    |
| docutils                   | 1.64 sec                                                    | 1.65 sec: 1.01x slower                                                   |
| xml_etree_process          | 37.2 ms                                                     | 37.6 ms: 1.01x slower                                                    |
| scimark_fft                | 179 ms                                                      | 182 ms: 1.01x slower                                                     |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                    |
| json_loads                 | 13.0 us                                                     | 13.5 us: 1.04x slower                                                    |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                    |
| xml_etree_generate         | 52.5 ms                                                     | 54.8 ms: 1.04x slower                                                    |
| coverage                   | 43.4 ms                                                     | 46.0 ms: 1.06x slower                                                    |
| regex_v8                   | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                    |
| pathlib                    | 70.9 ms                                                     | 76.2 ms: 1.07x slower                                                    |
| json                       | 2.98 ms                                                     | 3.21 ms: 1.08x slower                                                    |
| unpickle_list              | 2.59 us                                                     | 2.83 us: 1.09x slower                                                    |
| unpickle                   | 7.57 us                                                     | 8.40 us: 1.11x slower                                                    |
| pickle                     | 6.64 us                                                     | 7.37 us: 1.11x slower                                                    |
| pickle_list                | 2.70 us                                                     | 3.08 us: 1.14x slower                                                    |
| telco                      | 4.06 ms                                                     | 5.10 ms: 1.25x slower                                                    |
| create_gc_cycles           | 713 us                                                      | 895 us: 1.25x slower                                                     |
| async_generators           | 177 ms                                                      | 235 ms: 1.33x slower                                                     |
| thrift                     | 494 us                                                      | 7.84 ms: 15.88x slower                                                   |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                             |

Benchmark hidden because not significant (3): aiohttp, python_startup, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown