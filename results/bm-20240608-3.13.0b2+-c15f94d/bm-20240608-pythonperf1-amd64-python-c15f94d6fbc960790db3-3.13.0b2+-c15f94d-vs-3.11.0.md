# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: windows-amd64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 208 ms: 1.02x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.62 sec: 1.01x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.5 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 258 ms: 1.57x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 204 ms: 1.51x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 265 ms: 1.51x faster                                                        |
| async_tree_io              | 808 ms                                                      | 580 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.1 ms: 1.08x faster                                                       |
| nbody          | 70.3 ms                                                     | 64.9 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.1 ms: 1.16x faster                                                       |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 17.6 ms: 1.24x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.60 ms: 1.45x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 124 us: 1.27x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.07x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 92.1 ms: 1.06x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.9 ms: 1.04x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.3 us: 1.01x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.8 ms: 1.02x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.70 us: 1.04x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.89 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.16 us: 1.08x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.09x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.45 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.6 ms: 1.01x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 31.8 ms: 1.26x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 14.7 ms: 1.26x faster                                                       |
| mako            | 7.58 ms                                                     | 6.41 ms: 1.18x faster                                                       |
| django_template | 24.4 ms                                                     | 22.6 ms: 1.08x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.19x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 102 us: 3.18x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.4 ms: 1.75x faster                                                       |
| pylint                     | 323 ms                                                      | 205 ms: 1.58x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 258 ms: 1.57x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 477 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 204 ms: 1.51x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.4 us: 1.51x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 265 ms: 1.51x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.60 ms: 1.45x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.88 ms: 1.43x faster                                                       |
| async_tree_io              | 808 ms                                                      | 580 ms: 1.39x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.46 sec: 1.39x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 52.6 ns: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                                        |
| raytrace                   | 213 ms                                                      | 159 ms: 1.34x faster                                                        |
| chaos                      | 48.4 ms                                                     | 37.9 ms: 1.28x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 124 us: 1.27x faster                                                        |
| sqlglot_parse              | 953 us                                                      | 755 us: 1.26x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 31.8 ms: 1.26x faster                                                       |
| richards_super             | 38.7 ms                                                     | 30.8 ms: 1.26x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 14.7 ms: 1.26x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.71 ms: 1.23x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 55.9 ms: 1.22x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 38.2 ms: 1.21x faster                                                       |
| go                         | 101 ms                                                      | 83.4 ms: 1.21x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 964 us: 1.21x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.69 us: 1.21x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.41 ms: 1.18x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.0 us: 1.18x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 85.3 ms: 1.17x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 78.1 ms: 1.16x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.37 sec: 1.16x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.17 us: 1.16x faster                                                       |
| sympy_str                  | 185 ms                                                      | 160 ms: 1.16x faster                                                        |
| richards                   | 31.4 ms                                                     | 27.3 ms: 1.15x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 54.7 ms: 1.15x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.15x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.1 ms: 1.13x faster                                                       |
| deepcopy                   | 246 us                                                      | 218 us: 1.13x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 965 ms: 1.13x faster                                                        |
| pyflate                    | 312 ms                                                      | 278 ms: 1.12x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 471 ms: 1.12x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 787 us: 1.11x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 172 ms: 1.10x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.60 us: 1.10x faster                                                       |
| mypy2                      | 459 ms                                                      | 418 ms: 1.10x faster                                                        |
| sympy_expand               | 299 ms                                                      | 272 ms: 1.10x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.5 ms: 1.10x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 45.0 ms: 1.09x faster                                                       |
| float                      | 54.4 ms                                                     | 50.1 ms: 1.08x faster                                                       |
| nbody                      | 70.3 ms                                                     | 64.9 ms: 1.08x faster                                                       |
| django_template            | 24.4 ms                                                     | 22.6 ms: 1.08x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 63.4 ms: 1.08x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.40 ms: 1.07x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.07x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 92.1 ms: 1.06x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 73.9 ms: 1.06x faster                                                       |
| scimark_fft                | 179 ms                                                      | 170 ms: 1.05x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 32.8 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 71.8 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.98 us: 1.04x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.9 ms: 1.04x faster                                                       |
| fannkuch                   | 253 ms                                                      | 244 ms: 1.04x faster                                                        |
| 2to3                       | 214 ms                                                      | 208 ms: 1.02x faster                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 16.6 ms: 1.01x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.62 sec: 1.01x faster                                                      |
| pickle_dict                | 18.5 us                                                     | 18.3 us: 1.01x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| aiohttp                    | 883 us                                                      | 898 us: 1.02x slower                                                        |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.8 ms: 1.02x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 65.0 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.70 us: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.4 ms: 1.06x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.89 us: 1.07x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.16 us: 1.08x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.09x slower                                                       |
| pycparser                  | 720 ms                                                      | 786 ms: 1.09x slower                                                        |
| unpickle                   | 7.57 us                                                     | 8.45 us: 1.12x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.68 ms: 1.15x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 17.6 ms: 1.24x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 900 us: 1.26x slower                                                        |
| async_generators           | 177 ms                                                      | 225 ms: 1.27x slower                                                        |
| thrift                     | 494 us                                                      | 7.90 ms: 16.00x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (4): json, coverage, xml_etree_process, pidigits
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown