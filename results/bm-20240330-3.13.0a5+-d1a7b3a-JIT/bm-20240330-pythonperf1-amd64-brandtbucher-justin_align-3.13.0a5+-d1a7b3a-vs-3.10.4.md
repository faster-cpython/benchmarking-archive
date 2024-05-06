# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 217 ms: 1.13x faster                                                      |
| chameleon      | 5.79 ms                                                     | 4.86 ms: 1.19x faster                                                     |
| docutils       | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                    |
| html5lib       | 51.0 ms                                                     | 35.5 ms: 1.44x faster                                                     |
| tornado_http   | 108 ms                                                      | 83.5 ms: 1.30x faster                                                     |
| Geometric mean | (ref)                                                       | 1.24x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 213 ms: 2.04x faster                                                      |
| async_tree_memoization  | 526 ms                                                      | 265 ms: 1.99x faster                                                      |
| async_tree_io           | 1.11 sec                                                    | 565 ms: 1.96x faster                                                      |
| async_tree_cpu_io_mixed | 638 ms                                                      | 376 ms: 1.69x faster                                                      |
| Geometric mean          | (ref)                                                       | 1.92x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 47.3 ms: 1.31x faster                                                     |
| nbody          | 71.3 ms                                                     | 57.7 ms: 1.24x faster                                                     |
| pidigits       | 149 ms                                                      | 146 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                       | 1.18x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 83.3 ms: 1.27x faster                                                     |
| regex_dna      | 136 ms                                                      | 119 ms: 1.14x faster                                                      |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                     |
| regex_v8       | 15.4 ms                                                     | 14.7 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                       | 1.13x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                     |
| pickle_pure_python   | 270 us                                                      | 174 us: 1.55x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 129 us: 1.43x faster                                                      |
| tomli_loads          | 1.67 sec                                                    | 1.20 sec: 1.39x faster                                                    |
| xml_etree_process    | 44.5 ms                                                     | 36.3 ms: 1.22x faster                                                     |
| xml_etree_parse      | 96.8 ms                                                     | 91.5 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 65.0 ms                                                     | 61.4 ms: 1.06x faster                                                     |
| unpickle             | 9.09 us                                                     | 8.70 us: 1.04x faster                                                     |
| xml_etree_generate   | 55.5 ms                                                     | 53.3 ms: 1.04x faster                                                     |
| unpickle_list        | 2.71 us                                                     | 2.74 us: 1.01x slower                                                     |
| json_loads           | 14.0 us                                                     | 14.4 us: 1.03x slower                                                     |
| pickle_list          | 2.75 us                                                     | 2.91 us: 1.06x slower                                                     |
| pickle_dict          | 17.2 us                                                     | 18.3 us: 1.06x slower                                                     |
| pickle               | 6.85 us                                                     | 7.37 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.14x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 22.3 ms: 1.08x slower                                                     |
| python_startup_no_site | 15.5 ms                                                     | 20.3 ms: 1.31x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.19x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.75 ms: 1.57x faster                                                     |
| genshi_text     | 19.8 ms                                                     | 15.0 ms: 1.32x faster                                                     |
| django_template | 28.9 ms                                                     | 22.5 ms: 1.29x faster                                                     |
| genshi_xml      | 41.0 ms                                                     | 33.0 ms: 1.24x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.35x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 69.0 us: 4.87x faster                                                     |
| deltablue                | 4.19 ms                                                     | 2.02 ms: 2.07x faster                                                     |
| async_tree_none          | 435 ms                                                      | 213 ms: 2.04x faster                                                      |
| async_tree_memoization   | 526 ms                                                      | 265 ms: 1.99x faster                                                      |
| async_tree_io            | 1.11 sec                                                    | 565 ms: 1.96x faster                                                      |
| pylint                   | 350 ms                                                      | 195 ms: 1.80x faster                                                      |
| logging_silent           | 94.6 ns                                                     | 52.8 ns: 1.79x faster                                                     |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 376 ms: 1.69x faster                                                      |
| generators               | 32.4 ms                                                     | 19.3 ms: 1.67x faster                                                     |
| json_dumps               | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                     |
| richards_super           | 52.2 ms                                                     | 32.2 ms: 1.62x faster                                                     |
| chaos                    | 61.7 ms                                                     | 39.0 ms: 1.58x faster                                                     |
| asyncio_tcp              | 732 ms                                                      | 464 ms: 1.58x faster                                                      |
| sqlglot_parse            | 1.22 ms                                                     | 772 us: 1.57x faster                                                      |
| mako                     | 9.03 ms                                                     | 5.75 ms: 1.57x faster                                                     |
| raytrace                 | 273 ms                                                      | 176 ms: 1.56x faster                                                      |
| pickle_pure_python       | 270 us                                                      | 174 us: 1.55x faster                                                      |
| spectral_norm            | 77.3 ms                                                     | 51.1 ms: 1.51x faster                                                     |
| go                       | 139 ms                                                      | 92.2 ms: 1.51x faster                                                     |
| sqlglot_transpile        | 1.48 ms                                                     | 990 us: 1.49x faster                                                      |
| richards                 | 42.4 ms                                                     | 28.7 ms: 1.48x faster                                                     |
| pyflate                  | 409 ms                                                      | 278 ms: 1.47x faster                                                      |
| comprehensions           | 16.5 us                                                     | 11.3 us: 1.46x faster                                                     |
| html5lib                 | 51.0 ms                                                     | 35.5 ms: 1.44x faster                                                     |
| unpickle_pure_python     | 183 us                                                      | 129 us: 1.43x faster                                                      |
| scimark_monte_carlo      | 57.3 ms                                                     | 40.3 ms: 1.42x faster                                                     |
| crypto_pyaes             | 62.5 ms                                                     | 44.0 ms: 1.42x faster                                                     |
| tomli_loads              | 1.67 sec                                                    | 1.20 sec: 1.39x faster                                                    |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.55 sec: 1.37x faster                                                    |
| deepcopy_memo            | 28.8 us                                                     | 21.3 us: 1.35x faster                                                     |
| genshi_text              | 19.8 ms                                                     | 15.0 ms: 1.32x faster                                                     |
| float                    | 61.7 ms                                                     | 47.3 ms: 1.31x faster                                                     |
| tornado_http             | 108 ms                                                      | 83.5 ms: 1.30x faster                                                     |
| django_template          | 28.9 ms                                                     | 22.5 ms: 1.29x faster                                                     |
| mdp                      | 1.78 sec                                                    | 1.38 sec: 1.29x faster                                                    |
| pycparser                | 930 ms                                                      | 727 ms: 1.28x faster                                                      |
| pprint_pformat           | 1.22 sec                                                    | 953 ms: 1.28x faster                                                      |
| regex_compile            | 106 ms                                                      | 83.3 ms: 1.27x faster                                                     |
| scimark_sor              | 106 ms                                                      | 83.8 ms: 1.27x faster                                                     |
| pprint_safe_repr         | 592 ms                                                      | 467 ms: 1.27x faster                                                      |
| hexiom                   | 5.74 ms                                                     | 4.53 ms: 1.27x faster                                                     |
| coroutines               | 16.0 ms                                                     | 12.8 ms: 1.25x faster                                                     |
| mypy2                    | 555 ms                                                      | 446 ms: 1.25x faster                                                      |
| genshi_xml               | 41.0 ms                                                     | 33.0 ms: 1.24x faster                                                     |
| nbody                    | 71.3 ms                                                     | 57.7 ms: 1.24x faster                                                     |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.22 ms: 1.22x faster                                                     |
| dulwich_log              | 50.5 ms                                                     | 41.2 ms: 1.22x faster                                                     |
| xml_etree_process        | 44.5 ms                                                     | 36.3 ms: 1.22x faster                                                     |
| sympy_sum                | 107 ms                                                      | 88.1 ms: 1.21x faster                                                     |
| sqlite_synth             | 1.91 us                                                     | 1.59 us: 1.20x faster                                                     |
| chameleon                | 5.79 ms                                                     | 4.86 ms: 1.19x faster                                                     |
| deepcopy                 | 255 us                                                      | 217 us: 1.18x faster                                                      |
| sympy_str                | 194 ms                                                      | 166 ms: 1.17x faster                                                      |
| bench_thread_pool        | 958 us                                                      | 824 us: 1.16x faster                                                      |
| deepcopy_reduce          | 2.20 us                                                     | 1.90 us: 1.16x faster                                                     |
| sympy_integrate          | 15.3 ms                                                     | 13.2 ms: 1.16x faster                                                     |
| docutils                 | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                    |
| sqlglot_optimize         | 39.8 ms                                                     | 34.9 ms: 1.14x faster                                                     |
| regex_dna                | 136 ms                                                      | 119 ms: 1.14x faster                                                      |
| sqlglot_normalize        | 205 ms                                                      | 181 ms: 1.14x faster                                                      |
| 2to3                     | 246 ms                                                      | 217 ms: 1.13x faster                                                      |
| fannkuch                 | 256 ms                                                      | 229 ms: 1.12x faster                                                      |
| nqueens                  | 66.6 ms                                                     | 59.8 ms: 1.11x faster                                                     |
| sympy_expand             | 314 ms                                                      | 284 ms: 1.11x faster                                                      |
| aiohttp                  | 995 us                                                      | 899 us: 1.11x faster                                                      |
| scimark_fft              | 187 ms                                                      | 170 ms: 1.10x faster                                                      |
| logging_format           | 6.76 us                                                     | 6.23 us: 1.08x faster                                                     |
| scimark_lu               | 85.8 ms                                                     | 79.9 ms: 1.07x faster                                                     |
| logging_simple           | 6.22 us                                                     | 5.80 us: 1.07x faster                                                     |
| xml_etree_parse          | 96.8 ms                                                     | 91.5 ms: 1.06x faster                                                     |
| xml_etree_iterparse      | 65.0 ms                                                     | 61.4 ms: 1.06x faster                                                     |
| json                     | 3.14 ms                                                     | 2.97 ms: 1.06x faster                                                     |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                     |
| meteor_contest           | 75.9 ms                                                     | 72.3 ms: 1.05x faster                                                     |
| regex_v8                 | 15.4 ms                                                     | 14.7 ms: 1.05x faster                                                     |
| unpickle                 | 9.09 us                                                     | 8.70 us: 1.04x faster                                                     |
| xml_etree_generate       | 55.5 ms                                                     | 53.3 ms: 1.04x faster                                                     |
| pidigits                 | 149 ms                                                      | 146 ms: 1.02x faster                                                      |
| unpickle_list            | 2.71 us                                                     | 2.74 us: 1.01x slower                                                     |
| pathlib                  | 75.7 ms                                                     | 77.4 ms: 1.02x slower                                                     |
| json_loads               | 14.0 us                                                     | 14.4 us: 1.03x slower                                                     |
| pickle_list              | 2.75 us                                                     | 2.91 us: 1.06x slower                                                     |
| pickle_dict              | 17.2 us                                                     | 18.3 us: 1.06x slower                                                     |
| create_gc_cycles         | 800 us                                                      | 855 us: 1.07x slower                                                      |
| pickle                   | 6.85 us                                                     | 7.37 us: 1.08x slower                                                     |
| bench_mp_pool            | 62.0 ms                                                     | 67.3 ms: 1.08x slower                                                     |
| python_startup           | 20.6 ms                                                     | 22.3 ms: 1.08x slower                                                     |
| gc_traversal             | 1.41 ms                                                     | 1.53 ms: 1.09x slower                                                     |
| async_generators         | 222 ms                                                      | 241 ms: 1.09x slower                                                      |
| unpack_sequence          | 39.6 ns                                                     | 45.6 ns: 1.15x slower                                                     |
| telco                    | 3.94 ms                                                     | 4.65 ms: 1.18x slower                                                     |
| coverage                 | 39.0 ms                                                     | 46.6 ms: 1.19x slower                                                     |
| python_startup_no_site   | 15.5 ms                                                     | 20.3 ms: 1.31x slower                                                     |
| thrift                   | 617 us                                                      | 8.83 ms: 14.30x slower                                                    |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                              |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown