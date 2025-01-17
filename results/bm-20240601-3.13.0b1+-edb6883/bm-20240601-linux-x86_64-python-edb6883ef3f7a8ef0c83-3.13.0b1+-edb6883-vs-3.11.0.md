# Results vs. 3.11.0

- fork: python
- ref: edb6883ef3f7a8ef0c83
- machine: linux-x86_64
- commit hash: edb6883
- commit date: 2024-06-01
- overall geometric mean: 1.06x faster
- HPT reliability: 98.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                   |
| chameleon      | 6.70 ms                                                | 6.89 ms: 1.03x slower                                                  |
| docutils       | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                 |
| html5lib       | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                  |
| tornado_http   | 98.1 ms                                                | 93.8 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                   |
| async_tree_none            | 528 ms                                                 | 371 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                   |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 939 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.1 ms: 1.07x faster                                                  |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| float          | 78.9 ms                                                | 78.7 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                   |
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                  |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                   |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                                   |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                 |
| pickle_dict          | 34.6 us                                                | 33.5 us: 1.03x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                   |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                  |
| unpickle             | 13.8 us                                                | 14.6 us: 1.06x slower                                                  |
| xml_etree_process    | 56.9 ms                                                | 60.4 ms: 1.06x slower                                                  |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                  |
| xml_etree_generate   | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                  |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                  |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.5 ms: 1.06x faster                                                  |
| mako            | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                  |
| genshi_text     | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                  |
| django_template | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-linux-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 164 us: 3.16x faster                                                   |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.56x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                 |
| pylint                     | 476 ms                                                 | 315 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                   |
| async_tree_none            | 528 ms                                                 | 371 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 939 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                                   |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.28 ms: 1.20x faster                                                  |
| chaos                      | 71.9 ms                                                | 60.2 ms: 1.19x faster                                                  |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                  |
| raytrace                   | 309 ms                                                 | 271 ms: 1.14x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                                   |
| nqueens                    | 87.9 ms                                                | 79.5 ms: 1.11x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.25 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                   |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.56 sec: 1.08x faster                                                 |
| richards_super             | 61.9 ms                                                | 57.2 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                  |
| djangocms                  | 33.5 us                                                | 31.4 us: 1.07x faster                                                  |
| logging_format             | 6.81 us                                                | 6.38 us: 1.07x faster                                                  |
| nbody                      | 96.0 ms                                                | 90.1 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                   |
| genshi_xml                 | 53.4 ms                                                | 50.5 ms: 1.06x faster                                                  |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                 |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                  |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                                  |
| tornado_http               | 98.1 ms                                                | 93.8 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 67.8 ms: 1.04x faster                                                  |
| gc_traversal               | 4.01 ms                                                | 3.85 ms: 1.04x faster                                                  |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                   |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                  |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                 |
| pickle_dict                | 34.6 us                                                | 33.5 us: 1.03x faster                                                  |
| crypto_pyaes               | 76.7 ms                                                | 74.4 ms: 1.03x faster                                                  |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                   |
| fannkuch                   | 405 ms                                                 | 395 ms: 1.03x faster                                                   |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                 |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                   |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                   |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 741 ms: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 55.1 ms: 1.00x faster                                                  |
| float                      | 78.9 ms                                                | 78.7 ms: 1.00x faster                                                  |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 117 ms: 1.01x slower                                                   |
| json                       | 5.24 ms                                                | 5.29 ms: 1.01x slower                                                  |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                  |
| richards                   | 49.8 ms                                                | 50.7 ms: 1.02x slower                                                  |
| genshi_text                | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                  |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                   |
| django_template            | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                  |
| dulwich_log                | 64.6 ms                                                | 66.4 ms: 1.03x slower                                                  |
| chameleon                  | 6.70 ms                                                | 6.89 ms: 1.03x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.19 ms: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                  |
| html5lib                   | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                  |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                                   |
| unpickle                   | 13.8 us                                                | 14.6 us: 1.06x slower                                                  |
| aiohttp                    | 1.12 ms                                                | 1.18 ms: 1.06x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 60.4 ms: 1.06x slower                                                  |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                  |
| gunicorn                   | 1.20 ms                                                | 1.28 ms: 1.06x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                  |
| docutils                   | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                 |
| mypy2                      | 686 ms                                                 | 734 ms: 1.07x slower                                                   |
| pyflate                    | 434 ms                                                 | 468 ms: 1.08x slower                                                   |
| scimark_fft                | 345 ms                                                 | 375 ms: 1.09x slower                                                   |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                                   |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                                  |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.12x slower                                                  |
| sqlite_synth               | 2.57 us                                                | 3.01 us: 1.17x slower                                                  |
| coverage                   | 78.8 ms                                                | 92.6 ms: 1.18x slower                                                  |
| async_generators           | 374 ms                                                 | 440 ms: 1.18x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                  |
| flaskblogging              | 7.28 ms                                                | 8.93 ms: 1.23x slower                                                  |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                  |
| telco                      | 6.86 ms                                                | 8.62 ms: 1.26x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_list, bench_thread_pool, dask
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.81% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x