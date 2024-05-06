# Results vs. 3.12.0

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: ced0ca9
- commit date: 2024-04-16
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 210 ms: 1.04x faster                                                     |
| chameleon      | 4.98 ms                                                     | 4.80 ms: 1.04x faster                                                    |
| docutils       | 1.66 sec                                                    | 1.65 sec: 1.01x faster                                                   |
| tornado_http   | 89.5 ms                                                     | 80.8 ms: 1.11x faster                                                    |
| Geometric mean | (ref)                                                       | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.38x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 217 ms: 1.31x faster                                                     |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                     |
| async_tree_memoization     | 339 ms                                                      | 270 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 391 ms: 1.25x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 617 ms: 1.25x faster                                                     |
| async_tree_io              | 731 ms                                                      | 595 ms: 1.23x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 50.7 ms: 1.12x faster                                                    |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                     |
| nbody          | 71.9 ms                                                     | 70.8 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                       | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 79.8 ms: 1.10x faster                                                    |
| regex_dna      | 126 ms                                                      | 116 ms: 1.08x faster                                                     |
| regex_effbot   | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                    |
| regex_v8       | 14.2 ms                                                     | 18.3 ms: 1.28x slower                                                    |
| Geometric mean | (ref)                                                       | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 176 us: 1.11x faster                                                     |
| unpickle_pure_python | 133 us                                                      | 125 us: 1.06x faster                                                     |
| pickle               | 7.43 us                                                     | 7.13 us: 1.04x faster                                                    |
| xml_etree_generate   | 55.8 ms                                                     | 54.5 ms: 1.02x faster                                                    |
| xml_etree_iterparse  | 65.2 ms                                                     | 64.1 ms: 1.02x faster                                                    |
| xml_etree_process    | 37.7 ms                                                     | 37.2 ms: 1.01x faster                                                    |
| json_dumps           | 5.70 ms                                                     | 5.64 ms: 1.01x faster                                                    |
| unpickle             | 8.18 us                                                     | 8.25 us: 1.01x slower                                                    |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                    |
| unpickle_list        | 2.75 us                                                     | 2.83 us: 1.03x slower                                                    |
| tomli_loads          | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                   |
| pickle_list          | 2.83 us                                                     | 3.16 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 16.0 ms: 1.02x faster                                                    |
| python_startup         | 19.5 ms                                                     | 19.7 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.33 ms: 1.12x faster                                                    |
| django_template | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.38x faster                                                     |
| comprehensions             | 14.1 us                                                     | 10.7 us: 1.32x faster                                                    |
| async_tree_none_tg         | 285 ms                                                      | 217 ms: 1.31x faster                                                     |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                     |
| typing_runtime_protocols   | 95.1 us                                                     | 73.9 us: 1.29x faster                                                    |
| async_tree_memoization     | 339 ms                                                      | 270 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 391 ms: 1.25x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 617 ms: 1.25x faster                                                     |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.69 sec: 1.24x faster                                                   |
| raytrace                   | 192 ms                                                      | 156 ms: 1.23x faster                                                     |
| async_tree_io              | 731 ms                                                      | 595 ms: 1.23x faster                                                     |
| mypy2                      | 509 ms                                                      | 419 ms: 1.22x faster                                                     |
| chaos                      | 43.3 ms                                                     | 38.3 ms: 1.13x faster                                                    |
| dulwich_log                | 44.3 ms                                                     | 39.5 ms: 1.12x faster                                                    |
| float                      | 56.8 ms                                                     | 50.7 ms: 1.12x faster                                                    |
| mako                       | 7.09 ms                                                     | 6.33 ms: 1.12x faster                                                    |
| logging_silent             | 60.5 ns                                                     | 54.1 ns: 1.12x faster                                                    |
| pickle_pure_python         | 195 us                                                      | 176 us: 1.11x faster                                                     |
| tornado_http               | 89.5 ms                                                     | 80.8 ms: 1.11x faster                                                    |
| deltablue                  | 2.16 ms                                                     | 1.95 ms: 1.11x faster                                                    |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.8 ms: 1.10x faster                                                    |
| regex_compile              | 87.5 ms                                                     | 79.8 ms: 1.10x faster                                                    |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.09x faster                                                    |
| hexiom                     | 4.10 ms                                                     | 3.77 ms: 1.09x faster                                                    |
| sympy_str                  | 175 ms                                                      | 161 ms: 1.09x faster                                                     |
| deepcopy_memo              | 23.7 us                                                     | 21.8 us: 1.09x faster                                                    |
| regex_dna                  | 126 ms                                                      | 116 ms: 1.08x faster                                                     |
| sympy_sum                  | 91.5 ms                                                     | 84.5 ms: 1.08x faster                                                    |
| bench_mp_pool              | 69.2 ms                                                     | 63.8 ms: 1.08x faster                                                    |
| deepcopy                   | 238 us                                                      | 221 us: 1.08x faster                                                     |
| go                         | 91.6 ms                                                     | 85.1 ms: 1.08x faster                                                    |
| spectral_norm              | 66.9 ms                                                     | 62.5 ms: 1.07x faster                                                    |
| richards                   | 28.4 ms                                                     | 26.5 ms: 1.07x faster                                                    |
| sqlite_synth               | 1.76 us                                                     | 1.65 us: 1.07x faster                                                    |
| richards_super             | 32.1 ms                                                     | 30.2 ms: 1.06x faster                                                    |
| unpickle_pure_python       | 133 us                                                      | 125 us: 1.06x faster                                                     |
| bench_thread_pool          | 857 us                                                      | 809 us: 1.06x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 760 us: 1.06x faster                                                     |
| sqlglot_normalize          | 187 ms                                                      | 177 ms: 1.06x faster                                                     |
| pathlib                    | 80.5 ms                                                     | 76.1 ms: 1.06x faster                                                    |
| generators                 | 22.5 ms                                                     | 21.4 ms: 1.05x faster                                                    |
| pprint_pformat             | 1.05 sec                                                    | 993 ms: 1.05x faster                                                     |
| logging_format             | 6.72 us                                                     | 6.38 us: 1.05x faster                                                    |
| sqlglot_transpile          | 1.02 ms                                                     | 971 us: 1.05x faster                                                     |
| logging_simple             | 6.28 us                                                     | 5.96 us: 1.05x faster                                                    |
| nqueens                    | 62.8 ms                                                     | 59.7 ms: 1.05x faster                                                    |
| pprint_safe_repr           | 513 ms                                                      | 489 ms: 1.05x faster                                                     |
| async_generators           | 239 ms                                                      | 229 ms: 1.05x faster                                                     |
| sympy_expand               | 284 ms                                                      | 272 ms: 1.04x faster                                                     |
| pickle                     | 7.43 us                                                     | 7.13 us: 1.04x faster                                                    |
| regex_effbot               | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                    |
| crypto_pyaes               | 48.5 ms                                                     | 46.6 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 2.09 us                                                     | 2.01 us: 1.04x faster                                                    |
| 2to3                       | 218 ms                                                      | 210 ms: 1.04x faster                                                     |
| chameleon                  | 4.98 ms                                                     | 4.80 ms: 1.04x faster                                                    |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                     |
| scimark_sor                | 78.8 ms                                                     | 76.3 ms: 1.03x faster                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 33.4 ms: 1.03x faster                                                    |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                    |
| meteor_contest             | 74.6 ms                                                     | 72.7 ms: 1.03x faster                                                    |
| asyncio_tcp                | 487 ms                                                      | 475 ms: 1.03x faster                                                     |
| xml_etree_generate         | 55.8 ms                                                     | 54.5 ms: 1.02x faster                                                    |
| django_template            | 22.9 ms                                                     | 22.5 ms: 1.02x faster                                                    |
| python_startup_no_site     | 16.2 ms                                                     | 16.0 ms: 1.02x faster                                                    |
| pyflate                    | 295 ms                                                      | 290 ms: 1.02x faster                                                     |
| scimark_lu                 | 58.9 ms                                                     | 57.9 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 65.2 ms                                                     | 64.1 ms: 1.02x faster                                                    |
| nbody                      | 71.9 ms                                                     | 70.8 ms: 1.02x faster                                                    |
| xml_etree_process          | 37.7 ms                                                     | 37.2 ms: 1.01x faster                                                    |
| aiohttp                    | 884 us                                                      | 875 us: 1.01x faster                                                     |
| json_dumps                 | 5.70 ms                                                     | 5.64 ms: 1.01x faster                                                    |
| docutils                   | 1.66 sec                                                    | 1.65 sec: 1.01x faster                                                   |
| unpickle                   | 8.18 us                                                     | 8.25 us: 1.01x slower                                                    |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                    |
| python_startup             | 19.5 ms                                                     | 19.7 ms: 1.01x slower                                                    |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                    |
| mdp                        | 1.37 sec                                                    | 1.39 sec: 1.01x slower                                                   |
| scimark_fft                | 184 ms                                                      | 190 ms: 1.03x slower                                                     |
| unpickle_list              | 2.75 us                                                     | 2.83 us: 1.03x slower                                                    |
| tomli_loads                | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                   |
| fannkuch                   | 247 ms                                                      | 257 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.68 ms: 1.05x slower                                                    |
| pickle_list                | 2.83 us                                                     | 3.16 us: 1.12x slower                                                    |
| coverage                   | 40.8 ms                                                     | 46.4 ms: 1.14x slower                                                    |
| create_gc_cycles           | 752 us                                                      | 899 us: 1.20x slower                                                     |
| telco                      | 4.13 ms                                                     | 5.09 ms: 1.23x slower                                                    |
| regex_v8                   | 14.2 ms                                                     | 18.3 ms: 1.28x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                             |

Benchmark hidden because not significant (4): pycparser, json_loads, xml_etree_parse, json
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240416-3.13.0a6+-ced0ca9/bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown