# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: linux-x86_64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.05x faster
- HPT reliability: 84.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 274 ms: 1.04x slower                                       |
| chameleon      | 6.70 ms                                                | 7.22 ms: 1.08x slower                                      |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                     |
| html5lib       | 64.8 ms                                                | 67.2 ms: 1.04x slower                                      |
| tornado_http   | 98.1 ms                                                | 94.6 ms: 1.04x faster                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                       |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                       |
| async_tree_io              | 1.29 sec                                               | 939 ms: 1.37x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                       |
| Geometric mean             | (ref)                                                  | 1.36x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.3 ms: 1.09x faster                                      |
| pidigits       | 194 ms                                                 | 191 ms: 1.01x faster                                       |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                      |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                       |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                      |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                       |
| tomli_loads          | 2.30 sec                                               | 2.12 sec: 1.09x faster                                     |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                       |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                       |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                      |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                      |
| unpickle_list        | 5.21 us                                                | 5.34 us: 1.02x slower                                      |
| pickle               | 11.0 us                                                | 11.5 us: 1.04x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 61.2 ms: 1.08x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 87.4 ms: 1.08x slower                                      |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                      |
| pickle_list          | 4.59 us                                                | 5.11 us: 1.11x slower                                      |
| Geometric mean       | (ref)                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                      |
| python_startup         | 8.56 ms                                                | 10.8 ms: 1.26x slower                                      |
| Geometric mean         | (ref)                                                  | 1.22x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.6 ms: 1.04x faster                                      |
| django_template | 33.5 ms                                                | 34.8 ms: 1.04x slower                                      |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                      |
| mako            | 10.7 ms                                                | 11.2 ms: 1.05x slower                                      |
| Geometric mean  | (ref)                                                  | 1.03x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                       |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                     |
| pylint                     | 476 ms                                                 | 317 ms: 1.50x faster                                       |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                       |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                       |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                       |
| async_tree_io              | 1.29 sec                                               | 939 ms: 1.37x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                       |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                       |
| deltablue                  | 3.92 ms                                                | 3.25 ms: 1.21x faster                                      |
| chaos                      | 71.9 ms                                                | 61.3 ms: 1.17x faster                                      |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                      |
| raytrace                   | 309 ms                                                 | 267 ms: 1.16x faster                                       |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                       |
| hexiom                     | 6.89 ms                                                | 6.30 ms: 1.09x faster                                      |
| nbody                      | 96.0 ms                                                | 88.3 ms: 1.09x faster                                      |
| tomli_loads                | 2.30 sec                                               | 2.12 sec: 1.09x faster                                     |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                      |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                       |
| logging_simple             | 6.22 us                                                | 5.74 us: 1.08x faster                                      |
| nqueens                    | 87.9 ms                                                | 81.4 ms: 1.08x faster                                      |
| richards_super             | 61.9 ms                                                | 57.4 ms: 1.08x faster                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                      |
| pathlib                    | 18.5 ms                                                | 17.3 ms: 1.07x faster                                      |
| djangocms                  | 33.5 us                                                | 31.5 us: 1.06x faster                                      |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                       |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                       |
| logging_format             | 6.81 us                                                | 6.47 us: 1.05x faster                                      |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                       |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                      |
| tornado_http               | 98.1 ms                                                | 94.6 ms: 1.04x faster                                      |
| genshi_xml                 | 53.4 ms                                                | 51.6 ms: 1.04x faster                                      |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                       |
| go                         | 149 ms                                                 | 145 ms: 1.03x faster                                       |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.03x faster                                       |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                     |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 69.2 ms: 1.02x faster                                      |
| pidigits                   | 194 ms                                                 | 191 ms: 1.01x faster                                       |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                       |
| deepcopy_memo              | 40.2 us                                                | 39.7 us: 1.01x faster                                      |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                      |
| fannkuch                   | 405 ms                                                 | 402 ms: 1.01x faster                                       |
| gc_traversal               | 4.01 ms                                                | 3.98 ms: 1.01x faster                                      |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                      |
| sqlglot_optimize           | 55.3 ms                                                | 55.5 ms: 1.00x slower                                      |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.00x slower                                     |
| deepcopy                   | 365 us                                                 | 367 us: 1.01x slower                                       |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                      |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                       |
| crypto_pyaes               | 76.7 ms                                                | 77.5 ms: 1.01x slower                                      |
| dask                       | 365 ms                                                 | 369 ms: 1.01x slower                                       |
| json                       | 5.24 ms                                                | 5.31 ms: 1.01x slower                                      |
| pprint_safe_repr           | 747 ms                                                 | 758 ms: 1.01x slower                                       |
| richards                   | 49.8 ms                                                | 50.9 ms: 1.02x slower                                      |
| unpickle_list              | 5.21 us                                                | 5.34 us: 1.02x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                       |
| 2to3                       | 264 ms                                                 | 274 ms: 1.04x slower                                       |
| html5lib                   | 64.8 ms                                                | 67.2 ms: 1.04x slower                                      |
| django_template            | 33.5 ms                                                | 34.8 ms: 1.04x slower                                      |
| dulwich_log                | 64.6 ms                                                | 67.2 ms: 1.04x slower                                      |
| deepcopy_reduce            | 3.22 us                                                | 3.35 us: 1.04x slower                                      |
| pickle                     | 11.0 us                                                | 11.5 us: 1.04x slower                                      |
| scimark_lu                 | 116 ms                                                 | 122 ms: 1.05x slower                                       |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.27 ms: 1.05x slower                                      |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                       |
| scimark_sor                | 121 ms                                                 | 127 ms: 1.05x slower                                       |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                      |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.18 ms: 1.06x slower                                      |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                     |
| gunicorn                   | 1.20 ms                                                | 1.28 ms: 1.07x slower                                      |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                       |
| xml_etree_process          | 56.9 ms                                                | 61.2 ms: 1.08x slower                                      |
| chameleon                  | 6.70 ms                                                | 7.22 ms: 1.08x slower                                      |
| xml_etree_generate         | 81.1 ms                                                | 87.4 ms: 1.08x slower                                      |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                       |
| mypy2                      | 686 ms                                                 | 742 ms: 1.08x slower                                       |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                      |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                      |
| pickle_list                | 4.59 us                                                | 5.11 us: 1.11x slower                                      |
| pyflate                    | 434 ms                                                 | 484 ms: 1.12x slower                                       |
| scimark_fft                | 345 ms                                                 | 392 ms: 1.14x slower                                       |
| sqlite_synth               | 2.57 us                                                | 2.99 us: 1.16x slower                                      |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                      |
| coverage                   | 78.8 ms                                                | 93.1 ms: 1.18x slower                                      |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                       |
| telco                      | 6.86 ms                                                | 8.41 ms: 1.23x slower                                      |
| flaskblogging              | 7.28 ms                                                | 9.01 ms: 1.24x slower                                      |
| python_startup             | 8.56 ms                                                | 10.8 ms: 1.26x slower                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (4): xml_etree_iterparse, bench_thread_pool, float, pprint_pformat
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 84.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x