# Results vs. base

- fork: brandtbucher
- ref: exits
- machine: linux-x86_64
- commit hash: b9f3875
- commit date: 2024-05-02
- overall geometric mean: 1.00x faster
- HPT reliability: 95.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| chameleon      | 6.97 ms                                                                | 7.05 ms: 1.01x slower                                         |
| docutils       | 2.94 sec                                                               | 2.93 sec: 1.00x faster                                        |
| html5lib       | 69.0 ms                                                                | 66.6 ms: 1.04x faster                                         |
| tornado_http   | 96.9 ms                                                                | 96.2 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                  |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 189 ms: 1.09x faster                                          |
| nbody          | 80.9 ms                                                                | 80.0 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                                | 24.1 ms: 1.04x faster                                         |
| regex_dna      | 226 ms                                                                 | 223 ms: 1.01x faster                                          |
| regex_effbot   | 3.63 ms                                                                | 3.60 ms: 1.01x faster                                         |
| regex_compile  | 138 ms                                                                 | 139 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle_dict          | 35.7 us                                                                | 34.7 us: 1.03x faster                                         |
| xml_etree_generate   | 87.5 ms                                                                | 86.6 ms: 1.01x faster                                         |
| xml_etree_iterparse  | 102 ms                                                                 | 101 ms: 1.01x faster                                          |
| json_dumps           | 10.5 ms                                                                | 10.5 ms: 1.01x faster                                         |
| json_loads           | 27.7 us                                                                | 27.5 us: 1.01x faster                                         |
| tomli_loads          | 1.93 sec                                                               | 1.92 sec: 1.01x faster                                        |
| pickle               | 11.9 us                                                                | 11.9 us: 1.00x faster                                         |
| unpickle_pure_python | 219 us                                                                 | 218 us: 1.00x faster                                          |
| unpickle_list        | 5.20 us                                                                | 5.30 us: 1.02x slower                                         |
| unpickle             | 15.2 us                                                                | 16.1 us: 1.06x slower                                         |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (4): xml_etree_process, pickle_pure_python, pickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                         |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 9.73 ms                                                                | 9.69 ms: 1.01x faster                                         |
| genshi_xml     | 57.8 ms                                                                | 59.3 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark               | bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits                | 206 ms                                                                 | 189 ms: 1.09x faster                                          |
| logging_silent          | 103 ns                                                                 | 99.1 ns: 1.04x faster                                         |
| regex_v8                | 25.1 ms                                                                | 24.1 ms: 1.04x faster                                         |
| html5lib                | 69.0 ms                                                                | 66.6 ms: 1.04x faster                                         |
| pickle_dict             | 35.7 us                                                                | 34.7 us: 1.03x faster                                         |
| fannkuch                | 357 ms                                                                 | 349 ms: 1.02x faster                                          |
| logging_format          | 6.49 us                                                                | 6.37 us: 1.02x faster                                         |
| deltablue               | 3.83 ms                                                                | 3.76 ms: 1.02x faster                                         |
| spectral_norm           | 96.4 ms                                                                | 94.8 ms: 1.02x faster                                         |
| hexiom                  | 6.73 ms                                                                | 6.62 ms: 1.02x faster                                         |
| dulwich_log             | 70.2 ms                                                                | 69.2 ms: 1.02x faster                                         |
| thrift                  | 825 us                                                                 | 814 us: 1.01x faster                                          |
| comprehensions          | 17.0 us                                                                | 16.8 us: 1.01x faster                                         |
| xml_etree_generate      | 87.5 ms                                                                | 86.6 ms: 1.01x faster                                         |
| nbody                   | 80.9 ms                                                                | 80.0 ms: 1.01x faster                                         |
| xml_etree_iterparse     | 102 ms                                                                 | 101 ms: 1.01x faster                                          |
| regex_dna               | 226 ms                                                                 | 223 ms: 1.01x faster                                          |
| logging_simple          | 5.87 us                                                                | 5.81 us: 1.01x faster                                         |
| json_dumps              | 10.5 ms                                                                | 10.5 ms: 1.01x faster                                         |
| regex_effbot            | 3.63 ms                                                                | 3.60 ms: 1.01x faster                                         |
| tornado_http            | 96.9 ms                                                                | 96.2 ms: 1.01x faster                                         |
| json_loads              | 27.7 us                                                                | 27.5 us: 1.01x faster                                         |
| tomli_loads             | 1.93 sec                                                               | 1.92 sec: 1.01x faster                                        |
| mako                    | 9.73 ms                                                                | 9.69 ms: 1.01x faster                                         |
| sympy_sum               | 169 ms                                                                 | 168 ms: 1.00x faster                                          |
| pickle                  | 11.9 us                                                                | 11.9 us: 1.00x faster                                         |
| asyncio_tcp_ssl         | 1.87 sec                                                               | 1.86 sec: 1.00x faster                                        |
| scimark_fft             | 315 ms                                                                 | 314 ms: 1.00x faster                                          |
| unpickle_pure_python    | 219 us                                                                 | 218 us: 1.00x faster                                          |
| docutils                | 2.94 sec                                                               | 2.93 sec: 1.00x faster                                        |
| python_startup          | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                         |
| scimark_lu              | 126 ms                                                                 | 127 ms: 1.00x slower                                          |
| pathlib                 | 17.8 ms                                                                | 18.0 ms: 1.01x slower                                         |
| generators              | 30.1 ms                                                                | 30.3 ms: 1.01x slower                                         |
| mdp                     | 2.57 sec                                                               | 2.59 sec: 1.01x slower                                        |
| create_gc_cycles        | 1.77 ms                                                                | 1.78 ms: 1.01x slower                                         |
| regex_compile           | 138 ms                                                                 | 139 ms: 1.01x slower                                          |
| coverage                | 92.5 ms                                                                | 93.2 ms: 1.01x slower                                         |
| deepcopy_reduce         | 3.21 us                                                                | 3.24 us: 1.01x slower                                         |
| chameleon               | 6.97 ms                                                                | 7.05 ms: 1.01x slower                                         |
| telco                   | 8.45 ms                                                                | 8.55 ms: 1.01x slower                                         |
| gc_traversal            | 3.77 ms                                                                | 3.81 ms: 1.01x slower                                         |
| scimark_sparse_mat_mult | 4.49 ms                                                                | 4.55 ms: 1.01x slower                                         |
| crypto_pyaes            | 69.1 ms                                                                | 70.1 ms: 1.02x slower                                         |
| richards_super          | 48.2 ms                                                                | 49.0 ms: 1.02x slower                                         |
| unpickle_list           | 5.20 us                                                                | 5.30 us: 1.02x slower                                         |
| asyncio_tcp             | 520 ms                                                                 | 532 ms: 1.02x slower                                          |
| pyflate                 | 442 ms                                                                 | 453 ms: 1.02x slower                                          |
| pprint_pformat          | 1.49 sec                                                               | 1.53 sec: 1.03x slower                                        |
| genshi_xml              | 57.8 ms                                                                | 59.3 ms: 1.03x slower                                         |
| djangocms               | 31.3 us                                                                | 32.3 us: 1.03x slower                                         |
| unpickle                | 15.2 us                                                                | 16.1 us: 1.06x slower                                         |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (49): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, genshi_text, json, pylint, async_tree_cpu_io_mixed, meteor_contest, gunicorn, chaos, mypy2, typing_runtime_protocols, xml_etree_process, sympy_expand, 2to3, sympy_str, sqlglot_optimize, async_generators, aiohttp, pickle_pure_python, sqlglot_parse, deepcopy, sympy_integrate, bench_thread_pool, sqlglot_transpile, python_startup_no_site, async_tree_memoization, richards, scimark_sor, async_tree_none, async_tree_io, dask, bench_mp_pool, sqlite_synth, float, pickle_list, coroutines, sqlglot_normalize, raytrace, asyncio_websockets, pycparser, go, django_template, deepcopy_memo, async_tree_io_tg, xml_etree_parse, scimark_monte_carlo, nqueens, pprint_safe_repr

# HPT report

- Reliability score: 95.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x