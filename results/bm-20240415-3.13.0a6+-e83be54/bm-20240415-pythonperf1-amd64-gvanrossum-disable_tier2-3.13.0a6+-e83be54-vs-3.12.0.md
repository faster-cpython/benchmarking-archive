# Results vs. 3.12.0

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: e83be54
- commit date: 2024-04-15
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 211 ms: 1.03x faster                                                     |
| chameleon      | 4.98 ms                                                     | 4.83 ms: 1.03x faster                                                    |
| tornado_http   | 89.5 ms                                                     | 82.1 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                       | 1.04x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 273 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 389 ms: 1.29x faster                                                     |
| async_tree_none            | 291 ms                                                      | 227 ms: 1.28x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 225 ms: 1.27x faster                                                     |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 397 ms: 1.23x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 626 ms: 1.23x faster                                                     |
| async_tree_io              | 731 ms                                                      | 602 ms: 1.21x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 50.9 ms: 1.11x faster                                                    |
| nbody          | 71.9 ms                                                     | 68.5 ms: 1.05x faster                                                    |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                       | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 78.9 ms: 1.11x faster                                                    |
| regex_dna      | 126 ms                                                      | 117 ms: 1.08x faster                                                     |
| regex_effbot   | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                       | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 180 us: 1.09x faster                                                     |
| unpickle_pure_python | 133 us                                                      | 128 us: 1.04x faster                                                     |
| json_loads           | 13.9 us                                                     | 13.5 us: 1.03x faster                                                    |
| xml_etree_iterparse  | 65.2 ms                                                     | 63.6 ms: 1.02x faster                                                    |
| xml_etree_generate   | 55.8 ms                                                     | 54.8 ms: 1.02x faster                                                    |
| json_dumps           | 5.70 ms                                                     | 5.65 ms: 1.01x faster                                                    |
| pickle               | 7.43 us                                                     | 7.37 us: 1.01x faster                                                    |
| unpickle             | 8.18 us                                                     | 8.40 us: 1.03x slower                                                    |
| unpickle_list        | 2.75 us                                                     | 2.83 us: 1.03x slower                                                    |
| tomli_loads          | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                   |
| pickle_list          | 2.83 us                                                     | 3.08 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.00x faster                                                             |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 19.5 ms                                                     | 19.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.34 ms: 1.12x faster                                                    |
| django_template | 22.9 ms                                                     | 23.6 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                       | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 273 ms: 1.35x faster                                                     |
| comprehensions             | 14.1 us                                                     | 10.6 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 389 ms: 1.29x faster                                                     |
| async_tree_none            | 291 ms                                                      | 227 ms: 1.28x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 225 ms: 1.27x faster                                                     |
| typing_runtime_protocols   | 95.1 us                                                     | 75.5 us: 1.26x faster                                                    |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 397 ms: 1.23x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 626 ms: 1.23x faster                                                     |
| async_tree_io              | 731 ms                                                      | 602 ms: 1.21x faster                                                     |
| mypy2                      | 509 ms                                                      | 424 ms: 1.20x faster                                                     |
| raytrace                   | 192 ms                                                      | 164 ms: 1.17x faster                                                     |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.79 sec: 1.17x faster                                                   |
| chaos                      | 43.3 ms                                                     | 38.1 ms: 1.14x faster                                                    |
| mako                       | 7.09 ms                                                     | 6.34 ms: 1.12x faster                                                    |
| float                      | 56.8 ms                                                     | 50.9 ms: 1.11x faster                                                    |
| dulwich_log                | 44.3 ms                                                     | 39.9 ms: 1.11x faster                                                    |
| regex_compile              | 87.5 ms                                                     | 78.9 ms: 1.11x faster                                                    |
| spectral_norm              | 66.9 ms                                                     | 60.9 ms: 1.10x faster                                                    |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.9 ms: 1.10x faster                                                    |
| scimark_sor                | 78.8 ms                                                     | 72.0 ms: 1.09x faster                                                    |
| scimark_lu                 | 58.9 ms                                                     | 53.8 ms: 1.09x faster                                                    |
| deepcopy_memo              | 23.7 us                                                     | 21.7 us: 1.09x faster                                                    |
| crypto_pyaes               | 48.5 ms                                                     | 44.5 ms: 1.09x faster                                                    |
| tornado_http               | 89.5 ms                                                     | 82.1 ms: 1.09x faster                                                    |
| pickle_pure_python         | 195 us                                                      | 180 us: 1.09x faster                                                     |
| bench_mp_pool              | 69.2 ms                                                     | 63.7 ms: 1.09x faster                                                    |
| sympy_str                  | 175 ms                                                      | 161 ms: 1.08x faster                                                     |
| sympy_sum                  | 91.5 ms                                                     | 84.5 ms: 1.08x faster                                                    |
| regex_dna                  | 126 ms                                                      | 117 ms: 1.08x faster                                                     |
| hexiom                     | 4.10 ms                                                     | 3.79 ms: 1.08x faster                                                    |
| generators                 | 22.5 ms                                                     | 20.9 ms: 1.08x faster                                                    |
| coroutines                 | 14.3 ms                                                     | 13.3 ms: 1.07x faster                                                    |
| nqueens                    | 62.8 ms                                                     | 58.9 ms: 1.07x faster                                                    |
| logging_silent             | 60.5 ns                                                     | 56.8 ns: 1.06x faster                                                    |
| sqlite_synth               | 1.76 us                                                     | 1.66 us: 1.06x faster                                                    |
| bench_thread_pool          | 857 us                                                      | 807 us: 1.06x faster                                                     |
| pathlib                    | 80.5 ms                                                     | 76.2 ms: 1.06x faster                                                    |
| deepcopy                   | 238 us                                                      | 226 us: 1.05x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 764 us: 1.05x faster                                                     |
| pprint_safe_repr           | 513 ms                                                      | 489 ms: 1.05x faster                                                     |
| nbody                      | 71.9 ms                                                     | 68.5 ms: 1.05x faster                                                    |
| logging_simple             | 6.28 us                                                     | 5.98 us: 1.05x faster                                                    |
| pprint_pformat             | 1.05 sec                                                    | 996 ms: 1.05x faster                                                     |
| deltablue                  | 2.16 ms                                                     | 2.06 ms: 1.05x faster                                                    |
| sqlglot_transpile          | 1.02 ms                                                     | 979 us: 1.04x faster                                                     |
| logging_format             | 6.72 us                                                     | 6.46 us: 1.04x faster                                                    |
| unpickle_pure_python       | 133 us                                                      | 128 us: 1.04x faster                                                     |
| regex_effbot               | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                    |
| sympy_integrate            | 13.0 ms                                                     | 12.5 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 2.09 us                                                     | 2.02 us: 1.04x faster                                                    |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                     |
| sympy_expand               | 284 ms                                                      | 275 ms: 1.03x faster                                                     |
| 2to3                       | 218 ms                                                      | 211 ms: 1.03x faster                                                     |
| json_loads                 | 13.9 us                                                     | 13.5 us: 1.03x faster                                                    |
| chameleon                  | 4.98 ms                                                     | 4.83 ms: 1.03x faster                                                    |
| pyflate                    | 295 ms                                                      | 286 ms: 1.03x faster                                                     |
| xml_etree_iterparse        | 65.2 ms                                                     | 63.6 ms: 1.02x faster                                                    |
| async_generators           | 239 ms                                                      | 235 ms: 1.02x faster                                                     |
| xml_etree_generate         | 55.8 ms                                                     | 54.8 ms: 1.02x faster                                                    |
| scimark_fft                | 184 ms                                                      | 182 ms: 1.02x faster                                                     |
| sqlglot_normalize          | 187 ms                                                      | 185 ms: 1.01x faster                                                     |
| go                         | 91.6 ms                                                     | 90.8 ms: 1.01x faster                                                    |
| json_dumps                 | 5.70 ms                                                     | 5.65 ms: 1.01x faster                                                    |
| pickle                     | 7.43 us                                                     | 7.37 us: 1.01x faster                                                    |
| meteor_contest             | 74.6 ms                                                     | 74.2 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 34.7 ms: 1.01x slower                                                    |
| mdp                        | 1.37 sec                                                    | 1.39 sec: 1.01x slower                                                   |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                    |
| python_startup             | 19.5 ms                                                     | 19.8 ms: 1.02x slower                                                    |
| unpickle                   | 8.18 us                                                     | 8.40 us: 1.03x slower                                                    |
| unpickle_list              | 2.75 us                                                     | 2.83 us: 1.03x slower                                                    |
| django_template            | 22.9 ms                                                     | 23.6 ms: 1.03x slower                                                    |
| richards                   | 28.4 ms                                                     | 29.3 ms: 1.03x slower                                                    |
| richards_super             | 32.1 ms                                                     | 33.3 ms: 1.04x slower                                                    |
| tomli_loads                | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                   |
| json                       | 3.05 ms                                                     | 3.21 ms: 1.05x slower                                                    |
| pycparser                  | 699 ms                                                      | 753 ms: 1.08x slower                                                     |
| pickle_list                | 2.83 us                                                     | 3.08 us: 1.09x slower                                                    |
| coverage                   | 40.8 ms                                                     | 46.0 ms: 1.13x slower                                                    |
| create_gc_cycles           | 752 us                                                      | 895 us: 1.19x slower                                                     |
| telco                      | 4.13 ms                                                     | 5.10 ms: 1.23x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                             |

Benchmark hidden because not significant (10): asyncio_tcp, docutils, scimark_sparse_mat_mult, xml_etree_process, xml_etree_parse, fannkuch, pickle_dict, aiohttp, python_startup_no_site, regex_v8
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240415-3.13.0a6+-e83be54/bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown