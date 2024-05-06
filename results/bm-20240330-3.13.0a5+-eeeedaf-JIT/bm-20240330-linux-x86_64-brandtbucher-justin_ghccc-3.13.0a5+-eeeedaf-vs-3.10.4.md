# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 276 ms: 1.26x faster                                                 |
| chameleon      | 9.68 ms                                                | 7.05 ms: 1.37x faster                                                |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                               |
| html5lib       | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                |
| tornado_http   | 136 ms                                                 | 97.0 ms: 1.41x faster                                                |
| Geometric mean | (ref)                                                  | 1.29x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.05x faster                                                 |
| async_tree_memoization  | 870 ms                                                 | 450 ms: 1.93x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 929 ms: 1.90x faster                                                 |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 87.0 ms: 1.77x faster                                                |
| float          | 117 ms                                                 | 72.8 ms: 1.61x faster                                                |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.42x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 143 ms: 1.32x faster                                                 |
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                |
| regex_dna      | 227 ms                                                 | 219 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.11x faster                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 308 us: 1.57x faster                                                 |
| tomli_loads          | 3.14 sec                                               | 2.02 sec: 1.56x faster                                               |
| unpickle_pure_python | 331 us                                                 | 229 us: 1.45x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                 |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.05x faster                                                 |
| pickle_list          | 5.08 us                                                | 4.97 us: 1.02x faster                                                |
| unpickle             | 14.4 us                                                | 15.2 us: 1.05x slower                                                |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                |
| pickle_dict          | 29.6 us                                                | 34.2 us: 1.16x slower                                                |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                         |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 9.49 ms: 1.60x slower                                                |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 9.96 ms: 1.64x faster                                                |
| django_template | 48.2 ms                                                | 36.4 ms: 1.32x faster                                                |
| genshi_text     | 31.8 ms                                                | 24.9 ms: 1.28x faster                                                |
| genshi_xml      | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.79x faster                                                 |
| generators               | 80.1 ms                                                | 29.8 ms: 2.68x faster                                                |
| deltablue                | 7.91 ms                                                | 3.48 ms: 2.27x faster                                                |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.05x faster                                                 |
| async_tree_memoization   | 870 ms                                                 | 450 ms: 1.93x faster                                                 |
| chaos                    | 115 ms                                                 | 60.3 ms: 1.92x faster                                                |
| async_tree_io            | 1.77 sec                                               | 929 ms: 1.90x faster                                                 |
| pylint                   | 551 ms                                                 | 299 ms: 1.85x faster                                                 |
| richards_super           | 94.7 ms                                                | 51.7 ms: 1.83x faster                                                |
| logging_silent           | 190 ns                                                 | 104 ns: 1.83x faster                                                 |
| crypto_pyaes             | 128 ms                                                 | 70.1 ms: 1.82x faster                                                |
| scimark_monte_carlo      | 118 ms                                                 | 64.9 ms: 1.82x faster                                                |
| raytrace                 | 507 ms                                                 | 279 ms: 1.82x faster                                                 |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                 |
| nbody                    | 154 ms                                                 | 87.0 ms: 1.77x faster                                                |
| richards                 | 79.3 ms                                                | 46.0 ms: 1.72x faster                                                |
| spectral_norm            | 170 ms                                                 | 101 ms: 1.69x faster                                                 |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                 |
| comprehensions           | 28.8 us                                                | 17.4 us: 1.65x faster                                                |
| mako                     | 16.3 ms                                                | 9.96 ms: 1.64x faster                                                |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.64x faster                                                |
| scimark_sor              | 220 ms                                                 | 136 ms: 1.62x faster                                                 |
| float                    | 117 ms                                                 | 72.8 ms: 1.61x faster                                                |
| pyflate                  | 716 ms                                                 | 451 ms: 1.59x faster                                                 |
| pickle_pure_python       | 484 us                                                 | 308 us: 1.57x faster                                                 |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.57x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                                |
| tomli_loads              | 3.14 sec                                               | 2.02 sec: 1.56x faster                                               |
| go                       | 240 ms                                                 | 158 ms: 1.52x faster                                                 |
| hexiom                   | 10.4 ms                                                | 6.88 ms: 1.51x faster                                                |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.33 ms: 1.50x faster                                                |
| scimark_fft              | 466 ms                                                 | 319 ms: 1.46x faster                                                 |
| deepcopy_memo            | 58.5 us                                                | 40.1 us: 1.46x faster                                                |
| fannkuch                 | 532 ms                                                 | 367 ms: 1.45x faster                                                 |
| unpickle_pure_python     | 331 us                                                 | 229 us: 1.45x faster                                                 |
| tornado_http             | 136 ms                                                 | 97.0 ms: 1.41x faster                                                |
| logging_simple           | 8.30 us                                                | 5.94 us: 1.40x faster                                                |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.40x faster                                               |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                               |
| logging_format           | 9.09 us                                                | 6.57 us: 1.38x faster                                                |
| pprint_safe_repr         | 1.02 sec                                               | 738 ms: 1.38x faster                                                 |
| chameleon                | 9.68 ms                                                | 7.05 ms: 1.37x faster                                                |
| scimark_lu               | 176 ms                                                 | 130 ms: 1.35x faster                                                 |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                |
| django_template          | 48.2 ms                                                | 36.4 ms: 1.32x faster                                                |
| pycparser                | 1.58 sec                                               | 1.19 sec: 1.32x faster                                               |
| deepcopy                 | 479 us                                                 | 363 us: 1.32x faster                                                 |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                |
| regex_compile            | 188 ms                                                 | 143 ms: 1.32x faster                                                 |
| html5lib                 | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                |
| thrift                   | 1.07 ms                                                | 821 us: 1.30x faster                                                 |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                |
| genshi_text              | 31.8 ms                                                | 24.9 ms: 1.28x faster                                                |
| 2to3                     | 348 ms                                                 | 276 ms: 1.26x faster                                                 |
| sqlglot_normalize        | 143 ms                                                 | 115 ms: 1.24x faster                                                 |
| djangocms                | 38.4 us                                                | 31.3 us: 1.23x faster                                                |
| sympy_sum                | 196 ms                                                 | 164 ms: 1.20x faster                                                 |
| genshi_xml               | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                |
| sympy_str                | 346 ms                                                 | 291 ms: 1.19x faster                                                 |
| sympy_integrate          | 25.8 ms                                                | 21.7 ms: 1.19x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 58.7 ms: 1.18x faster                                                |
| dulwich_log              | 84.3 ms                                                | 71.6 ms: 1.18x faster                                                |
| dask                     | 441 ms                                                 | 376 ms: 1.17x faster                                                 |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                                |
| nqueens                  | 106 ms                                                 | 91.2 ms: 1.16x faster                                                |
| bench_thread_pool        | 986 us                                                 | 858 us: 1.15x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                |
| sympy_expand             | 566 ms                                                 | 497 ms: 1.14x faster                                                 |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                               |
| mypy2                    | 894 ms                                                 | 794 ms: 1.13x faster                                                 |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                 |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                 |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                |
| mdp                      | 2.85 sec                                               | 2.64 sec: 1.08x faster                                               |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                |
| sqlite_synth             | 3.02 us                                                | 2.84 us: 1.06x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.05x faster                                                 |
| json                     | 5.69 ms                                                | 5.50 ms: 1.04x faster                                                |
| regex_dna                | 227 ms                                                 | 219 ms: 1.03x faster                                                 |
| pickle_list              | 5.08 us                                                | 4.97 us: 1.02x faster                                                |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                 |
| gc_traversal             | 3.62 ms                                                | 3.69 ms: 1.02x slower                                                |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                                 |
| create_gc_cycles         | 1.62 ms                                                | 1.66 ms: 1.03x slower                                                |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.05x slower                                                |
| async_generators         | 444 ms                                                 | 468 ms: 1.06x slower                                                 |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                |
| pickle_dict              | 29.6 us                                                | 34.2 us: 1.16x slower                                                |
| telco                    | 7.27 ms                                                | 8.55 ms: 1.18x slower                                                |
| coverage                 | 79.4 ms                                                | 96.9 ms: 1.22x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 9.49 ms: 1.60x slower                                                |
| unpack_sequence          | 60.0 ns                                                | 115 ns: 1.91x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                         |

Benchmark hidden because not significant (3): regex_effbot, bench_mp_pool, unpickle_list
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x