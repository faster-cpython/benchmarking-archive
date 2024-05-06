# Results vs. 3.10.4

- fork: python
- ref: v3.12.3
- machine: linux-x86_64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 266 ms: 1.31x faster                                   |
| chameleon      | 9.68 ms                                                | 6.94 ms: 1.40x faster                                  |
| docutils       | 3.30 sec                                               | 2.73 sec: 1.21x faster                                 |
| html5lib       | 88.9 ms                                                | 64.5 ms: 1.38x faster                                  |
| tornado_http   | 136 ms                                                 | 96.9 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                  | 1.34x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 481 ms: 1.52x faster                                   |
| async_tree_io           | 1.77 sec                                               | 1.18 sec: 1.49x faster                                 |
| async_tree_memoization  | 870 ms                                                 | 586 ms: 1.48x faster                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 734 ms: 1.38x faster                                   |
| Geometric mean          | (ref)                                                  | 1.47x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 154 ms                                                 | 93.1 ms: 1.65x faster                                  |
| float          | 117 ms                                                 | 83.5 ms: 1.40x faster                                  |
| pidigits       | 191 ms                                                 | 197 ms: 1.03x slower                                   |
| Geometric mean | (ref)                                                  | 1.31x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                   |
| regex_v8       | 27.8 ms                                                | 23.3 ms: 1.19x faster                                  |
| regex_dna      | 227 ms                                                 | 211 ms: 1.08x faster                                   |
| regex_effbot   | 3.63 ms                                                | 3.77 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.14x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 313 us: 1.55x faster                                   |
| unpickle_pure_python | 331 us                                                 | 221 us: 1.49x faster                                   |
| tomli_loads          | 3.14 sec                                               | 2.23 sec: 1.41x faster                                 |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                  |
| xml_etree_process    | 79.1 ms                                                | 60.1 ms: 1.32x faster                                  |
| xml_etree_generate   | 99.4 ms                                                | 88.9 ms: 1.12x faster                                  |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                   |
| json_loads           | 31.2 us                                                | 29.9 us: 1.04x faster                                  |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                   |
| unpickle_list        | 5.20 us                                                | 5.04 us: 1.03x faster                                  |
| pickle_list          | 5.08 us                                                | 5.05 us: 1.01x faster                                  |
| pickle               | 10.7 us                                                | 11.7 us: 1.09x slower                                  |
| unpickle             | 14.4 us                                                | 15.8 us: 1.10x slower                                  |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.18x slower                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 9.54 ms: 1.53x faster                                  |
| python_startup_no_site | 5.93 ms                                                | 6.87 ms: 1.16x slower                                  |
| Geometric mean         | (ref)                                                  | 1.15x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.1 ms: 1.47x faster                                  |
| genshi_text     | 31.8 ms                                                | 22.1 ms: 1.44x faster                                  |
| django_template | 48.2 ms                                                | 34.2 ms: 1.41x faster                                  |
| genshi_xml      | 66.0 ms                                                | 50.6 ms: 1.31x faster                                  |
| Geometric mean  | (ref)                                                  | 1.40x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 119 us: 4.57x faster                                   |
| generators               | 80.1 ms                                                | 28.6 ms: 2.80x faster                                  |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                  |
| logging_silent           | 190 ns                                                 | 96.6 ns: 1.96x faster                                  |
| richards_super           | 94.7 ms                                                | 48.9 ms: 1.94x faster                                  |
| richards                 | 79.3 ms                                                | 42.5 ms: 1.86x faster                                  |
| chaos                    | 115 ms                                                 | 64.9 ms: 1.78x faster                                  |
| asyncio_tcp              | 922 ms                                                 | 519 ms: 1.78x faster                                   |
| go                       | 240 ms                                                 | 135 ms: 1.77x faster                                   |
| comprehensions           | 28.8 us                                                | 16.4 us: 1.75x faster                                  |
| scimark_sor              | 220 ms                                                 | 126 ms: 1.74x faster                                   |
| pylint                   | 551 ms                                                 | 318 ms: 1.73x faster                                   |
| raytrace                 | 507 ms                                                 | 297 ms: 1.70x faster                                   |
| hexiom                   | 10.4 ms                                                | 6.27 ms: 1.66x faster                                  |
| nbody                    | 154 ms                                                 | 93.1 ms: 1.65x faster                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.34 ms: 1.61x faster                                  |
| scimark_monte_carlo      | 118 ms                                                 | 73.4 ms: 1.61x faster                                  |
| pyflate                  | 716 ms                                                 | 458 ms: 1.56x faster                                   |
| pickle_pure_python       | 484 us                                                 | 313 us: 1.55x faster                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.67 ms: 1.54x faster                                  |
| deepcopy_memo            | 58.5 us                                                | 38.2 us: 1.53x faster                                  |
| python_startup           | 14.6 ms                                                | 9.54 ms: 1.53x faster                                  |
| crypto_pyaes             | 128 ms                                                 | 84.3 ms: 1.52x faster                                  |
| async_tree_none          | 728 ms                                                 | 481 ms: 1.52x faster                                   |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.51x faster                                   |
| coroutines               | 35.1 ms                                                | 23.3 ms: 1.50x faster                                  |
| async_tree_io            | 1.77 sec                                               | 1.18 sec: 1.49x faster                                 |
| unpickle_pure_python     | 331 us                                                 | 221 us: 1.49x faster                                   |
| async_tree_memoization   | 870 ms                                                 | 586 ms: 1.48x faster                                   |
| mako                     | 16.3 ms                                                | 11.1 ms: 1.47x faster                                  |
| scimark_lu               | 176 ms                                                 | 121 ms: 1.45x faster                                   |
| genshi_text              | 31.8 ms                                                | 22.1 ms: 1.44x faster                                  |
| django_template          | 48.2 ms                                                | 34.2 ms: 1.41x faster                                  |
| tomli_loads              | 3.14 sec                                               | 2.23 sec: 1.41x faster                                 |
| tornado_http             | 136 ms                                                 | 96.9 ms: 1.41x faster                                  |
| float                    | 117 ms                                                 | 83.5 ms: 1.40x faster                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                 |
| chameleon                | 9.68 ms                                                | 6.94 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 734 ms: 1.38x faster                                   |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.38x faster                                 |
| html5lib                 | 88.9 ms                                                | 64.5 ms: 1.38x faster                                  |
| pprint_safe_repr         | 1.02 sec                                               | 742 ms: 1.37x faster                                   |
| logging_simple           | 8.30 us                                                | 6.12 us: 1.36x faster                                  |
| deepcopy                 | 479 us                                                 | 354 us: 1.35x faster                                   |
| logging_format           | 9.09 us                                                | 6.73 us: 1.35x faster                                  |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                   |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.34x faster                                 |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                  |
| sqlglot_normalize        | 143 ms                                                 | 107 ms: 1.34x faster                                   |
| fannkuch                 | 532 ms                                                 | 402 ms: 1.32x faster                                   |
| xml_etree_process        | 79.1 ms                                                | 60.1 ms: 1.32x faster                                  |
| 2to3                     | 348 ms                                                 | 266 ms: 1.31x faster                                   |
| thrift                   | 1.07 ms                                                | 821 us: 1.31x faster                                   |
| genshi_xml               | 66.0 ms                                                | 50.6 ms: 1.31x faster                                  |
| nqueens                  | 106 ms                                                 | 81.2 ms: 1.30x faster                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.98 ms: 1.30x faster                                  |
| sqlalchemy_imperative    | 23.3 ms                                                | 18.0 ms: 1.30x faster                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.29x faster                                  |
| sympy_integrate          | 25.8 ms                                                | 20.0 ms: 1.29x faster                                  |
| mypy2                    | 894 ms                                                 | 694 ms: 1.29x faster                                   |
| sqlglot_optimize         | 69.2 ms                                                | 53.9 ms: 1.28x faster                                  |
| dulwich_log              | 84.3 ms                                                | 66.0 ms: 1.28x faster                                  |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.27x faster                                   |
| aiohttp                  | 1.44 ms                                                | 1.13 ms: 1.27x faster                                  |
| sympy_str                | 346 ms                                                 | 274 ms: 1.26x faster                                   |
| gunicorn                 | 1.53 ms                                                | 1.22 ms: 1.25x faster                                  |
| scimark_fft              | 466 ms                                                 | 378 ms: 1.23x faster                                   |
| sympy_expand             | 566 ms                                                 | 462 ms: 1.22x faster                                   |
| djangocms                | 38.4 us                                                | 31.7 us: 1.21x faster                                  |
| docutils                 | 3.30 sec                                               | 2.73 sec: 1.21x faster                                 |
| dask                     | 441 ms                                                 | 366 ms: 1.20x faster                                   |
| regex_v8                 | 27.8 ms                                                | 23.3 ms: 1.19x faster                                  |
| sqlalchemy_declarative   | 172 ms                                                 | 145 ms: 1.18x faster                                   |
| bench_thread_pool        | 986 us                                                 | 838 us: 1.18x faster                                   |
| xml_etree_generate       | 99.4 ms                                                | 88.9 ms: 1.12x faster                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.47 ms: 1.10x faster                                  |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                  |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.08x faster                                   |
| regex_dna                | 227 ms                                                 | 211 ms: 1.08x faster                                   |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                   |
| json                     | 5.69 ms                                                | 5.33 ms: 1.07x faster                                  |
| sqlite_synth             | 3.02 us                                                | 2.86 us: 1.06x faster                                  |
| coverage                 | 79.4 ms                                                | 75.2 ms: 1.06x faster                                  |
| json_loads               | 31.2 us                                                | 29.9 us: 1.04x faster                                  |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                   |
| unpickle_list            | 5.20 us                                                | 5.04 us: 1.03x faster                                  |
| mdp                      | 2.85 sec                                               | 2.80 sec: 1.02x faster                                 |
| pickle_list              | 5.08 us                                                | 5.05 us: 1.01x faster                                  |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                  |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                   |
| telco                    | 7.27 ms                                                | 7.35 ms: 1.01x slower                                  |
| gc_traversal             | 3.62 ms                                                | 3.73 ms: 1.03x slower                                  |
| async_generators         | 444 ms                                                 | 457 ms: 1.03x slower                                   |
| pidigits                 | 191 ms                                                 | 197 ms: 1.03x slower                                   |
| regex_effbot             | 3.63 ms                                                | 3.77 ms: 1.04x slower                                  |
| pickle                   | 10.7 us                                                | 11.7 us: 1.09x slower                                  |
| unpickle                 | 14.4 us                                                | 15.8 us: 1.10x slower                                  |
| python_startup_no_site   | 5.93 ms                                                | 6.87 ms: 1.16x slower                                  |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.18x slower                                  |
| Geometric mean           | (ref)                                                  | 1.34x faster                                           |
Ignored benchmarks (2) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, unpack_sequence
Ignored benchmarks (4) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.10x