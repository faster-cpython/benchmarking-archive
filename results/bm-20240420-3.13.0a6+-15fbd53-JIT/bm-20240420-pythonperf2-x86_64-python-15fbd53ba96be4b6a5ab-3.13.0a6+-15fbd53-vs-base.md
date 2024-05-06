# Results vs. base

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                                                                                  | 298 ms: 1.04x slower                                                                                                        |
| docutils       | 2.97 sec                                                                                                                | 3.05 sec: 1.02x slower                                                                                                      |
| html5lib       | 73.1 ms                                                                                                                 | 74.6 ms: 1.02x slower                                                                                                       |
| tornado_http   | 120 ms                                                                                                                  | 122 ms: 1.02x slower                                                                                                        |
| Geometric mean | (ref)                                                                                                                   | 1.02x slower                                                                                                                |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 578 ms                                                                                                                  | 595 ms: 1.03x slower                                                                                                        |
| Geometric mean             | (ref)                                                                                                                   | 1.01x slower                                                                                                                |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 263 ms                                                                                                                  | 261 ms: 1.01x faster                                                                                                        |
| nbody          | 86.9 ms                                                                                                                 | 98.2 ms: 1.13x slower                                                                                                       |
| Geometric mean | (ref)                                                                                                                   | 1.04x slower                                                                                                                |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                                                                                 | 3.47 ms: 1.01x faster                                                                                                       |
| regex_dna      | 242 ms                                                                                                                  | 241 ms: 1.01x faster                                                                                                        |
| regex_compile  | 143 ms                                                                                                                  | 145 ms: 1.01x slower                                                                                                        |
| regex_v8       | 25.2 ms                                                                                                                 | 26.2 ms: 1.04x slower                                                                                                       |
| Geometric mean | (ref)                                                                                                                   | 1.01x slower                                                                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 106 ms                                                                                                                  | 101 ms: 1.05x faster                                                                                                        |
| xml_etree_parse      | 151 ms                                                                                                                  | 144 ms: 1.04x faster                                                                                                        |
| unpickle_list        | 4.81 us                                                                                                                 | 4.60 us: 1.04x faster                                                                                                       |
| tomli_loads          | 2.19 sec                                                                                                                | 2.14 sec: 1.03x faster                                                                                                      |
| xml_etree_process    | 58.9 ms                                                                                                                 | 57.6 ms: 1.02x faster                                                                                                       |
| pickle_pure_python   | 307 us                                                                                                                  | 311 us: 1.01x slower                                                                                                        |
| json_dumps           | 10.6 ms                                                                                                                 | 10.8 ms: 1.02x slower                                                                                                       |
| unpickle             | 14.9 us                                                                                                                 | 15.3 us: 1.03x slower                                                                                                       |
| unpickle_pure_python | 211 us                                                                                                                  | 219 us: 1.04x slower                                                                                                        |
| pickle_dict          | 30.8 us                                                                                                                 | 32.5 us: 1.05x slower                                                                                                       |
| pickle               | 10.2 us                                                                                                                 | 10.8 us: 1.05x slower                                                                                                       |
| Geometric mean       | (ref)                                                                                                                   | 1.00x slower                                                                                                                |

Benchmark hidden because not significant (3): pickle_list, xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.9 ms                                                                                                                 | 13.5 ms: 1.05x slower                                                                                                       |
| python_startup_no_site | 8.88 ms                                                                                                                 | 9.45 ms: 1.06x slower                                                                                                       |
| Geometric mean         | (ref)                                                                                                                   | 1.06x slower                                                                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 27.2 ms                                                                                                                 | 26.0 ms: 1.05x faster                                                                                                       |
| mako            | 10.1 ms                                                                                                                 | 9.93 ms: 1.02x faster                                                                                                       |
| genshi_xml      | 57.2 ms                                                                                                                 | 58.3 ms: 1.02x slower                                                                                                       |
| django_template | 37.9 ms                                                                                                                 | 39.4 ms: 1.04x slower                                                                                                       |
| Geometric mean  | (ref)                                                                                                                   | 1.00x faster                                                                                                                |

All benchmarks:
===============

| Benchmark                  | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------:|
| richards_super             | 57.6 ms                                                                                                                 | 52.2 ms: 1.10x faster                                                                                                       |
| richards                   | 50.9 ms                                                                                                                 | 46.2 ms: 1.10x faster                                                                                                       |
| spectral_norm              | 97.9 ms                                                                                                                 | 92.7 ms: 1.06x faster                                                                                                       |
| xml_etree_iterparse        | 106 ms                                                                                                                  | 101 ms: 1.05x faster                                                                                                        |
| genshi_text                | 27.2 ms                                                                                                                 | 26.0 ms: 1.05x faster                                                                                                       |
| xml_etree_parse            | 151 ms                                                                                                                  | 144 ms: 1.04x faster                                                                                                        |
| unpickle_list              | 4.81 us                                                                                                                 | 4.60 us: 1.04x faster                                                                                                       |
| gc_traversal               | 4.58 ms                                                                                                                 | 4.40 ms: 1.04x faster                                                                                                       |
| coverage                   | 82.9 ms                                                                                                                 | 79.5 ms: 1.04x faster                                                                                                       |
| deepcopy                   | 397 us                                                                                                                  | 382 us: 1.04x faster                                                                                                        |
| deepcopy_reduce            | 3.50 us                                                                                                                 | 3.40 us: 1.03x faster                                                                                                       |
| tomli_loads                | 2.19 sec                                                                                                                | 2.14 sec: 1.03x faster                                                                                                      |
| create_gc_cycles           | 1.93 ms                                                                                                                 | 1.88 ms: 1.02x faster                                                                                                       |
| xml_etree_process          | 58.9 ms                                                                                                                 | 57.6 ms: 1.02x faster                                                                                                       |
| deepcopy_memo              | 38.0 us                                                                                                                 | 37.3 us: 1.02x faster                                                                                                       |
| logging_format             | 7.03 us                                                                                                                 | 6.89 us: 1.02x faster                                                                                                       |
| mako                       | 10.1 ms                                                                                                                 | 9.93 ms: 1.02x faster                                                                                                       |
| json                       | 5.44 ms                                                                                                                 | 5.35 ms: 1.02x faster                                                                                                       |
| regex_effbot               | 3.51 ms                                                                                                                 | 3.47 ms: 1.01x faster                                                                                                       |
| sqlite_synth               | 2.72 us                                                                                                                 | 2.68 us: 1.01x faster                                                                                                       |
| asyncio_tcp                | 378 ms                                                                                                                  | 374 ms: 1.01x faster                                                                                                        |
| telco                      | 8.13 ms                                                                                                                 | 8.06 ms: 1.01x faster                                                                                                       |
| pidigits                   | 263 ms                                                                                                                  | 261 ms: 1.01x faster                                                                                                        |
| regex_dna                  | 242 ms                                                                                                                  | 241 ms: 1.01x faster                                                                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                                                                                | 1.58 sec: 1.00x slower                                                                                                      |
| logging_silent             | 94.3 ns                                                                                                                 | 94.7 ns: 1.00x slower                                                                                                       |
| sympy_expand               | 506 ms                                                                                                                  | 510 ms: 1.01x slower                                                                                                        |
| pathlib                    | 17.3 ms                                                                                                                 | 17.5 ms: 1.01x slower                                                                                                       |
| scimark_sparse_mat_mult    | 4.15 ms                                                                                                                 | 4.20 ms: 1.01x slower                                                                                                       |
| pycparser                  | 1.22 sec                                                                                                                | 1.23 sec: 1.01x slower                                                                                                      |
| pickle_pure_python         | 307 us                                                                                                                  | 311 us: 1.01x slower                                                                                                        |
| regex_compile              | 143 ms                                                                                                                  | 145 ms: 1.01x slower                                                                                                        |
| tornado_http               | 120 ms                                                                                                                  | 122 ms: 1.02x slower                                                                                                        |
| json_dumps                 | 10.6 ms                                                                                                                 | 10.8 ms: 1.02x slower                                                                                                       |
| genshi_xml                 | 57.2 ms                                                                                                                 | 58.3 ms: 1.02x slower                                                                                                       |
| pyflate                    | 474 ms                                                                                                                  | 483 ms: 1.02x slower                                                                                                        |
| html5lib                   | 73.1 ms                                                                                                                 | 74.6 ms: 1.02x slower                                                                                                       |
| docutils                   | 2.97 sec                                                                                                                | 3.05 sec: 1.02x slower                                                                                                      |
| typing_runtime_protocols   | 118 us                                                                                                                  | 121 us: 1.03x slower                                                                                                        |
| unpickle                   | 14.9 us                                                                                                                 | 15.3 us: 1.03x slower                                                                                                       |
| meteor_contest             | 128 ms                                                                                                                  | 131 ms: 1.03x slower                                                                                                        |
| async_tree_cpu_io_mixed_tg | 578 ms                                                                                                                  | 595 ms: 1.03x slower                                                                                                        |
| sqlglot_normalize          | 119 ms                                                                                                                  | 123 ms: 1.03x slower                                                                                                        |
| sympy_str                  | 296 ms                                                                                                                  | 306 ms: 1.03x slower                                                                                                        |
| bench_thread_pool          | 896 us                                                                                                                  | 926 us: 1.03x slower                                                                                                        |
| mdp                        | 2.50 sec                                                                                                                | 2.59 sec: 1.03x slower                                                                                                      |
| fannkuch                   | 361 ms                                                                                                                  | 374 ms: 1.03x slower                                                                                                        |
| pprint_safe_repr           | 800 ms                                                                                                                  | 831 ms: 1.04x slower                                                                                                        |
| regex_v8                   | 25.2 ms                                                                                                                 | 26.2 ms: 1.04x slower                                                                                                       |
| django_template            | 37.9 ms                                                                                                                 | 39.4 ms: 1.04x slower                                                                                                       |
| unpickle_pure_python       | 211 us                                                                                                                  | 219 us: 1.04x slower                                                                                                        |
| sqlglot_transpile          | 1.76 ms                                                                                                                 | 1.84 ms: 1.04x slower                                                                                                       |
| sqlglot_parse              | 1.38 ms                                                                                                                 | 1.44 ms: 1.04x slower                                                                                                       |
| 2to3                       | 285 ms                                                                                                                  | 298 ms: 1.04x slower                                                                                                        |
| python_startup             | 12.9 ms                                                                                                                 | 13.5 ms: 1.05x slower                                                                                                       |
| coroutines                 | 21.1 ms                                                                                                                 | 22.1 ms: 1.05x slower                                                                                                       |
| sympy_sum                  | 155 ms                                                                                                                  | 162 ms: 1.05x slower                                                                                                        |
| pprint_pformat             | 1.62 sec                                                                                                                | 1.71 sec: 1.05x slower                                                                                                      |
| pylint                     | 344 ms                                                                                                                  | 362 ms: 1.05x slower                                                                                                        |
| pickle_dict                | 30.8 us                                                                                                                 | 32.5 us: 1.05x slower                                                                                                       |
| pickle                     | 10.2 us                                                                                                                 | 10.8 us: 1.05x slower                                                                                                       |
| sqlglot_optimize           | 59.3 ms                                                                                                                 | 62.6 ms: 1.05x slower                                                                                                       |
| gunicorn                   | 1.03 ms                                                                                                                 | 1.10 ms: 1.06x slower                                                                                                       |
| aiohttp                    | 1.06 ms                                                                                                                 | 1.13 ms: 1.06x slower                                                                                                       |
| mypy2                      | 773 ms                                                                                                                  | 820 ms: 1.06x slower                                                                                                        |
| python_startup_no_site     | 8.88 ms                                                                                                                 | 9.45 ms: 1.06x slower                                                                                                       |
| raytrace                   | 254 ms                                                                                                                  | 271 ms: 1.07x slower                                                                                                        |
| crypto_pyaes               | 72.2 ms                                                                                                                 | 77.3 ms: 1.07x slower                                                                                                       |
| sympy_integrate            | 23.3 ms                                                                                                                 | 25.0 ms: 1.07x slower                                                                                                       |
| async_generators           | 359 ms                                                                                                                  | 388 ms: 1.08x slower                                                                                                        |
| scimark_fft                | 291 ms                                                                                                                  | 316 ms: 1.08x slower                                                                                                        |
| chaos                      | 58.5 ms                                                                                                                 | 65.6 ms: 1.12x slower                                                                                                       |
| comprehensions             | 17.0 us                                                                                                                 | 19.2 us: 1.13x slower                                                                                                       |
| nbody                      | 86.9 ms                                                                                                                 | 98.2 ms: 1.13x slower                                                                                                       |
| go                         | 156 ms                                                                                                                  | 178 ms: 1.14x slower                                                                                                        |
| nqueens                    | 86.6 ms                                                                                                                 | 100 ms: 1.16x slower                                                                                                        |
| deltablue                  | 3.26 ms                                                                                                                 | 3.83 ms: 1.17x slower                                                                                                       |
| hexiom                     | 5.98 ms                                                                                                                 | 7.15 ms: 1.20x slower                                                                                                       |
| scimark_monte_carlo        | 60.3 ms                                                                                                                 | 72.6 ms: 1.20x slower                                                                                                       |
| scimark_sor                | 120 ms                                                                                                                  | 152 ms: 1.27x slower                                                                                                        |
| scimark_lu                 | 95.8 ms                                                                                                                 | 125 ms: 1.31x slower                                                                                                        |
| Geometric mean             | (ref)                                                                                                                   | 1.03x slower                                                                                                                |

Benchmark hidden because not significant (19): asyncio_websockets, thrift, dulwich_log, async_tree_none, pickle_list, async_tree_io_tg, async_tree_cpu_io_mixed, xml_etree_generate, chameleon, logging_simple, async_tree_none_tg, json_loads, async_tree_memoization, generators, float, async_tree_io, dask, async_tree_memoization_tg, bench_mp_pool

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x