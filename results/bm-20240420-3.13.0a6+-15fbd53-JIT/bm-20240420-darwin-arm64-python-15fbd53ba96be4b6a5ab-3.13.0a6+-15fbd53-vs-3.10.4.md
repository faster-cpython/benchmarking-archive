# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 168 ms: 1.14x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.47 ms: 1.40x faster                                                  |
| docutils       | 1.73 sec                                               | 1.49 sec: 1.16x faster                                                 |
| html5lib       | 42.4 ms                                                | 31.1 ms: 1.36x faster                                                  |
| tornado_http   | 86.7 ms                                                | 76.6 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 201 ms: 1.93x faster                                                   |
| async_tree_memoization  | 474 ms                                                 | 268 ms: 1.77x faster                                                   |
| async_tree_io           | 980 ms                                                 | 557 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 460 ms: 1.41x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.71x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 48.6 ms: 1.42x faster                                                  |
| nbody          | 93.0 ms                                                | 70.1 ms: 1.33x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| regex_compile  | 95.3 ms                                                | 83.3 ms: 1.14x faster                                                  |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.57 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 180 us: 1.56x faster                                                   |
| unpickle_pure_python | 194 us                                                 | 135 us: 1.44x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.26 sec: 1.35x faster                                                 |
| json_dumps           | 8.11 ms                                                | 6.35 ms: 1.28x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 36.7 ms: 1.27x faster                                                  |
| xml_etree_parse      | 108 ms                                                 | 97.8 ms: 1.10x faster                                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 67.7 ms: 1.07x faster                                                  |
| xml_etree_generate   | 53.5 ms                                                | 52.8 ms: 1.01x faster                                                  |
| json_loads           | 16.4 us                                                | 17.0 us: 1.04x slower                                                  |
| unpickle             | 8.80 us                                                | 9.18 us: 1.04x slower                                                  |
| pickle               | 6.97 us                                                | 7.43 us: 1.06x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| pickle_list          | 2.74 us                                                | 3.01 us: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.3 ms: 1.22x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 10.5 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.87 ms: 1.44x faster                                                  |
| django_template | 26.4 ms                                                | 20.4 ms: 1.29x faster                                                  |
| genshi_text     | 17.3 ms                                                | 14.6 ms: 1.19x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 30.8 ms: 1.10x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 68.1 us: 4.74x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.47 ms: 1.99x faster                                                  |
| async_tree_none          | 388 ms                                                 | 201 ms: 1.93x faster                                                   |
| raytrace                 | 301 ms                                                 | 163 ms: 1.85x faster                                                   |
| logging_silent           | 117 ns                                                 | 63.5 ns: 1.85x faster                                                  |
| async_tree_memoization   | 474 ms                                                 | 268 ms: 1.77x faster                                                   |
| richards_super           | 57.8 ms                                                | 32.8 ms: 1.77x faster                                                  |
| async_tree_io            | 980 ms                                                 | 557 ms: 1.76x faster                                                   |
| chaos                    | 65.8 ms                                                | 37.9 ms: 1.74x faster                                                  |
| richards                 | 48.7 ms                                                | 29.5 ms: 1.65x faster                                                  |
| sqlglot_parse            | 1.24 ms                                                | 758 us: 1.64x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 407 ms: 1.62x faster                                                   |
| pylint                   | 277 ms                                                 | 176 ms: 1.57x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 180 us: 1.56x faster                                                   |
| crypto_pyaes             | 71.8 ms                                                | 46.2 ms: 1.55x faster                                                  |
| sqlglot_transpile        | 1.44 ms                                                | 929 us: 1.55x faster                                                   |
| scimark_monte_carlo      | 65.6 ms                                                | 43.0 ms: 1.52x faster                                                  |
| mypy2                    | 607 ms                                                 | 402 ms: 1.51x faster                                                   |
| logging_simple           | 4.45 us                                                | 3.07 us: 1.45x faster                                                  |
| logging_format           | 4.83 us                                                | 3.34 us: 1.44x faster                                                  |
| deepcopy_memo            | 34.7 us                                                | 24.1 us: 1.44x faster                                                  |
| mako                     | 9.87 ms                                                | 6.87 ms: 1.44x faster                                                  |
| unpickle_pure_python     | 194 us                                                 | 135 us: 1.44x faster                                                   |
| comprehensions           | 16.9 us                                                | 11.8 us: 1.43x faster                                                  |
| go                       | 151 ms                                                 | 106 ms: 1.42x faster                                                   |
| float                    | 69.0 ms                                                | 48.6 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 460 ms: 1.41x faster                                                   |
| chameleon                | 6.26 ms                                                | 4.47 ms: 1.40x faster                                                  |
| html5lib                 | 42.4 ms                                                | 31.1 ms: 1.36x faster                                                  |
| pyflate                  | 427 ms                                                 | 314 ms: 1.36x faster                                                   |
| pycparser                | 877 ms                                                 | 645 ms: 1.36x faster                                                   |
| tomli_loads              | 1.71 sec                                               | 1.26 sec: 1.35x faster                                                 |
| nbody                    | 93.0 ms                                                | 70.1 ms: 1.33x faster                                                  |
| pprint_safe_repr         | 641 ms                                                 | 486 ms: 1.32x faster                                                   |
| hexiom                   | 6.19 ms                                                | 4.71 ms: 1.31x faster                                                  |
| pprint_pformat           | 1.30 sec                                               | 995 ms: 1.31x faster                                                   |
| thrift                   | 572 us                                                 | 437 us: 1.31x faster                                                   |
| django_template          | 26.4 ms                                                | 20.4 ms: 1.29x faster                                                  |
| spectral_norm            | 94.8 ms                                                | 73.7 ms: 1.29x faster                                                  |
| deepcopy                 | 272 us                                                 | 212 us: 1.28x faster                                                   |
| json_dumps               | 8.11 ms                                                | 6.35 ms: 1.28x faster                                                  |
| xml_etree_process        | 46.5 ms                                                | 36.7 ms: 1.27x faster                                                  |
| deepcopy_reduce          | 2.33 us                                                | 1.84 us: 1.26x faster                                                  |
| scimark_lu               | 103 ms                                                 | 81.6 ms: 1.26x faster                                                  |
| dulwich_log              | 35.3 ms                                                | 28.4 ms: 1.24x faster                                                  |
| sympy_sum                | 92.2 ms                                                | 74.8 ms: 1.23x faster                                                  |
| generators               | 32.3 ms                                                | 26.4 ms: 1.22x faster                                                  |
| scimark_sor              | 128 ms                                                 | 105 ms: 1.22x faster                                                   |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.21x faster                                                 |
| coroutines               | 20.7 ms                                                | 17.2 ms: 1.20x faster                                                  |
| genshi_text              | 17.3 ms                                                | 14.6 ms: 1.19x faster                                                  |
| sympy_str                | 165 ms                                                 | 139 ms: 1.19x faster                                                   |
| sympy_integrate          | 13.1 ms                                                | 11.2 ms: 1.18x faster                                                  |
| fannkuch                 | 303 ms                                                 | 258 ms: 1.17x faster                                                   |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| docutils                 | 1.73 sec                                               | 1.49 sec: 1.16x faster                                                 |
| sympy_expand             | 269 ms                                                 | 234 ms: 1.15x faster                                                   |
| dask                     | 253 ms                                                 | 221 ms: 1.15x faster                                                   |
| regex_compile            | 95.3 ms                                                | 83.3 ms: 1.14x faster                                                  |
| 2to3                     | 192 ms                                                 | 168 ms: 1.14x faster                                                   |
| tornado_http             | 86.7 ms                                                | 76.6 ms: 1.13x faster                                                  |
| scimark_fft              | 224 ms                                                 | 201 ms: 1.12x faster                                                   |
| sqlglot_optimize         | 36.8 ms                                                | 33.1 ms: 1.11x faster                                                  |
| xml_etree_parse          | 108 ms                                                 | 97.8 ms: 1.10x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 173 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.12 ms: 1.10x faster                                                  |
| genshi_xml               | 33.8 ms                                                | 30.8 ms: 1.10x faster                                                  |
| gunicorn                 | 1.30 ms                                                | 1.19 ms: 1.09x faster                                                  |
| aiohttp                  | 1.22 ms                                                | 1.12 ms: 1.09x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 487 us: 1.08x faster                                                   |
| nqueens                  | 63.8 ms                                                | 59.3 ms: 1.08x faster                                                  |
| xml_etree_iterparse      | 72.1 ms                                                | 67.7 ms: 1.07x faster                                                  |
| meteor_contest           | 77.7 ms                                                | 73.1 ms: 1.06x faster                                                  |
| json                     | 3.08 ms                                                | 2.91 ms: 1.06x faster                                                  |
| pathlib                  | 24.5 ms                                                | 23.5 ms: 1.04x faster                                                  |
| mdp                      | 1.63 sec                                               | 1.57 sec: 1.04x faster                                                 |
| xml_etree_generate       | 53.5 ms                                                | 52.8 ms: 1.01x faster                                                  |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                  |
| create_gc_cycles         | 860 us                                                 | 872 us: 1.01x slower                                                   |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                                  |
| json_loads               | 16.4 us                                                | 17.0 us: 1.04x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.18 us: 1.04x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.57 ms: 1.05x slower                                                  |
| pickle                   | 6.97 us                                                | 7.43 us: 1.06x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.57 us: 1.08x slower                                                  |
| unpickle_list            | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| pickle_list              | 2.74 us                                                | 3.01 us: 1.10x slower                                                  |
| coverage                 | 41.5 ms                                                | 46.4 ms: 1.12x slower                                                  |
| python_startup           | 10.9 ms                                                | 13.3 ms: 1.22x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 46.2 ms: 1.24x slower                                                  |
| async_generators         | 231 ms                                                 | 296 ms: 1.28x slower                                                   |
| telco                    | 3.49 ms                                                | 4.58 ms: 1.31x slower                                                  |
| python_startup_no_site   | 7.91 ms                                                | 10.5 ms: 1.32x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, pidigits
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.39x