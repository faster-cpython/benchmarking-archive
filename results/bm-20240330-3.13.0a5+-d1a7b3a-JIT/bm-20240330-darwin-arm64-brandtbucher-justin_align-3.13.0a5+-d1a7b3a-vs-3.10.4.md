# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: darwin-arm64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 174 ms: 1.10x faster                                                 |
| chameleon      | 6.26 ms                                                | 4.47 ms: 1.40x faster                                                |
| docutils       | 1.73 sec                                               | 1.55 sec: 1.12x faster                                               |
| html5lib       | 42.4 ms                                                | 33.4 ms: 1.27x faster                                                |
| tornado_http   | 86.7 ms                                                | 76.9 ms: 1.13x faster                                                |
| Geometric mean | (ref)                                                  | 1.20x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization  | 474 ms                                                 | 265 ms: 1.79x faster                                                 |
| async_tree_io           | 980 ms                                                 | 565 ms: 1.73x faster                                                 |
| async_tree_none         | 388 ms                                                 | 227 ms: 1.71x faster                                                 |
| async_tree_cpu_io_mixed | 649 ms                                                 | 461 ms: 1.41x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.65x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.2 ms: 1.40x faster                                                |
| nbody          | 93.0 ms                                                | 70.2 ms: 1.33x faster                                                |
| Geometric mean | (ref)                                                  | 1.23x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 79.5 ms: 1.20x faster                                                |
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                                 |
| regex_v8       | 17.1 ms                                                | 17.1 ms: 1.00x faster                                                |
| regex_effbot   | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.53x faster                                                 |
| unpickle_pure_python | 194 us                                                 | 143 us: 1.36x faster                                                 |
| tomli_loads          | 1.71 sec                                               | 1.29 sec: 1.32x faster                                               |
| json_dumps           | 8.11 ms                                                | 6.35 ms: 1.28x faster                                                |
| xml_etree_process    | 46.5 ms                                                | 37.1 ms: 1.25x faster                                                |
| xml_etree_parse      | 108 ms                                                 | 106 ms: 1.02x faster                                                 |
| xml_etree_generate   | 53.5 ms                                                | 54.1 ms: 1.01x slower                                                |
| unpickle             | 8.80 us                                                | 9.11 us: 1.04x slower                                                |
| json_loads           | 16.4 us                                                | 17.0 us: 1.04x slower                                                |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.06x slower                                                |
| pickle               | 6.97 us                                                | 7.45 us: 1.07x slower                                                |
| pickle_list          | 2.74 us                                                | 2.97 us: 1.08x slower                                                |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.13x slower                                                |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.4 ms: 1.23x slower                                                |
| python_startup_no_site | 7.91 ms                                                | 11.7 ms: 1.48x slower                                                |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.94 ms: 1.42x faster                                                |
| django_template | 26.4 ms                                                | 20.7 ms: 1.27x faster                                                |
| genshi_text     | 17.3 ms                                                | 14.8 ms: 1.18x faster                                                |
| genshi_xml      | 33.8 ms                                                | 31.2 ms: 1.08x faster                                                |
| Geometric mean  | (ref)                                                  | 1.23x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.8 us: 4.63x faster                                                |
| deltablue                | 4.91 ms                                                | 2.35 ms: 2.09x faster                                                |
| async_tree_memoization   | 474 ms                                                 | 265 ms: 1.79x faster                                                 |
| logging_silent           | 117 ns                                                 | 65.7 ns: 1.78x faster                                                |
| pylint                   | 277 ms                                                 | 156 ms: 1.77x faster                                                 |
| async_tree_io            | 980 ms                                                 | 565 ms: 1.73x faster                                                 |
| chaos                    | 65.8 ms                                                | 38.4 ms: 1.71x faster                                                |
| async_tree_none          | 388 ms                                                 | 227 ms: 1.71x faster                                                 |
| raytrace                 | 301 ms                                                 | 178 ms: 1.69x faster                                                 |
| richards_super           | 57.8 ms                                                | 34.9 ms: 1.66x faster                                                |
| sqlglot_parse            | 1.24 ms                                                | 766 us: 1.62x faster                                                 |
| asyncio_tcp              | 659 ms                                                 | 425 ms: 1.55x faster                                                 |
| richards                 | 48.7 ms                                                | 31.4 ms: 1.55x faster                                                |
| sqlglot_transpile        | 1.44 ms                                                | 935 us: 1.54x faster                                                 |
| crypto_pyaes             | 71.8 ms                                                | 46.7 ms: 1.54x faster                                                |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.53x faster                                                 |
| scimark_monte_carlo      | 65.6 ms                                                | 43.8 ms: 1.50x faster                                                |
| mypy2                    | 607 ms                                                 | 410 ms: 1.48x faster                                                 |
| go                       | 151 ms                                                 | 104 ms: 1.45x faster                                                 |
| deepcopy_memo            | 34.7 us                                                | 24.2 us: 1.43x faster                                                |
| mako                     | 9.87 ms                                                | 6.94 ms: 1.42x faster                                                |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 461 ms: 1.41x faster                                                 |
| float                    | 69.0 ms                                                | 49.2 ms: 1.40x faster                                                |
| comprehensions           | 16.9 us                                                | 12.1 us: 1.40x faster                                                |
| chameleon                | 6.26 ms                                                | 4.47 ms: 1.40x faster                                                |
| unpickle_pure_python     | 194 us                                                 | 143 us: 1.36x faster                                                 |
| logging_simple           | 4.45 us                                                | 3.27 us: 1.36x faster                                                |
| logging_format           | 4.83 us                                                | 3.57 us: 1.35x faster                                                |
| pprint_safe_repr         | 641 ms                                                 | 483 ms: 1.33x faster                                                 |
| nbody                    | 93.0 ms                                                | 70.2 ms: 1.33x faster                                                |
| thrift                   | 572 us                                                 | 432 us: 1.32x faster                                                 |
| pycparser                | 877 ms                                                 | 662 ms: 1.32x faster                                                 |
| pprint_pformat           | 1.30 sec                                               | 987 ms: 1.32x faster                                                 |
| tomli_loads              | 1.71 sec                                               | 1.29 sec: 1.32x faster                                               |
| pyflate                  | 427 ms                                                 | 328 ms: 1.30x faster                                                 |
| spectral_norm            | 94.8 ms                                                | 73.8 ms: 1.28x faster                                                |
| json_dumps               | 8.11 ms                                                | 6.35 ms: 1.28x faster                                                |
| django_template          | 26.4 ms                                                | 20.7 ms: 1.27x faster                                                |
| deepcopy                 | 272 us                                                 | 213 us: 1.27x faster                                                 |
| html5lib                 | 42.4 ms                                                | 33.4 ms: 1.27x faster                                                |
| hexiom                   | 6.19 ms                                                | 4.92 ms: 1.26x faster                                                |
| scimark_lu               | 103 ms                                                 | 81.9 ms: 1.26x faster                                                |
| xml_etree_process        | 46.5 ms                                                | 37.1 ms: 1.25x faster                                                |
| deepcopy_reduce          | 2.33 us                                                | 1.86 us: 1.25x faster                                                |
| coroutines               | 20.7 ms                                                | 16.7 ms: 1.24x faster                                                |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.30 sec: 1.23x faster                                               |
| generators               | 32.3 ms                                                | 26.4 ms: 1.22x faster                                                |
| sympy_sum                | 92.2 ms                                                | 75.7 ms: 1.22x faster                                                |
| regex_compile            | 95.3 ms                                                | 79.5 ms: 1.20x faster                                                |
| scimark_sor              | 128 ms                                                 | 108 ms: 1.19x faster                                                 |
| sympy_str                | 165 ms                                                 | 140 ms: 1.18x faster                                                 |
| genshi_text              | 17.3 ms                                                | 14.8 ms: 1.18x faster                                                |
| dulwich_log              | 35.3 ms                                                | 30.1 ms: 1.17x faster                                                |
| fannkuch                 | 303 ms                                                 | 260 ms: 1.16x faster                                                 |
| sympy_integrate          | 13.1 ms                                                | 11.3 ms: 1.16x faster                                                |
| dask                     | 253 ms                                                 | 221 ms: 1.15x faster                                                 |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                                 |
| sympy_expand             | 269 ms                                                 | 237 ms: 1.14x faster                                                 |
| aiohttp                  | 1.22 ms                                                | 1.08 ms: 1.13x faster                                                |
| tornado_http             | 86.7 ms                                                | 76.9 ms: 1.13x faster                                                |
| scimark_fft              | 224 ms                                                 | 200 ms: 1.12x faster                                                 |
| docutils                 | 1.73 sec                                               | 1.55 sec: 1.12x faster                                               |
| 2to3                     | 192 ms                                                 | 174 ms: 1.10x faster                                                 |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.12 ms: 1.10x faster                                                |
| sqlglot_optimize         | 36.8 ms                                                | 33.6 ms: 1.09x faster                                                |
| genshi_xml               | 33.8 ms                                                | 31.2 ms: 1.08x faster                                                |
| sqlglot_normalize        | 190 ms                                                 | 176 ms: 1.08x faster                                                 |
| gunicorn                 | 1.30 ms                                                | 1.20 ms: 1.08x faster                                                |
| bench_thread_pool        | 527 us                                                 | 493 us: 1.07x faster                                                 |
| meteor_contest           | 77.7 ms                                                | 73.9 ms: 1.05x faster                                                |
| nqueens                  | 63.8 ms                                                | 60.7 ms: 1.05x faster                                                |
| mdp                      | 1.63 sec                                               | 1.57 sec: 1.04x faster                                               |
| json                     | 3.08 ms                                                | 3.03 ms: 1.02x faster                                                |
| xml_etree_parse          | 108 ms                                                 | 106 ms: 1.02x faster                                                 |
| create_gc_cycles         | 860 us                                                 | 848 us: 1.01x faster                                                 |
| regex_v8                 | 17.1 ms                                                | 17.1 ms: 1.00x faster                                                |
| xml_etree_generate       | 53.5 ms                                                | 54.1 ms: 1.01x slower                                                |
| pathlib                  | 24.5 ms                                                | 24.9 ms: 1.02x slower                                                |
| unpickle                 | 8.80 us                                                | 9.11 us: 1.04x slower                                                |
| json_loads               | 16.4 us                                                | 17.0 us: 1.04x slower                                                |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.04x slower                                                |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.06x slower                                                |
| regex_effbot             | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                |
| pickle                   | 6.97 us                                                | 7.45 us: 1.07x slower                                                |
| pickle_list              | 2.74 us                                                | 2.97 us: 1.08x slower                                                |
| sqlite_synth             | 1.46 us                                                | 1.59 us: 1.09x slower                                                |
| coverage                 | 41.5 ms                                                | 46.4 ms: 1.12x slower                                                |
| unpickle_list            | 2.69 us                                                | 3.05 us: 1.13x slower                                                |
| python_startup           | 10.9 ms                                                | 13.4 ms: 1.23x slower                                                |
| bench_mp_pool            | 37.4 ms                                                | 46.5 ms: 1.24x slower                                                |
| async_generators         | 231 ms                                                 | 299 ms: 1.29x slower                                                 |
| telco                    | 3.49 ms                                                | 4.54 ms: 1.30x slower                                                |
| python_startup_no_site   | 7.91 ms                                                | 11.7 ms: 1.48x slower                                                |
| unpack_sequence          | 39.0 ns                                                | 115 ns: 2.94x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.20x faster                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, pidigits, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (12) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.40x