# Results vs. base

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.00x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 334 ms                                                                 | 332 ms: 1.01x faster                                                |
| docutils       | 3.31 sec                                                               | 3.28 sec: 1.01x faster                                              |
| html5lib       | 73.3 ms                                                                | 75.6 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 195 ms: 1.11x faster                                                |
| nbody          | 209 ms                                                                 | 203 ms: 1.03x faster                                                |
| float          | 136 ms                                                                 | 139 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 27.0 ms                                                                | 27.2 ms: 1.01x slower                                               |
| regex_effbot   | 3.85 ms                                                                | 3.88 ms: 1.01x slower                                               |
| regex_dna      | 232 ms                                                                 | 235 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_list        | 5.32 us                                                                | 5.24 us: 1.02x faster                                               |
| tomli_loads          | 3.46 sec                                                               | 3.41 sec: 1.01x faster                                              |
| pickle_pure_python   | 318 us                                                                 | 314 us: 1.01x faster                                                |
| json_dumps           | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                               |
| xml_etree_process    | 71.0 ms                                                                | 70.4 ms: 1.01x faster                                               |
| unpickle_pure_python | 407 us                                                                 | 406 us: 1.00x faster                                                |
| xml_etree_parse      | 161 ms                                                                 | 163 ms: 1.01x slower                                                |
| pickle               | 11.7 us                                                                | 12.1 us: 1.03x slower                                               |
| pickle_list          | 4.93 us                                                                | 5.20 us: 1.05x slower                                               |
| pickle_dict          | 33.9 us                                                                | 35.8 us: 1.05x slower                                               |
| unpickle             | 15.8 us                                                                | 16.8 us: 1.07x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 21.2 ms                                                                | 20.9 ms: 1.01x faster                                               |
| django_template | 43.1 ms                                                                | 42.9 ms: 1.00x faster                                               |
| genshi_text     | 26.7 ms                                                                | 27.3 ms: 1.02x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits                | 217 ms                                                                 | 195 ms: 1.11x faster                                                |
| mdp                     | 3.19 sec                                                               | 2.99 sec: 1.06x faster                                              |
| scimark_lu              | 215 ms                                                                 | 208 ms: 1.04x faster                                                |
| comprehensions          | 36.5 us                                                                | 35.2 us: 1.04x faster                                               |
| logging_silent          | 113 ns                                                                 | 109 ns: 1.03x faster                                                |
| logging_format          | 7.65 us                                                                | 7.42 us: 1.03x faster                                               |
| logging_simple          | 6.92 us                                                                | 6.72 us: 1.03x faster                                               |
| nbody                   | 209 ms                                                                 | 203 ms: 1.03x faster                                                |
| pprint_safe_repr        | 1.27 sec                                                               | 1.24 sec: 1.02x faster                                              |
| fannkuch                | 769 ms                                                                 | 754 ms: 1.02x faster                                                |
| scimark_sor             | 177 ms                                                                 | 174 ms: 1.02x faster                                                |
| pprint_pformat          | 2.63 sec                                                               | 2.59 sec: 1.02x faster                                              |
| coroutines              | 23.1 ms                                                                | 22.8 ms: 1.02x faster                                               |
| unpickle_list           | 5.32 us                                                                | 5.24 us: 1.02x faster                                               |
| go                      | 229 ms                                                                 | 226 ms: 1.02x faster                                                |
| hexiom                  | 15.4 ms                                                                | 15.1 ms: 1.02x faster                                               |
| spectral_norm           | 240 ms                                                                 | 237 ms: 1.02x faster                                                |
| tomli_loads             | 3.46 sec                                                               | 3.41 sec: 1.01x faster                                              |
| richards                | 75.5 ms                                                                | 74.5 ms: 1.01x faster                                               |
| pycparser               | 1.41 sec                                                               | 1.39 sec: 1.01x faster                                              |
| deepcopy_memo           | 51.2 us                                                                | 50.5 us: 1.01x faster                                               |
| mako                    | 21.2 ms                                                                | 20.9 ms: 1.01x faster                                               |
| pickle_pure_python      | 318 us                                                                 | 314 us: 1.01x faster                                                |
| meteor_contest          | 146 ms                                                                 | 144 ms: 1.01x faster                                                |
| json_dumps              | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                               |
| raytrace                | 378 ms                                                                 | 374 ms: 1.01x faster                                                |
| pyflate                 | 888 ms                                                                 | 880 ms: 1.01x faster                                                |
| sqlglot_parse           | 1.64 ms                                                                | 1.63 ms: 1.01x faster                                               |
| xml_etree_process       | 71.0 ms                                                                | 70.4 ms: 1.01x faster                                               |
| scimark_fft             | 636 ms                                                                 | 630 ms: 1.01x faster                                                |
| thrift                  | 852 us                                                                 | 846 us: 1.01x faster                                                |
| docutils                | 3.31 sec                                                               | 3.28 sec: 1.01x faster                                              |
| create_gc_cycles        | 1.78 ms                                                                | 1.77 ms: 1.01x faster                                               |
| gunicorn                | 1.37 ms                                                                | 1.36 ms: 1.01x faster                                               |
| 2to3                    | 334 ms                                                                 | 332 ms: 1.01x faster                                                |
| nqueens                 | 152 ms                                                                 | 151 ms: 1.00x faster                                                |
| sqlglot_transpile       | 1.98 ms                                                                | 1.97 ms: 1.00x faster                                               |
| richards_super          | 81.5 ms                                                                | 81.1 ms: 1.00x faster                                               |
| asyncio_tcp_ssl         | 1.87 sec                                                               | 1.86 sec: 1.00x faster                                              |
| unpickle_pure_python    | 407 us                                                                 | 406 us: 1.00x faster                                                |
| crypto_pyaes            | 128 ms                                                                 | 127 ms: 1.00x faster                                                |
| django_template         | 43.1 ms                                                                | 42.9 ms: 1.00x faster                                               |
| gc_traversal            | 3.96 ms                                                                | 3.95 ms: 1.00x faster                                               |
| sympy_integrate         | 25.6 ms                                                                | 25.5 ms: 1.00x faster                                               |
| asyncio_tcp             | 514 ms                                                                 | 513 ms: 1.00x faster                                                |
| sqlglot_optimize        | 71.2 ms                                                                | 71.1 ms: 1.00x faster                                               |
| dulwich_log             | 75.6 ms                                                                | 75.8 ms: 1.00x slower                                               |
| deepcopy                | 393 us                                                                 | 395 us: 1.01x slower                                                |
| scimark_monte_carlo     | 137 ms                                                                 | 138 ms: 1.01x slower                                                |
| async_generators        | 503 ms                                                                 | 507 ms: 1.01x slower                                                |
| regex_v8                | 27.0 ms                                                                | 27.2 ms: 1.01x slower                                               |
| scimark_sparse_mat_mult | 9.19 ms                                                                | 9.27 ms: 1.01x slower                                               |
| pathlib                 | 18.6 ms                                                                | 18.8 ms: 1.01x slower                                               |
| regex_effbot            | 3.85 ms                                                                | 3.88 ms: 1.01x slower                                               |
| coverage                | 98.3 ms                                                                | 99.3 ms: 1.01x slower                                               |
| xml_etree_parse         | 161 ms                                                                 | 163 ms: 1.01x slower                                                |
| regex_dna               | 232 ms                                                                 | 235 ms: 1.01x slower                                                |
| sqlite_synth            | 3.11 us                                                                | 3.16 us: 1.02x slower                                               |
| deepcopy_reduce         | 3.36 us                                                                | 3.41 us: 1.02x slower                                               |
| float                   | 136 ms                                                                 | 139 ms: 1.02x slower                                                |
| genshi_text             | 26.7 ms                                                                | 27.3 ms: 1.02x slower                                               |
| html5lib                | 73.3 ms                                                                | 75.6 ms: 1.03x slower                                               |
| pickle                  | 11.7 us                                                                | 12.1 us: 1.03x slower                                               |
| pickle_list             | 4.93 us                                                                | 5.20 us: 1.05x slower                                               |
| pickle_dict             | 33.9 us                                                                | 35.8 us: 1.05x slower                                               |
| unpickle                | 15.8 us                                                                | 16.8 us: 1.07x slower                                               |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (35): deltablue, async_tree_io, djangocms, xml_etree_iterparse, async_tree_io_tg, aiohttp, pylint, typing_runtime_protocols, genshi_xml, tornado_http, async_tree_memoization_tg, async_tree_none_tg, json, mypy2, bench_thread_pool, sympy_str, bench_mp_pool, regex_compile, chaos, telco, xml_etree_generate, async_tree_cpu_io_mixed, sqlglot_normalize, asyncio_websockets, python_startup, python_startup_no_site, generators, sympy_sum, sympy_expand, async_tree_memoization, chameleon, json_loads, async_tree_cpu_io_mixed_tg, dask, async_tree_none

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x