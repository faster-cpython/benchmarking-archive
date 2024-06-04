# Results vs. 3.11.0

- fork: python
- ref: 6b10467fbc0b67bf217e
- machine: darwin-arm64
- commit hash: 6b10467
- commit date: 2024-06-03
- overall geometric mean: 1.04x faster
- HPT reliability: 98.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.52x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 160 ms: 1.04x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.27 ms: 1.01x faster                                                  |
| html5lib       | 33.0 ms                                                | 31.3 ms: 1.05x faster                                                  |
| tornado_http   | 69.1 ms                                                | 65.4 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 237 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                   |
| async_tree_none            | 282 ms                                                 | 208 ms: 1.36x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 256 ms: 1.31x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 554 ms: 1.31x faster                                                   |
| async_tree_io              | 697 ms                                                 | 550 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 450 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 465 ms: 1.11x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.8 ms: 1.04x faster                                                  |
| nbody          | 61.7 ms                                                | 60.8 ms: 1.02x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.2 ms: 1.07x faster                                                  |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.36 ms: 1.18x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 179 us: 1.07x faster                                                   |
| unpickle_pure_python | 149 us                                                 | 142 us: 1.05x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 102 ms: 1.02x slower                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 71.5 ms: 1.05x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                                  |
| pickle               | 6.98 us                                                | 7.48 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.1 ms: 1.10x slower                                                  |
| unpickle             | 8.29 us                                                | 9.23 us: 1.11x slower                                                  |
| pickle_list          | 2.70 us                                                | 3.02 us: 1.12x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.45 sec: 1.14x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 52.1 ms: 1.14x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 10.8 ms: 1.26x slower                                                  |
| python_startup         | 10.8 ms                                                | 13.8 ms: 1.28x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.94 ms: 1.14x faster                                                  |
| django_template | 20.1 ms                                                | 19.3 ms: 1.04x faster                                                  |
| genshi_text     | 14.4 ms                                                | 13.9 ms: 1.04x faster                                                  |
| genshi_xml      | 28.5 ms                                                | 29.7 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 91.0 us: 3.31x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 412 ms: 1.56x faster                                                   |
| pylint                     | 253 ms                                                 | 168 ms: 1.50x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 237 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                   |
| raytrace                   | 206 ms                                                 | 148 ms: 1.39x faster                                                   |
| chaos                      | 47.4 ms                                                | 34.6 ms: 1.37x faster                                                  |
| async_tree_none            | 282 ms                                                 | 208 ms: 1.36x faster                                                   |
| generators                 | 30.3 ms                                                | 22.7 ms: 1.34x faster                                                  |
| comprehensions             | 14.4 us                                                | 10.9 us: 1.32x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 256 ms: 1.31x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 554 ms: 1.31x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.15 ms: 1.28x faster                                                  |
| async_tree_io              | 697 ms                                                 | 550 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 450 ms: 1.22x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 736 us: 1.21x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.36 ms: 1.18x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 896 us: 1.17x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 69.4 ms: 1.16x faster                                                  |
| mako                       | 7.93 ms                                                | 6.94 ms: 1.14x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 22.6 us: 1.14x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.23 sec: 1.13x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.09 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 465 ms: 1.11x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.07 us: 1.11x faster                                                  |
| logging_format             | 3.67 us                                                | 3.36 us: 1.09x faster                                                  |
| sympy_str                  | 144 ms                                                 | 132 ms: 1.09x faster                                                   |
| sympy_integrate            | 11.3 ms                                                | 10.3 ms: 1.09x faster                                                  |
| logging_silent             | 66.5 ns                                                | 61.6 ns: 1.08x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.0 ms: 1.07x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 179 us: 1.07x faster                                                   |
| regex_compile              | 72.8 ms                                                | 68.2 ms: 1.07x faster                                                  |
| richards_super             | 37.3 ms                                                | 35.0 ms: 1.07x faster                                                  |
| nqueens                    | 55.9 ms                                                | 52.8 ms: 1.06x faster                                                  |
| tornado_http               | 69.1 ms                                                | 65.4 ms: 1.06x faster                                                  |
| deepcopy                   | 215 us                                                 | 204 us: 1.06x faster                                                   |
| html5lib                   | 33.0 ms                                                | 31.3 ms: 1.05x faster                                                  |
| pathlib                    | 23.2 ms                                                | 22.1 ms: 1.05x faster                                                  |
| go                         | 105 ms                                                 | 100 ms: 1.05x faster                                                   |
| unpickle_pure_python       | 149 us                                                 | 142 us: 1.05x faster                                                   |
| dulwich_log                | 28.6 ms                                                | 27.4 ms: 1.05x faster                                                  |
| float                      | 50.8 ms                                                | 48.8 ms: 1.04x faster                                                  |
| django_template            | 20.1 ms                                                | 19.3 ms: 1.04x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 941 ms: 1.04x faster                                                   |
| genshi_text                | 14.4 ms                                                | 13.9 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 478 ms                                                 | 463 ms: 1.03x faster                                                   |
| pycparser                  | 659 ms                                                 | 639 ms: 1.03x faster                                                   |
| aiohttp                    | 1.02 ms                                                | 1.00 ms: 1.02x faster                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 42.6 ms: 1.02x faster                                                  |
| scimark_lu                 | 67.7 ms                                                | 66.6 ms: 1.02x faster                                                  |
| sympy_expand               | 229 ms                                                 | 226 ms: 1.02x faster                                                   |
| nbody                      | 61.7 ms                                                | 60.8 ms: 1.02x faster                                                  |
| meteor_contest             | 71.1 ms                                                | 70.1 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.78 ms: 1.01x faster                                                  |
| bench_thread_pool          | 465 us                                                 | 460 us: 1.01x faster                                                   |
| chameleon                  | 4.30 ms                                                | 4.27 ms: 1.01x faster                                                  |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                                   |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 66.6 ms: 1.01x slower                                                  |
| mypy2                      | 372 ms                                                 | 379 ms: 1.02x slower                                                   |
| xml_etree_parse            | 100 ms                                                 | 102 ms: 1.02x slower                                                   |
| coverage                   | 43.9 ms                                                | 44.9 ms: 1.02x slower                                                  |
| richards                   | 31.1 ms                                                | 31.9 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 167 ms: 1.03x slower                                                   |
| fannkuch                   | 240 ms                                                 | 248 ms: 1.03x slower                                                   |
| 2to3                       | 154 ms                                                 | 160 ms: 1.04x slower                                                   |
| mdp                        | 1.48 sec                                               | 1.54 sec: 1.04x slower                                                 |
| genshi_xml                 | 28.5 ms                                                | 29.7 ms: 1.04x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 71.5 ms: 1.05x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 31.0 ms: 1.05x slower                                                  |
| scimark_fft                | 173 ms                                                 | 182 ms: 1.05x slower                                                   |
| crypto_pyaes               | 47.5 ms                                                | 50.0 ms: 1.05x slower                                                  |
| thrift                     | 410 us                                                 | 437 us: 1.07x slower                                                   |
| json                       | 2.75 ms                                                | 2.93 ms: 1.07x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.48 us: 1.07x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.90 us: 1.08x slower                                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 37.1 ms: 1.10x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.23 us: 1.11x slower                                                  |
| pyflate                    | 284 ms                                                 | 318 ms: 1.12x slower                                                   |
| bench_mp_pool              | 41.0 ms                                                | 46.0 ms: 1.12x slower                                                  |
| pickle_list                | 2.70 us                                                | 3.02 us: 1.12x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.45 sec: 1.14x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 52.1 ms: 1.14x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 94.8 ms: 1.20x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.53 us: 1.22x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 892 us: 1.26x slower                                                   |
| python_startup_no_site     | 8.57 ms                                                | 10.8 ms: 1.26x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.8 ms: 1.28x slower                                                  |
| flaskblogging              | 2.35 ms                                                | 3.11 ms: 1.32x slower                                                  |
| telco                      | 3.17 ms                                                | 4.53 ms: 1.43x slower                                                  |
| async_generators           | 192 ms                                                 | 281 ms: 1.47x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (4): gunicorn, dask, docutils, deepcopy_reduce
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240603-3.13.0b1+-6b10467/bm-20240603-darwin-arm64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 98.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.52x