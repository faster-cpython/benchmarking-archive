# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 172 ms: 1.11x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.68 ms: 1.34x faster                                                  |
| docutils       | 1.73 sec                                               | 1.57 sec: 1.11x faster                                                 |
| html5lib       | 42.4 ms                                                | 32.2 ms: 1.31x faster                                                  |
| tornado_http   | 86.7 ms                                                | 78.8 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.19x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 212 ms: 1.83x faster                                                   |
| async_tree_io           | 980 ms                                                 | 576 ms: 1.70x faster                                                   |
| async_tree_memoization  | 474 ms                                                 | 280 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 472 ms: 1.38x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.64x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 83.4 ms: 1.12x faster                                                  |
| float          | 69.0 ms                                                | 64.7 ms: 1.07x faster                                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| regex_compile  | 95.3 ms                                                | 92.8 ms: 1.03x faster                                                  |
| regex_v8       | 17.1 ms                                                | 17.6 ms: 1.02x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.63 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 184 us: 1.53x faster                                                   |
| json_dumps           | 8.11 ms                                                | 6.39 ms: 1.27x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 39.1 ms: 1.19x faster                                                  |
| xml_etree_parse      | 108 ms                                                 | 99.0 ms: 1.09x faster                                                  |
| unpickle_pure_python | 194 us                                                 | 181 us: 1.07x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.66 sec: 1.03x faster                                                 |
| xml_etree_iterparse  | 72.1 ms                                                | 73.0 ms: 1.01x slower                                                  |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                  |
| unpickle             | 8.80 us                                                | 9.21 us: 1.05x slower                                                  |
| xml_etree_generate   | 53.5 ms                                                | 56.8 ms: 1.06x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| pickle               | 6.97 us                                                | 7.47 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.91 us: 1.08x slower                                                  |
| pickle_list          | 2.74 us                                                | 3.02 us: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 12.0 ms: 1.10x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 9.19 ms: 1.16x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 26.4 ms                                                | 22.3 ms: 1.18x faster                                                  |
| genshi_text     | 17.3 ms                                                | 15.0 ms: 1.16x faster                                                  |
| mako            | 9.87 ms                                                | 9.33 ms: 1.06x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 32.0 ms: 1.06x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.11x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 71.2 us: 4.53x faster                                                  |
| async_tree_none          | 388 ms                                                 | 212 ms: 1.83x faster                                                   |
| logging_silent           | 117 ns                                                 | 65.6 ns: 1.79x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.81 ms: 1.75x faster                                                  |
| async_tree_io            | 980 ms                                                 | 576 ms: 1.70x faster                                                   |
| async_tree_memoization   | 474 ms                                                 | 280 ms: 1.69x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 393 ms: 1.68x faster                                                   |
| raytrace                 | 301 ms                                                 | 181 ms: 1.66x faster                                                   |
| pylint                   | 277 ms                                                 | 179 ms: 1.54x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 184 us: 1.53x faster                                                   |
| sqlglot_parse            | 1.24 ms                                                | 833 us: 1.49x faster                                                   |
| mypy2                    | 607 ms                                                 | 408 ms: 1.49x faster                                                   |
| richards_super           | 57.8 ms                                                | 39.0 ms: 1.48x faster                                                  |
| sqlglot_transpile        | 1.44 ms                                                | 1.00 ms: 1.44x faster                                                  |
| logging_format           | 4.83 us                                                | 3.47 us: 1.39x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.21 us: 1.38x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 472 ms: 1.38x faster                                                   |
| richards                 | 48.7 ms                                                | 35.4 ms: 1.37x faster                                                  |
| chaos                    | 65.8 ms                                                | 48.4 ms: 1.36x faster                                                  |
| chameleon                | 6.26 ms                                                | 4.68 ms: 1.34x faster                                                  |
| html5lib                 | 42.4 ms                                                | 32.2 ms: 1.31x faster                                                  |
| pycparser                | 877 ms                                                 | 672 ms: 1.30x faster                                                   |
| thrift                   | 572 us                                                 | 443 us: 1.29x faster                                                   |
| deepcopy_memo            | 34.7 us                                                | 27.3 us: 1.27x faster                                                  |
| go                       | 151 ms                                                 | 119 ms: 1.27x faster                                                   |
| json_dumps               | 8.11 ms                                                | 6.39 ms: 1.27x faster                                                  |
| crypto_pyaes             | 71.8 ms                                                | 56.6 ms: 1.27x faster                                                  |
| generators               | 32.3 ms                                                | 26.0 ms: 1.24x faster                                                  |
| deepcopy                 | 272 us                                                 | 219 us: 1.24x faster                                                   |
| coroutines               | 20.7 ms                                                | 16.8 ms: 1.23x faster                                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.90 us: 1.23x faster                                                  |
| dulwich_log              | 35.3 ms                                                | 28.9 ms: 1.22x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.21x faster                                                 |
| xml_etree_process        | 46.5 ms                                                | 39.1 ms: 1.19x faster                                                  |
| django_template          | 26.4 ms                                                | 22.3 ms: 1.18x faster                                                  |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| genshi_text              | 17.3 ms                                                | 15.0 ms: 1.16x faster                                                  |
| scimark_sor              | 128 ms                                                 | 112 ms: 1.14x faster                                                   |
| dask                     | 253 ms                                                 | 222 ms: 1.14x faster                                                   |
| sympy_sum                | 92.2 ms                                                | 81.0 ms: 1.14x faster                                                  |
| sympy_integrate          | 13.1 ms                                                | 11.8 ms: 1.12x faster                                                  |
| nbody                    | 93.0 ms                                                | 83.4 ms: 1.12x faster                                                  |
| 2to3                     | 192 ms                                                 | 172 ms: 1.11x faster                                                   |
| docutils                 | 1.73 sec                                               | 1.57 sec: 1.11x faster                                                 |
| sympy_expand             | 269 ms                                                 | 244 ms: 1.10x faster                                                   |
| tornado_http             | 86.7 ms                                                | 78.8 ms: 1.10x faster                                                  |
| gunicorn                 | 1.30 ms                                                | 1.19 ms: 1.09x faster                                                  |
| sympy_str                | 165 ms                                                 | 151 ms: 1.09x faster                                                   |
| pprint_safe_repr         | 641 ms                                                 | 587 ms: 1.09x faster                                                   |
| xml_etree_parse          | 108 ms                                                 | 99.0 ms: 1.09x faster                                                  |
| pprint_pformat           | 1.30 sec                                               | 1.20 sec: 1.09x faster                                                 |
| unpickle_pure_python     | 194 us                                                 | 181 us: 1.07x faster                                                   |
| float                    | 69.0 ms                                                | 64.7 ms: 1.07x faster                                                  |
| aiohttp                  | 1.22 ms                                                | 1.15 ms: 1.06x faster                                                  |
| mako                     | 9.87 ms                                                | 9.33 ms: 1.06x faster                                                  |
| genshi_xml               | 33.8 ms                                                | 32.0 ms: 1.06x faster                                                  |
| json                     | 3.08 ms                                                | 2.93 ms: 1.05x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 503 us: 1.05x faster                                                   |
| sqlglot_normalize        | 190 ms                                                 | 181 ms: 1.05x faster                                                   |
| sqlglot_optimize         | 36.8 ms                                                | 35.2 ms: 1.05x faster                                                  |
| hexiom                   | 6.19 ms                                                | 5.96 ms: 1.04x faster                                                  |
| tomli_loads              | 1.71 sec                                               | 1.66 sec: 1.03x faster                                                 |
| regex_compile            | 95.3 ms                                                | 92.8 ms: 1.03x faster                                                  |
| comprehensions           | 16.9 us                                                | 16.5 us: 1.02x faster                                                  |
| pyflate                  | 427 ms                                                 | 418 ms: 1.02x faster                                                   |
| scimark_monte_carlo      | 65.6 ms                                                | 64.3 ms: 1.02x faster                                                  |
| scimark_lu               | 103 ms                                                 | 101 ms: 1.02x faster                                                   |
| pathlib                  | 24.5 ms                                                | 24.0 ms: 1.02x faster                                                  |
| mdp                      | 1.63 sec                                               | 1.61 sec: 1.01x faster                                                 |
| pidigits                 | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| xml_etree_iterparse      | 72.1 ms                                                | 73.0 ms: 1.01x slower                                                  |
| meteor_contest           | 77.7 ms                                                | 78.9 ms: 1.01x slower                                                  |
| create_gc_cycles         | 860 us                                                 | 877 us: 1.02x slower                                                   |
| regex_v8                 | 17.1 ms                                                | 17.6 ms: 1.02x slower                                                  |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.21 us: 1.05x slower                                                  |
| spectral_norm            | 94.8 ms                                                | 100 ms: 1.06x slower                                                   |
| xml_etree_generate       | 53.5 ms                                                | 56.8 ms: 1.06x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.63 ms: 1.07x slower                                                  |
| pickle                   | 6.97 us                                                | 7.47 us: 1.07x slower                                                  |
| unpickle_list            | 2.69 us                                                | 2.91 us: 1.08x slower                                                  |
| nqueens                  | 63.8 ms                                                | 69.9 ms: 1.10x slower                                                  |
| scimark_fft              | 224 ms                                                 | 246 ms: 1.10x slower                                                   |
| pickle_list              | 2.74 us                                                | 3.02 us: 1.10x slower                                                  |
| python_startup           | 10.9 ms                                                | 12.0 ms: 1.10x slower                                                  |
| coverage                 | 41.5 ms                                                | 46.2 ms: 1.11x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.63 us: 1.12x slower                                                  |
| fannkuch                 | 303 ms                                                 | 341 ms: 1.13x slower                                                   |
| python_startup_no_site   | 7.91 ms                                                | 9.19 ms: 1.16x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 43.6 ms: 1.17x slower                                                  |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 4.00 ms: 1.17x slower                                                  |
| async_generators         | 231 ms                                                 | 294 ms: 1.27x slower                                                   |
| telco                    | 3.49 ms                                                | 4.72 ms: 1.35x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.15x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x