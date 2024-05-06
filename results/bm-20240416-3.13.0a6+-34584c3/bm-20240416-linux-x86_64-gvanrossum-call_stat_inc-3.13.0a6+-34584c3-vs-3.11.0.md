# Results vs. 3.11.0

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 34584c3
- commit date: 2024-04-16
- overall geometric mean: 1.07x faster
- HPT reliability: 97.36%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                |
| chameleon      | 6.70 ms                                                | 6.96 ms: 1.04x slower                                               |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                              |
| html5lib       | 64.8 ms                                                | 67.2 ms: 1.04x slower                                               |
| tornado_http   | 98.1 ms                                                | 94.2 ms: 1.04x faster                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 922 ms: 1.40x faster                                                |
| async_tree_io              | 1.29 sec                                               | 930 ms: 1.38x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.1 ms: 1.05x faster                                               |
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                |
| regex_effbot   | 3.51 ms                                                | 3.71 ms: 1.06x slower                                               |
| regex_dna      | 205 ms                                                 | 222 ms: 1.08x slower                                                |
| regex_v8       | 22.9 ms                                                | 24.9 ms: 1.09x slower                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.25x faster                                               |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                               |
| tomli_loads          | 2.30 sec                                               | 2.21 sec: 1.04x faster                                              |
| unpickle_list        | 5.21 us                                                | 5.03 us: 1.04x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                                |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                               |
| xml_etree_process    | 56.9 ms                                                | 60.8 ms: 1.07x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 88.7 ms: 1.09x slower                                               |
| pickle               | 11.0 us                                                | 12.0 us: 1.10x slower                                               |
| pickle_list          | 4.59 us                                                | 5.40 us: 1.18x slower                                               |
| unpickle             | 13.8 us                                                | 17.0 us: 1.23x slower                                               |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.13 ms: 1.19x slower                                               |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                               |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.9 ms: 1.01x faster                                               |
| mako            | 10.7 ms                                                | 11.0 ms: 1.03x slower                                               |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                               |
| genshi_text     | 22.5 ms                                                | 23.9 ms: 1.06x slower                                               |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 116 us: 4.48x faster                                                |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 507 ms: 1.73x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                              |
| pylint                     | 476 ms                                                 | 320 ms: 1.49x faster                                                |
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 922 ms: 1.40x faster                                                |
| async_tree_io              | 1.29 sec                                               | 930 ms: 1.38x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                |
| comprehensions             | 23.6 us                                                | 17.1 us: 1.38x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.25x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                |
| chaos                      | 71.9 ms                                                | 60.2 ms: 1.19x faster                                               |
| deltablue                  | 3.92 ms                                                | 3.29 ms: 1.19x faster                                               |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.18x faster                                               |
| raytrace                   | 309 ms                                                 | 263 ms: 1.17x faster                                                |
| richards_super             | 61.9 ms                                                | 54.4 ms: 1.14x faster                                               |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                               |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                               |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                |
| hexiom                     | 6.89 ms                                                | 6.37 ms: 1.08x faster                                               |
| nqueens                    | 87.9 ms                                                | 81.6 ms: 1.08x faster                                               |
| logging_simple             | 6.22 us                                                | 5.78 us: 1.08x faster                                               |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                              |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                               |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                |
| pathlib                    | 18.5 ms                                                | 17.5 ms: 1.06x faster                                               |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                                |
| nbody                      | 96.0 ms                                                | 91.1 ms: 1.05x faster                                               |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                               |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                               |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                               |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                               |
| fannkuch                   | 405 ms                                                 | 387 ms: 1.05x faster                                                |
| tomli_loads                | 2.30 sec                                               | 2.21 sec: 1.04x faster                                              |
| tornado_http               | 98.1 ms                                                | 94.2 ms: 1.04x faster                                               |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                |
| unpickle_list              | 5.21 us                                                | 5.03 us: 1.04x faster                                               |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                |
| deepcopy                   | 365 us                                                 | 354 us: 1.03x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 68.5 ms: 1.03x faster                                               |
| richards                   | 49.8 ms                                                | 48.4 ms: 1.03x faster                                               |
| crypto_pyaes               | 76.7 ms                                                | 74.7 ms: 1.03x faster                                               |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.03x faster                                                |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                              |
| gc_traversal               | 4.01 ms                                                | 3.96 ms: 1.01x faster                                               |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.01x faster                                                |
| deepcopy_reduce            | 3.22 us                                                | 3.18 us: 1.01x faster                                               |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                                |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                |
| genshi_xml                 | 53.4 ms                                                | 52.9 ms: 1.01x faster                                               |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                               |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                |
| bench_thread_pool          | 834 us                                                 | 838 us: 1.00x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 55.6 ms: 1.01x slower                                               |
| scimark_sor                | 121 ms                                                 | 122 ms: 1.01x slower                                                |
| pprint_safe_repr           | 747 ms                                                 | 754 ms: 1.01x slower                                                |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                               |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.17 ms: 1.03x slower                                               |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                               |
| dulwich_log                | 64.6 ms                                                | 66.7 ms: 1.03x slower                                               |
| html5lib                   | 64.8 ms                                                | 67.2 ms: 1.04x slower                                               |
| chameleon                  | 6.70 ms                                                | 6.96 ms: 1.04x slower                                               |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                               |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.05x slower                                                |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                               |
| regex_effbot               | 3.51 ms                                                | 3.71 ms: 1.06x slower                                               |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                               |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                              |
| genshi_text                | 22.5 ms                                                | 23.9 ms: 1.06x slower                                               |
| xml_etree_process          | 56.9 ms                                                | 60.8 ms: 1.07x slower                                               |
| scimark_fft                | 345 ms                                                 | 370 ms: 1.07x slower                                                |
| pyflate                    | 434 ms                                                 | 467 ms: 1.08x slower                                                |
| mypy2                      | 686 ms                                                 | 741 ms: 1.08x slower                                                |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.08x slower                                                |
| regex_v8                   | 22.9 ms                                                | 24.9 ms: 1.09x slower                                               |
| xml_etree_generate         | 81.1 ms                                                | 88.7 ms: 1.09x slower                                               |
| pickle                     | 11.0 us                                                | 12.0 us: 1.10x slower                                               |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                               |
| pickle_list                | 4.59 us                                                | 5.40 us: 1.18x slower                                               |
| async_generators           | 374 ms                                                 | 443 ms: 1.18x slower                                                |
| python_startup_no_site     | 6.01 ms                                                | 7.13 ms: 1.19x slower                                               |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                               |
| coverage                   | 78.8 ms                                                | 96.8 ms: 1.23x slower                                               |
| unpickle                   | 13.8 us                                                | 17.0 us: 1.23x slower                                               |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                               |
| telco                      | 6.86 ms                                                | 8.65 ms: 1.26x slower                                               |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                        |

Benchmark hidden because not significant (5): pprint_pformat, float, json, xml_etree_iterparse, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.36% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x