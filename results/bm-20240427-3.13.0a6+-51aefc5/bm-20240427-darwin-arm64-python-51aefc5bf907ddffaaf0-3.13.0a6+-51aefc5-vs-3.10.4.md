# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 180 ms: 1.06x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.54 ms: 1.38x faster                                                  |
| docutils       | 1.73 sec                                               | 1.45 sec: 1.19x faster                                                 |
| html5lib       | 42.4 ms                                                | 31.9 ms: 1.33x faster                                                  |
| tornado_http   | 86.7 ms                                                | 76.6 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 203 ms: 1.92x faster                                                   |
| async_tree_memoization  | 474 ms                                                 | 270 ms: 1.75x faster                                                   |
| async_tree_io           | 980 ms                                                 | 572 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 466 ms: 1.39x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.68x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 69.7 ms: 1.33x faster                                                  |
| float          | 69.0 ms                                                | 52.0 ms: 1.33x faster                                                  |
| Geometric mean | (ref)                                                  | 1.21x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 69.6 ms: 1.37x faster                                                  |
| regex_dna      | 174 ms                                                 | 150 ms: 1.17x faster                                                   |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.02x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.58 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 184 us: 1.52x faster                                                   |
| unpickle_pure_python | 194 us                                                 | 141 us: 1.38x faster                                                   |
| json_dumps           | 8.11 ms                                                | 6.23 ms: 1.30x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 37.6 ms: 1.24x faster                                                  |
| tomli_loads          | 1.71 sec                                               | 1.51 sec: 1.13x faster                                                 |
| xml_etree_parse      | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| xml_etree_generate   | 53.5 ms                                                | 55.1 ms: 1.03x slower                                                  |
| json_loads           | 16.4 us                                                | 17.0 us: 1.04x slower                                                  |
| unpickle             | 8.80 us                                                | 9.22 us: 1.05x slower                                                  |
| pickle               | 6.97 us                                                | 7.45 us: 1.07x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.3 us: 1.08x slower                                                  |
| pickle_list          | 2.74 us                                                | 2.96 us: 1.08x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.95 us: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.6 ms: 1.25x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 10.8 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 7.09 ms: 1.39x faster                                                  |
| django_template | 26.4 ms                                                | 20.2 ms: 1.30x faster                                                  |
| genshi_text     | 17.3 ms                                                | 15.0 ms: 1.16x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 31.4 ms: 1.08x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.23x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 94.9 us: 3.40x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.21 ms: 2.23x faster                                                  |
| raytrace                 | 301 ms                                                 | 154 ms: 1.95x faster                                                   |
| async_tree_none          | 388 ms                                                 | 203 ms: 1.92x faster                                                   |
| logging_silent           | 117 ns                                                 | 64.9 ns: 1.81x faster                                                  |
| chaos                    | 65.8 ms                                                | 36.5 ms: 1.80x faster                                                  |
| async_tree_memoization   | 474 ms                                                 | 270 ms: 1.75x faster                                                   |
| async_tree_io            | 980 ms                                                 | 572 ms: 1.71x faster                                                   |
| richards_super           | 57.8 ms                                                | 35.5 ms: 1.63x faster                                                  |
| sqlglot_parse            | 1.24 ms                                                | 765 us: 1.63x faster                                                   |
| comprehensions           | 16.9 us                                                | 10.5 us: 1.62x faster                                                  |
| pylint                   | 277 ms                                                 | 172 ms: 1.61x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 412 ms: 1.60x faster                                                   |
| sqlglot_transpile        | 1.44 ms                                                | 928 us: 1.55x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 184 us: 1.52x faster                                                   |
| crypto_pyaes             | 71.8 ms                                                | 47.3 ms: 1.52x faster                                                  |
| richards                 | 48.7 ms                                                | 32.2 ms: 1.51x faster                                                  |
| go                       | 151 ms                                                 | 102 ms: 1.48x faster                                                   |
| scimark_lu               | 103 ms                                                 | 69.5 ms: 1.48x faster                                                  |
| deepcopy_memo            | 34.7 us                                                | 23.6 us: 1.47x faster                                                  |
| hexiom                   | 6.19 ms                                                | 4.25 ms: 1.46x faster                                                  |
| scimark_monte_carlo      | 65.6 ms                                                | 45.2 ms: 1.45x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.18 us: 1.40x faster                                                  |
| logging_format           | 4.83 us                                                | 3.46 us: 1.40x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 466 ms: 1.39x faster                                                   |
| mako                     | 9.87 ms                                                | 7.09 ms: 1.39x faster                                                  |
| unpickle_pure_python     | 194 us                                                 | 141 us: 1.38x faster                                                   |
| chameleon                | 6.26 ms                                                | 4.54 ms: 1.38x faster                                                  |
| pycparser                | 877 ms                                                 | 641 ms: 1.37x faster                                                   |
| regex_compile            | 95.3 ms                                                | 69.6 ms: 1.37x faster                                                  |
| nbody                    | 93.0 ms                                                | 69.7 ms: 1.33x faster                                                  |
| html5lib                 | 42.4 ms                                                | 31.9 ms: 1.33x faster                                                  |
| float                    | 69.0 ms                                                | 52.0 ms: 1.33x faster                                                  |
| pprint_pformat           | 1.30 sec                                               | 988 ms: 1.32x faster                                                   |
| pprint_safe_repr         | 641 ms                                                 | 485 ms: 1.32x faster                                                   |
| pyflate                  | 427 ms                                                 | 324 ms: 1.32x faster                                                   |
| spectral_norm            | 94.8 ms                                                | 72.1 ms: 1.31x faster                                                  |
| mypy2                    | 607 ms                                                 | 464 ms: 1.31x faster                                                   |
| django_template          | 26.4 ms                                                | 20.2 ms: 1.30x faster                                                  |
| json_dumps               | 8.11 ms                                                | 6.23 ms: 1.30x faster                                                  |
| sympy_sum                | 92.2 ms                                                | 70.9 ms: 1.30x faster                                                  |
| scimark_sor              | 128 ms                                                 | 99.3 ms: 1.29x faster                                                  |
| thrift                   | 572 us                                                 | 443 us: 1.29x faster                                                   |
| deepcopy                 | 272 us                                                 | 213 us: 1.28x faster                                                   |
| dulwich_log              | 35.3 ms                                                | 27.9 ms: 1.27x faster                                                  |
| sympy_integrate          | 13.1 ms                                                | 10.4 ms: 1.26x faster                                                  |
| xml_etree_process        | 46.5 ms                                                | 37.6 ms: 1.24x faster                                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.88 us: 1.24x faster                                                  |
| sympy_str                | 165 ms                                                 | 134 ms: 1.23x faster                                                   |
| coroutines               | 20.7 ms                                                | 16.9 ms: 1.23x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.22x faster                                                 |
| docutils                 | 1.73 sec                                               | 1.45 sec: 1.19x faster                                                 |
| fannkuch                 | 303 ms                                                 | 256 ms: 1.18x faster                                                   |
| sympy_expand             | 269 ms                                                 | 229 ms: 1.17x faster                                                   |
| regex_dna                | 174 ms                                                 | 150 ms: 1.17x faster                                                   |
| gunicorn                 | 1.30 ms                                                | 1.12 ms: 1.16x faster                                                  |
| genshi_text              | 17.3 ms                                                | 15.0 ms: 1.16x faster                                                  |
| dask                     | 253 ms                                                 | 221 ms: 1.15x faster                                                   |
| nqueens                  | 63.8 ms                                                | 55.6 ms: 1.15x faster                                                  |
| sqlglot_optimize         | 36.8 ms                                                | 32.2 ms: 1.14x faster                                                  |
| generators               | 32.3 ms                                                | 28.3 ms: 1.14x faster                                                  |
| aiohttp                  | 1.22 ms                                                | 1.08 ms: 1.14x faster                                                  |
| tornado_http             | 86.7 ms                                                | 76.6 ms: 1.13x faster                                                  |
| tomli_loads              | 1.71 sec                                               | 1.51 sec: 1.13x faster                                                 |
| scimark_fft              | 224 ms                                                 | 199 ms: 1.13x faster                                                   |
| bench_thread_pool        | 527 us                                                 | 470 us: 1.12x faster                                                   |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.07 ms: 1.12x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 173 ms: 1.10x faster                                                   |
| meteor_contest           | 77.7 ms                                                | 71.7 ms: 1.08x faster                                                  |
| genshi_xml               | 33.8 ms                                                | 31.4 ms: 1.08x faster                                                  |
| 2to3                     | 192 ms                                                 | 180 ms: 1.06x faster                                                   |
| mdp                      | 1.63 sec                                               | 1.54 sec: 1.06x faster                                                 |
| json                     | 3.08 ms                                                | 2.91 ms: 1.06x faster                                                  |
| xml_etree_parse          | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| pathlib                  | 24.5 ms                                                | 24.0 ms: 1.02x faster                                                  |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                                   |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.02x slower                                                  |
| xml_etree_generate       | 53.5 ms                                                | 55.1 ms: 1.03x slower                                                  |
| json_loads               | 16.4 us                                                | 17.0 us: 1.04x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.58 ms: 1.05x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.22 us: 1.05x slower                                                  |
| create_gc_cycles         | 860 us                                                 | 903 us: 1.05x slower                                                   |
| sqlite_synth             | 1.46 us                                                | 1.55 us: 1.07x slower                                                  |
| pickle                   | 6.97 us                                                | 7.45 us: 1.07x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.3 us: 1.08x slower                                                  |
| pickle_list              | 2.74 us                                                | 2.96 us: 1.08x slower                                                  |
| coverage                 | 41.5 ms                                                | 44.8 ms: 1.08x slower                                                  |
| unpickle_list            | 2.69 us                                                | 2.95 us: 1.10x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 44.0 ms: 1.18x slower                                                  |
| async_generators         | 231 ms                                                 | 287 ms: 1.24x slower                                                   |
| python_startup           | 10.9 ms                                                | 13.6 ms: 1.25x slower                                                  |
| telco                    | 3.49 ms                                                | 4.47 ms: 1.28x slower                                                  |
| python_startup_no_site   | 7.91 ms                                                | 10.8 ms: 1.36x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (2): pidigits, xml_etree_iterparse
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.14x