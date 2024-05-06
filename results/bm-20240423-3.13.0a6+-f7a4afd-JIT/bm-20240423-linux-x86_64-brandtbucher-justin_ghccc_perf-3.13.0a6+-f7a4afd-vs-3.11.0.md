# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_perf
- machine: linux-x86_64
- commit hash: f7a4afd
- commit date: 2024-04-23
- overall geometric mean: 1.07x faster
- HPT reliability: 96.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                      |
| chameleon      | 6.70 ms                                                | 7.00 ms: 1.05x slower                                                     |
| docutils       | 2.66 sec                                               | 2.91 sec: 1.09x slower                                                    |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                     |
| tornado_http   | 98.1 ms                                                | 95.7 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 360 ms: 1.47x faster                                                      |
| async_tree_none_tg         | 491 ms                                                 | 340 ms: 1.45x faster                                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                      |
| async_tree_memoization     | 639 ms                                                 | 458 ms: 1.39x faster                                                      |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                                      |
| async_tree_io_tg           | 1.29 sec                                               | 949 ms: 1.36x faster                                                      |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                      |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 618 ms: 1.21x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 82.4 ms: 1.16x faster                                                     |
| float          | 78.9 ms                                                | 74.9 ms: 1.05x faster                                                     |
| pidigits       | 194 ms                                                 | 192 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                  | 1.07x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                      |
| regex_v8       | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                     |
| regex_effbot   | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                     |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                     |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.18x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                      |
| unpickle_pure_python | 242 us                                                 | 227 us: 1.07x faster                                                      |
| xml_etree_iterparse  | 108 ms                                                 | 103 ms: 1.05x faster                                                      |
| pickle_pure_python   | 320 us                                                 | 307 us: 1.04x faster                                                      |
| json_loads           | 29.2 us                                                | 28.3 us: 1.03x faster                                                     |
| unpickle_list        | 5.21 us                                                | 5.18 us: 1.01x faster                                                     |
| pickle_dict          | 34.6 us                                                | 34.4 us: 1.01x faster                                                     |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                     |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                     |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                     |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                     |
| pickle_list          | 4.59 us                                                | 5.17 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.60 ms: 1.26x slower                                                     |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                     |
| genshi_xml      | 53.4 ms                                                | 54.5 ms: 1.02x slower                                                     |
| genshi_text     | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                     |
| django_template | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.65x faster                                                      |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                     |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.71x faster                                                      |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                    |
| async_tree_none            | 528 ms                                                 | 360 ms: 1.47x faster                                                      |
| async_tree_none_tg         | 491 ms                                                 | 340 ms: 1.45x faster                                                      |
| pylint                     | 476 ms                                                 | 335 ms: 1.42x faster                                                      |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                      |
| async_tree_memoization     | 639 ms                                                 | 458 ms: 1.39x faster                                                      |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                                      |
| comprehensions             | 23.6 us                                                | 17.1 us: 1.38x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 949 ms: 1.36x faster                                                      |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                     |
| richards_super             | 61.9 ms                                                | 48.9 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                      |
| coroutines                 | 27.0 ms                                                | 22.2 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 618 ms: 1.21x faster                                                      |
| chaos                      | 71.9 ms                                                | 60.7 ms: 1.18x faster                                                     |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.18x faster                                                    |
| richards                   | 49.8 ms                                                | 42.3 ms: 1.18x faster                                                     |
| nbody                      | 96.0 ms                                                | 82.4 ms: 1.16x faster                                                     |
| raytrace                   | 309 ms                                                 | 272 ms: 1.13x faster                                                      |
| fannkuch                   | 405 ms                                                 | 364 ms: 1.11x faster                                                      |
| spectral_norm              | 108 ms                                                 | 97.8 ms: 1.11x faster                                                     |
| crypto_pyaes               | 76.7 ms                                                | 69.6 ms: 1.10x faster                                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 64.2 ms: 1.10x faster                                                     |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                      |
| scimark_fft                | 345 ms                                                 | 315 ms: 1.10x faster                                                      |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                      |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.62 ms: 1.09x faster                                                     |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                     |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                     |
| unpickle_pure_python       | 242 us                                                 | 227 us: 1.07x faster                                                      |
| deltablue                  | 3.92 ms                                                | 3.68 ms: 1.07x faster                                                     |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                     |
| gc_traversal               | 4.01 ms                                                | 3.80 ms: 1.05x faster                                                     |
| float                      | 78.9 ms                                                | 74.9 ms: 1.05x faster                                                     |
| xml_etree_iterparse        | 108 ms                                                 | 103 ms: 1.05x faster                                                      |
| hexiom                     | 6.89 ms                                                | 6.58 ms: 1.05x faster                                                     |
| logging_simple             | 6.22 us                                                | 5.94 us: 1.05x faster                                                     |
| djangocms                  | 33.5 us                                                | 32.1 us: 1.05x faster                                                     |
| pickle_pure_python         | 320 us                                                 | 307 us: 1.04x faster                                                      |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                     |
| logging_format             | 6.81 us                                                | 6.56 us: 1.04x faster                                                     |
| deepcopy_memo              | 40.2 us                                                | 38.8 us: 1.03x faster                                                     |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                    |
| json_loads                 | 29.2 us                                                | 28.3 us: 1.03x faster                                                     |
| tornado_http               | 98.1 ms                                                | 95.7 ms: 1.02x faster                                                     |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                     |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                                    |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                      |
| deepcopy                   | 365 us                                                 | 360 us: 1.02x faster                                                      |
| sympy_str                  | 297 ms                                                 | 293 ms: 1.01x faster                                                      |
| pidigits                   | 194 ms                                                 | 192 ms: 1.01x faster                                                      |
| pprint_safe_repr           | 747 ms                                                 | 741 ms: 1.01x faster                                                      |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                      |
| unpickle_list              | 5.21 us                                                | 5.18 us: 1.01x faster                                                     |
| pickle_dict                | 34.6 us                                                | 34.4 us: 1.01x faster                                                     |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                      |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.01x slower                                                      |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                     |
| genshi_xml                 | 53.4 ms                                                | 54.5 ms: 1.02x slower                                                     |
| bench_thread_pool          | 834 us                                                 | 853 us: 1.02x slower                                                      |
| mdp                        | 2.77 sec                                               | 2.84 sec: 1.02x slower                                                    |
| pyflate                    | 434 ms                                                 | 444 ms: 1.02x slower                                                      |
| sympy_expand               | 484 ms                                                 | 496 ms: 1.02x slower                                                      |
| dask                       | 365 ms                                                 | 374 ms: 1.02x slower                                                      |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                      |
| sqlglot_optimize           | 55.3 ms                                                | 57.3 ms: 1.04x slower                                                     |
| go                         | 149 ms                                                 | 154 ms: 1.04x slower                                                      |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                      |
| chameleon                  | 6.70 ms                                                | 7.00 ms: 1.05x slower                                                     |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                     |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                                      |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.06x slower                                                     |
| thrift                     | 784 us                                                 | 830 us: 1.06x slower                                                      |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                     |
| dulwich_log                | 64.6 ms                                                | 68.9 ms: 1.07x slower                                                     |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                     |
| regex_v8                   | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                     |
| regex_effbot               | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                     |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                                     |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                     |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                     |
| django_template            | 33.5 ms                                                | 36.7 ms: 1.09x slower                                                     |
| docutils                   | 2.66 sec                                               | 2.91 sec: 1.09x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                     |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                      |
| scimark_lu                 | 116 ms                                                 | 128 ms: 1.10x slower                                                      |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                     |
| pickle_list                | 4.59 us                                                | 5.17 us: 1.13x slower                                                     |
| mypy2                      | 686 ms                                                 | 783 ms: 1.14x slower                                                      |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.24x slower                                                     |
| async_generators           | 374 ms                                                 | 465 ms: 1.24x slower                                                      |
| coverage                   | 78.8 ms                                                | 98.6 ms: 1.25x slower                                                     |
| python_startup_no_site     | 6.01 ms                                                | 7.60 ms: 1.26x slower                                                     |
| telco                      | 6.86 ms                                                | 8.67 ms: 1.26x slower                                                     |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                              |

Benchmark hidden because not significant (3): bench_mp_pool, nqueens, deepcopy_reduce
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x