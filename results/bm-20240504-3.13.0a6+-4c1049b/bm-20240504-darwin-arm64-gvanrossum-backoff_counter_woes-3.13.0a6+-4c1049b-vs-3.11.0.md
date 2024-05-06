# Results vs. 3.11.0

- fork: gvanrossum
- ref: backoff_counter_woes
- machine: darwin-arm64
- commit hash: 4c1049b
- commit date: 2024-05-04
- overall geometric mean: 1.03x faster
- HPT reliability: 96.49%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 159 ms: 1.03x slower                                                       |
| chameleon      | 4.30 ms                                                | 4.38 ms: 1.02x slower                                                      |
| docutils       | 1.43 sec                                               | 1.46 sec: 1.02x slower                                                     |
| html5lib       | 33.0 ms                                                | 31.2 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 240 ms: 1.47x faster                                                       |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                       |
| async_tree_none            | 282 ms                                                 | 210 ms: 1.34x faster                                                       |
| async_tree_memoization     | 336 ms                                                 | 255 ms: 1.32x faster                                                       |
| async_tree_io_tg           | 724 ms                                                 | 573 ms: 1.26x faster                                                       |
| async_tree_io              | 697 ms                                                 | 561 ms: 1.24x faster                                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 454 ms: 1.21x faster                                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 465 ms: 1.12x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.6 ms: 1.05x faster                                                      |
| nbody          | 61.7 ms                                                | 59.3 ms: 1.04x faster                                                      |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                  | 1.03x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 139 ms: 1.07x faster                                                       |
| regex_compile  | 72.8 ms                                                | 68.7 ms: 1.06x faster                                                      |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                      |
| regex_v8       | 15.1 ms                                                | 16.6 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.14 ms: 1.23x faster                                                      |
| pickle_pure_python   | 191 us                                                 | 181 us: 1.06x faster                                                       |
| unpickle_pure_python | 149 us                                                 | 142 us: 1.05x faster                                                       |
| xml_etree_parse      | 100 ms                                                 | 98.1 ms: 1.02x faster                                                      |
| xml_etree_iterparse  | 68.3 ms                                                | 67.7 ms: 1.01x faster                                                      |
| pickle               | 6.98 us                                                | 7.44 us: 1.07x slower                                                      |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                                      |
| xml_etree_process    | 33.6 ms                                                | 37.0 ms: 1.10x slower                                                      |
| pickle_list          | 2.70 us                                                | 2.99 us: 1.11x slower                                                      |
| json_loads           | 15.3 us                                                | 17.2 us: 1.12x slower                                                      |
| tomli_loads          | 1.27 sec                                               | 1.45 sec: 1.14x slower                                                     |
| xml_etree_generate   | 45.8 ms                                                | 53.1 ms: 1.16x slower                                                      |
| unpickle             | 8.29 us                                                | 9.67 us: 1.17x slower                                                      |
| unpickle_list        | 2.69 us                                                | 3.26 us: 1.22x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.7 ms: 1.27x slower                                                      |
| python_startup_no_site | 8.57 ms                                                | 10.9 ms: 1.28x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.89 ms: 1.15x faster                                                      |
| genshi_text     | 14.4 ms                                                | 13.9 ms: 1.04x faster                                                      |
| django_template | 20.1 ms                                                | 19.4 ms: 1.04x faster                                                      |
| genshi_xml      | 28.5 ms                                                | 30.0 ms: 1.05x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 88.9 us: 3.38x faster                                                      |
| asyncio_tcp                | 643 ms                                                 | 398 ms: 1.62x faster                                                       |
| pylint                     | 253 ms                                                 | 168 ms: 1.50x faster                                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 240 ms: 1.47x faster                                                       |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                       |
| raytrace                   | 206 ms                                                 | 148 ms: 1.39x faster                                                       |
| chaos                      | 47.4 ms                                                | 34.7 ms: 1.37x faster                                                      |
| comprehensions             | 14.4 us                                                | 10.6 us: 1.36x faster                                                      |
| generators                 | 30.3 ms                                                | 22.6 ms: 1.34x faster                                                      |
| async_tree_none            | 282 ms                                                 | 210 ms: 1.34x faster                                                       |
| async_tree_memoization     | 336 ms                                                 | 255 ms: 1.32x faster                                                       |
| deltablue                  | 2.75 ms                                                | 2.15 ms: 1.28x faster                                                      |
| async_tree_io_tg           | 724 ms                                                 | 573 ms: 1.26x faster                                                       |
| async_tree_io              | 697 ms                                                 | 561 ms: 1.24x faster                                                       |
| json_dumps                 | 7.53 ms                                                | 6.14 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 454 ms: 1.21x faster                                                       |
| sqlglot_parse              | 890 us                                                 | 737 us: 1.21x faster                                                       |
| sqlglot_transpile          | 1.05 ms                                                | 900 us: 1.17x faster                                                       |
| sympy_sum                  | 80.2 ms                                                | 69.4 ms: 1.16x faster                                                      |
| mako                       | 7.93 ms                                                | 6.89 ms: 1.15x faster                                                      |
| deepcopy_memo              | 25.7 us                                                | 22.9 us: 1.12x faster                                                      |
| logging_simple             | 3.41 us                                                | 3.04 us: 1.12x faster                                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 465 ms: 1.12x faster                                                       |
| hexiom                     | 4.58 ms                                                | 4.10 ms: 1.12x faster                                                      |
| logging_format             | 3.67 us                                                | 3.33 us: 1.10x faster                                                      |
| logging_silent             | 66.5 ns                                                | 60.5 ns: 1.10x faster                                                      |
| sympy_integrate            | 11.3 ms                                                | 10.3 ms: 1.10x faster                                                      |
| sympy_str                  | 144 ms                                                 | 132 ms: 1.09x faster                                                       |
| regex_dna                  | 148 ms                                                 | 139 ms: 1.07x faster                                                       |
| deepcopy                   | 215 us                                                 | 202 us: 1.07x faster                                                       |
| regex_compile              | 72.8 ms                                                | 68.7 ms: 1.06x faster                                                      |
| nqueens                    | 55.9 ms                                                | 52.8 ms: 1.06x faster                                                      |
| pickle_pure_python         | 191 us                                                 | 181 us: 1.06x faster                                                       |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                     |
| go                         | 105 ms                                                 | 99.7 ms: 1.06x faster                                                      |
| richards_super             | 37.3 ms                                                | 35.3 ms: 1.06x faster                                                      |
| html5lib                   | 33.0 ms                                                | 31.2 ms: 1.06x faster                                                      |
| unpickle_pure_python       | 149 us                                                 | 142 us: 1.05x faster                                                       |
| dulwich_log                | 28.6 ms                                                | 27.3 ms: 1.05x faster                                                      |
| coroutines                 | 17.2 ms                                                | 16.4 ms: 1.05x faster                                                      |
| float                      | 50.8 ms                                                | 48.6 ms: 1.05x faster                                                      |
| nbody                      | 61.7 ms                                                | 59.3 ms: 1.04x faster                                                      |
| pycparser                  | 659 ms                                                 | 634 ms: 1.04x faster                                                       |
| genshi_text                | 14.4 ms                                                | 13.9 ms: 1.04x faster                                                      |
| crypto_pyaes               | 47.5 ms                                                | 45.8 ms: 1.04x faster                                                      |
| django_template            | 20.1 ms                                                | 19.4 ms: 1.04x faster                                                      |
| pprint_pformat             | 979 ms                                                 | 949 ms: 1.03x faster                                                       |
| scimark_monte_carlo        | 43.5 ms                                                | 42.4 ms: 1.03x faster                                                      |
| xml_etree_parse            | 100 ms                                                 | 98.1 ms: 1.02x faster                                                      |
| pprint_safe_repr           | 478 ms                                                 | 469 ms: 1.02x faster                                                       |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.76 ms: 1.02x faster                                                      |
| pathlib                    | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                      |
| sympy_expand               | 229 ms                                                 | 227 ms: 1.01x faster                                                       |
| deepcopy_reduce            | 1.79 us                                                | 1.78 us: 1.01x faster                                                      |
| bench_thread_pool          | 465 us                                                 | 461 us: 1.01x faster                                                       |
| xml_etree_iterparse        | 68.3 ms                                                | 67.7 ms: 1.01x faster                                                      |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                       |
| meteor_contest             | 71.1 ms                                                | 71.5 ms: 1.01x slower                                                      |
| mdp                        | 1.48 sec                                               | 1.50 sec: 1.01x slower                                                     |
| spectral_norm              | 65.7 ms                                                | 66.5 ms: 1.01x slower                                                      |
| chameleon                  | 4.30 ms                                                | 4.38 ms: 1.02x slower                                                      |
| docutils                   | 1.43 sec                                               | 1.46 sec: 1.02x slower                                                     |
| sqlglot_normalize          | 162 ms                                                 | 166 ms: 1.02x slower                                                       |
| 2to3                       | 154 ms                                                 | 159 ms: 1.03x slower                                                       |
| coverage                   | 43.9 ms                                                | 45.4 ms: 1.04x slower                                                      |
| richards                   | 31.1 ms                                                | 32.2 ms: 1.04x slower                                                      |
| gc_traversal               | 2.38 ms                                                | 2.49 ms: 1.05x slower                                                      |
| sqlglot_optimize           | 29.6 ms                                                | 31.0 ms: 1.05x slower                                                      |
| genshi_xml                 | 28.5 ms                                                | 30.0 ms: 1.05x slower                                                      |
| aiohttp                    | 1.02 ms                                                | 1.08 ms: 1.05x slower                                                      |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                      |
| scimark_fft                | 173 ms                                                 | 184 ms: 1.06x slower                                                       |
| pickle                     | 6.98 us                                                | 7.44 us: 1.07x slower                                                      |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                                      |
| thrift                     | 410 us                                                 | 440 us: 1.07x slower                                                       |
| fannkuch                   | 240 ms                                                 | 258 ms: 1.08x slower                                                       |
| regex_v8                   | 15.1 ms                                                | 16.6 ms: 1.10x slower                                                      |
| json                       | 2.75 ms                                                | 3.03 ms: 1.10x slower                                                      |
| xml_etree_process          | 33.6 ms                                                | 37.0 ms: 1.10x slower                                                      |
| pickle_list                | 2.70 us                                                | 2.99 us: 1.11x slower                                                      |
| bench_mp_pool              | 41.0 ms                                                | 45.7 ms: 1.11x slower                                                      |
| json_loads                 | 15.3 us                                                | 17.2 us: 1.12x slower                                                      |
| pyflate                    | 284 ms                                                 | 321 ms: 1.13x slower                                                       |
| tomli_loads                | 1.27 sec                                               | 1.45 sec: 1.14x slower                                                     |
| xml_etree_generate         | 45.8 ms                                                | 53.1 ms: 1.16x slower                                                      |
| unpickle                   | 8.29 us                                                | 9.67 us: 1.17x slower                                                      |
| scimark_sor                | 79.2 ms                                                | 95.1 ms: 1.20x slower                                                      |
| unpickle_list              | 2.69 us                                                | 3.26 us: 1.22x slower                                                      |
| mypy2                      | 372 ms                                                 | 458 ms: 1.23x slower                                                       |
| sqlite_synth               | 1.26 us                                                | 1.55 us: 1.23x slower                                                      |
| python_startup             | 10.8 ms                                                | 13.7 ms: 1.27x slower                                                      |
| python_startup_no_site     | 8.57 ms                                                | 10.9 ms: 1.28x slower                                                      |
| create_gc_cycles           | 711 us                                                 | 946 us: 1.33x slower                                                       |
| telco                      | 3.17 ms                                                | 4.40 ms: 1.39x slower                                                      |
| async_generators           | 192 ms                                                 | 279 ms: 1.45x slower                                                       |
| flaskblogging              | 2.35 ms                                                | 5.18 ms: 2.20x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (5): dask, asyncio_websockets, scimark_lu, gunicorn, tornado_http
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240504-3.13.0a6+-4c1049b/bm-20240504-darwin-arm64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 96.49% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x