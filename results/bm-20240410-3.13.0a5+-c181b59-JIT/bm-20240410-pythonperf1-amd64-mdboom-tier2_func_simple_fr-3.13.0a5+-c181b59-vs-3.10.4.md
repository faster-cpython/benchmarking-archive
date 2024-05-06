# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 220 ms: 1.12x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.68 ms: 1.24x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.69 sec: 1.14x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.2 ms: 1.45x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.7 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 268 ms: 1.96x faster                                                        |
| async_tree_none         | 435 ms                                                      | 223 ms: 1.96x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 589 ms: 1.88x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 389 ms: 1.64x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.86x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                       |
| nbody          | 71.3 ms                                                     | 57.5 ms: 1.24x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.19x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 86.6 ms: 1.22x faster                                                       |
| regex_dna      | 136 ms                                                      | 116 ms: 1.18x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 14.3 ms: 1.08x faster                                                       |
| regex_effbot   | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.59 ms: 1.64x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 172 us: 1.57x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.21 sec: 1.38x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 132 us: 1.38x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 36.8 ms: 1.21x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 60.6 ms: 1.07x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 90.7 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.78 us: 1.02x slower                                                       |
| pickle               | 6.85 us                                                     | 7.22 us: 1.05x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.99 us: 1.09x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.8 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.5 ms: 1.05x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 19.6 ms: 1.26x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.15x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.71 ms: 1.58x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 15.4 ms: 1.28x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 34.7 ms: 1.18x faster                                                       |
| Geometric mean | (ref)                                                       | 1.34x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 73.1 us: 4.60x faster                                                       |
| async_tree_memoization   | 526 ms                                                      | 268 ms: 1.96x faster                                                        |
| async_tree_none          | 435 ms                                                      | 223 ms: 1.96x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.16 ms: 1.94x faster                                                       |
| async_tree_io            | 1.11 sec                                                    | 589 ms: 1.88x faster                                                        |
| pylint                   | 350 ms                                                      | 195 ms: 1.80x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.0 ns: 1.79x faster                                                       |
| richards_super           | 52.2 ms                                                     | 30.2 ms: 1.73x faster                                                       |
| raytrace                 | 273 ms                                                      | 165 ms: 1.66x faster                                                        |
| generators               | 32.4 ms                                                     | 19.7 ms: 1.65x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.59 ms: 1.64x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 389 ms: 1.64x faster                                                        |
| chaos                    | 61.7 ms                                                     | 38.7 ms: 1.60x faster                                                       |
| richards                 | 42.4 ms                                                     | 26.7 ms: 1.59x faster                                                       |
| mako                     | 9.03 ms                                                     | 5.71 ms: 1.58x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 172 us: 1.57x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 468 ms: 1.56x faster                                                        |
| sqlglot_parse            | 1.22 ms                                                     | 780 us: 1.56x faster                                                        |
| comprehensions           | 16.5 us                                                     | 10.8 us: 1.53x faster                                                       |
| go                       | 139 ms                                                      | 92.7 ms: 1.50x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 51.6 ms: 1.50x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.4 ms: 1.49x faster                                                       |
| pyflate                  | 409 ms                                                      | 274 ms: 1.49x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 1.00 ms: 1.47x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.2 ms: 1.45x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 44.5 ms: 1.41x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.52 sec: 1.39x faster                                                      |
| tomli_loads              | 1.67 sec                                                    | 1.21 sec: 1.38x faster                                                      |
| unpickle_pure_python     | 183 us                                                      | 132 us: 1.38x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 21.1 us: 1.36x faster                                                       |
| pycparser                | 930 ms                                                      | 686 ms: 1.36x faster                                                        |
| float                    | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 4.41 ms: 1.30x faster                                                       |
| tornado_http             | 108 ms                                                      | 83.7 ms: 1.29x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 945 ms: 1.29x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 15.4 ms: 1.28x faster                                                       |
| scimark_sor              | 106 ms                                                      | 83.0 ms: 1.28x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 470 ms: 1.26x faster                                                        |
| mdp                      | 1.78 sec                                                    | 1.43 sec: 1.24x faster                                                      |
| nbody                    | 71.3 ms                                                     | 57.5 ms: 1.24x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.68 ms: 1.24x faster                                                       |
| mypy2                    | 555 ms                                                      | 450 ms: 1.23x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 41.0 ms: 1.23x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                       |
| regex_compile            | 106 ms                                                      | 86.6 ms: 1.22x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.57 us: 1.21x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.8 ms: 1.21x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 71.0 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.26 ms: 1.20x faster                                                       |
| sympy_sum                | 107 ms                                                      | 88.9 ms: 1.20x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 34.7 ms: 1.18x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 811 us: 1.18x faster                                                        |
| regex_dna                | 136 ms                                                      | 116 ms: 1.18x faster                                                        |
| sympy_str                | 194 ms                                                      | 167 ms: 1.17x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.3 ms: 1.15x faster                                                       |
| deepcopy                 | 255 us                                                      | 224 us: 1.14x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 35.0 ms: 1.14x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.69 sec: 1.14x faster                                                      |
| sqlglot_normalize        | 205 ms                                                      | 181 ms: 1.13x faster                                                        |
| scimark_fft              | 187 ms                                                      | 166 ms: 1.13x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.97 us: 1.12x faster                                                       |
| 2to3                     | 246 ms                                                      | 220 ms: 1.12x faster                                                        |
| sympy_expand             | 314 ms                                                      | 282 ms: 1.11x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.12 us: 1.10x faster                                                       |
| fannkuch                 | 256 ms                                                      | 232 ms: 1.10x faster                                                        |
| aiohttp                  | 995 us                                                      | 902 us: 1.10x faster                                                        |
| json                     | 3.14 ms                                                     | 2.88 ms: 1.09x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.71 us: 1.09x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 14.3 ms: 1.08x faster                                                       |
| nqueens                  | 66.6 ms                                                     | 62.0 ms: 1.07x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 60.6 ms: 1.07x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 90.7 ms: 1.07x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 72.3 ms: 1.05x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| pathlib                  | 75.7 ms                                                     | 74.9 ms: 1.01x faster                                                       |
| unpickle_list            | 2.71 us                                                     | 2.78 us: 1.02x slower                                                       |
| python_startup           | 20.6 ms                                                     | 21.5 ms: 1.05x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.22 us: 1.05x slower                                                       |
| async_generators         | 222 ms                                                      | 238 ms: 1.07x slower                                                        |
| pickle_list              | 2.75 us                                                     | 2.99 us: 1.09x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 67.6 ms: 1.09x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.8 us: 1.09x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.56 ms: 1.10x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 899 us: 1.12x slower                                                        |
| coverage                 | 39.0 ms                                                     | 45.3 ms: 1.16x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.71 ms: 1.19x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 19.6 ms: 1.26x slower                                                       |
| thrift                   | 617 us                                                      | 8.68 ms: 14.05x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                                |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown