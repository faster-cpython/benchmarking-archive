# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 281 ms: 1.24x faster                                                 |
| chameleon      | 9.68 ms                                                | 7.22 ms: 1.34x faster                                                |
| docutils       | 3.30 sec                                               | 2.91 sec: 1.13x faster                                               |
| html5lib       | 88.9 ms                                                | 66.7 ms: 1.33x faster                                                |
| tornado_http   | 136 ms                                                 | 97.5 ms: 1.40x faster                                                |
| Geometric mean | (ref)                                                  | 1.29x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 952 ms: 1.86x faster                                                 |
| async_tree_none         | 728 ms                                                 | 394 ms: 1.85x faster                                                 |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 603 ms: 1.69x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.82x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 93.6 ms: 1.64x faster                                                |
| float          | 117 ms                                                 | 78.4 ms: 1.49x faster                                                |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.35x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 153 ms: 1.23x faster                                                 |
| regex_v8       | 27.8 ms                                                | 25.1 ms: 1.10x faster                                                |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                 |
| regex_effbot   | 3.63 ms                                                | 3.82 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 306 us: 1.58x faster                                                 |
| tomli_loads          | 3.14 sec                                               | 2.18 sec: 1.44x faster                                               |
| unpickle_pure_python | 331 us                                                 | 251 us: 1.32x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.32x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.30x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                 |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                 |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                                |
| unpickle             | 14.4 us                                                | 15.2 us: 1.05x slower                                                |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                |
| pickle_dict          | 29.6 us                                                | 34.1 us: 1.15x slower                                                |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                         |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 9.51 ms: 1.60x slower                                                |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.4 ms: 1.44x faster                                                |
| django_template | 48.2 ms                                                | 36.1 ms: 1.33x faster                                                |
| genshi_text     | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                |
| genshi_xml      | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                |
| Geometric mean  | (ref)                                                  | 1.30x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.79x faster                                                 |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                |
| deltablue                | 7.91 ms                                                | 3.50 ms: 2.26x faster                                                |
| logging_silent           | 190 ns                                                 | 99.6 ns: 1.90x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                 |
| async_tree_io            | 1.77 sec                                               | 952 ms: 1.86x faster                                                 |
| async_tree_none          | 728 ms                                                 | 394 ms: 1.85x faster                                                 |
| pylint                   | 551 ms                                                 | 300 ms: 1.84x faster                                                 |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                 |
| chaos                    | 115 ms                                                 | 64.4 ms: 1.79x faster                                                |
| richards_super           | 94.7 ms                                                | 54.6 ms: 1.74x faster                                                |
| raytrace                 | 507 ms                                                 | 296 ms: 1.71x faster                                                 |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 603 ms: 1.69x faster                                                 |
| crypto_pyaes             | 128 ms                                                 | 77.1 ms: 1.66x faster                                                |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                 |
| nbody                    | 154 ms                                                 | 93.6 ms: 1.64x faster                                                |
| richards                 | 79.3 ms                                                | 48.7 ms: 1.63x faster                                                |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.63x faster                                                |
| scimark_monte_carlo      | 118 ms                                                 | 73.3 ms: 1.61x faster                                                |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.58x faster                                                 |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                                |
| go                       | 240 ms                                                 | 159 ms: 1.51x faster                                                 |
| comprehensions           | 28.8 us                                                | 19.3 us: 1.49x faster                                                |
| float                    | 117 ms                                                 | 78.4 ms: 1.49x faster                                                |
| deepcopy_memo            | 58.5 us                                                | 40.0 us: 1.46x faster                                                |
| tomli_loads              | 3.14 sec                                               | 2.18 sec: 1.44x faster                                               |
| mako                     | 16.3 ms                                                | 11.4 ms: 1.44x faster                                                |
| pyflate                  | 716 ms                                                 | 505 ms: 1.42x faster                                                 |
| spectral_norm            | 170 ms                                                 | 121 ms: 1.40x faster                                                 |
| tornado_http             | 136 ms                                                 | 97.5 ms: 1.40x faster                                                |
| logging_simple           | 8.30 us                                                | 5.98 us: 1.39x faster                                                |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                               |
| logging_format           | 9.09 us                                                | 6.55 us: 1.39x faster                                                |
| hexiom                   | 10.4 ms                                                | 7.56 ms: 1.38x faster                                                |
| chameleon                | 9.68 ms                                                | 7.22 ms: 1.34x faster                                                |
| django_template          | 48.2 ms                                                | 36.1 ms: 1.33x faster                                                |
| html5lib                 | 88.9 ms                                                | 66.7 ms: 1.33x faster                                                |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.33x faster                                               |
| unpickle_pure_python     | 331 us                                                 | 251 us: 1.32x faster                                                 |
| deepcopy                 | 479 us                                                 | 364 us: 1.32x faster                                                 |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.32x faster                                                |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                |
| scimark_lu               | 176 ms                                                 | 134 ms: 1.31x faster                                                 |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.30x faster                                                |
| scimark_fft              | 466 ms                                                 | 357 ms: 1.30x faster                                                 |
| pprint_pformat           | 2.10 sec                                               | 1.61 sec: 1.30x faster                                               |
| thrift                   | 1.07 ms                                                | 823 us: 1.30x faster                                                 |
| fannkuch                 | 532 ms                                                 | 411 ms: 1.29x faster                                                 |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                |
| pprint_safe_repr         | 1.02 sec                                               | 798 ms: 1.28x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.09 ms: 1.27x faster                                                |
| genshi_text              | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                                 |
| 2to3                     | 348 ms                                                 | 281 ms: 1.24x faster                                                 |
| regex_compile            | 188 ms                                                 | 153 ms: 1.23x faster                                                 |
| djangocms                | 38.4 us                                                | 31.8 us: 1.21x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 57.8 ms: 1.20x faster                                                |
| genshi_xml               | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                |
| dulwich_log              | 84.3 ms                                                | 71.4 ms: 1.18x faster                                                |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.18x faster                                                 |
| sympy_str                | 346 ms                                                 | 294 ms: 1.18x faster                                                 |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                                |
| dask                     | 441 ms                                                 | 377 ms: 1.17x faster                                                 |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                                |
| bench_thread_pool        | 986 us                                                 | 857 us: 1.15x faster                                                 |
| sympy_expand             | 566 ms                                                 | 499 ms: 1.13x faster                                                 |
| nqueens                  | 106 ms                                                 | 93.4 ms: 1.13x faster                                                |
| docutils                 | 3.30 sec                                               | 2.91 sec: 1.13x faster                                               |
| xml_etree_generate       | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                |
| mypy2                    | 894 ms                                                 | 792 ms: 1.13x faster                                                 |
| regex_v8                 | 27.8 ms                                                | 25.1 ms: 1.10x faster                                                |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                |
| mdp                      | 2.85 sec                                               | 2.66 sec: 1.07x faster                                               |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                 |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                                 |
| pathlib                  | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                |
| sqlite_synth             | 3.02 us                                                | 2.85 us: 1.06x faster                                                |
| json                     | 5.69 ms                                                | 5.36 ms: 1.06x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                 |
| pickle_list              | 5.08 us                                                | 4.96 us: 1.02x faster                                                |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                 |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                 |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                                 |
| gc_traversal             | 3.62 ms                                                | 3.71 ms: 1.02x slower                                                |
| create_gc_cycles         | 1.62 ms                                                | 1.66 ms: 1.03x slower                                                |
| async_generators         | 444 ms                                                 | 462 ms: 1.04x slower                                                 |
| regex_effbot             | 3.63 ms                                                | 3.82 ms: 1.05x slower                                                |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.05x slower                                                |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                |
| pickle_dict              | 29.6 us                                                | 34.1 us: 1.15x slower                                                |
| telco                    | 7.27 ms                                                | 8.68 ms: 1.19x slower                                                |
| coverage                 | 79.4 ms                                                | 97.8 ms: 1.23x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 9.51 ms: 1.60x slower                                                |
| unpack_sequence          | 60.0 ns                                                | 125 ns: 2.08x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.29x faster                                                         |

Benchmark hidden because not significant (2): bench_mp_pool, unpickle_list
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.19x