# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-amd64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| chameleon      | 4.98 ms                                                     | 4.79 ms: 1.04x faster                                                     |
| docutils       | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                    |
| tornado_http   | 89.5 ms                                                     | 85.5 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 203 ms: 1.41x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                      |
| async_tree_none            | 291 ms                                                      | 214 ms: 1.36x faster                                                      |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 376 ms: 1.30x faster                                                      |
| async_tree_io              | 731 ms                                                      | 567 ms: 1.29x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 267 ms: 1.27x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 619 ms: 1.25x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.32x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 58.3 ms: 1.23x faster                                                     |
| float          | 56.8 ms                                                     | 46.0 ms: 1.23x faster                                                     |
| pidigits       | 152 ms                                                      | 146 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                       | 1.17x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 116 ms: 1.09x faster                                                      |
| regex_compile  | 87.5 ms                                                     | 83.8 ms: 1.04x faster                                                     |
| regex_effbot   | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                     |
| regex_v8       | 14.2 ms                                                     | 14.6 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                       | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.17 sec: 1.17x faster                                                    |
| pickle_pure_python   | 195 us                                                      | 173 us: 1.13x faster                                                      |
| xml_etree_iterparse  | 65.2 ms                                                     | 60.7 ms: 1.07x faster                                                     |
| unpickle_pure_python | 133 us                                                      | 125 us: 1.06x faster                                                      |
| xml_etree_generate   | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| xml_etree_parse      | 93.0 ms                                                     | 90.1 ms: 1.03x faster                                                     |
| json_dumps           | 5.70 ms                                                     | 5.55 ms: 1.03x faster                                                     |
| pickle               | 7.43 us                                                     | 7.26 us: 1.02x faster                                                     |
| xml_etree_process    | 37.7 ms                                                     | 37.1 ms: 1.02x faster                                                     |
| pickle_dict          | 18.4 us                                                     | 18.5 us: 1.00x slower                                                     |
| unpickle_list        | 2.75 us                                                     | 2.77 us: 1.01x slower                                                     |
| pickle_list          | 2.83 us                                                     | 2.86 us: 1.01x slower                                                     |
| unpickle             | 8.18 us                                                     | 8.50 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 22.0 ms: 1.13x slower                                                     |
| python_startup_no_site | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 5.22 ms: 1.36x faster                                                     |
| django_template | 22.9 ms                                                     | 23.3 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                       | 1.16x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| spectral_norm              | 66.9 ms                                                     | 46.1 ms: 1.45x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 203 ms: 1.41x faster                                                      |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.51 sec: 1.39x faster                                                    |
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                      |
| async_tree_none            | 291 ms                                                      | 214 ms: 1.36x faster                                                      |
| mako                       | 7.09 ms                                                     | 5.22 ms: 1.36x faster                                                     |
| typing_runtime_protocols   | 95.1 us                                                     | 70.2 us: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                      |
| comprehensions             | 14.1 us                                                     | 10.8 us: 1.31x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 376 ms: 1.30x faster                                                      |
| async_tree_io              | 731 ms                                                      | 567 ms: 1.29x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 267 ms: 1.27x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 619 ms: 1.25x faster                                                      |
| nbody                      | 71.9 ms                                                     | 58.3 ms: 1.23x faster                                                     |
| float                      | 56.8 ms                                                     | 46.0 ms: 1.23x faster                                                     |
| scimark_monte_carlo        | 43.7 ms                                                     | 36.1 ms: 1.21x faster                                                     |
| scimark_fft                | 184 ms                                                      | 153 ms: 1.20x faster                                                      |
| tomli_loads                | 1.37 sec                                                    | 1.17 sec: 1.17x faster                                                    |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.19 ms: 1.17x faster                                                     |
| crypto_pyaes               | 48.5 ms                                                     | 41.9 ms: 1.16x faster                                                     |
| chaos                      | 43.3 ms                                                     | 37.9 ms: 1.14x faster                                                     |
| logging_silent             | 60.5 ns                                                     | 53.1 ns: 1.14x faster                                                     |
| pickle_pure_python         | 195 us                                                      | 173 us: 1.13x faster                                                      |
| mypy2                      | 509 ms                                                      | 453 ms: 1.13x faster                                                      |
| generators                 | 22.5 ms                                                     | 20.0 ms: 1.12x faster                                                     |
| fannkuch                   | 247 ms                                                      | 220 ms: 1.12x faster                                                      |
| sqlite_synth               | 1.76 us                                                     | 1.57 us: 1.12x faster                                                     |
| pyflate                    | 295 ms                                                      | 264 ms: 1.12x faster                                                      |
| pprint_safe_repr           | 513 ms                                                      | 466 ms: 1.10x faster                                                      |
| pprint_pformat             | 1.05 sec                                                    | 951 ms: 1.10x faster                                                      |
| raytrace                   | 192 ms                                                      | 176 ms: 1.09x faster                                                      |
| regex_dna                  | 126 ms                                                      | 116 ms: 1.09x faster                                                      |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                     |
| xml_etree_iterparse        | 65.2 ms                                                     | 60.7 ms: 1.07x faster                                                     |
| deepcopy_memo              | 23.7 us                                                     | 22.1 us: 1.07x faster                                                     |
| logging_format             | 6.72 us                                                     | 6.27 us: 1.07x faster                                                     |
| logging_simple             | 6.28 us                                                     | 5.86 us: 1.07x faster                                                     |
| dulwich_log                | 44.3 ms                                                     | 41.5 ms: 1.07x faster                                                     |
| unpickle_pure_python       | 133 us                                                      | 125 us: 1.06x faster                                                      |
| deepcopy                   | 238 us                                                      | 225 us: 1.06x faster                                                      |
| deepcopy_reduce            | 2.09 us                                                     | 1.98 us: 1.06x faster                                                     |
| xml_etree_generate         | 55.8 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| deltablue                  | 2.16 ms                                                     | 2.06 ms: 1.05x faster                                                     |
| tornado_http               | 89.5 ms                                                     | 85.5 ms: 1.05x faster                                                     |
| sympy_str                  | 175 ms                                                      | 167 ms: 1.05x faster                                                      |
| regex_compile              | 87.5 ms                                                     | 83.8 ms: 1.04x faster                                                     |
| regex_effbot               | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                     |
| sympy_sum                  | 91.5 ms                                                     | 87.7 ms: 1.04x faster                                                     |
| chameleon                  | 4.98 ms                                                     | 4.79 ms: 1.04x faster                                                     |
| pathlib                    | 80.5 ms                                                     | 77.4 ms: 1.04x faster                                                     |
| pidigits                   | 152 ms                                                      | 146 ms: 1.04x faster                                                      |
| nqueens                    | 62.8 ms                                                     | 60.4 ms: 1.04x faster                                                     |
| meteor_contest             | 74.6 ms                                                     | 72.0 ms: 1.04x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 779 us: 1.03x faster                                                      |
| xml_etree_parse            | 93.0 ms                                                     | 90.1 ms: 1.03x faster                                                     |
| bench_thread_pool          | 857 us                                                      | 833 us: 1.03x faster                                                      |
| sqlglot_transpile          | 1.02 ms                                                     | 995 us: 1.03x faster                                                      |
| bench_mp_pool              | 69.2 ms                                                     | 67.4 ms: 1.03x faster                                                     |
| asyncio_tcp                | 487 ms                                                      | 475 ms: 1.03x faster                                                      |
| json_dumps                 | 5.70 ms                                                     | 5.55 ms: 1.03x faster                                                     |
| pickle                     | 7.43 us                                                     | 7.26 us: 1.02x faster                                                     |
| xml_etree_process          | 37.7 ms                                                     | 37.1 ms: 1.02x faster                                                     |
| sqlglot_normalize          | 187 ms                                                      | 186 ms: 1.01x faster                                                      |
| pickle_dict                | 18.4 us                                                     | 18.5 us: 1.00x slower                                                     |
| scimark_sor                | 78.8 ms                                                     | 79.3 ms: 1.01x slower                                                     |
| unpickle_list              | 2.75 us                                                     | 2.77 us: 1.01x slower                                                     |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                     |
| pickle_list                | 2.83 us                                                     | 2.86 us: 1.01x slower                                                     |
| sympy_expand               | 284 ms                                                      | 288 ms: 1.01x slower                                                      |
| django_template            | 22.9 ms                                                     | 23.3 ms: 1.02x slower                                                     |
| docutils                   | 1.66 sec                                                    | 1.69 sec: 1.02x slower                                                    |
| richards_super             | 32.1 ms                                                     | 32.7 ms: 1.02x slower                                                     |
| sympy_integrate            | 13.0 ms                                                     | 13.2 ms: 1.02x slower                                                     |
| regex_v8                   | 14.2 ms                                                     | 14.6 ms: 1.02x slower                                                     |
| aiohttp                    | 884 us                                                      | 909 us: 1.03x slower                                                      |
| async_generators           | 239 ms                                                      | 247 ms: 1.03x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 35.8 ms: 1.04x slower                                                     |
| richards                   | 28.4 ms                                                     | 29.5 ms: 1.04x slower                                                     |
| unpickle                   | 8.18 us                                                     | 8.50 us: 1.04x slower                                                     |
| go                         | 91.6 ms                                                     | 95.3 ms: 1.04x slower                                                     |
| hexiom                     | 4.10 ms                                                     | 4.47 ms: 1.09x slower                                                     |
| mdp                        | 1.37 sec                                                    | 1.51 sec: 1.10x slower                                                    |
| python_startup             | 19.5 ms                                                     | 22.0 ms: 1.13x slower                                                     |
| create_gc_cycles           | 752 us                                                      | 850 us: 1.13x slower                                                      |
| telco                      | 4.13 ms                                                     | 4.69 ms: 1.14x slower                                                     |
| coverage                   | 40.8 ms                                                     | 46.7 ms: 1.14x slower                                                     |
| python_startup_no_site     | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                     |
| scimark_lu                 | 58.9 ms                                                     | 71.8 ms: 1.22x slower                                                     |
| unpack_sequence            | 37.5 ns                                                     | 60.8 ns: 1.62x slower                                                     |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                              |

Benchmark hidden because not significant (4): json, 2to3, json_loads, pycparser
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown