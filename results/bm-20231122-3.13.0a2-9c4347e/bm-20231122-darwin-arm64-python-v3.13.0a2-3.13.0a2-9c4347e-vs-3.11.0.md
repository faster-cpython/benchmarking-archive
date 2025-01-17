# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a2
- machine: darwin-arm64
- commit hash: 9c4347e
- commit date: 2023-11-22
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 192 ms: 1.24x slower                                       |
| chameleon      | 4.30 ms                                                | 4.73 ms: 1.10x slower                                      |
| docutils       | 1.43 sec                                               | 1.46 sec: 1.02x slower                                     |
| html5lib       | 33.0 ms                                                | 36.0 ms: 1.09x slower                                      |
| tornado_http   | 69.1 ms                                                | 76.9 ms: 1.11x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 282 ms                                                 | 255 ms: 1.11x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 332 ms: 1.06x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 690 ms: 1.05x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 267 ms: 1.03x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 539 ms: 1.02x faster                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 522 ms: 1.01x slower                                       |
| async_tree_io              | 697 ms                                                 | 706 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                       |
| float          | 50.8 ms                                                | 56.4 ms: 1.11x slower                                      |
| nbody          | 61.7 ms                                                | 70.8 ms: 1.15x slower                                      |
| Geometric mean | (ref)                                                  | 1.09x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.02x slower                                       |
| regex_compile  | 72.8 ms                                                | 74.9 ms: 1.03x slower                                      |
| regex_effbot   | 2.43 ms                                                | 2.57 ms: 1.06x slower                                      |
| regex_v8       | 15.1 ms                                                | 17.1 ms: 1.13x slower                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.61 ms: 1.14x faster                                      |
| pickle_pure_python   | 191 us                                                 | 198 us: 1.03x slower                                       |
| unpickle_pure_python | 149 us                                                 | 155 us: 1.04x slower                                       |
| xml_etree_iterparse  | 68.3 ms                                                | 71.3 ms: 1.05x slower                                      |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                      |
| pickle               | 6.98 us                                                | 7.39 us: 1.06x slower                                      |
| unpickle             | 8.29 us                                                | 9.10 us: 1.10x slower                                      |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.10x slower                                      |
| unpickle_list        | 2.69 us                                                | 2.98 us: 1.11x slower                                      |
| json_loads           | 15.3 us                                                | 17.2 us: 1.12x slower                                      |
| xml_etree_process    | 33.6 ms                                                | 39.5 ms: 1.18x slower                                      |
| tomli_loads          | 1.27 sec                                               | 1.53 sec: 1.20x slower                                     |
| xml_etree_generate   | 45.8 ms                                                | 56.2 ms: 1.23x slower                                      |
| Geometric mean       | (ref)                                                  | 1.08x slower                                               |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.9 ms: 1.29x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 12.4 ms: 1.44x slower                                      |
| Geometric mean         | (ref)                                                  | 1.37x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.39 ms: 1.07x faster                                      |
| django_template | 20.1 ms                                                | 21.5 ms: 1.07x slower                                      |
| genshi_text     | 14.4 ms                                                | 15.7 ms: 1.09x slower                                      |
| genshi_xml      | 28.5 ms                                                | 33.0 ms: 1.16x slower                                      |
| Geometric mean  | (ref)                                                  | 1.06x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 73.6 us: 4.09x faster                                      |
| pylint                     | 253 ms                                                 | 168 ms: 1.50x faster                                       |
| asyncio_tcp                | 643 ms                                                 | 436 ms: 1.47x faster                                       |
| comprehensions             | 14.4 us                                                | 11.4 us: 1.27x faster                                      |
| raytrace                   | 206 ms                                                 | 178 ms: 1.15x faster                                       |
| chaos                      | 47.4 ms                                                | 41.2 ms: 1.15x faster                                      |
| json_dumps                 | 7.53 ms                                                | 6.61 ms: 1.14x faster                                      |
| deltablue                  | 2.75 ms                                                | 2.44 ms: 1.13x faster                                      |
| sympy_sum                  | 80.2 ms                                                | 72.0 ms: 1.11x faster                                      |
| async_tree_none            | 282 ms                                                 | 255 ms: 1.11x faster                                       |
| sqlglot_parse              | 890 us                                                 | 807 us: 1.10x faster                                       |
| generators                 | 30.3 ms                                                | 28.0 ms: 1.08x faster                                      |
| mako                       | 7.93 ms                                                | 7.39 ms: 1.07x faster                                      |
| sqlglot_transpile          | 1.05 ms                                                | 980 us: 1.07x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 332 ms: 1.06x faster                                       |
| sympy_integrate            | 11.3 ms                                                | 10.6 ms: 1.06x faster                                      |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.05x faster                                     |
| sympy_str                  | 144 ms                                                 | 137 ms: 1.05x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 690 ms: 1.05x faster                                       |
| deepcopy_memo              | 25.7 us                                                | 24.8 us: 1.04x faster                                      |
| async_tree_none_tg         | 276 ms                                                 | 267 ms: 1.03x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 539 ms: 1.02x faster                                       |
| create_gc_cycles           | 711 us                                                 | 703 us: 1.01x faster                                       |
| go                         | 105 ms                                                 | 105 ms: 1.00x faster                                       |
| gc_traversal               | 2.38 ms                                                | 2.40 ms: 1.00x slower                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 522 ms: 1.01x slower                                       |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                       |
| deepcopy                   | 215 us                                                 | 218 us: 1.01x slower                                       |
| crypto_pyaes               | 47.5 ms                                                | 48.0 ms: 1.01x slower                                      |
| async_tree_io              | 697 ms                                                 | 706 ms: 1.01x slower                                       |
| docutils                   | 1.43 sec                                               | 1.46 sec: 1.02x slower                                     |
| richards_super             | 37.3 ms                                                | 38.0 ms: 1.02x slower                                      |
| sympy_expand               | 229 ms                                                 | 234 ms: 1.02x slower                                       |
| dulwich_log                | 28.6 ms                                                | 29.2 ms: 1.02x slower                                      |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.02x slower                                       |
| meteor_contest             | 71.1 ms                                                | 73.0 ms: 1.03x slower                                      |
| regex_compile              | 72.8 ms                                                | 74.9 ms: 1.03x slower                                      |
| pprint_pformat             | 979 ms                                                 | 1.01 sec: 1.03x slower                                     |
| pickle_pure_python         | 191 us                                                 | 198 us: 1.03x slower                                       |
| pprint_safe_repr           | 478 ms                                                 | 496 ms: 1.04x slower                                       |
| logging_simple             | 3.41 us                                                | 3.54 us: 1.04x slower                                      |
| hexiom                     | 4.58 ms                                                | 4.77 ms: 1.04x slower                                      |
| unpickle_pure_python       | 149 us                                                 | 155 us: 1.04x slower                                       |
| nqueens                    | 55.9 ms                                                | 58.4 ms: 1.04x slower                                      |
| xml_etree_iterparse        | 68.3 ms                                                | 71.3 ms: 1.05x slower                                      |
| logging_format             | 3.67 us                                                | 3.84 us: 1.05x slower                                      |
| mdp                        | 1.48 sec                                               | 1.56 sec: 1.05x slower                                     |
| logging_silent             | 66.5 ns                                                | 69.9 ns: 1.05x slower                                      |
| pycparser                  | 659 ms                                                 | 694 ms: 1.05x slower                                       |
| pathlib                    | 23.2 ms                                                | 24.4 ms: 1.05x slower                                      |
| regex_effbot               | 2.43 ms                                                | 2.57 ms: 1.06x slower                                      |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                      |
| pickle                     | 6.98 us                                                | 7.39 us: 1.06x slower                                      |
| bench_thread_pool          | 465 us                                                 | 493 us: 1.06x slower                                       |
| django_template            | 20.1 ms                                                | 21.5 ms: 1.07x slower                                      |
| scimark_monte_carlo        | 43.5 ms                                                | 46.6 ms: 1.07x slower                                      |
| deepcopy_reduce            | 1.79 us                                                | 1.92 us: 1.07x slower                                      |
| coverage                   | 43.9 ms                                                | 47.1 ms: 1.07x slower                                      |
| scimark_lu                 | 67.7 ms                                                | 72.7 ms: 1.07x slower                                      |
| json                       | 2.75 ms                                                | 2.97 ms: 1.08x slower                                      |
| genshi_text                | 14.4 ms                                                | 15.7 ms: 1.09x slower                                      |
| html5lib                   | 33.0 ms                                                | 36.0 ms: 1.09x slower                                      |
| bench_mp_pool              | 41.0 ms                                                | 44.7 ms: 1.09x slower                                      |
| richards                   | 31.1 ms                                                | 33.9 ms: 1.09x slower                                      |
| coroutines                 | 17.2 ms                                                | 18.8 ms: 1.09x slower                                      |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.08 ms: 1.10x slower                                      |
| unpickle                   | 8.29 us                                                | 9.10 us: 1.10x slower                                      |
| chameleon                  | 4.30 ms                                                | 4.73 ms: 1.10x slower                                      |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.10x slower                                      |
| sqlglot_normalize          | 162 ms                                                 | 179 ms: 1.11x slower                                       |
| unpickle_list              | 2.69 us                                                | 2.98 us: 1.11x slower                                      |
| float                      | 50.8 ms                                                | 56.4 ms: 1.11x slower                                      |
| tornado_http               | 69.1 ms                                                | 76.9 ms: 1.11x slower                                      |
| thrift                     | 410 us                                                 | 457 us: 1.11x slower                                       |
| json_loads                 | 15.3 us                                                | 17.2 us: 1.12x slower                                      |
| sqlglot_optimize           | 29.6 ms                                                | 33.3 ms: 1.12x slower                                      |
| spectral_norm              | 65.7 ms                                                | 74.0 ms: 1.13x slower                                      |
| regex_v8                   | 15.1 ms                                                | 17.1 ms: 1.13x slower                                      |
| fannkuch                   | 240 ms                                                 | 270 ms: 1.13x slower                                       |
| nbody                      | 61.7 ms                                                | 70.8 ms: 1.15x slower                                      |
| genshi_xml                 | 28.5 ms                                                | 33.0 ms: 1.16x slower                                      |
| scimark_fft                | 173 ms                                                 | 200 ms: 1.16x slower                                       |
| xml_etree_process          | 33.6 ms                                                | 39.5 ms: 1.18x slower                                      |
| pyflate                    | 284 ms                                                 | 335 ms: 1.18x slower                                       |
| gunicorn                   | 1.10 ms                                                | 1.31 ms: 1.19x slower                                      |
| tomli_loads                | 1.27 sec                                               | 1.53 sec: 1.20x slower                                     |
| xml_etree_generate         | 45.8 ms                                                | 56.2 ms: 1.23x slower                                      |
| aiohttp                    | 1.02 ms                                                | 1.26 ms: 1.23x slower                                      |
| 2to3                       | 154 ms                                                 | 192 ms: 1.24x slower                                       |
| sqlite_synth               | 1.26 us                                                | 1.58 us: 1.26x slower                                      |
| python_startup             | 10.8 ms                                                | 13.9 ms: 1.29x slower                                      |
| scimark_sor                | 79.2 ms                                                | 104 ms: 1.31x slower                                       |
| telco                      | 3.17 ms                                                | 4.54 ms: 1.43x slower                                      |
| python_startup_no_site     | 8.57 ms                                                | 12.4 ms: 1.44x slower                                      |
| async_generators           | 192 ms                                                 | 294 ms: 1.53x slower                                       |
| mypy2                      | 372 ms                                                 | 596 ms: 1.60x slower                                       |
| flaskblogging              | 2.35 ms                                                | 3.89 ms: 1.66x slower                                      |
| Geometric mean             | (ref)                                                  | 1.04x slower                                               |

Benchmark hidden because not significant (3): async_tree_memoization, xml_etree_parse, asyncio_websockets
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20231122-3.13.0a2-9c4347e/bm-20231122-darwin-arm64-python-v3.13.0a2-3.13.0a2-9c4347e.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.04x