# Results vs. 3.11.0

- fork: gvanrossum
- ref: backoff_counter_woes
- machine: linux-x86_64
- commit hash: 4c1049b
- commit date: 2024-05-04
- overall geometric mean: 1.05x faster
- HPT reliability: 95.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                       |
| chameleon      | 6.70 ms                                                | 7.15 ms: 1.07x slower                                                      |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                     |
| html5lib       | 64.8 ms                                                | 68.8 ms: 1.06x slower                                                      |
| tornado_http   | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 370 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 928 ms: 1.40x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 466 ms: 1.37x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 941 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 582 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 628 ms: 1.19x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.4 ms: 1.06x faster                                                      |
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                       |
| float          | 78.9 ms                                                | 78.5 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                       |
| regex_effbot   | 3.51 ms                                                | 3.79 ms: 1.08x slower                                                      |
| regex_dna      | 205 ms                                                 | 232 ms: 1.13x slower                                                       |
| regex_v8       | 22.9 ms                                                | 26.0 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                  | 1.08x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                      |
| unpickle_pure_python | 242 us                                                 | 225 us: 1.07x faster                                                       |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                     |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                                      |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.03x faster                                                       |
| pickle_pure_python   | 320 us                                                 | 314 us: 1.02x faster                                                       |
| unpickle_list        | 5.21 us                                                | 5.44 us: 1.04x slower                                                      |
| pickle_dict          | 34.6 us                                                | 36.4 us: 1.05x slower                                                      |
| xml_etree_process    | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                      |
| xml_etree_generate   | 81.1 ms                                                | 88.1 ms: 1.09x slower                                                      |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                                      |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                      |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.21 ms: 1.20x slower                                                      |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.2 ms: 1.02x faster                                                      |
| mako            | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                      |
| genshi_text     | 22.5 ms                                                | 22.8 ms: 1.01x slower                                                      |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 168 us: 3.10x faster                                                       |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.56x faster                                                      |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                     |
| pylint                     | 476 ms                                                 | 322 ms: 1.48x faster                                                       |
| async_tree_none            | 528 ms                                                 | 370 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                       |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                       |
| async_tree_io_tg           | 1.29 sec                                               | 928 ms: 1.40x faster                                                       |
| async_tree_memoization     | 639 ms                                                 | 466 ms: 1.37x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 941 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 582 ms: 1.31x faster                                                       |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                      |
| chaos                      | 71.9 ms                                                | 58.9 ms: 1.22x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 628 ms: 1.19x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.29 ms: 1.19x faster                                                      |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                       |
| coroutines                 | 27.0 ms                                                | 23.5 ms: 1.15x faster                                                      |
| hexiom                     | 6.89 ms                                                | 6.18 ms: 1.12x faster                                                      |
| richards_super             | 61.9 ms                                                | 56.4 ms: 1.10x faster                                                      |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                       |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                      |
| unpickle_pure_python       | 242 us                                                 | 225 us: 1.07x faster                                                       |
| logging_simple             | 6.22 us                                                | 5.82 us: 1.07x faster                                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.06x faster                                                      |
| nbody                      | 96.0 ms                                                | 90.4 ms: 1.06x faster                                                      |
| pathlib                    | 18.5 ms                                                | 17.5 ms: 1.06x faster                                                      |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                     |
| logging_format             | 6.81 us                                                | 6.46 us: 1.05x faster                                                      |
| nqueens                    | 87.9 ms                                                | 83.4 ms: 1.05x faster                                                      |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                                      |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                                      |
| sympy_str                  | 297 ms                                                 | 283 ms: 1.05x faster                                                       |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                      |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                                     |
| tornado_http               | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                      |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.03x faster                                                       |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                       |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                       |
| genshi_xml                 | 53.4 ms                                                | 52.2 ms: 1.02x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 314 us: 1.02x faster                                                       |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 69.6 ms: 1.02x faster                                                      |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                       |
| sympy_expand               | 484 ms                                                 | 477 ms: 1.01x faster                                                       |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                                       |
| deepcopy                   | 365 us                                                 | 363 us: 1.01x faster                                                       |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                       |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                      |
| float                      | 78.9 ms                                                | 78.5 ms: 1.01x faster                                                      |
| pprint_pformat             | 1.55 sec                                               | 1.55 sec: 1.01x faster                                                     |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.00x faster                                                       |
| gc_traversal               | 4.01 ms                                                | 3.99 ms: 1.00x faster                                                      |
| sqlglot_optimize           | 55.3 ms                                                | 55.5 ms: 1.00x slower                                                      |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                                      |
| pprint_safe_repr           | 747 ms                                                 | 755 ms: 1.01x slower                                                       |
| richards                   | 49.8 ms                                                | 50.4 ms: 1.01x slower                                                      |
| json                       | 5.24 ms                                                | 5.31 ms: 1.01x slower                                                      |
| genshi_text                | 22.5 ms                                                | 22.8 ms: 1.01x slower                                                      |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                                       |
| spectral_norm              | 108 ms                                                 | 110 ms: 1.02x slower                                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.29 us: 1.02x slower                                                      |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                       |
| dulwich_log                | 64.6 ms                                                | 66.6 ms: 1.03x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 120 ms: 1.03x slower                                                       |
| unpickle_list              | 5.21 us                                                | 5.44 us: 1.04x slower                                                      |
| thrift                     | 784 us                                                 | 818 us: 1.04x slower                                                       |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.29 ms: 1.05x slower                                                      |
| pickle_dict                | 34.6 us                                                | 36.4 us: 1.05x slower                                                      |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.06x slower                                                       |
| html5lib                   | 64.8 ms                                                | 68.8 ms: 1.06x slower                                                      |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                     |
| aiohttp                    | 1.12 ms                                                | 1.19 ms: 1.07x slower                                                      |
| chameleon                  | 6.70 ms                                                | 7.15 ms: 1.07x slower                                                      |
| xml_etree_process          | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                      |
| gunicorn                   | 1.20 ms                                                | 1.29 ms: 1.07x slower                                                      |
| scimark_fft                | 345 ms                                                 | 372 ms: 1.08x slower                                                       |
| regex_effbot               | 3.51 ms                                                | 3.79 ms: 1.08x slower                                                      |
| mypy2                      | 686 ms                                                 | 744 ms: 1.08x slower                                                       |
| xml_etree_generate         | 81.1 ms                                                | 88.1 ms: 1.09x slower                                                      |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                                      |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                                       |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                      |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                      |
| sqlite_synth               | 2.57 us                                                | 2.90 us: 1.13x slower                                                      |
| regex_dna                  | 205 ms                                                 | 232 ms: 1.13x slower                                                       |
| regex_v8                   | 22.9 ms                                                | 26.0 ms: 1.14x slower                                                      |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.21 ms: 1.20x slower                                                      |
| coverage                   | 78.8 ms                                                | 94.7 ms: 1.20x slower                                                      |
| flaskblogging              | 7.28 ms                                                | 9.02 ms: 1.24x slower                                                      |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                      |
| telco                      | 6.86 ms                                                | 8.60 ms: 1.25x slower                                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.84 ms: 1.29x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                               |

Benchmark hidden because not significant (4): xml_etree_iterparse, bench_thread_pool, deepcopy_memo, crypto_pyaes
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 95.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x