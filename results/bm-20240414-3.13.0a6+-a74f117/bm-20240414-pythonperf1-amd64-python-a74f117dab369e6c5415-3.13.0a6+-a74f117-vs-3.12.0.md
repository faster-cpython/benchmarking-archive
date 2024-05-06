# Results vs. 3.12.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 210 ms: 1.04x faster                                                        |
| docutils       | 1.66 sec                                                    | 1.64 sec: 1.01x faster                                                      |
| tornado_http   | 89.5 ms                                                     | 82.2 ms: 1.09x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 268 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 386 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 224 ms: 1.30x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 222 ms: 1.29x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 272 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 620 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 394 ms: 1.24x faster                                                        |
| async_tree_io              | 731 ms                                                      | 597 ms: 1.22x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.28x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 51.6 ms: 1.10x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| nbody          | 71.9 ms                                                     | 70.2 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 79.8 ms: 1.10x faster                                                       |
| regex_dna      | 126 ms                                                      | 122 ms: 1.04x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 16.0 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 179 us: 1.09x faster                                                        |
| pickle               | 7.43 us                                                     | 7.14 us: 1.04x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 129 us: 1.03x faster                                                        |
| xml_etree_parse      | 93.0 ms                                                     | 91.2 ms: 1.02x faster                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 64.0 ms: 1.02x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.64 ms: 1.01x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 55.3 ms: 1.01x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.80 us: 1.02x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.36 us: 1.02x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| pickle_list          | 2.83 us                                                     | 2.94 us: 1.04x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 20.3 ms: 1.04x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 17.0 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 6.38 ms: 1.11x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 268 ms: 1.37x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.8 us: 1.31x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 386 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 224 ms: 1.30x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 73.8 us: 1.29x faster                                                       |
| async_tree_none_tg         | 285 ms                                                      | 222 ms: 1.29x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 272 ms: 1.25x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.68 sec: 1.25x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 620 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 394 ms: 1.24x faster                                                        |
| async_tree_io              | 731 ms                                                      | 597 ms: 1.22x faster                                                        |
| mypy2                      | 509 ms                                                      | 418 ms: 1.22x faster                                                        |
| raytrace                   | 192 ms                                                      | 165 ms: 1.17x faster                                                        |
| mako                       | 7.09 ms                                                     | 6.38 ms: 1.11x faster                                                       |
| chaos                      | 43.3 ms                                                     | 39.2 ms: 1.11x faster                                                       |
| float                      | 56.8 ms                                                     | 51.6 ms: 1.10x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.3 ms: 1.10x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 79.8 ms: 1.10x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 82.2 ms: 1.09x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 179 us: 1.09x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 40.6 ms: 1.08x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 64.2 ms: 1.08x faster                                                       |
| sympy_str                  | 175 ms                                                      | 163 ms: 1.08x faster                                                        |
| deepcopy                   | 238 us                                                      | 222 us: 1.07x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.64 us: 1.07x faster                                                       |
| sympy_sum                  | 91.5 ms                                                     | 85.4 ms: 1.07x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 75.2 ms: 1.07x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 56.8 ns: 1.07x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 22.3 us: 1.06x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.04 ms: 1.06x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 45.7 ms: 1.06x faster                                                       |
| hexiom                     | 4.10 ms                                                     | 3.87 ms: 1.06x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 63.3 ms: 1.06x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 811 us: 1.06x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.98 us: 1.05x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.42 us: 1.05x faster                                                       |
| pprint_safe_repr           | 513 ms                                                      | 491 ms: 1.04x faster                                                        |
| pprint_pformat             | 1.05 sec                                                    | 1.00 sec: 1.04x faster                                                      |
| sqlglot_normalize          | 187 ms                                                      | 179 ms: 1.04x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.14 us: 1.04x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 982 us: 1.04x faster                                                        |
| generators                 | 22.5 ms                                                     | 21.7 ms: 1.04x faster                                                       |
| regex_dna                  | 126 ms                                                      | 122 ms: 1.04x faster                                                        |
| 2to3                       | 218 ms                                                      | 210 ms: 1.04x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.02 us: 1.04x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 776 us: 1.04x faster                                                        |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| sympy_expand               | 284 ms                                                      | 274 ms: 1.04x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 129 us: 1.03x faster                                                        |
| scimark_lu                 | 58.9 ms                                                     | 57.0 ms: 1.03x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 60.8 ms: 1.03x faster                                                       |
| scimark_sor                | 78.8 ms                                                     | 76.6 ms: 1.03x faster                                                       |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 72.8 ms: 1.02x faster                                                       |
| nbody                      | 71.9 ms                                                     | 70.2 ms: 1.02x faster                                                       |
| pyflate                    | 295 ms                                                      | 289 ms: 1.02x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 91.2 ms: 1.02x faster                                                       |
| async_generators           | 239 ms                                                      | 235 ms: 1.02x faster                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 64.0 ms: 1.02x faster                                                       |
| go                         | 91.6 ms                                                     | 90.0 ms: 1.02x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 34.0 ms: 1.02x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| docutils                   | 1.66 sec                                                    | 1.64 sec: 1.01x faster                                                      |
| json_dumps                 | 5.70 ms                                                     | 5.64 ms: 1.01x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 55.3 ms: 1.01x faster                                                       |
| json_loads                 | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| richards_super             | 32.1 ms                                                     | 32.3 ms: 1.01x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.80 us: 1.02x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.36 us: 1.02x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| pickle_list                | 2.83 us                                                     | 2.94 us: 1.04x slower                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.66 ms: 1.04x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.3 ms: 1.04x slower                                                       |
| fannkuch                   | 247 ms                                                      | 257 ms: 1.04x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 17.0 ms: 1.04x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.49 sec: 1.08x slower                                                      |
| pycparser                  | 699 ms                                                      | 772 ms: 1.10x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 16.0 ms: 1.12x slower                                                       |
| coverage                   | 40.8 ms                                                     | 46.0 ms: 1.13x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 895 us: 1.19x slower                                                        |
| telco                      | 4.13 ms                                                     | 5.05 ms: 1.22x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                                |

Benchmark hidden because not significant (7): asyncio_tcp, xml_etree_process, richards, aiohttp, json, scimark_fft, chameleon
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown