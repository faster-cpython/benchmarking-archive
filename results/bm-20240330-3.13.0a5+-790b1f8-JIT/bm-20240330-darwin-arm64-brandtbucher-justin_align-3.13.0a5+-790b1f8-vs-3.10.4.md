# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: darwin-arm64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 173 ms: 1.11x faster                                                 |
| chameleon      | 6.26 ms                                                | 4.52 ms: 1.39x faster                                                |
| docutils       | 1.73 sec                                               | 1.55 sec: 1.11x faster                                               |
| html5lib       | 42.4 ms                                                | 33.5 ms: 1.26x faster                                                |
| tornado_http   | 86.7 ms                                                | 76.8 ms: 1.13x faster                                                |
| Geometric mean | (ref)                                                  | 1.19x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization  | 474 ms                                                 | 265 ms: 1.79x faster                                                 |
| async_tree_io           | 980 ms                                                 | 567 ms: 1.73x faster                                                 |
| async_tree_none         | 388 ms                                                 | 227 ms: 1.71x faster                                                 |
| async_tree_cpu_io_mixed | 649 ms                                                 | 462 ms: 1.41x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.65x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.3 ms: 1.40x faster                                                |
| nbody          | 93.0 ms                                                | 70.1 ms: 1.33x faster                                                |
| Geometric mean | (ref)                                                  | 1.23x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 79.6 ms: 1.20x faster                                                |
| regex_dna      | 174 ms                                                 | 152 ms: 1.15x faster                                                 |
| regex_v8       | 17.1 ms                                                | 17.1 ms: 1.01x faster                                                |
| regex_effbot   | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.53x faster                                                 |
| unpickle_pure_python | 194 us                                                 | 143 us: 1.36x faster                                                 |
| tomli_loads          | 1.71 sec                                               | 1.30 sec: 1.31x faster                                               |
| json_dumps           | 8.11 ms                                                | 6.32 ms: 1.28x faster                                                |
| xml_etree_process    | 46.5 ms                                                | 36.8 ms: 1.26x faster                                                |
| xml_etree_parse      | 108 ms                                                 | 105 ms: 1.02x faster                                                 |
| xml_etree_generate   | 53.5 ms                                                | 54.1 ms: 1.01x slower                                                |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                |
| unpickle             | 8.80 us                                                | 9.10 us: 1.03x slower                                                |
| pickle               | 6.97 us                                                | 7.41 us: 1.06x slower                                                |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                |
| pickle_list          | 2.74 us                                                | 2.98 us: 1.09x slower                                                |
| unpickle_list        | 2.69 us                                                | 3.06 us: 1.14x slower                                                |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.3 ms: 1.22x slower                                                |
| python_startup_no_site | 7.91 ms                                                | 11.6 ms: 1.46x slower                                                |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.92 ms: 1.43x faster                                                |
| django_template | 26.4 ms                                                | 20.7 ms: 1.28x faster                                                |
| genshi_text     | 17.3 ms                                                | 14.8 ms: 1.17x faster                                                |
| genshi_xml      | 33.8 ms                                                | 31.2 ms: 1.08x faster                                                |
| Geometric mean  | (ref)                                                  | 1.23x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.7 us: 4.63x faster                                                |
| deltablue                | 4.91 ms                                                | 2.35 ms: 2.09x faster                                                |
| async_tree_memoization   | 474 ms                                                 | 265 ms: 1.79x faster                                                 |
| logging_silent           | 117 ns                                                 | 65.7 ns: 1.78x faster                                                |
| pylint                   | 277 ms                                                 | 156 ms: 1.77x faster                                                 |
| async_tree_io            | 980 ms                                                 | 567 ms: 1.73x faster                                                 |
| chaos                    | 65.8 ms                                                | 38.3 ms: 1.72x faster                                                |
| async_tree_none          | 388 ms                                                 | 227 ms: 1.71x faster                                                 |
| raytrace                 | 301 ms                                                 | 178 ms: 1.69x faster                                                 |
| richards_super           | 57.8 ms                                                | 34.5 ms: 1.68x faster                                                |
| sqlglot_parse            | 1.24 ms                                                | 765 us: 1.63x faster                                                 |
| richards                 | 48.7 ms                                                | 31.2 ms: 1.56x faster                                                |
| sqlglot_transpile        | 1.44 ms                                                | 935 us: 1.54x faster                                                 |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.53x faster                                                 |
| crypto_pyaes             | 71.8 ms                                                | 46.9 ms: 1.53x faster                                                |
| asyncio_tcp              | 659 ms                                                 | 431 ms: 1.53x faster                                                 |
| scimark_monte_carlo      | 65.6 ms                                                | 43.8 ms: 1.50x faster                                                |
| mypy2                    | 607 ms                                                 | 410 ms: 1.48x faster                                                 |
| go                       | 151 ms                                                 | 104 ms: 1.45x faster                                                 |
| deepcopy_memo            | 34.7 us                                                | 24.2 us: 1.43x faster                                                |
| mako                     | 9.87 ms                                                | 6.92 ms: 1.43x faster                                                |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 462 ms: 1.41x faster                                                 |
| float                    | 69.0 ms                                                | 49.3 ms: 1.40x faster                                                |
| comprehensions           | 16.9 us                                                | 12.1 us: 1.40x faster                                                |
| chameleon                | 6.26 ms                                                | 4.52 ms: 1.39x faster                                                |
| logging_simple           | 4.45 us                                                | 3.27 us: 1.36x faster                                                |
| unpickle_pure_python     | 194 us                                                 | 143 us: 1.36x faster                                                 |
| logging_format           | 4.83 us                                                | 3.59 us: 1.35x faster                                                |
| nbody                    | 93.0 ms                                                | 70.1 ms: 1.33x faster                                                |
| pycparser                | 877 ms                                                 | 661 ms: 1.33x faster                                                 |
| pprint_safe_repr         | 641 ms                                                 | 483 ms: 1.33x faster                                                 |
| pprint_pformat           | 1.30 sec                                               | 986 ms: 1.32x faster                                                 |
| tomli_loads              | 1.71 sec                                               | 1.30 sec: 1.31x faster                                               |
| thrift                   | 572 us                                                 | 437 us: 1.31x faster                                                 |
| pyflate                  | 427 ms                                                 | 328 ms: 1.30x faster                                                 |
| spectral_norm            | 94.8 ms                                                | 73.8 ms: 1.28x faster                                                |
| json_dumps               | 8.11 ms                                                | 6.32 ms: 1.28x faster                                                |
| deepcopy                 | 272 us                                                 | 212 us: 1.28x faster                                                 |
| django_template          | 26.4 ms                                                | 20.7 ms: 1.28x faster                                                |
| xml_etree_process        | 46.5 ms                                                | 36.8 ms: 1.26x faster                                                |
| html5lib                 | 42.4 ms                                                | 33.5 ms: 1.26x faster                                                |
| hexiom                   | 6.19 ms                                                | 4.91 ms: 1.26x faster                                                |
| deepcopy_reduce          | 2.33 us                                                | 1.86 us: 1.25x faster                                                |
| scimark_lu               | 103 ms                                                 | 82.4 ms: 1.25x faster                                                |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.30 sec: 1.23x faster                                               |
| coroutines               | 20.7 ms                                                | 16.9 ms: 1.23x faster                                                |
| generators               | 32.3 ms                                                | 26.4 ms: 1.23x faster                                                |
| sympy_sum                | 92.2 ms                                                | 75.5 ms: 1.22x faster                                                |
| regex_compile            | 95.3 ms                                                | 79.6 ms: 1.20x faster                                                |
| scimark_sor              | 128 ms                                                 | 108 ms: 1.19x faster                                                 |
| sympy_str                | 165 ms                                                 | 140 ms: 1.18x faster                                                 |
| dulwich_log              | 35.3 ms                                                | 30.0 ms: 1.18x faster                                                |
| genshi_text              | 17.3 ms                                                | 14.8 ms: 1.17x faster                                                |
| fannkuch                 | 303 ms                                                 | 259 ms: 1.17x faster                                                 |
| sympy_integrate          | 13.1 ms                                                | 11.3 ms: 1.16x faster                                                |
| regex_dna                | 174 ms                                                 | 152 ms: 1.15x faster                                                 |
| dask                     | 253 ms                                                 | 221 ms: 1.15x faster                                                 |
| sympy_expand             | 269 ms                                                 | 236 ms: 1.14x faster                                                 |
| tornado_http             | 86.7 ms                                                | 76.8 ms: 1.13x faster                                                |
| docutils                 | 1.73 sec                                               | 1.55 sec: 1.11x faster                                               |
| scimark_fft              | 224 ms                                                 | 202 ms: 1.11x faster                                                 |
| gunicorn                 | 1.30 ms                                                | 1.17 ms: 1.11x faster                                                |
| 2to3                     | 192 ms                                                 | 173 ms: 1.11x faster                                                 |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.12 ms: 1.10x faster                                                |
| aiohttp                  | 1.22 ms                                                | 1.12 ms: 1.09x faster                                                |
| sqlglot_optimize         | 36.8 ms                                                | 33.6 ms: 1.09x faster                                                |
| genshi_xml               | 33.8 ms                                                | 31.2 ms: 1.08x faster                                                |
| sqlglot_normalize        | 190 ms                                                 | 176 ms: 1.08x faster                                                 |
| bench_thread_pool        | 527 us                                                 | 492 us: 1.07x faster                                                 |
| meteor_contest           | 77.7 ms                                                | 73.9 ms: 1.05x faster                                                |
| nqueens                  | 63.8 ms                                                | 60.9 ms: 1.05x faster                                                |
| json                     | 3.08 ms                                                | 2.97 ms: 1.04x faster                                                |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                               |
| xml_etree_parse          | 108 ms                                                 | 105 ms: 1.02x faster                                                 |
| pathlib                  | 24.5 ms                                                | 24.0 ms: 1.02x faster                                                |
| create_gc_cycles         | 860 us                                                 | 844 us: 1.02x faster                                                 |
| regex_v8                 | 17.1 ms                                                | 17.1 ms: 1.01x faster                                                |
| xml_etree_generate       | 53.5 ms                                                | 54.1 ms: 1.01x slower                                                |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                |
| unpickle                 | 8.80 us                                                | 9.10 us: 1.03x slower                                                |
| gc_traversal             | 2.36 ms                                                | 2.45 ms: 1.03x slower                                                |
| pickle                   | 6.97 us                                                | 7.41 us: 1.06x slower                                                |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                |
| regex_effbot             | 2.46 ms                                                | 2.62 ms: 1.07x slower                                                |
| sqlite_synth             | 1.46 us                                                | 1.58 us: 1.08x slower                                                |
| pickle_list              | 2.74 us                                                | 2.98 us: 1.09x slower                                                |
| coverage                 | 41.5 ms                                                | 47.0 ms: 1.13x slower                                                |
| unpickle_list            | 2.69 us                                                | 3.06 us: 1.14x slower                                                |
| python_startup           | 10.9 ms                                                | 13.3 ms: 1.22x slower                                                |
| bench_mp_pool            | 37.4 ms                                                | 46.4 ms: 1.24x slower                                                |
| telco                    | 3.49 ms                                                | 4.54 ms: 1.30x slower                                                |
| async_generators         | 231 ms                                                 | 302 ms: 1.30x slower                                                 |
| python_startup_no_site   | 7.91 ms                                                | 11.6 ms: 1.46x slower                                                |
| unpack_sequence          | 39.0 ns                                                | 115 ns: 2.95x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.20x faster                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, pidigits, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (12) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.40x