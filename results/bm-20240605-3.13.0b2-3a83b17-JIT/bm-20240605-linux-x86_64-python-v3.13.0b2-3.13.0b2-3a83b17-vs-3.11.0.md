# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: linux-x86_64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.06x faster
- HPT reliability: 94.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.06x slower                                       |
| chameleon      | 6.70 ms                                                | 7.11 ms: 1.06x slower                                      |
| docutils       | 2.66 sec                                               | 2.99 sec: 1.12x slower                                     |
| html5lib       | 64.8 ms                                                | 69.1 ms: 1.07x slower                                      |
| tornado_http   | 98.1 ms                                                | 96.9 ms: 1.01x faster                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                       |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                       |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                       |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 945 ms: 1.37x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                       |
| Geometric mean             | (ref)                                                  | 1.37x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 83.5 ms: 1.15x faster                                      |
| float          | 78.9 ms                                                | 73.0 ms: 1.08x faster                                      |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                       |
| Geometric mean | (ref)                                                  | 1.09x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                       |
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                      |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                      |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                       |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.29x faster                                      |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                     |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                       |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                       |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                       |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                       |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                      |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                      |
| unpickle_list        | 5.21 us                                                | 5.26 us: 1.01x slower                                      |
| xml_etree_generate   | 81.1 ms                                                | 82.9 ms: 1.02x slower                                      |
| xml_etree_process    | 56.9 ms                                                | 58.5 ms: 1.03x slower                                      |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                      |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                      |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                      |
| Geometric mean       | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.62 ms: 1.27x slower                                      |
| python_startup         | 8.56 ms                                                | 11.3 ms: 1.32x slower                                      |
| Geometric mean         | (ref)                                                  | 1.29x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.83 ms: 1.08x faster                                      |
| django_template | 33.5 ms                                                | 36.4 ms: 1.08x slower                                      |
| genshi_xml      | 53.4 ms                                                | 60.2 ms: 1.13x slower                                      |
| genshi_text     | 22.5 ms                                                | 25.5 ms: 1.13x slower                                      |
| Geometric mean  | (ref)                                                  | 1.06x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.01x faster                                       |
| generators                 | 74.9 ms                                                | 33.5 ms: 2.23x faster                                      |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                       |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                     |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                       |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                      |
| async_tree_memoization     | 639 ms                                                 | 456 ms: 1.40x faster                                       |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                       |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                       |
| async_tree_io_tg           | 1.29 sec                                               | 945 ms: 1.37x faster                                       |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                       |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.29x faster                                      |
| richards_super             | 61.9 ms                                                | 48.4 ms: 1.28x faster                                      |
| chaos                      | 71.9 ms                                                | 58.5 ms: 1.23x faster                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                       |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                      |
| richards                   | 49.8 ms                                                | 41.7 ms: 1.19x faster                                      |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                     |
| nbody                      | 96.0 ms                                                | 83.5 ms: 1.15x faster                                      |
| fannkuch                   | 405 ms                                                 | 358 ms: 1.13x faster                                       |
| crypto_pyaes               | 76.7 ms                                                | 68.0 ms: 1.13x faster                                      |
| scimark_monte_carlo        | 70.7 ms                                                | 62.7 ms: 1.13x faster                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.48 ms: 1.12x faster                                      |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.11x faster                                      |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                       |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                       |
| logging_simple             | 6.22 us                                                | 5.70 us: 1.09x faster                                      |
| scimark_fft                | 345 ms                                                 | 317 ms: 1.09x faster                                       |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                       |
| mako                       | 10.7 ms                                                | 9.83 ms: 1.08x faster                                      |
| float                      | 78.9 ms                                                | 73.0 ms: 1.08x faster                                      |
| logging_format             | 6.81 us                                                | 6.30 us: 1.08x faster                                      |
| deepcopy_memo              | 40.2 us                                                | 37.3 us: 1.08x faster                                      |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.08x faster                                      |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                     |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                       |
| pathlib                    | 18.5 ms                                                | 17.4 ms: 1.06x faster                                      |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                       |
| deltablue                  | 3.92 ms                                                | 3.70 ms: 1.06x faster                                      |
| spectral_norm              | 108 ms                                                 | 102 ms: 1.06x faster                                       |
| mdp                        | 2.77 sec                                               | 2.62 sec: 1.06x faster                                     |
| pprint_safe_repr           | 747 ms                                                 | 715 ms: 1.05x faster                                       |
| gc_traversal               | 4.01 ms                                                | 3.88 ms: 1.03x faster                                      |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                       |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                       |
| hexiom                     | 6.89 ms                                                | 6.67 ms: 1.03x faster                                      |
| djangocms                  | 33.5 us                                                | 32.8 us: 1.02x faster                                      |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                       |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                     |
| nqueens                    | 87.9 ms                                                | 86.5 ms: 1.02x faster                                      |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                      |
| tornado_http               | 98.1 ms                                                | 96.9 ms: 1.01x faster                                      |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                      |
| pyflate                    | 434 ms                                                 | 436 ms: 1.01x slower                                       |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                      |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                       |
| unpickle_list              | 5.21 us                                                | 5.26 us: 1.01x slower                                      |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.01x slower                                       |
| go                         | 149 ms                                                 | 151 ms: 1.02x slower                                       |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                       |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                       |
| json                       | 5.24 ms                                                | 5.34 ms: 1.02x slower                                      |
| xml_etree_generate         | 81.1 ms                                                | 82.9 ms: 1.02x slower                                      |
| deepcopy                   | 365 us                                                 | 375 us: 1.03x slower                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.30 us: 1.03x slower                                      |
| xml_etree_process          | 56.9 ms                                                | 58.5 ms: 1.03x slower                                      |
| sqlglot_optimize           | 55.3 ms                                                | 56.8 ms: 1.03x slower                                      |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                       |
| dask                       | 365 ms                                                 | 377 ms: 1.03x slower                                       |
| bench_thread_pool          | 834 us                                                 | 867 us: 1.04x slower                                       |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                      |
| sympy_expand               | 484 ms                                                 | 510 ms: 1.05x slower                                       |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                      |
| thrift                     | 784 us                                                 | 826 us: 1.05x slower                                       |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.06x slower                                       |
| chameleon                  | 6.70 ms                                                | 7.11 ms: 1.06x slower                                      |
| 2to3                       | 264 ms                                                 | 281 ms: 1.06x slower                                       |
| html5lib                   | 64.8 ms                                                | 69.1 ms: 1.07x slower                                      |
| dulwich_log                | 64.6 ms                                                | 69.7 ms: 1.08x slower                                      |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                      |
| django_template            | 33.5 ms                                                | 36.4 ms: 1.08x slower                                      |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                      |
| scimark_lu                 | 116 ms                                                 | 127 ms: 1.10x slower                                       |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                      |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                      |
| sqlite_synth               | 2.57 us                                                | 2.88 us: 1.12x slower                                      |
| gunicorn                   | 1.20 ms                                                | 1.34 ms: 1.12x slower                                      |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.12x slower                                      |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                       |
| docutils                   | 2.66 sec                                               | 2.99 sec: 1.12x slower                                     |
| genshi_xml                 | 53.4 ms                                                | 60.2 ms: 1.13x slower                                      |
| genshi_text                | 22.5 ms                                                | 25.5 ms: 1.13x slower                                      |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                      |
| telco                      | 6.86 ms                                                | 8.12 ms: 1.18x slower                                      |
| mypy2                      | 686 ms                                                 | 814 ms: 1.19x slower                                       |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.62 ms: 1.27x slower                                      |
| flaskblogging              | 7.28 ms                                                | 9.27 ms: 1.27x slower                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.83 ms: 1.28x slower                                      |
| python_startup             | 8.56 ms                                                | 11.3 ms: 1.32x slower                                      |
| Geometric mean             | (ref)                                                  | 1.06x faster                                               |
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17-JIT/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 94.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x