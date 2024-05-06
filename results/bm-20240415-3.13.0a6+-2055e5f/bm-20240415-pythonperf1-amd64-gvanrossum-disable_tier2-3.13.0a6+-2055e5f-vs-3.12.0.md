# Results vs. 3.12.0

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 211 ms: 1.03x faster                                                     |
| chameleon      | 4.98 ms                                                     | 4.87 ms: 1.02x faster                                                    |
| tornado_http   | 89.5 ms                                                     | 82.6 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                       | 1.04x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 274 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 389 ms: 1.29x faster                                                     |
| async_tree_none            | 291 ms                                                      | 229 ms: 1.27x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 225 ms: 1.27x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 627 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 399 ms: 1.23x faster                                                     |
| async_tree_memoization     | 339 ms                                                      | 278 ms: 1.22x faster                                                     |
| async_tree_io              | 731 ms                                                      | 606 ms: 1.21x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 53.0 ms: 1.07x faster                                                    |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                     |
| nbody          | 71.9 ms                                                     | 69.8 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                       | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 80.8 ms: 1.08x faster                                                    |
| regex_dna      | 126 ms                                                      | 120 ms: 1.06x faster                                                     |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                    |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                       | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|---------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python  | 195 us                                                      | 183 us: 1.07x faster                                                     |
| xml_etree_iterparse | 65.2 ms                                                     | 63.8 ms: 1.02x faster                                                    |
| json_loads          | 13.9 us                                                     | 13.6 us: 1.02x faster                                                    |
| xml_etree_parse     | 93.0 ms                                                     | 92.3 ms: 1.01x faster                                                    |
| xml_etree_generate  | 55.8 ms                                                     | 56.6 ms: 1.01x slower                                                    |
| unpickle            | 8.18 us                                                     | 8.32 us: 1.02x slower                                                    |
| xml_etree_process   | 37.7 ms                                                     | 38.5 ms: 1.02x slower                                                    |
| tomli_loads         | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                   |
| pickle_dict         | 18.4 us                                                     | 19.8 us: 1.08x slower                                                    |
| pickle_list         | 2.83 us                                                     | 3.18 us: 1.13x slower                                                    |
| Geometric mean      | (ref)                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (4): unpickle_pure_python, unpickle_list, json_dumps, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 16.8 ms: 1.03x slower                                                    |
| python_startup         | 19.5 ms                                                     | 20.3 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.36 ms: 1.11x faster                                                    |
| django_template | 22.9 ms                                                     | 23.3 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                       | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 274 ms: 1.34x faster                                                     |
| comprehensions             | 14.1 us                                                     | 10.7 us: 1.32x faster                                                    |
| typing_runtime_protocols   | 95.1 us                                                     | 72.8 us: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 389 ms: 1.29x faster                                                     |
| async_tree_none            | 291 ms                                                      | 229 ms: 1.27x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 225 ms: 1.27x faster                                                     |
| async_tree_io_tg           | 771 ms                                                      | 627 ms: 1.23x faster                                                     |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.71 sec: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 399 ms: 1.23x faster                                                     |
| async_tree_memoization     | 339 ms                                                      | 278 ms: 1.22x faster                                                     |
| async_tree_io              | 731 ms                                                      | 606 ms: 1.21x faster                                                     |
| mypy2                      | 509 ms                                                      | 424 ms: 1.20x faster                                                     |
| raytrace                   | 192 ms                                                      | 168 ms: 1.15x faster                                                     |
| chaos                      | 43.3 ms                                                     | 38.8 ms: 1.12x faster                                                    |
| mako                       | 7.09 ms                                                     | 6.36 ms: 1.11x faster                                                    |
| dulwich_log                | 44.3 ms                                                     | 40.6 ms: 1.09x faster                                                    |
| tornado_http               | 89.5 ms                                                     | 82.6 ms: 1.08x faster                                                    |
| generators                 | 22.5 ms                                                     | 20.8 ms: 1.08x faster                                                    |
| regex_compile              | 87.5 ms                                                     | 80.8 ms: 1.08x faster                                                    |
| deepcopy_memo              | 23.7 us                                                     | 21.9 us: 1.08x faster                                                    |
| sympy_sum                  | 91.5 ms                                                     | 84.8 ms: 1.08x faster                                                    |
| sympy_str                  | 175 ms                                                      | 162 ms: 1.08x faster                                                     |
| float                      | 56.8 ms                                                     | 53.0 ms: 1.07x faster                                                    |
| crypto_pyaes               | 48.5 ms                                                     | 45.2 ms: 1.07x faster                                                    |
| deepcopy                   | 238 us                                                      | 222 us: 1.07x faster                                                     |
| pickle_pure_python         | 195 us                                                      | 183 us: 1.07x faster                                                     |
| bench_mp_pool              | 69.2 ms                                                     | 64.7 ms: 1.07x faster                                                    |
| logging_silent             | 60.5 ns                                                     | 56.6 ns: 1.07x faster                                                    |
| bench_thread_pool          | 857 us                                                      | 803 us: 1.07x faster                                                     |
| coroutines                 | 14.3 ms                                                     | 13.4 ms: 1.07x faster                                                    |
| pathlib                    | 80.5 ms                                                     | 76.1 ms: 1.06x faster                                                    |
| sqlite_synth               | 1.76 us                                                     | 1.67 us: 1.06x faster                                                    |
| regex_dna                  | 126 ms                                                      | 120 ms: 1.06x faster                                                     |
| hexiom                     | 4.10 ms                                                     | 3.89 ms: 1.06x faster                                                    |
| deltablue                  | 2.16 ms                                                     | 2.05 ms: 1.05x faster                                                    |
| pprint_pformat             | 1.05 sec                                                    | 996 ms: 1.05x faster                                                     |
| scimark_lu                 | 58.9 ms                                                     | 56.1 ms: 1.05x faster                                                    |
| pprint_safe_repr           | 513 ms                                                      | 489 ms: 1.05x faster                                                     |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.7 ms: 1.05x faster                                                    |
| nqueens                    | 62.8 ms                                                     | 60.0 ms: 1.05x faster                                                    |
| logging_simple             | 6.28 us                                                     | 6.03 us: 1.04x faster                                                    |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                     |
| sqlglot_transpile          | 1.02 ms                                                     | 989 us: 1.03x faster                                                     |
| scimark_sor                | 78.8 ms                                                     | 76.2 ms: 1.03x faster                                                    |
| 2to3                       | 218 ms                                                      | 211 ms: 1.03x faster                                                     |
| deepcopy_reduce            | 2.09 us                                                     | 2.03 us: 1.03x faster                                                    |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                    |
| nbody                      | 71.9 ms                                                     | 69.8 ms: 1.03x faster                                                    |
| logging_format             | 6.72 us                                                     | 6.52 us: 1.03x faster                                                    |
| sympy_expand               | 284 ms                                                      | 276 ms: 1.03x faster                                                     |
| sympy_integrate            | 13.0 ms                                                     | 12.6 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 187 ms                                                      | 182 ms: 1.03x faster                                                     |
| chameleon                  | 4.98 ms                                                     | 4.87 ms: 1.02x faster                                                    |
| async_generators           | 239 ms                                                      | 234 ms: 1.02x faster                                                     |
| xml_etree_iterparse        | 65.2 ms                                                     | 63.8 ms: 1.02x faster                                                    |
| json_loads                 | 13.9 us                                                     | 13.6 us: 1.02x faster                                                    |
| sqlglot_parse              | 804 us                                                      | 790 us: 1.02x faster                                                     |
| pyflate                    | 295 ms                                                      | 289 ms: 1.02x faster                                                     |
| spectral_norm              | 66.9 ms                                                     | 65.8 ms: 1.02x faster                                                    |
| meteor_contest             | 74.6 ms                                                     | 73.6 ms: 1.01x faster                                                    |
| xml_etree_parse            | 93.0 ms                                                     | 92.3 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 34.3 ms: 1.01x faster                                                    |
| go                         | 91.6 ms                                                     | 91.0 ms: 1.01x faster                                                    |
| xml_etree_generate         | 55.8 ms                                                     | 56.6 ms: 1.01x slower                                                    |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                    |
| unpickle                   | 8.18 us                                                     | 8.32 us: 1.02x slower                                                    |
| django_template            | 22.9 ms                                                     | 23.3 ms: 1.02x slower                                                    |
| xml_etree_process          | 37.7 ms                                                     | 38.5 ms: 1.02x slower                                                    |
| scimark_fft                | 184 ms                                                      | 188 ms: 1.02x slower                                                     |
| fannkuch                   | 247 ms                                                      | 253 ms: 1.03x slower                                                     |
| python_startup_no_site     | 16.2 ms                                                     | 16.8 ms: 1.03x slower                                                    |
| tomli_loads                | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                   |
| python_startup             | 19.5 ms                                                     | 20.3 ms: 1.04x slower                                                    |
| richards_super             | 32.1 ms                                                     | 33.7 ms: 1.05x slower                                                    |
| richards                   | 28.4 ms                                                     | 29.9 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.70 ms: 1.06x slower                                                    |
| pycparser                  | 699 ms                                                      | 739 ms: 1.06x slower                                                     |
| pickle_dict                | 18.4 us                                                     | 19.8 us: 1.08x slower                                                    |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                    |
| pickle_list                | 2.83 us                                                     | 3.18 us: 1.13x slower                                                    |
| coverage                   | 40.8 ms                                                     | 47.3 ms: 1.16x slower                                                    |
| create_gc_cycles           | 752 us                                                      | 888 us: 1.18x slower                                                     |
| telco                      | 4.13 ms                                                     | 5.05 ms: 1.22x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.04x faster                                                             |

Benchmark hidden because not significant (9): asyncio_tcp, docutils, aiohttp, unpickle_pure_python, unpickle_list, mdp, json_dumps, pickle, json
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240415-3.13.0a6+-2055e5f/bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown