# Results vs. 3.11.0

- fork: gvanrossum
- ref: disable_tier2
- machine: linux-x86_64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.08x faster
- HPT reliability: 99.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.01x slower                                                |
| chameleon      | 6.70 ms                                                | 6.91 ms: 1.03x slower                                               |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                              |
| html5lib       | 64.8 ms                                                | 67.5 ms: 1.04x slower                                               |
| tornado_http   | 98.1 ms                                                | 94.3 ms: 1.04x faster                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 331 ms: 1.48x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 438 ms: 1.43x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 908 ms: 1.43x faster                                                |
| async_tree_io              | 1.29 sec                                               | 916 ms: 1.40x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 85.7 ms: 1.12x faster                                               |
| float          | 78.9 ms                                                | 77.7 ms: 1.02x faster                                               |
| pidigits       | 194 ms                                                 | 198 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.06x faster                                                |
| regex_effbot   | 3.51 ms                                                | 3.82 ms: 1.09x slower                                               |
| regex_dna      | 205 ms                                                 | 226 ms: 1.11x slower                                                |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                               |
| Geometric mean | (ref)                                                  | 1.07x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.25x faster                                               |
| unpickle_pure_python | 242 us                                                 | 212 us: 1.14x faster                                                |
| tomli_loads          | 2.30 sec                                               | 2.09 sec: 1.10x faster                                              |
| pickle_pure_python   | 320 us                                                 | 298 us: 1.07x faster                                                |
| json_loads           | 29.2 us                                                | 27.9 us: 1.05x faster                                               |
| unpickle_list        | 5.21 us                                                | 5.07 us: 1.03x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                |
| pickle_dict          | 34.6 us                                                | 34.0 us: 1.02x faster                                               |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                               |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 86.9 ms: 1.07x slower                                               |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                               |
| unpickle             | 13.8 us                                                | 17.0 us: 1.23x slower                                               |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                               |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                               |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.4 ms: 1.02x faster                                               |
| mako            | 10.7 ms                                                | 10.8 ms: 1.01x slower                                               |
| django_template | 33.5 ms                                                | 34.4 ms: 1.03x slower                                               |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                               |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.53x faster                                                |
| generators                 | 74.9 ms                                                | 29.4 ms: 2.55x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                              |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 331 ms: 1.48x faster                                                |
| comprehensions             | 23.6 us                                                | 16.2 us: 1.46x faster                                               |
| async_tree_memoization_tg  | 626 ms                                                 | 438 ms: 1.43x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 908 ms: 1.43x faster                                                |
| async_tree_io              | 1.29 sec                                               | 916 ms: 1.40x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.25x faster                                               |
| deltablue                  | 3.92 ms                                                | 3.14 ms: 1.25x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                |
| chaos                      | 71.9 ms                                                | 59.5 ms: 1.21x faster                                               |
| raytrace                   | 309 ms                                                 | 259 ms: 1.19x faster                                                |
| richards_super             | 61.9 ms                                                | 52.2 ms: 1.19x faster                                               |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                               |
| logging_silent             | 111 ns                                                 | 96.2 ns: 1.15x faster                                               |
| unpickle_pure_python       | 242 us                                                 | 212 us: 1.14x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.27 ms: 1.13x faster                                               |
| hexiom                     | 6.89 ms                                                | 6.13 ms: 1.12x faster                                               |
| nbody                      | 96.0 ms                                                | 85.7 ms: 1.12x faster                                               |
| nqueens                    | 87.9 ms                                                | 79.6 ms: 1.10x faster                                               |
| tomli_loads                | 2.30 sec                                               | 2.09 sec: 1.10x faster                                              |
| logging_simple             | 6.22 us                                                | 5.64 us: 1.10x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                               |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                |
| logging_format             | 6.81 us                                                | 6.26 us: 1.09x faster                                               |
| mdp                        | 2.77 sec                                               | 2.56 sec: 1.08x faster                                              |
| deepcopy_memo              | 40.2 us                                                | 37.1 us: 1.08x faster                                               |
| richards                   | 49.8 ms                                                | 46.3 ms: 1.08x faster                                               |
| pickle_pure_python         | 320 us                                                 | 298 us: 1.07x faster                                                |
| djangocms                  | 33.5 us                                                | 31.3 us: 1.07x faster                                               |
| go                         | 149 ms                                                 | 140 ms: 1.06x faster                                                |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                |
| sympy_integrate            | 21.5 ms                                                | 20.2 ms: 1.06x faster                                               |
| regex_compile              | 141 ms                                                 | 134 ms: 1.06x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 67.3 ms: 1.05x faster                                               |
| json_loads                 | 29.2 us                                                | 27.9 us: 1.05x faster                                               |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                               |
| deepcopy                   | 365 us                                                 | 351 us: 1.04x faster                                                |
| tornado_http               | 98.1 ms                                                | 94.3 ms: 1.04x faster                                               |
| fannkuch                   | 405 ms                                                 | 391 ms: 1.04x faster                                                |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                                |
| unpickle_list              | 5.21 us                                                | 5.07 us: 1.03x faster                                               |
| crypto_pyaes               | 76.7 ms                                                | 74.8 ms: 1.03x faster                                               |
| genshi_xml                 | 53.4 ms                                                | 52.4 ms: 1.02x faster                                               |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                |
| pickle_dict                | 34.6 us                                                | 34.0 us: 1.02x faster                                               |
| deepcopy_reduce            | 3.22 us                                                | 3.16 us: 1.02x faster                                               |
| json                       | 5.24 ms                                                | 5.16 ms: 1.02x faster                                               |
| float                      | 78.9 ms                                                | 77.7 ms: 1.02x faster                                               |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                              |
| sqlglot_optimize           | 55.3 ms                                                | 54.7 ms: 1.01x faster                                               |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                |
| scimark_sor                | 121 ms                                                 | 120 ms: 1.01x faster                                                |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                |
| gc_traversal               | 4.01 ms                                                | 4.01 ms: 1.00x slower                                               |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.01x slower                                               |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.01x slower                                              |
| 2to3                       | 264 ms                                                 | 268 ms: 1.01x slower                                                |
| dulwich_log                | 64.6 ms                                                | 65.9 ms: 1.02x slower                                               |
| pidigits                   | 194 ms                                                 | 198 ms: 1.02x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                |
| spectral_norm              | 108 ms                                                 | 111 ms: 1.02x slower                                                |
| django_template            | 33.5 ms                                                | 34.4 ms: 1.03x slower                                               |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.17 ms: 1.03x slower                                               |
| chameleon                  | 6.70 ms                                                | 6.91 ms: 1.03x slower                                               |
| html5lib                   | 64.8 ms                                                | 67.5 ms: 1.04x slower                                               |
| thrift                     | 784 us                                                 | 818 us: 1.04x slower                                                |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                              |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                               |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                               |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                               |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                               |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                               |
| pyflate                    | 434 ms                                                 | 463 ms: 1.07x slower                                                |
| scimark_fft                | 345 ms                                                 | 369 ms: 1.07x slower                                                |
| xml_etree_generate         | 81.1 ms                                                | 86.9 ms: 1.07x slower                                               |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                               |
| regex_effbot               | 3.51 ms                                                | 3.82 ms: 1.09x slower                                               |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.11x slower                                                |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                               |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                               |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                               |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                               |
| coverage                   | 78.8 ms                                                | 96.4 ms: 1.22x slower                                               |
| unpickle                   | 13.8 us                                                | 17.0 us: 1.23x slower                                               |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                               |
| telco                      | 6.86 ms                                                | 8.69 ms: 1.27x slower                                               |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                        |

Benchmark hidden because not significant (5): xml_etree_iterparse, bench_mp_pool, bench_thread_pool, pprint_safe_repr, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.58% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x