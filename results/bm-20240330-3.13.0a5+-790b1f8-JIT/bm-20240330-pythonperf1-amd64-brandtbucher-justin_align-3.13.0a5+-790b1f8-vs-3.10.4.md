# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 220 ms: 1.12x faster                                                      |
| chameleon      | 5.79 ms                                                     | 4.74 ms: 1.22x faster                                                     |
| docutils       | 1.92 sec                                                    | 1.69 sec: 1.14x faster                                                    |
| html5lib       | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                     |
| tornado_http   | 108 ms                                                      | 83.9 ms: 1.29x faster                                                     |
| Geometric mean | (ref)                                                       | 1.23x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 216 ms: 2.02x faster                                                      |
| async_tree_memoization  | 526 ms                                                      | 268 ms: 1.96x faster                                                      |
| async_tree_io           | 1.11 sec                                                    | 570 ms: 1.95x faster                                                      |
| async_tree_cpu_io_mixed | 638 ms                                                      | 375 ms: 1.70x faster                                                      |
| Geometric mean          | (ref)                                                       | 1.90x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 47.2 ms: 1.31x faster                                                     |
| nbody          | 71.3 ms                                                     | 59.0 ms: 1.21x faster                                                     |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                       | 1.17x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 89.1 ms: 1.19x faster                                                     |
| regex_dna      | 136 ms                                                      | 118 ms: 1.16x faster                                                      |
| regex_v8       | 15.4 ms                                                     | 14.2 ms: 1.09x faster                                                     |
| regex_effbot   | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                       | 1.12x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.57 ms: 1.64x faster                                                     |
| pickle_pure_python   | 270 us                                                      | 172 us: 1.57x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 136 us: 1.35x faster                                                      |
| tomli_loads          | 1.67 sec                                                    | 1.32 sec: 1.27x faster                                                    |
| xml_etree_process    | 44.5 ms                                                     | 37.0 ms: 1.20x faster                                                     |
| xml_etree_parse      | 96.8 ms                                                     | 89.6 ms: 1.08x faster                                                     |
| unpickle             | 9.09 us                                                     | 8.56 us: 1.06x faster                                                     |
| xml_etree_iterparse  | 65.0 ms                                                     | 61.3 ms: 1.06x faster                                                     |
| xml_etree_generate   | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| json_loads           | 14.0 us                                                     | 14.5 us: 1.04x slower                                                     |
| pickle               | 6.85 us                                                     | 7.16 us: 1.05x slower                                                     |
| pickle_list          | 2.75 us                                                     | 2.88 us: 1.05x slower                                                     |
| pickle_dict          | 17.2 us                                                     | 18.5 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                              |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                     |
| python_startup_no_site | 15.5 ms                                                     | 19.6 ms: 1.26x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.08 ms: 1.49x faster                                                     |
| genshi_text     | 19.8 ms                                                     | 15.0 ms: 1.32x faster                                                     |
| django_template | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                     |
| genshi_xml      | 41.0 ms                                                     | 33.3 ms: 1.23x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.33x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 70.6 us: 4.76x faster                                                     |
| deltablue                | 4.19 ms                                                     | 2.02 ms: 2.07x faster                                                     |
| async_tree_none          | 435 ms                                                      | 216 ms: 2.02x faster                                                      |
| async_tree_memoization   | 526 ms                                                      | 268 ms: 1.96x faster                                                      |
| async_tree_io            | 1.11 sec                                                    | 570 ms: 1.95x faster                                                      |
| pylint                   | 350 ms                                                      | 195 ms: 1.79x faster                                                      |
| logging_silent           | 94.6 ns                                                     | 53.1 ns: 1.78x faster                                                     |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 375 ms: 1.70x faster                                                      |
| json_dumps               | 9.16 ms                                                     | 5.57 ms: 1.64x faster                                                     |
| generators               | 32.4 ms                                                     | 20.3 ms: 1.59x faster                                                     |
| pickle_pure_python       | 270 us                                                      | 172 us: 1.57x faster                                                      |
| chaos                    | 61.7 ms                                                     | 40.1 ms: 1.54x faster                                                     |
| raytrace                 | 273 ms                                                      | 178 ms: 1.53x faster                                                      |
| sqlglot_parse            | 1.22 ms                                                     | 796 us: 1.53x faster                                                      |
| asyncio_tcp              | 732 ms                                                      | 480 ms: 1.53x faster                                                      |
| richards_super           | 52.2 ms                                                     | 34.4 ms: 1.52x faster                                                     |
| mako                     | 9.03 ms                                                     | 6.08 ms: 1.49x faster                                                     |
| sqlglot_transpile        | 1.48 ms                                                     | 1.01 ms: 1.45x faster                                                     |
| go                       | 139 ms                                                      | 96.7 ms: 1.44x faster                                                     |
| html5lib                 | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                     |
| crypto_pyaes             | 62.5 ms                                                     | 44.9 ms: 1.39x faster                                                     |
| spectral_norm            | 77.3 ms                                                     | 55.6 ms: 1.39x faster                                                     |
| pyflate                  | 409 ms                                                      | 296 ms: 1.38x faster                                                      |
| comprehensions           | 16.5 us                                                     | 12.0 us: 1.38x faster                                                     |
| richards                 | 42.4 ms                                                     | 31.0 ms: 1.37x faster                                                     |
| scimark_monte_carlo      | 57.3 ms                                                     | 42.3 ms: 1.35x faster                                                     |
| unpickle_pure_python     | 183 us                                                      | 136 us: 1.35x faster                                                      |
| genshi_text              | 19.8 ms                                                     | 15.0 ms: 1.32x faster                                                     |
| float                    | 61.7 ms                                                     | 47.2 ms: 1.31x faster                                                     |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.63 sec: 1.30x faster                                                    |
| deepcopy_memo            | 28.8 us                                                     | 22.3 us: 1.29x faster                                                     |
| tornado_http             | 108 ms                                                      | 83.9 ms: 1.29x faster                                                     |
| pycparser                | 930 ms                                                      | 725 ms: 1.28x faster                                                      |
| django_template          | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                     |
| tomli_loads              | 1.67 sec                                                    | 1.32 sec: 1.27x faster                                                    |
| scimark_sor              | 106 ms                                                      | 84.1 ms: 1.26x faster                                                     |
| dulwich_log              | 50.5 ms                                                     | 40.9 ms: 1.23x faster                                                     |
| genshi_xml               | 41.0 ms                                                     | 33.3 ms: 1.23x faster                                                     |
| mypy2                    | 555 ms                                                      | 453 ms: 1.23x faster                                                      |
| chameleon                | 5.79 ms                                                     | 4.74 ms: 1.22x faster                                                     |
| coroutines               | 16.0 ms                                                     | 13.1 ms: 1.22x faster                                                     |
| sympy_sum                | 107 ms                                                      | 87.9 ms: 1.22x faster                                                     |
| nbody                    | 71.3 ms                                                     | 59.0 ms: 1.21x faster                                                     |
| xml_etree_process        | 44.5 ms                                                     | 37.0 ms: 1.20x faster                                                     |
| sqlite_synth             | 1.91 us                                                     | 1.60 us: 1.20x faster                                                     |
| pprint_safe_repr         | 592 ms                                                      | 496 ms: 1.19x faster                                                      |
| regex_compile            | 106 ms                                                      | 89.1 ms: 1.19x faster                                                     |
| pprint_pformat           | 1.22 sec                                                    | 1.03 sec: 1.18x faster                                                    |
| deepcopy                 | 255 us                                                      | 219 us: 1.17x faster                                                      |
| mdp                      | 1.78 sec                                                    | 1.54 sec: 1.16x faster                                                    |
| regex_dna                | 136 ms                                                      | 118 ms: 1.16x faster                                                      |
| bench_thread_pool        | 958 us                                                      | 828 us: 1.16x faster                                                      |
| sympy_str                | 194 ms                                                      | 168 ms: 1.16x faster                                                      |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.38 ms: 1.14x faster                                                     |
| sympy_integrate          | 15.3 ms                                                     | 13.4 ms: 1.14x faster                                                     |
| deepcopy_reduce          | 2.20 us                                                     | 1.94 us: 1.14x faster                                                     |
| scimark_lu               | 85.8 ms                                                     | 75.5 ms: 1.14x faster                                                     |
| docutils                 | 1.92 sec                                                    | 1.69 sec: 1.14x faster                                                    |
| sqlglot_normalize        | 205 ms                                                      | 182 ms: 1.13x faster                                                      |
| sqlglot_optimize         | 39.8 ms                                                     | 35.3 ms: 1.13x faster                                                     |
| 2to3                     | 246 ms                                                      | 220 ms: 1.12x faster                                                      |
| aiohttp                  | 995 us                                                      | 903 us: 1.10x faster                                                      |
| hexiom                   | 5.74 ms                                                     | 5.22 ms: 1.10x faster                                                     |
| regex_v8                 | 15.4 ms                                                     | 14.2 ms: 1.09x faster                                                     |
| sympy_expand             | 314 ms                                                      | 290 ms: 1.09x faster                                                      |
| xml_etree_parse          | 96.8 ms                                                     | 89.6 ms: 1.08x faster                                                     |
| regex_effbot             | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                     |
| unpickle                 | 9.09 us                                                     | 8.56 us: 1.06x faster                                                     |
| xml_etree_iterparse      | 65.0 ms                                                     | 61.3 ms: 1.06x faster                                                     |
| scimark_fft              | 187 ms                                                      | 178 ms: 1.05x faster                                                      |
| xml_etree_generate       | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| nqueens                  | 66.6 ms                                                     | 63.6 ms: 1.05x faster                                                     |
| logging_format           | 6.76 us                                                     | 6.51 us: 1.04x faster                                                     |
| meteor_contest           | 75.9 ms                                                     | 73.4 ms: 1.03x faster                                                     |
| logging_simple           | 6.22 us                                                     | 6.05 us: 1.03x faster                                                     |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                      |
| pathlib                  | 75.7 ms                                                     | 77.5 ms: 1.02x slower                                                     |
| fannkuch                 | 256 ms                                                      | 263 ms: 1.03x slower                                                      |
| json_loads               | 14.0 us                                                     | 14.5 us: 1.04x slower                                                     |
| pickle                   | 6.85 us                                                     | 7.16 us: 1.05x slower                                                     |
| pickle_list              | 2.75 us                                                     | 2.88 us: 1.05x slower                                                     |
| create_gc_cycles         | 800 us                                                      | 851 us: 1.06x slower                                                      |
| python_startup           | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                     |
| pickle_dict              | 17.2 us                                                     | 18.5 us: 1.07x slower                                                     |
| gc_traversal             | 1.41 ms                                                     | 1.52 ms: 1.08x slower                                                     |
| bench_mp_pool            | 62.0 ms                                                     | 67.3 ms: 1.08x slower                                                     |
| async_generators         | 222 ms                                                      | 244 ms: 1.10x slower                                                      |
| coverage                 | 39.0 ms                                                     | 44.7 ms: 1.15x slower                                                     |
| telco                    | 3.94 ms                                                     | 4.91 ms: 1.25x slower                                                     |
| python_startup_no_site   | 15.5 ms                                                     | 19.6 ms: 1.26x slower                                                     |
| unpack_sequence          | 39.6 ns                                                     | 57.5 ns: 1.45x slower                                                     |
| thrift                   | 617 us                                                      | 9.29 ms: 15.05x slower                                                    |
| Geometric mean           | (ref)                                                       | 1.19x faster                                                              |

Benchmark hidden because not significant (2): unpickle_list, json
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: unknown