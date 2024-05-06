# Results vs. 3.12.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 4.98 ms                                                     | 4.67 ms: 1.07x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 83.0 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 214 ms: 1.33x faster                                                        |
| async_tree_none            | 291 ms                                                      | 219 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 386 ms: 1.30x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 267 ms: 1.27x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 607 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 392 ms: 1.25x faster                                                        |
| async_tree_io              | 731 ms                                                      | 590 ms: 1.24x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.30x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 58.3 ms: 1.23x faster                                                       |
| float          | 56.8 ms                                                     | 46.7 ms: 1.22x faster                                                       |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.16x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 120 ms: 1.05x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                       |
| regex_compile  | 87.5 ms                                                     | 86.8 ms: 1.01x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 15.0 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.18 sec: 1.15x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 171 us: 1.15x faster                                                        |
| unpickle_pure_python | 133 us                                                      | 123 us: 1.08x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 90.0 ms: 1.03x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.52 ms: 1.03x faster                                                       |
| pickle               | 7.43 us                                                     | 7.23 us: 1.03x faster                                                       |
| xml_etree_process    | 37.7 ms                                                     | 37.0 ms: 1.02x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.5 us: 1.01x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.91 us: 1.03x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.80 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (2): unpickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 17.8 ms: 1.09x slower                                                       |
| python_startup         | 19.5 ms                                                     | 21.4 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.72 ms: 1.24x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 265 ms: 1.38x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 71.1 us: 1.34x faster                                                       |
| async_tree_none_tg         | 285 ms                                                      | 214 ms: 1.33x faster                                                        |
| async_tree_none            | 291 ms                                                      | 219 ms: 1.33x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.58 sec: 1.32x faster                                                      |
| comprehensions             | 14.1 us                                                     | 10.7 us: 1.32x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 51.3 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 386 ms: 1.30x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 267 ms: 1.27x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 607 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 392 ms: 1.25x faster                                                        |
| async_tree_io              | 731 ms                                                      | 590 ms: 1.24x faster                                                        |
| mako                       | 7.09 ms                                                     | 5.72 ms: 1.24x faster                                                       |
| nbody                      | 71.9 ms                                                     | 58.3 ms: 1.23x faster                                                       |
| float                      | 56.8 ms                                                     | 46.7 ms: 1.22x faster                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.18 sec: 1.15x faster                                                      |
| pickle_pure_python         | 195 us                                                      | 171 us: 1.15x faster                                                        |
| generators                 | 22.5 ms                                                     | 19.8 ms: 1.14x faster                                                       |
| mypy2                      | 509 ms                                                      | 447 ms: 1.14x faster                                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.5 ms: 1.14x faster                                                       |
| raytrace                   | 192 ms                                                      | 170 ms: 1.13x faster                                                        |
| deepcopy_memo              | 23.7 us                                                     | 21.0 us: 1.13x faster                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.27 ms: 1.13x faster                                                       |
| scimark_fft                | 184 ms                                                      | 165 ms: 1.12x faster                                                        |
| chaos                      | 43.3 ms                                                     | 38.9 ms: 1.12x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.58 us: 1.11x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 943 ms: 1.11x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 54.9 ns: 1.10x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 44.3 ms: 1.10x faster                                                       |
| pyflate                    | 295 ms                                                      | 269 ms: 1.09x faster                                                        |
| deepcopy                   | 238 us                                                      | 218 us: 1.09x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.09x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.5 ms: 1.09x faster                                                       |
| fannkuch                   | 247 ms                                                      | 226 ms: 1.09x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 470 ms: 1.09x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.77 us: 1.09x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 791 us: 1.08x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 123 us: 1.08x faster                                                        |
| tornado_http               | 89.5 ms                                                     | 83.0 ms: 1.08x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.94 us: 1.08x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 74.8 ms: 1.08x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.26 us: 1.07x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.67 ms: 1.07x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| richards                   | 28.4 ms                                                     | 27.0 ms: 1.05x faster                                                       |
| richards_super             | 32.1 ms                                                     | 30.6 ms: 1.05x faster                                                       |
| regex_dna                  | 126 ms                                                      | 120 ms: 1.05x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 179 ms: 1.05x faster                                                        |
| sympy_str                  | 175 ms                                                      | 168 ms: 1.04x faster                                                        |
| meteor_contest             | 74.6 ms                                                     | 71.7 ms: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| nqueens                    | 62.8 ms                                                     | 60.5 ms: 1.04x faster                                                       |
| sympy_sum                  | 91.5 ms                                                     | 88.3 ms: 1.04x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 90.0 ms: 1.03x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.52 ms: 1.03x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 67.2 ms: 1.03x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.23 us: 1.03x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 783 us: 1.03x faster                                                        |
| sqlglot_transpile          | 1.02 ms                                                     | 995 us: 1.03x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 37.0 ms: 1.02x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 86.8 ms: 1.01x faster                                                       |
| async_generators           | 239 ms                                                      | 240 ms: 1.00x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 34.7 ms: 1.01x slower                                                       |
| sympy_expand               | 284 ms                                                      | 286 ms: 1.01x slower                                                        |
| pickle_dict                | 18.4 us                                                     | 18.5 us: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.68 sec: 1.01x slower                                                      |
| aiohttp                    | 884 us                                                      | 898 us: 1.01x slower                                                        |
| deltablue                  | 2.16 ms                                                     | 2.20 ms: 1.02x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.91 us: 1.03x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.3 ms: 1.03x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.0 ms: 1.05x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 83.1 ms: 1.06x slower                                                       |
| json                       | 3.05 ms                                                     | 3.22 ms: 1.06x slower                                                       |
| pycparser                  | 699 ms                                                      | 740 ms: 1.06x slower                                                        |
| unpickle                   | 8.18 us                                                     | 8.80 us: 1.08x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.45 ms: 1.09x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 17.8 ms: 1.09x slower                                                       |
| python_startup             | 19.5 ms                                                     | 21.4 ms: 1.10x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.53 sec: 1.12x slower                                                      |
| coverage                   | 40.8 ms                                                     | 46.4 ms: 1.14x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.83 ms: 1.17x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 884 us: 1.17x slower                                                        |
| scimark_lu                 | 58.9 ms                                                     | 73.2 ms: 1.24x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (5): asyncio_tcp, unpickle_list, json_loads, 2to3, go
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown