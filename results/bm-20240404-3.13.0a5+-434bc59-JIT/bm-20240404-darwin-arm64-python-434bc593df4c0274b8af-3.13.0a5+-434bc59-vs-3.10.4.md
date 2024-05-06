# Results vs. 3.10.4

- fork: python
- ref: 434bc593df4c0274b8af
- machine: darwin-arm64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 172 ms: 1.12x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.49 ms: 1.39x faster                                                  |
| docutils       | 1.73 sec                                               | 1.56 sec: 1.11x faster                                                 |
| html5lib       | 42.4 ms                                                | 34.6 ms: 1.22x faster                                                  |
| tornado_http   | 86.7 ms                                                | 77.3 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                  | 1.19x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 203 ms: 1.91x faster                                                   |
| async_tree_memoization  | 474 ms                                                 | 262 ms: 1.81x faster                                                   |
| async_tree_io           | 980 ms                                                 | 576 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 463 ms: 1.40x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.69x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.4 ms: 1.40x faster                                                  |
| nbody          | 93.0 ms                                                | 70.7 ms: 1.32x faster                                                  |
| Geometric mean | (ref)                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 157 ms: 1.11x faster                                                   |
| regex_compile  | 95.3 ms                                                | 85.6 ms: 1.11x faster                                                  |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.02x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.89 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 180 us: 1.56x faster                                                   |
| unpickle_pure_python | 194 us                                                 | 141 us: 1.38x faster                                                   |
| tomli_loads          | 1.71 sec                                               | 1.28 sec: 1.33x faster                                                 |
| json_dumps           | 8.11 ms                                                | 6.33 ms: 1.28x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 37.3 ms: 1.25x faster                                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 72.9 ms: 1.01x slower                                                  |
| xml_etree_generate   | 53.5 ms                                                | 54.7 ms: 1.02x slower                                                  |
| json_loads           | 16.4 us                                                | 16.9 us: 1.03x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.06x slower                                                  |
| pickle               | 6.97 us                                                | 7.45 us: 1.07x slower                                                  |
| pickle_list          | 2.74 us                                                | 2.97 us: 1.09x slower                                                  |
| unpickle             | 8.80 us                                                | 9.67 us: 1.10x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.3 ms: 1.23x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 11.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 9.87 ms                                                | 6.94 ms: 1.42x faster                                                  |
| genshi_text    | 17.3 ms                                                | 14.8 ms: 1.17x faster                                                  |
| genshi_xml     | 33.8 ms                                                | 31.5 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.21x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.1 us: 4.67x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.48 ms: 1.98x faster                                                  |
| async_tree_none          | 388 ms                                                 | 203 ms: 1.91x faster                                                   |
| raytrace                 | 301 ms                                                 | 163 ms: 1.85x faster                                                   |
| async_tree_memoization   | 474 ms                                                 | 262 ms: 1.81x faster                                                   |
| pylint                   | 277 ms                                                 | 154 ms: 1.80x faster                                                   |
| logging_silent           | 117 ns                                                 | 65.4 ns: 1.79x faster                                                  |
| richards_super           | 57.8 ms                                                | 32.9 ms: 1.76x faster                                                  |
| chaos                    | 65.8 ms                                                | 38.6 ms: 1.71x faster                                                  |
| async_tree_io            | 980 ms                                                 | 576 ms: 1.70x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 394 ms: 1.67x faster                                                   |
| richards                 | 48.7 ms                                                | 29.2 ms: 1.67x faster                                                  |
| sqlglot_parse            | 1.24 ms                                                | 765 us: 1.63x faster                                                   |
| pickle_pure_python       | 281 us                                                 | 180 us: 1.56x faster                                                   |
| crypto_pyaes             | 71.8 ms                                                | 46.5 ms: 1.54x faster                                                  |
| sqlglot_transpile        | 1.44 ms                                                | 939 us: 1.54x faster                                                   |
| scimark_monte_carlo      | 65.6 ms                                                | 43.8 ms: 1.50x faster                                                  |
| mypy2                    | 607 ms                                                 | 409 ms: 1.48x faster                                                   |
| deepcopy_memo            | 34.7 us                                                | 24.1 us: 1.44x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.12 us: 1.43x faster                                                  |
| mako                     | 9.87 ms                                                | 6.94 ms: 1.42x faster                                                  |
| go                       | 151 ms                                                 | 106 ms: 1.42x faster                                                   |
| comprehensions           | 16.9 us                                                | 12.0 us: 1.41x faster                                                  |
| logging_format           | 4.83 us                                                | 3.43 us: 1.41x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 463 ms: 1.40x faster                                                   |
| float                    | 69.0 ms                                                | 49.4 ms: 1.40x faster                                                  |
| chameleon                | 6.26 ms                                                | 4.49 ms: 1.39x faster                                                  |
| unpickle_pure_python     | 194 us                                                 | 141 us: 1.38x faster                                                   |
| pyflate                  | 427 ms                                                 | 316 ms: 1.35x faster                                                   |
| pycparser                | 877 ms                                                 | 654 ms: 1.34x faster                                                   |
| tomli_loads              | 1.71 sec                                               | 1.28 sec: 1.33x faster                                                 |
| nbody                    | 93.0 ms                                                | 70.7 ms: 1.32x faster                                                  |
| pprint_safe_repr         | 641 ms                                                 | 492 ms: 1.30x faster                                                   |
| pprint_pformat           | 1.30 sec                                               | 1.00 sec: 1.30x faster                                                 |
| hexiom                   | 6.19 ms                                                | 4.81 ms: 1.29x faster                                                  |
| spectral_norm            | 94.8 ms                                                | 73.7 ms: 1.29x faster                                                  |
| deepcopy                 | 272 us                                                 | 211 us: 1.29x faster                                                   |
| json_dumps               | 8.11 ms                                                | 6.33 ms: 1.28x faster                                                  |
| thrift                   | 572 us                                                 | 450 us: 1.27x faster                                                   |
| deepcopy_reduce          | 2.33 us                                                | 1.86 us: 1.25x faster                                                  |
| xml_etree_process        | 46.5 ms                                                | 37.3 ms: 1.25x faster                                                  |
| scimark_lu               | 103 ms                                                 | 82.7 ms: 1.24x faster                                                  |
| generators               | 32.3 ms                                                | 26.3 ms: 1.23x faster                                                  |
| html5lib                 | 42.4 ms                                                | 34.6 ms: 1.22x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.31 sec: 1.22x faster                                                 |
| coroutines               | 20.7 ms                                                | 17.0 ms: 1.22x faster                                                  |
| dulwich_log              | 35.3 ms                                                | 29.0 ms: 1.22x faster                                                  |
| scimark_sor              | 128 ms                                                 | 106 ms: 1.21x faster                                                   |
| sympy_sum                | 92.2 ms                                                | 76.6 ms: 1.20x faster                                                  |
| genshi_text              | 17.3 ms                                                | 14.8 ms: 1.17x faster                                                  |
| sympy_str                | 165 ms                                                 | 142 ms: 1.16x faster                                                   |
| fannkuch                 | 303 ms                                                 | 261 ms: 1.16x faster                                                   |
| sympy_integrate          | 13.1 ms                                                | 11.4 ms: 1.15x faster                                                  |
| dask                     | 253 ms                                                 | 221 ms: 1.14x faster                                                   |
| aiohttp                  | 1.22 ms                                                | 1.07 ms: 1.14x faster                                                  |
| sympy_expand             | 269 ms                                                 | 237 ms: 1.13x faster                                                   |
| tornado_http             | 86.7 ms                                                | 77.3 ms: 1.12x faster                                                  |
| scimark_fft              | 224 ms                                                 | 200 ms: 1.12x faster                                                   |
| 2to3                     | 192 ms                                                 | 172 ms: 1.12x faster                                                   |
| regex_dna                | 174 ms                                                 | 157 ms: 1.11x faster                                                   |
| regex_compile            | 95.3 ms                                                | 85.6 ms: 1.11x faster                                                  |
| docutils                 | 1.73 sec                                               | 1.56 sec: 1.11x faster                                                 |
| gunicorn                 | 1.30 ms                                                | 1.19 ms: 1.09x faster                                                  |
| sqlglot_optimize         | 36.8 ms                                                | 33.7 ms: 1.09x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 486 us: 1.09x faster                                                   |
| sqlglot_normalize        | 190 ms                                                 | 176 ms: 1.08x faster                                                   |
| genshi_xml               | 33.8 ms                                                | 31.5 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.20 ms: 1.07x faster                                                  |
| meteor_contest           | 77.7 ms                                                | 73.4 ms: 1.06x faster                                                  |
| nqueens                  | 63.8 ms                                                | 60.4 ms: 1.06x faster                                                  |
| json                     | 3.08 ms                                                | 2.95 ms: 1.05x faster                                                  |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                                 |
| xml_etree_iterparse      | 72.1 ms                                                | 72.9 ms: 1.01x slower                                                  |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.02x slower                                                  |
| pathlib                  | 24.5 ms                                                | 24.9 ms: 1.02x slower                                                  |
| xml_etree_generate       | 53.5 ms                                                | 54.7 ms: 1.02x slower                                                  |
| json_loads               | 16.4 us                                                | 16.9 us: 1.03x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                                  |
| create_gc_cycles         | 860 us                                                 | 901 us: 1.05x slower                                                   |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.06x slower                                                  |
| pickle                   | 6.97 us                                                | 7.45 us: 1.07x slower                                                  |
| pickle_list              | 2.74 us                                                | 2.97 us: 1.09x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.59 us: 1.09x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.67 us: 1.10x slower                                                  |
| coverage                 | 41.5 ms                                                | 46.9 ms: 1.13x slower                                                  |
| unpickle_list            | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.89 ms: 1.18x slower                                                  |
| python_startup           | 10.9 ms                                                | 13.3 ms: 1.23x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 46.3 ms: 1.24x slower                                                  |
| async_generators         | 231 ms                                                 | 299 ms: 1.29x slower                                                   |
| telco                    | 3.49 ms                                                | 4.65 ms: 1.33x slower                                                  |
| python_startup_no_site   | 7.91 ms                                                | 11.6 ms: 1.47x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, asyncio_websockets, pidigits
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.39x