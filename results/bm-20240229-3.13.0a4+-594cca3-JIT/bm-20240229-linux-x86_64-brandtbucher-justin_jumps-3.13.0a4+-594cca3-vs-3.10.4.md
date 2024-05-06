# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_jumps
- machine: linux-x86_64
- commit hash: 594cca3
- commit date: 2024-02-29
- overall geometric mean: 1.32x faster \*
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 276 ms: 1.26x faster                                                 |
| chameleon      | 9.68 ms                                                | 6.69 ms: 1.45x faster                                                |
| docutils       | 3.30 sec                                               | 2.70 sec: 1.22x faster                                               |
| tornado_http   | 136 ms                                                 | 96.6 ms: 1.41x faster                                                |
| Geometric mean | (ref)                                                  | 1.33x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 434 ms: 1.68x faster                                                 |
| async_tree_memoization  | 870 ms                                                 | 560 ms: 1.55x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 1.18 sec: 1.50x faster                                               |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 702 ms: 1.45x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.54x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.9 ms: 1.65x faster                                                |
| float          | 117 ms                                                 | 78.2 ms: 1.50x faster                                                |
| pidigits       | 191 ms                                                 | 187 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.36x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 143 ms: 1.32x faster                                                 |
| regex_v8       | 27.8 ms                                                | 24.3 ms: 1.14x faster                                                |
| regex_effbot   | 3.63 ms                                                | 3.56 ms: 1.02x faster                                                |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.12x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                 |
| tomli_loads          | 3.14 sec                                               | 2.03 sec: 1.55x faster                                               |
| unpickle_pure_python | 331 us                                                 | 236 us: 1.40x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.3 ms: 1.38x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 58.2 ms: 1.36x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 85.9 ms: 1.16x faster                                                |
| json_loads           | 31.2 us                                                | 27.4 us: 1.14x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                 |
| xml_etree_parse      | 168 ms                                                 | 156 ms: 1.08x faster                                                 |
| unpickle_list        | 5.20 us                                                | 5.05 us: 1.03x faster                                                |
| pickle_list          | 5.08 us                                                | 5.01 us: 1.01x faster                                                |
| unpickle             | 14.4 us                                                | 14.6 us: 1.02x slower                                                |
| pickle               | 10.7 us                                                | 11.3 us: 1.06x slower                                                |
| pickle_dict          | 29.6 us                                                | 33.3 us: 1.13x slower                                                |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 12.2 ms: 1.19x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 10.9 ms: 1.84x slower                                                |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako      | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 111 us: 4.91x faster                                                 |
| generators               | 80.1 ms                                                | 29.3 ms: 2.73x faster                                                |
| deltablue                | 7.91 ms                                                | 3.40 ms: 2.33x faster                                                |
| logging_silent           | 190 ns                                                 | 100.0 ns: 1.90x faster                                               |
| asyncio_tcp              | 922 ms                                                 | 488 ms: 1.89x faster                                                 |
| chaos                    | 115 ms                                                 | 62.4 ms: 1.85x faster                                                |
| richards_super           | 94.7 ms                                                | 52.2 ms: 1.82x faster                                                |
| crypto_pyaes             | 128 ms                                                 | 72.5 ms: 1.76x faster                                                |
| raytrace                 | 507 ms                                                 | 288 ms: 1.76x faster                                                 |
| scimark_sor              | 220 ms                                                 | 126 ms: 1.75x faster                                                 |
| richards                 | 79.3 ms                                                | 46.7 ms: 1.70x faster                                                |
| comprehensions           | 28.8 us                                                | 17.0 us: 1.69x faster                                                |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                |
| async_tree_none          | 728 ms                                                 | 434 ms: 1.68x faster                                                 |
| scimark_monte_carlo      | 118 ms                                                 | 70.9 ms: 1.67x faster                                                |
| nbody                    | 154 ms                                                 | 92.9 ms: 1.65x faster                                                |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                 |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 560 ms: 1.55x faster                                                 |
| tomli_loads              | 3.14 sec                                               | 2.03 sec: 1.55x faster                                               |
| coroutines               | 35.1 ms                                                | 22.9 ms: 1.53x faster                                                |
| go                       | 240 ms                                                 | 157 ms: 1.53x faster                                                 |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.50x faster                                                 |
| deepcopy_memo            | 58.5 us                                                | 38.9 us: 1.50x faster                                                |
| async_tree_io            | 1.77 sec                                               | 1.18 sec: 1.50x faster                                               |
| float                    | 117 ms                                                 | 78.2 ms: 1.50x faster                                                |
| hexiom                   | 10.4 ms                                                | 7.02 ms: 1.48x faster                                                |
| logging_simple           | 8.30 us                                                | 5.61 us: 1.48x faster                                                |
| pyflate                  | 716 ms                                                 | 484 ms: 1.48x faster                                                 |
| logging_format           | 9.09 us                                                | 6.17 us: 1.47x faster                                                |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 702 ms: 1.45x faster                                                 |
| chameleon                | 9.68 ms                                                | 6.69 ms: 1.45x faster                                                |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.80 sec: 1.43x faster                                               |
| tornado_http             | 136 ms                                                 | 96.6 ms: 1.41x faster                                                |
| unpickle_pure_python     | 331 us                                                 | 236 us: 1.40x faster                                                 |
| scimark_fft              | 466 ms                                                 | 337 ms: 1.38x faster                                                 |
| json_dumps               | 14.2 ms                                                | 10.3 ms: 1.38x faster                                                |
| pprint_safe_repr         | 1.02 sec                                               | 742 ms: 1.37x faster                                                 |
| deepcopy                 | 479 us                                                 | 350 us: 1.37x faster                                                 |
| deepcopy_reduce          | 4.17 us                                                | 3.05 us: 1.37x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 58.2 ms: 1.36x faster                                                |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                               |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                               |
| scimark_lu               | 176 ms                                                 | 131 ms: 1.34x faster                                                 |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                                 |
| sqlglot_normalize        | 143 ms                                                 | 107 ms: 1.33x faster                                                 |
| regex_compile            | 188 ms                                                 | 143 ms: 1.32x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.93 ms: 1.31x faster                                                |
| 2to3                     | 348 ms                                                 | 276 ms: 1.26x faster                                                 |
| sympy_sum                | 196 ms                                                 | 158 ms: 1.25x faster                                                 |
| sympy_integrate          | 25.8 ms                                                | 20.9 ms: 1.24x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 56.0 ms: 1.23x faster                                                |
| sympy_str                | 346 ms                                                 | 281 ms: 1.23x faster                                                 |
| dulwich_log              | 84.3 ms                                                | 68.7 ms: 1.23x faster                                                |
| docutils                 | 3.30 sec                                               | 2.70 sec: 1.22x faster                                               |
| python_startup           | 14.6 ms                                                | 12.2 ms: 1.19x faster                                                |
| sympy_expand             | 566 ms                                                 | 478 ms: 1.18x faster                                                 |
| nqueens                  | 106 ms                                                 | 90.7 ms: 1.17x faster                                                |
| bench_thread_pool        | 986 us                                                 | 846 us: 1.17x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 85.9 ms: 1.16x faster                                                |
| regex_v8                 | 27.8 ms                                                | 24.3 ms: 1.14x faster                                                |
| json                     | 5.69 ms                                                | 5.00 ms: 1.14x faster                                                |
| json_loads               | 31.2 us                                                | 27.4 us: 1.14x faster                                                |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.11x faster                                                 |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                |
| mdp                      | 2.85 sec                                               | 2.61 sec: 1.09x faster                                               |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                 |
| create_gc_cycles         | 1.62 ms                                                | 1.49 ms: 1.09x faster                                                |
| sqlite_synth             | 3.02 us                                                | 2.81 us: 1.08x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 156 ms: 1.08x faster                                                 |
| unpickle_list            | 5.20 us                                                | 5.05 us: 1.03x faster                                                |
| pidigits                 | 191 ms                                                 | 187 ms: 1.02x faster                                                 |
| regex_effbot             | 3.63 ms                                                | 3.56 ms: 1.02x faster                                                |
| pickle_list              | 5.08 us                                                | 5.01 us: 1.01x faster                                                |
| asyncio_websockets       | 559 ms                                                 | 552 ms: 1.01x faster                                                 |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                 |
| unpickle                 | 14.4 us                                                | 14.6 us: 1.02x slower                                                |
| async_generators         | 444 ms                                                 | 457 ms: 1.03x slower                                                 |
| gc_traversal             | 3.62 ms                                                | 3.75 ms: 1.04x slower                                                |
| pickle                   | 10.7 us                                                | 11.3 us: 1.06x slower                                                |
| pickle_dict              | 29.6 us                                                | 33.3 us: 1.13x slower                                                |
| telco                    | 7.27 ms                                                | 8.37 ms: 1.15x slower                                                |
| bench_mp_pool            | 24.0 ms                                                | 27.8 ms: 1.16x slower                                                |
| coverage                 | 79.4 ms                                                | 95.6 ms: 1.20x slower                                                |
| unpack_sequence          | 60.0 ns                                                | 84.9 ns: 1.42x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 10.9 ms: 1.84x slower                                                |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                         |

Benchmark hidden because not significant (1): mypy2
Ignored benchmarks (13) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
Ignored benchmarks (4) of results/bm-20240229-3.13.0a4+-594cca3-JIT/bm-20240229-linux-x86_64-brandtbucher-justin_jumps-3.13.0a4+-594cca3.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg


# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.23x


# Memory

- memory change: 1.34x