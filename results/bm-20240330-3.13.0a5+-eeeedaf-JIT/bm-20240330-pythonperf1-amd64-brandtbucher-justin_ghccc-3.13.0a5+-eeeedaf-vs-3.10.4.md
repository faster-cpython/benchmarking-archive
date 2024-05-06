# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-amd64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 218 ms: 1.13x faster                                                      |
| chameleon      | 5.79 ms                                                     | 4.79 ms: 1.21x faster                                                     |
| docutils       | 1.92 sec                                                    | 1.69 sec: 1.13x faster                                                    |
| html5lib       | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                     |
| tornado_http   | 108 ms                                                      | 85.5 ms: 1.27x faster                                                     |
| Geometric mean | (ref)                                                       | 1.22x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 214 ms: 2.04x faster                                                      |
| async_tree_memoization  | 526 ms                                                      | 267 ms: 1.97x faster                                                      |
| async_tree_io           | 1.11 sec                                                    | 567 ms: 1.95x faster                                                      |
| async_tree_cpu_io_mixed | 638 ms                                                      | 376 ms: 1.70x faster                                                      |
| Geometric mean          | (ref)                                                       | 1.91x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.0 ms: 1.34x faster                                                     |
| nbody          | 71.3 ms                                                     | 58.3 ms: 1.22x faster                                                     |
| pidigits       | 149 ms                                                      | 146 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                       | 1.19x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 83.8 ms: 1.27x faster                                                     |
| regex_dna      | 136 ms                                                      | 116 ms: 1.18x faster                                                      |
| regex_effbot   | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                     |
| regex_v8       | 15.4 ms                                                     | 14.6 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                       | 1.14x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.55 ms: 1.65x faster                                                     |
| pickle_pure_python   | 270 us                                                      | 173 us: 1.56x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 125 us: 1.46x faster                                                      |
| tomli_loads          | 1.67 sec                                                    | 1.17 sec: 1.43x faster                                                    |
| xml_etree_process    | 44.5 ms                                                     | 37.1 ms: 1.20x faster                                                     |
| xml_etree_parse      | 96.8 ms                                                     | 90.1 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 65.0 ms                                                     | 60.7 ms: 1.07x faster                                                     |
| unpickle             | 9.09 us                                                     | 8.50 us: 1.07x faster                                                     |
| xml_etree_generate   | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| unpickle_list        | 2.71 us                                                     | 2.77 us: 1.02x slower                                                     |
| pickle_list          | 2.75 us                                                     | 2.86 us: 1.04x slower                                                     |
| pickle               | 6.85 us                                                     | 7.26 us: 1.06x slower                                                     |
| pickle_dict          | 17.2 us                                                     | 18.5 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.15x faster                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 22.0 ms: 1.07x slower                                                     |
| python_startup_no_site | 15.5 ms                                                     | 19.6 ms: 1.27x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.22 ms: 1.73x faster                                                     |
| genshi_text     | 19.8 ms                                                     | 15.1 ms: 1.31x faster                                                     |
| django_template | 28.9 ms                                                     | 23.3 ms: 1.24x faster                                                     |
| genshi_xml      | 41.0 ms                                                     | 34.0 ms: 1.21x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.36x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 70.2 us: 4.79x faster                                                     |
| async_tree_none          | 435 ms                                                      | 214 ms: 2.04x faster                                                      |
| deltablue                | 4.19 ms                                                     | 2.06 ms: 2.03x faster                                                     |
| async_tree_memoization   | 526 ms                                                      | 267 ms: 1.97x faster                                                      |
| async_tree_io            | 1.11 sec                                                    | 567 ms: 1.95x faster                                                      |
| pylint                   | 350 ms                                                      | 195 ms: 1.79x faster                                                      |
| logging_silent           | 94.6 ns                                                     | 53.1 ns: 1.78x faster                                                     |
| mako                     | 9.03 ms                                                     | 5.22 ms: 1.73x faster                                                     |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 376 ms: 1.70x faster                                                      |
| spectral_norm            | 77.3 ms                                                     | 46.1 ms: 1.68x faster                                                     |
| json_dumps               | 9.16 ms                                                     | 5.55 ms: 1.65x faster                                                     |
| chaos                    | 61.7 ms                                                     | 37.9 ms: 1.63x faster                                                     |
| generators               | 32.4 ms                                                     | 20.0 ms: 1.62x faster                                                     |
| richards_super           | 52.2 ms                                                     | 32.7 ms: 1.59x faster                                                     |
| scimark_monte_carlo      | 57.3 ms                                                     | 36.1 ms: 1.59x faster                                                     |
| sqlglot_parse            | 1.22 ms                                                     | 779 us: 1.56x faster                                                      |
| pickle_pure_python       | 270 us                                                      | 173 us: 1.56x faster                                                      |
| raytrace                 | 273 ms                                                      | 176 ms: 1.55x faster                                                      |
| pyflate                  | 409 ms                                                      | 264 ms: 1.55x faster                                                      |
| asyncio_tcp              | 732 ms                                                      | 475 ms: 1.54x faster                                                      |
| comprehensions           | 16.5 us                                                     | 10.8 us: 1.53x faster                                                     |
| crypto_pyaes             | 62.5 ms                                                     | 41.9 ms: 1.49x faster                                                     |
| sqlglot_transpile        | 1.48 ms                                                     | 995 us: 1.48x faster                                                      |
| unpickle_pure_python     | 183 us                                                      | 125 us: 1.46x faster                                                      |
| go                       | 139 ms                                                      | 95.3 ms: 1.46x faster                                                     |
| richards                 | 42.4 ms                                                     | 29.5 ms: 1.44x faster                                                     |
| tomli_loads              | 1.67 sec                                                    | 1.17 sec: 1.43x faster                                                    |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.51 sec: 1.40x faster                                                    |
| html5lib                 | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                     |
| float                    | 61.7 ms                                                     | 46.0 ms: 1.34x faster                                                     |
| scimark_sor              | 106 ms                                                      | 79.3 ms: 1.34x faster                                                     |
| genshi_text              | 19.8 ms                                                     | 15.1 ms: 1.31x faster                                                     |
| deepcopy_memo            | 28.8 us                                                     | 22.1 us: 1.30x faster                                                     |
| hexiom                   | 5.74 ms                                                     | 4.47 ms: 1.29x faster                                                     |
| pprint_pformat           | 1.22 sec                                                    | 951 ms: 1.28x faster                                                      |
| pycparser                | 930 ms                                                      | 728 ms: 1.28x faster                                                      |
| pprint_safe_repr         | 592 ms                                                      | 466 ms: 1.27x faster                                                      |
| tornado_http             | 108 ms                                                      | 85.5 ms: 1.27x faster                                                     |
| regex_compile            | 106 ms                                                      | 83.8 ms: 1.27x faster                                                     |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.19 ms: 1.24x faster                                                     |
| django_template          | 28.9 ms                                                     | 23.3 ms: 1.24x faster                                                     |
| mypy2                    | 555 ms                                                      | 453 ms: 1.23x faster                                                      |
| nbody                    | 71.3 ms                                                     | 58.3 ms: 1.22x faster                                                     |
| scimark_fft              | 187 ms                                                      | 153 ms: 1.22x faster                                                      |
| sympy_sum                | 107 ms                                                      | 87.7 ms: 1.22x faster                                                     |
| dulwich_log              | 50.5 ms                                                     | 41.5 ms: 1.22x faster                                                     |
| sqlite_synth             | 1.91 us                                                     | 1.57 us: 1.22x faster                                                     |
| chameleon                | 5.79 ms                                                     | 4.79 ms: 1.21x faster                                                     |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                     |
| genshi_xml               | 41.0 ms                                                     | 34.0 ms: 1.21x faster                                                     |
| xml_etree_process        | 44.5 ms                                                     | 37.1 ms: 1.20x faster                                                     |
| scimark_lu               | 85.8 ms                                                     | 71.8 ms: 1.19x faster                                                     |
| mdp                      | 1.78 sec                                                    | 1.51 sec: 1.18x faster                                                    |
| regex_dna                | 136 ms                                                      | 116 ms: 1.18x faster                                                      |
| fannkuch                 | 256 ms                                                      | 220 ms: 1.16x faster                                                      |
| sympy_str                | 194 ms                                                      | 167 ms: 1.16x faster                                                      |
| sympy_integrate          | 15.3 ms                                                     | 13.2 ms: 1.16x faster                                                     |
| bench_thread_pool        | 958 us                                                      | 833 us: 1.15x faster                                                      |
| deepcopy                 | 255 us                                                      | 225 us: 1.14x faster                                                      |
| docutils                 | 1.92 sec                                                    | 1.69 sec: 1.13x faster                                                    |
| 2to3                     | 246 ms                                                      | 218 ms: 1.13x faster                                                      |
| deepcopy_reduce          | 2.20 us                                                     | 1.98 us: 1.11x faster                                                     |
| sqlglot_optimize         | 39.8 ms                                                     | 35.8 ms: 1.11x faster                                                     |
| sqlglot_normalize        | 205 ms                                                      | 186 ms: 1.11x faster                                                      |
| nqueens                  | 66.6 ms                                                     | 60.4 ms: 1.10x faster                                                     |
| aiohttp                  | 995 us                                                      | 909 us: 1.10x faster                                                      |
| sympy_expand             | 314 ms                                                      | 288 ms: 1.09x faster                                                      |
| logging_format           | 6.76 us                                                     | 6.27 us: 1.08x faster                                                     |
| xml_etree_parse          | 96.8 ms                                                     | 90.1 ms: 1.07x faster                                                     |
| xml_etree_iterparse      | 65.0 ms                                                     | 60.7 ms: 1.07x faster                                                     |
| regex_effbot             | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                     |
| unpickle                 | 9.09 us                                                     | 8.50 us: 1.07x faster                                                     |
| logging_simple           | 6.22 us                                                     | 5.86 us: 1.06x faster                                                     |
| regex_v8                 | 15.4 ms                                                     | 14.6 ms: 1.06x faster                                                     |
| meteor_contest           | 75.9 ms                                                     | 72.0 ms: 1.05x faster                                                     |
| xml_etree_generate       | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                     |
| json                     | 3.14 ms                                                     | 3.01 ms: 1.04x faster                                                     |
| pidigits                 | 149 ms                                                      | 146 ms: 1.02x faster                                                      |
| unpickle_list            | 2.71 us                                                     | 2.77 us: 1.02x slower                                                     |
| pathlib                  | 75.7 ms                                                     | 77.4 ms: 1.02x slower                                                     |
| pickle_list              | 2.75 us                                                     | 2.86 us: 1.04x slower                                                     |
| pickle                   | 6.85 us                                                     | 7.26 us: 1.06x slower                                                     |
| create_gc_cycles         | 800 us                                                      | 850 us: 1.06x slower                                                      |
| python_startup           | 20.6 ms                                                     | 22.0 ms: 1.07x slower                                                     |
| pickle_dict              | 17.2 us                                                     | 18.5 us: 1.08x slower                                                     |
| bench_mp_pool            | 62.0 ms                                                     | 67.4 ms: 1.09x slower                                                     |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                     |
| async_generators         | 222 ms                                                      | 247 ms: 1.11x slower                                                      |
| telco                    | 3.94 ms                                                     | 4.69 ms: 1.19x slower                                                     |
| coverage                 | 39.0 ms                                                     | 46.7 ms: 1.20x slower                                                     |
| python_startup_no_site   | 15.5 ms                                                     | 19.6 ms: 1.27x slower                                                     |
| unpack_sequence          | 39.6 ns                                                     | 60.8 ns: 1.53x slower                                                     |
| thrift                   | 617 us                                                      | 9.19 ms: 14.89x slower                                                    |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                              |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown