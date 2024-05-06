# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 316 ms: 1.10x faster                                              |
| chameleon      | 9.68 ms                                                | 7.81 ms: 1.24x faster                                             |
| docutils       | 3.30 sec                                               | 3.13 sec: 1.05x faster                                            |
| html5lib       | 88.9 ms                                                | 72.2 ms: 1.23x faster                                             |
| tornado_http   | 136 ms                                                 | 104 ms: 1.32x faster                                              |
| Geometric mean | (ref)                                                  | 1.18x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 487 ms: 1.79x faster                                              |
| async_tree_io           | 1.77 sec                                               | 1.01 sec: 1.76x faster                                            |
| async_tree_none         | 728 ms                                                 | 421 ms: 1.73x faster                                              |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 632 ms: 1.61x faster                                              |
| Geometric mean          | (ref)                                                  | 1.72x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 117 ms                                                 | 99.2 ms: 1.18x faster                                             |
| nbody          | 154 ms                                                 | 130 ms: 1.18x faster                                              |
| pidigits       | 191 ms                                                 | 192 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                  | 1.11x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 26.5 ms: 1.05x faster                                             |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                              |
| regex_compile  | 188 ms                                                 | 196 ms: 1.04x slower                                              |
| Geometric mean | (ref)                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 322 us: 1.50x faster                                              |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                             |
| xml_etree_process    | 79.1 ms                                                | 66.3 ms: 1.19x faster                                             |
| tomli_loads          | 3.14 sec                                               | 2.77 sec: 1.13x faster                                            |
| json_loads           | 31.2 us                                                | 28.9 us: 1.08x faster                                             |
| unpickle_pure_python | 331 us                                                 | 316 us: 1.05x faster                                              |
| xml_etree_parse      | 168 ms                                                 | 163 ms: 1.03x faster                                              |
| xml_etree_generate   | 99.4 ms                                                | 98.8 ms: 1.01x faster                                             |
| pickle_list          | 5.08 us                                                | 5.23 us: 1.03x slower                                             |
| unpickle_list        | 5.20 us                                                | 5.39 us: 1.04x slower                                             |
| unpickle             | 14.4 us                                                | 15.6 us: 1.09x slower                                             |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                             |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.19x slower                                             |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                      |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.8 ms: 1.35x faster                                             |
| python_startup_no_site | 5.93 ms                                                | 9.17 ms: 1.55x slower                                             |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.8 ms: 1.18x faster                                             |
| genshi_text     | 31.8 ms                                                | 27.4 ms: 1.16x faster                                             |
| django_template | 48.2 ms                                                | 42.2 ms: 1.14x faster                                             |
| genshi_xml      | 66.0 ms                                                | 64.2 ms: 1.03x faster                                             |
| Geometric mean  | (ref)                                                  | 1.13x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 127 us: 4.29x faster                                              |
| generators               | 80.1 ms                                                | 30.9 ms: 2.60x faster                                             |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                              |
| async_tree_memoization   | 870 ms                                                 | 487 ms: 1.79x faster                                              |
| async_tree_io            | 1.77 sec                                               | 1.01 sec: 1.76x faster                                            |
| async_tree_none          | 728 ms                                                 | 421 ms: 1.73x faster                                              |
| deltablue                | 7.91 ms                                                | 4.66 ms: 1.70x faster                                             |
| logging_silent           | 190 ns                                                 | 112 ns: 1.69x faster                                              |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 632 ms: 1.61x faster                                              |
| pylint                   | 551 ms                                                 | 354 ms: 1.56x faster                                              |
| coroutines               | 35.1 ms                                                | 23.0 ms: 1.53x faster                                             |
| pickle_pure_python       | 484 us                                                 | 322 us: 1.50x faster                                              |
| chaos                    | 115 ms                                                 | 82.5 ms: 1.40x faster                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.56 ms: 1.39x faster                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.89 ms: 1.37x faster                                             |
| crypto_pyaes             | 128 ms                                                 | 94.4 ms: 1.35x faster                                             |
| python_startup           | 14.6 ms                                                | 10.8 ms: 1.35x faster                                             |
| tornado_http             | 136 ms                                                 | 104 ms: 1.32x faster                                              |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                             |
| raytrace                 | 507 ms                                                 | 391 ms: 1.30x faster                                              |
| thrift                   | 1.07 ms                                                | 834 us: 1.29x faster                                              |
| richards_super           | 94.7 ms                                                | 74.4 ms: 1.27x faster                                             |
| scimark_sor              | 220 ms                                                 | 173 ms: 1.27x faster                                              |
| deepcopy_reduce          | 4.17 us                                                | 3.31 us: 1.26x faster                                             |
| scimark_monte_carlo      | 118 ms                                                 | 94.1 ms: 1.26x faster                                             |
| go                       | 240 ms                                                 | 193 ms: 1.24x faster                                              |
| chameleon                | 9.68 ms                                                | 7.81 ms: 1.24x faster                                             |
| logging_format           | 9.09 us                                                | 7.36 us: 1.23x faster                                             |
| logging_simple           | 8.30 us                                                | 6.75 us: 1.23x faster                                             |
| html5lib                 | 88.9 ms                                                | 72.2 ms: 1.23x faster                                             |
| deepcopy                 | 479 us                                                 | 392 us: 1.22x faster                                              |
| xml_etree_process        | 79.1 ms                                                | 66.3 ms: 1.19x faster                                             |
| mako                     | 16.3 ms                                                | 13.8 ms: 1.18x faster                                             |
| richards                 | 79.3 ms                                                | 67.1 ms: 1.18x faster                                             |
| float                    | 117 ms                                                 | 99.2 ms: 1.18x faster                                             |
| deepcopy_memo            | 58.5 us                                                | 49.5 us: 1.18x faster                                             |
| nbody                    | 154 ms                                                 | 130 ms: 1.18x faster                                              |
| genshi_text              | 31.8 ms                                                | 27.4 ms: 1.16x faster                                             |
| comprehensions           | 28.8 us                                                | 24.7 us: 1.16x faster                                             |
| djangocms                | 38.4 us                                                | 33.1 us: 1.16x faster                                             |
| dask                     | 441 ms                                                 | 386 ms: 1.14x faster                                              |
| django_template          | 48.2 ms                                                | 42.2 ms: 1.14x faster                                             |
| aiohttp                  | 1.44 ms                                                | 1.26 ms: 1.14x faster                                             |
| tomli_loads              | 3.14 sec                                               | 2.77 sec: 1.13x faster                                            |
| spectral_norm            | 170 ms                                                 | 151 ms: 1.13x faster                                              |
| gunicorn                 | 1.53 ms                                                | 1.37 ms: 1.12x faster                                             |
| dulwich_log              | 84.3 ms                                                | 75.5 ms: 1.12x faster                                             |
| pycparser                | 1.58 sec                                               | 1.43 sec: 1.10x faster                                            |
| 2to3                     | 348 ms                                                 | 316 ms: 1.10x faster                                              |
| sqlglot_normalize        | 143 ms                                                 | 130 ms: 1.10x faster                                              |
| bench_thread_pool        | 986 us                                                 | 910 us: 1.08x faster                                              |
| json_loads               | 31.2 us                                                | 28.9 us: 1.08x faster                                             |
| sympy_sum                | 196 ms                                                 | 182 ms: 1.08x faster                                              |
| mypy2                    | 894 ms                                                 | 830 ms: 1.08x faster                                              |
| sympy_integrate          | 25.8 ms                                                | 24.0 ms: 1.08x faster                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.04 ms: 1.07x faster                                             |
| pyflate                  | 716 ms                                                 | 670 ms: 1.07x faster                                              |
| docutils                 | 3.30 sec                                               | 3.13 sec: 1.05x faster                                            |
| scimark_lu               | 176 ms                                                 | 167 ms: 1.05x faster                                              |
| regex_v8                 | 27.8 ms                                                | 26.5 ms: 1.05x faster                                             |
| unpickle_pure_python     | 331 us                                                 | 316 us: 1.05x faster                                              |
| fannkuch                 | 532 ms                                                 | 513 ms: 1.04x faster                                              |
| json                     | 5.69 ms                                                | 5.49 ms: 1.04x faster                                             |
| sqlglot_optimize         | 69.2 ms                                                | 66.9 ms: 1.03x faster                                             |
| xml_etree_parse          | 168 ms                                                 | 163 ms: 1.03x faster                                              |
| sympy_str                | 346 ms                                                 | 335 ms: 1.03x faster                                              |
| genshi_xml               | 66.0 ms                                                | 64.2 ms: 1.03x faster                                             |
| scimark_fft              | 466 ms                                                 | 457 ms: 1.02x faster                                              |
| sympy_expand             | 566 ms                                                 | 556 ms: 1.02x faster                                              |
| xml_etree_generate       | 99.4 ms                                                | 98.8 ms: 1.01x faster                                             |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                              |
| pidigits                 | 191 ms                                                 | 192 ms: 1.01x slower                                              |
| pprint_safe_repr         | 1.02 sec                                               | 1.03 sec: 1.01x slower                                            |
| pathlib                  | 20.5 ms                                                | 20.7 ms: 1.01x slower                                             |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                              |
| sqlite_synth             | 3.02 us                                                | 3.09 us: 1.02x slower                                             |
| pickle_list              | 5.08 us                                                | 5.23 us: 1.03x slower                                             |
| gc_traversal             | 3.62 ms                                                | 3.74 ms: 1.03x slower                                             |
| pprint_pformat           | 2.10 sec                                               | 2.17 sec: 1.03x slower                                            |
| unpickle_list            | 5.20 us                                                | 5.39 us: 1.04x slower                                             |
| regex_compile            | 188 ms                                                 | 196 ms: 1.04x slower                                              |
| create_gc_cycles         | 1.62 ms                                                | 1.69 ms: 1.04x slower                                             |
| mdp                      | 2.85 sec                                               | 3.02 sec: 1.06x slower                                            |
| meteor_contest           | 120 ms                                                 | 128 ms: 1.07x slower                                              |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.09x slower                                             |
| async_generators         | 444 ms                                                 | 483 ms: 1.09x slower                                              |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                             |
| unpack_sequence          | 60.0 ns                                                | 68.8 ns: 1.15x slower                                             |
| nqueens                  | 106 ms                                                 | 124 ms: 1.18x slower                                              |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.19x slower                                             |
| coverage                 | 79.4 ms                                                | 98.5 ms: 1.24x slower                                             |
| telco                    | 7.27 ms                                                | 9.69 ms: 1.33x slower                                             |
| python_startup_no_site   | 5.93 ms                                                | 9.17 ms: 1.55x slower                                             |
| Geometric mean           | (ref)                                                  | 1.15x faster                                                      |

Benchmark hidden because not significant (4): hexiom, regex_effbot, bench_mp_pool, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-7bb5618-PYTHON_UOPS/bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.10x