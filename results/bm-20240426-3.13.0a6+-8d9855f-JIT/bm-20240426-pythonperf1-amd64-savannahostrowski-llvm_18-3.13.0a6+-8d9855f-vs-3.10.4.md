# Results vs. 3.10.4

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-amd64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 228 ms: 1.08x faster                                                      |
| chameleon      | 5.79 ms                                                     | 4.77 ms: 1.21x faster                                                     |
| docutils       | 1.92 sec                                                    | 1.72 sec: 1.11x faster                                                    |
| html5lib       | 51.0 ms                                                     | 35.4 ms: 1.44x faster                                                     |
| tornado_http   | 108 ms                                                      | 93.0 ms: 1.17x faster                                                     |
| Geometric mean | (ref)                                                       | 1.20x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 224 ms: 1.94x faster                                                      |
| async_tree_memoization  | 526 ms                                                      | 272 ms: 1.93x faster                                                      |
| async_tree_io           | 1.11 sec                                                    | 599 ms: 1.85x faster                                                      |
| async_tree_cpu_io_mixed | 638 ms                                                      | 396 ms: 1.61x faster                                                      |
| Geometric mean          | (ref)                                                       | 1.83x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 45.9 ms: 1.34x faster                                                     |
| nbody          | 71.3 ms                                                     | 62.4 ms: 1.14x faster                                                     |
| pidigits       | 149 ms                                                      | 148 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                       | 1.16x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 88.0 ms: 1.20x faster                                                     |
| regex_dna      | 136 ms                                                      | 120 ms: 1.13x faster                                                      |
| regex_effbot   | 1.66 ms                                                     | 1.60 ms: 1.04x faster                                                     |
| regex_v8       | 15.4 ms                                                     | 15.6 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                       | 1.09x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.67 ms: 1.62x faster                                                     |
| pickle_pure_python   | 270 us                                                      | 173 us: 1.56x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 123 us: 1.48x faster                                                      |
| tomli_loads          | 1.67 sec                                                    | 1.18 sec: 1.41x faster                                                    |
| xml_etree_process    | 44.5 ms                                                     | 36.8 ms: 1.21x faster                                                     |
| unpickle             | 9.09 us                                                     | 8.56 us: 1.06x faster                                                     |
| xml_etree_iterparse  | 65.0 ms                                                     | 61.6 ms: 1.06x faster                                                     |
| xml_etree_parse      | 96.8 ms                                                     | 92.3 ms: 1.05x faster                                                     |
| xml_etree_generate   | 55.5 ms                                                     | 54.3 ms: 1.02x faster                                                     |
| json_loads           | 14.0 us                                                     | 14.3 us: 1.02x slower                                                     |
| unpickle_list        | 2.71 us                                                     | 2.79 us: 1.03x slower                                                     |
| pickle               | 6.85 us                                                     | 7.39 us: 1.08x slower                                                     |
| pickle_dict          | 17.2 us                                                     | 18.7 us: 1.09x slower                                                     |
| pickle_list          | 2.75 us                                                     | 3.12 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 22.4 ms: 1.09x slower                                                     |
| python_startup_no_site | 15.5 ms                                                     | 18.5 ms: 1.19x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.34 ms: 1.69x faster                                                     |
| django_template | 28.9 ms                                                     | 22.8 ms: 1.27x faster                                                     |
| genshi_text     | 19.8 ms                                                     | 16.7 ms: 1.19x faster                                                     |
| genshi_xml      | 41.0 ms                                                     | 39.1 ms: 1.05x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.28x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|--------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 113 us: 2.98x faster                                                      |
| async_tree_none          | 435 ms                                                      | 224 ms: 1.94x faster                                                      |
| async_tree_memoization   | 526 ms                                                      | 272 ms: 1.93x faster                                                      |
| deltablue                | 4.19 ms                                                     | 2.21 ms: 1.90x faster                                                     |
| async_tree_io            | 1.11 sec                                                    | 599 ms: 1.85x faster                                                      |
| logging_silent           | 94.6 ns                                                     | 53.4 ns: 1.77x faster                                                     |
| richards_super           | 52.2 ms                                                     | 30.2 ms: 1.73x faster                                                     |
| mako                     | 9.03 ms                                                     | 5.34 ms: 1.69x faster                                                     |
| raytrace                 | 273 ms                                                      | 167 ms: 1.64x faster                                                      |
| json_dumps               | 9.16 ms                                                     | 5.67 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 396 ms: 1.61x faster                                                      |
| generators               | 32.4 ms                                                     | 20.3 ms: 1.60x faster                                                     |
| sqlglot_parse            | 1.22 ms                                                     | 770 us: 1.58x faster                                                      |
| richards                 | 42.4 ms                                                     | 27.1 ms: 1.56x faster                                                     |
| pylint                   | 350 ms                                                      | 224 ms: 1.56x faster                                                      |
| pickle_pure_python       | 270 us                                                      | 173 us: 1.56x faster                                                      |
| comprehensions           | 16.5 us                                                     | 10.7 us: 1.54x faster                                                     |
| spectral_norm            | 77.3 ms                                                     | 50.4 ms: 1.53x faster                                                     |
| chaos                    | 61.7 ms                                                     | 40.4 ms: 1.53x faster                                                     |
| pyflate                  | 409 ms                                                      | 268 ms: 1.53x faster                                                      |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.2 ms: 1.50x faster                                                     |
| sqlglot_transpile        | 1.48 ms                                                     | 993 us: 1.49x faster                                                      |
| unpickle_pure_python     | 183 us                                                      | 123 us: 1.48x faster                                                      |
| html5lib                 | 51.0 ms                                                     | 35.4 ms: 1.44x faster                                                     |
| go                       | 139 ms                                                      | 97.2 ms: 1.43x faster                                                     |
| crypto_pyaes             | 62.5 ms                                                     | 44.3 ms: 1.41x faster                                                     |
| tomli_loads              | 1.67 sec                                                    | 1.18 sec: 1.41x faster                                                    |
| pprint_pformat           | 1.22 sec                                                    | 905 ms: 1.35x faster                                                      |
| pprint_safe_repr         | 592 ms                                                      | 440 ms: 1.34x faster                                                      |
| float                    | 61.7 ms                                                     | 45.9 ms: 1.34x faster                                                     |
| deepcopy_memo            | 28.8 us                                                     | 22.0 us: 1.31x faster                                                     |
| pycparser                | 930 ms                                                      | 721 ms: 1.29x faster                                                      |
| scimark_sor              | 106 ms                                                      | 83.4 ms: 1.27x faster                                                     |
| django_template          | 28.9 ms                                                     | 22.8 ms: 1.27x faster                                                     |
| coroutines               | 16.0 ms                                                     | 12.8 ms: 1.25x faster                                                     |
| mdp                      | 1.78 sec                                                    | 1.44 sec: 1.23x faster                                                    |
| scimark_lu               | 85.8 ms                                                     | 69.6 ms: 1.23x faster                                                     |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.22 ms: 1.23x faster                                                     |
| dulwich_log              | 50.5 ms                                                     | 41.2 ms: 1.23x faster                                                     |
| hexiom                   | 5.74 ms                                                     | 4.70 ms: 1.22x faster                                                     |
| chameleon                | 5.79 ms                                                     | 4.77 ms: 1.21x faster                                                     |
| xml_etree_process        | 44.5 ms                                                     | 36.8 ms: 1.21x faster                                                     |
| regex_compile            | 106 ms                                                      | 88.0 ms: 1.20x faster                                                     |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.76 sec: 1.20x faster                                                    |
| sympy_sum                | 107 ms                                                      | 89.8 ms: 1.19x faster                                                     |
| genshi_text              | 19.8 ms                                                     | 16.7 ms: 1.19x faster                                                     |
| mypy2                    | 555 ms                                                      | 471 ms: 1.18x faster                                                      |
| sqlite_synth             | 1.91 us                                                     | 1.63 us: 1.18x faster                                                     |
| tornado_http             | 108 ms                                                      | 93.0 ms: 1.17x faster                                                     |
| nbody                    | 71.3 ms                                                     | 62.4 ms: 1.14x faster                                                     |
| sympy_str                | 194 ms                                                      | 171 ms: 1.14x faster                                                      |
| deepcopy_reduce          | 2.20 us                                                     | 1.94 us: 1.14x faster                                                     |
| sqlglot_optimize         | 39.8 ms                                                     | 35.1 ms: 1.14x faster                                                     |
| regex_dna                | 136 ms                                                      | 120 ms: 1.13x faster                                                      |
| bench_thread_pool        | 958 us                                                      | 847 us: 1.13x faster                                                      |
| deepcopy                 | 255 us                                                      | 226 us: 1.13x faster                                                      |
| sympy_integrate          | 15.3 ms                                                     | 13.6 ms: 1.12x faster                                                     |
| sqlglot_normalize        | 205 ms                                                      | 183 ms: 1.12x faster                                                      |
| scimark_fft              | 187 ms                                                      | 167 ms: 1.12x faster                                                      |
| docutils                 | 1.92 sec                                                    | 1.72 sec: 1.11x faster                                                    |
| fannkuch                 | 256 ms                                                      | 231 ms: 1.11x faster                                                      |
| asyncio_tcp              | 732 ms                                                      | 670 ms: 1.09x faster                                                      |
| sympy_expand             | 314 ms                                                      | 289 ms: 1.09x faster                                                      |
| 2to3                     | 246 ms                                                      | 228 ms: 1.08x faster                                                      |
| logging_format           | 6.76 us                                                     | 6.34 us: 1.07x faster                                                     |
| unpickle                 | 9.09 us                                                     | 8.56 us: 1.06x faster                                                     |
| xml_etree_iterparse      | 65.0 ms                                                     | 61.6 ms: 1.06x faster                                                     |
| logging_simple           | 6.22 us                                                     | 5.91 us: 1.05x faster                                                     |
| genshi_xml               | 41.0 ms                                                     | 39.1 ms: 1.05x faster                                                     |
| xml_etree_parse          | 96.8 ms                                                     | 92.3 ms: 1.05x faster                                                     |
| regex_effbot             | 1.66 ms                                                     | 1.60 ms: 1.04x faster                                                     |
| meteor_contest           | 75.9 ms                                                     | 73.2 ms: 1.04x faster                                                     |
| aiohttp                  | 995 us                                                      | 963 us: 1.03x faster                                                      |
| nqueens                  | 66.6 ms                                                     | 65.0 ms: 1.02x faster                                                     |
| xml_etree_generate       | 55.5 ms                                                     | 54.3 ms: 1.02x faster                                                     |
| pidigits                 | 149 ms                                                      | 148 ms: 1.01x faster                                                      |
| regex_v8                 | 15.4 ms                                                     | 15.6 ms: 1.01x slower                                                     |
| json_loads               | 14.0 us                                                     | 14.3 us: 1.02x slower                                                     |
| unpickle_list            | 2.71 us                                                     | 2.79 us: 1.03x slower                                                     |
| json                     | 3.14 ms                                                     | 3.32 ms: 1.06x slower                                                     |
| pathlib                  | 75.7 ms                                                     | 80.9 ms: 1.07x slower                                                     |
| pickle                   | 6.85 us                                                     | 7.39 us: 1.08x slower                                                     |
| python_startup           | 20.6 ms                                                     | 22.4 ms: 1.09x slower                                                     |
| async_generators         | 222 ms                                                      | 241 ms: 1.09x slower                                                      |
| pickle_dict              | 17.2 us                                                     | 18.7 us: 1.09x slower                                                     |
| gc_traversal             | 1.41 ms                                                     | 1.58 ms: 1.12x slower                                                     |
| bench_mp_pool            | 62.0 ms                                                     | 69.5 ms: 1.12x slower                                                     |
| pickle_list              | 2.75 us                                                     | 3.12 us: 1.13x slower                                                     |
| coverage                 | 39.0 ms                                                     | 44.7 ms: 1.14x slower                                                     |
| create_gc_cycles         | 800 us                                                      | 932 us: 1.17x slower                                                      |
| python_startup_no_site   | 15.5 ms                                                     | 18.5 ms: 1.19x slower                                                     |
| telco                    | 3.94 ms                                                     | 4.72 ms: 1.20x slower                                                     |
| thrift                   | 617 us                                                      | 9.13 ms: 14.80x slower                                                    |
| Geometric mean           | (ref)                                                       | 1.19x faster                                                              |
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-8d9855f-JIT/bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: unknown