# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: linux-x86_64
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.05x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                       |
| chameleon      | 6.70 ms                                                | 6.85 ms: 1.02x slower                                      |
| docutils       | 2.66 sec                                               | 2.65 sec: 1.01x faster                                     |
| html5lib       | 64.8 ms                                                | 67.4 ms: 1.04x slower                                      |
| tornado_http   | 98.1 ms                                                | 97.1 ms: 1.01x faster                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 444 ms: 1.19x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 571 ms: 1.12x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 455 ms: 1.08x faster                                       |
| async_tree_io              | 1.29 sec                                               | 1.20 sec: 1.07x faster                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 585 ms: 1.07x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 1.22 sec: 1.06x faster                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 718 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 733 ms: 1.04x faster                                       |
| Geometric mean             | (ref)                                                  | 1.08x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.1 ms: 1.04x faster                                      |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                       |
| float          | 78.9 ms                                                | 83.1 ms: 1.05x slower                                      |
| Geometric mean | (ref)                                                  | 1.00x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 132 ms: 1.07x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.66 ms: 1.04x slower                                      |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                      |
| regex_dna      | 205 ms                                                 | 224 ms: 1.09x slower                                       |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.28x faster                                      |
| unpickle_pure_python | 242 us                                                 | 217 us: 1.12x faster                                       |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.20 sec: 1.05x faster                                     |
| json_loads           | 29.2 us                                                | 27.9 us: 1.04x faster                                      |
| unpickle_list        | 5.21 us                                                | 5.09 us: 1.02x faster                                      |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                       |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                       |
| pickle_dict          | 34.6 us                                                | 34.7 us: 1.00x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 59.3 ms: 1.04x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 86.9 ms: 1.07x slower                                      |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                      |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                      |
| pickle_list          | 4.59 us                                                | 5.28 us: 1.15x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.3 ms: 1.20x slower                                      |
| python_startup_no_site | 6.01 ms                                                | 8.87 ms: 1.48x slower                                      |
| Geometric mean         | (ref)                                                  | 1.33x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.8 ms: 1.01x faster                                      |
| genshi_text     | 22.5 ms                                                | 23.0 ms: 1.02x slower                                      |
| django_template | 33.5 ms                                                | 34.7 ms: 1.03x slower                                      |
| mako            | 10.7 ms                                                | 11.2 ms: 1.05x slower                                      |
| Geometric mean  | (ref)                                                  | 1.02x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-linux-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.65x faster                                       |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 501 ms: 1.75x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                     |
| pylint                     | 476 ms                                                 | 310 ms: 1.53x faster                                       |
| comprehensions             | 23.6 us                                                | 16.2 us: 1.46x faster                                      |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                      |
| deltablue                  | 3.92 ms                                                | 3.24 ms: 1.21x faster                                      |
| async_tree_none            | 528 ms                                                 | 444 ms: 1.19x faster                                       |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.18x faster                                      |
| chaos                      | 71.9 ms                                                | 61.2 ms: 1.17x faster                                      |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                       |
| richards_super             | 61.9 ms                                                | 54.1 ms: 1.14x faster                                      |
| logging_silent             | 111 ns                                                 | 97.7 ns: 1.14x faster                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.26 ms: 1.14x faster                                      |
| gc_traversal               | 4.01 ms                                                | 3.55 ms: 1.13x faster                                      |
| sympy_sum                  | 169 ms                                                 | 150 ms: 1.12x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 571 ms: 1.12x faster                                       |
| unpickle_pure_python       | 242 us                                                 | 217 us: 1.12x faster                                       |
| hexiom                     | 6.89 ms                                                | 6.20 ms: 1.11x faster                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.58 ms: 1.10x faster                                      |
| nqueens                    | 87.9 ms                                                | 81.0 ms: 1.09x faster                                      |
| sympy_str                  | 297 ms                                                 | 274 ms: 1.08x faster                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.64 ms: 1.08x faster                                      |
| async_tree_none_tg         | 491 ms                                                 | 455 ms: 1.08x faster                                       |
| sympy_integrate            | 21.5 ms                                                | 19.9 ms: 1.08x faster                                      |
| regex_compile              | 141 ms                                                 | 132 ms: 1.07x faster                                       |
| async_tree_io              | 1.29 sec                                               | 1.20 sec: 1.07x faster                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 585 ms: 1.07x faster                                       |
| logging_simple             | 6.22 us                                                | 5.83 us: 1.07x faster                                      |
| go                         | 149 ms                                                 | 139 ms: 1.07x faster                                       |
| crypto_pyaes               | 76.7 ms                                                | 72.0 ms: 1.06x faster                                      |
| djangocms                  | 33.5 us                                                | 31.5 us: 1.06x faster                                      |
| mdp                        | 2.77 sec                                               | 2.61 sec: 1.06x faster                                     |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                       |
| deepcopy_memo              | 40.2 us                                                | 37.9 us: 1.06x faster                                      |
| async_tree_io_tg           | 1.29 sec                                               | 1.22 sec: 1.06x faster                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 67.2 ms: 1.05x faster                                      |
| deepcopy                   | 365 us                                                 | 347 us: 1.05x faster                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.06 us: 1.05x faster                                      |
| tomli_loads                | 2.30 sec                                               | 2.20 sec: 1.05x faster                                     |
| sympy_expand               | 484 ms                                                 | 462 ms: 1.05x faster                                       |
| json_loads                 | 29.2 us                                                | 27.9 us: 1.04x faster                                      |
| sqlglot_normalize          | 113 ms                                                 | 108 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 718 ms: 1.04x faster                                       |
| logging_format             | 6.81 us                                                | 6.53 us: 1.04x faster                                      |
| nbody                      | 96.0 ms                                                | 92.1 ms: 1.04x faster                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 733 ms: 1.04x faster                                       |
| richards                   | 49.8 ms                                                | 48.1 ms: 1.03x faster                                      |
| scimark_lu                 | 116 ms                                                 | 113 ms: 1.03x faster                                       |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                     |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                       |
| unpickle_list              | 5.21 us                                                | 5.09 us: 1.02x faster                                      |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                       |
| sqlglot_optimize           | 55.3 ms                                                | 54.2 ms: 1.02x faster                                      |
| pprint_safe_repr           | 747 ms                                                 | 734 ms: 1.02x faster                                       |
| genshi_xml                 | 53.4 ms                                                | 52.8 ms: 1.01x faster                                      |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                       |
| tornado_http               | 98.1 ms                                                | 97.1 ms: 1.01x faster                                      |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                       |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                      |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                       |
| docutils                   | 2.66 sec                                               | 2.65 sec: 1.01x faster                                     |
| bench_thread_pool          | 834 us                                                 | 838 us: 1.00x slower                                       |
| pickle_dict                | 34.6 us                                                | 34.7 us: 1.00x slower                                      |
| pathlib                    | 18.5 ms                                                | 18.7 ms: 1.01x slower                                      |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                       |
| genshi_text                | 22.5 ms                                                | 23.0 ms: 1.02x slower                                      |
| chameleon                  | 6.70 ms                                                | 6.85 ms: 1.02x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                       |
| spectral_norm              | 108 ms                                                 | 111 ms: 1.02x slower                                       |
| thrift                     | 784 us                                                 | 807 us: 1.03x slower                                       |
| django_template            | 33.5 ms                                                | 34.7 ms: 1.03x slower                                      |
| pycparser                  | 1.19 sec                                               | 1.23 sec: 1.03x slower                                     |
| dulwich_log                | 64.6 ms                                                | 67.0 ms: 1.04x slower                                      |
| scimark_fft                | 345 ms                                                 | 359 ms: 1.04x slower                                       |
| html5lib                   | 64.8 ms                                                | 67.4 ms: 1.04x slower                                      |
| xml_etree_process          | 56.9 ms                                                | 59.3 ms: 1.04x slower                                      |
| regex_effbot               | 3.51 ms                                                | 3.66 ms: 1.04x slower                                      |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                      |
| float                      | 78.9 ms                                                | 83.1 ms: 1.05x slower                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.51 ms: 1.05x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                      |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                       |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                      |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                      |
| xml_etree_generate         | 81.1 ms                                                | 86.9 ms: 1.07x slower                                      |
| pyflate                    | 434 ms                                                 | 474 ms: 1.09x slower                                       |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                      |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.09x slower                                       |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                      |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.12x slower                                      |
| pickle_list                | 4.59 us                                                | 5.28 us: 1.15x slower                                      |
| flaskblogging              | 7.28 ms                                                | 8.75 ms: 1.20x slower                                      |
| python_startup             | 8.56 ms                                                | 10.3 ms: 1.20x slower                                      |
| coverage                   | 78.8 ms                                                | 96.3 ms: 1.22x slower                                      |
| telco                      | 6.86 ms                                                | 8.41 ms: 1.23x slower                                      |
| async_generators           | 374 ms                                                 | 459 ms: 1.23x slower                                       |
| mypy2                      | 686 ms                                                 | 865 ms: 1.26x slower                                       |
| python_startup_no_site     | 6.01 ms                                                | 8.87 ms: 1.48x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (1): json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x