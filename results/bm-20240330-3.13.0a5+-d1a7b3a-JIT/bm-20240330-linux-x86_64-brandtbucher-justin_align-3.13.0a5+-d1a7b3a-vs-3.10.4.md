# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 280 ms: 1.25x faster                                                 |
| chameleon      | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                               |
| html5lib       | 88.9 ms                                                | 68.6 ms: 1.30x faster                                                |
| tornado_http   | 136 ms                                                 | 97.3 ms: 1.40x faster                                                |
| Geometric mean | (ref)                                                  | 1.29x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.90x faster                                                 |
| async_tree_none         | 728 ms                                                 | 392 ms: 1.86x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 955 ms: 1.85x faster                                                 |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 603 ms: 1.69x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.82x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.4 ms: 1.66x faster                                                |
| float          | 117 ms                                                 | 77.2 ms: 1.52x faster                                                |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.37x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 146 ms: 1.29x faster                                                 |
| regex_v8       | 27.8 ms                                                | 25.6 ms: 1.08x faster                                                |
| regex_dna      | 227 ms                                                 | 231 ms: 1.02x slower                                                 |
| regex_effbot   | 3.63 ms                                                | 3.87 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 309 us: 1.57x faster                                                 |
| tomli_loads          | 3.14 sec                                               | 2.10 sec: 1.49x faster                                               |
| unpickle_pure_python | 331 us                                                 | 240 us: 1.38x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 89.2 ms: 1.11x faster                                                |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                 |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.05x faster                                                 |
| unpickle_list        | 5.20 us                                                | 5.06 us: 1.03x faster                                                |
| pickle_list          | 5.08 us                                                | 5.37 us: 1.06x slower                                                |
| unpickle             | 14.4 us                                                | 15.6 us: 1.09x slower                                                |
| pickle               | 10.7 us                                                | 12.5 us: 1.17x slower                                                |
| pickle_dict          | 29.6 us                                                | 35.3 us: 1.19x slower                                                |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 9.55 ms: 1.61x slower                                                |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.8 ms: 1.50x faster                                                |
| django_template | 48.2 ms                                                | 35.8 ms: 1.34x faster                                                |
| genshi_text     | 31.8 ms                                                | 24.6 ms: 1.29x faster                                                |
| genshi_xml      | 66.0 ms                                                | 55.3 ms: 1.19x faster                                                |
| Geometric mean  | (ref)                                                  | 1.33x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.75x faster                                                 |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                |
| deltablue                | 7.91 ms                                                | 3.52 ms: 2.25x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.90x faster                                                 |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                 |
| async_tree_none          | 728 ms                                                 | 392 ms: 1.86x faster                                                 |
| async_tree_io            | 1.77 sec                                               | 955 ms: 1.85x faster                                                 |
| pylint                   | 551 ms                                                 | 299 ms: 1.85x faster                                                 |
| chaos                    | 115 ms                                                 | 63.0 ms: 1.83x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                 |
| richards_super           | 94.7 ms                                                | 53.3 ms: 1.78x faster                                                |
| raytrace                 | 507 ms                                                 | 294 ms: 1.72x faster                                                 |
| crypto_pyaes             | 128 ms                                                 | 74.4 ms: 1.72x faster                                                |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 603 ms: 1.69x faster                                                 |
| richards                 | 79.3 ms                                                | 47.5 ms: 1.67x faster                                                |
| scimark_monte_carlo      | 118 ms                                                 | 70.9 ms: 1.67x faster                                                |
| nbody                    | 154 ms                                                 | 92.4 ms: 1.66x faster                                                |
| scimark_sor              | 220 ms                                                 | 133 ms: 1.65x faster                                                 |
| sqlglot_parse            | 2.17 ms                                                | 1.35 ms: 1.61x faster                                                |
| comprehensions           | 28.8 us                                                | 18.3 us: 1.57x faster                                                |
| pickle_pure_python       | 484 us                                                 | 309 us: 1.57x faster                                                 |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                                |
| go                       | 240 ms                                                 | 157 ms: 1.53x faster                                                 |
| float                    | 117 ms                                                 | 77.2 ms: 1.52x faster                                                |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.50x faster                                                |
| tomli_loads              | 3.14 sec                                               | 2.10 sec: 1.49x faster                                               |
| deepcopy_memo            | 58.5 us                                                | 39.6 us: 1.48x faster                                                |
| pyflate                  | 716 ms                                                 | 493 ms: 1.45x faster                                                 |
| spectral_norm            | 170 ms                                                 | 117 ms: 1.45x faster                                                 |
| hexiom                   | 10.4 ms                                                | 7.24 ms: 1.44x faster                                                |
| tornado_http             | 136 ms                                                 | 97.3 ms: 1.40x faster                                                |
| logging_simple           | 8.30 us                                                | 5.94 us: 1.40x faster                                                |
| logging_format           | 9.09 us                                                | 6.53 us: 1.39x faster                                                |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                               |
| chameleon                | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.38x faster                                               |
| unpickle_pure_python     | 331 us                                                 | 240 us: 1.38x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 746 ms: 1.36x faster                                                 |
| scimark_fft              | 466 ms                                                 | 343 ms: 1.36x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.80 ms: 1.35x faster                                                |
| django_template          | 48.2 ms                                                | 35.8 ms: 1.34x faster                                                |
| fannkuch                 | 532 ms                                                 | 397 ms: 1.34x faster                                                 |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.32x faster                                                 |
| deepcopy                 | 479 us                                                 | 365 us: 1.31x faster                                                 |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                |
| thrift                   | 1.07 ms                                                | 819 us: 1.31x faster                                                 |
| html5lib                 | 88.9 ms                                                | 68.6 ms: 1.30x faster                                                |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.29x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                |
| genshi_text              | 31.8 ms                                                | 24.6 ms: 1.29x faster                                                |
| regex_compile            | 188 ms                                                 | 146 ms: 1.29x faster                                                 |
| pycparser                | 1.58 sec                                               | 1.24 sec: 1.27x faster                                               |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.27x faster                                                 |
| 2to3                     | 348 ms                                                 | 280 ms: 1.25x faster                                                 |
| sympy_sum                | 196 ms                                                 | 164 ms: 1.20x faster                                                 |
| genshi_xml               | 66.0 ms                                                | 55.3 ms: 1.19x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 58.0 ms: 1.19x faster                                                |
| sympy_str                | 346 ms                                                 | 291 ms: 1.19x faster                                                 |
| dulwich_log              | 84.3 ms                                                | 71.2 ms: 1.18x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                |
| sympy_integrate          | 25.8 ms                                                | 21.8 ms: 1.18x faster                                                |
| djangocms                | 38.4 us                                                | 32.5 us: 1.18x faster                                                |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                |
| dask                     | 441 ms                                                 | 377 ms: 1.17x faster                                                 |
| sympy_expand             | 566 ms                                                 | 491 ms: 1.15x faster                                                 |
| bench_thread_pool        | 986 us                                                 | 856 us: 1.15x faster                                                 |
| nqueens                  | 106 ms                                                 | 92.7 ms: 1.14x faster                                                |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                               |
| mypy2                    | 894 ms                                                 | 789 ms: 1.13x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 89.2 ms: 1.11x faster                                                |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                |
| regex_v8                 | 27.8 ms                                                | 25.6 ms: 1.08x faster                                                |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                 |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                 |
| json                     | 5.69 ms                                                | 5.32 ms: 1.07x faster                                                |
| pathlib                  | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.05x faster                                                 |
| sqlite_synth             | 3.02 us                                                | 2.92 us: 1.04x faster                                                |
| unpickle_list            | 5.20 us                                                | 5.06 us: 1.03x faster                                                |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                 |
| mdp                      | 2.85 sec                                               | 2.83 sec: 1.01x faster                                               |
| bench_mp_pool            | 24.0 ms                                                | 24.2 ms: 1.01x slower                                                |
| regex_dna                | 227 ms                                                 | 231 ms: 1.02x slower                                                 |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                                 |
| create_gc_cycles         | 1.62 ms                                                | 1.69 ms: 1.05x slower                                                |
| async_generators         | 444 ms                                                 | 465 ms: 1.05x slower                                                 |
| pickle_list              | 5.08 us                                                | 5.37 us: 1.06x slower                                                |
| regex_effbot             | 3.63 ms                                                | 3.87 ms: 1.07x slower                                                |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.09x slower                                                |
| gc_traversal             | 3.62 ms                                                | 3.94 ms: 1.09x slower                                                |
| telco                    | 7.27 ms                                                | 8.48 ms: 1.17x slower                                                |
| pickle                   | 10.7 us                                                | 12.5 us: 1.17x slower                                                |
| pickle_dict              | 29.6 us                                                | 35.3 us: 1.19x slower                                                |
| coverage                 | 79.4 ms                                                | 97.1 ms: 1.22x slower                                                |
| unpack_sequence          | 60.0 ns                                                | 87.6 ns: 1.46x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 9.55 ms: 1.61x slower                                                |
| Geometric mean           | (ref)                                                  | 1.30x faster                                                         |
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x