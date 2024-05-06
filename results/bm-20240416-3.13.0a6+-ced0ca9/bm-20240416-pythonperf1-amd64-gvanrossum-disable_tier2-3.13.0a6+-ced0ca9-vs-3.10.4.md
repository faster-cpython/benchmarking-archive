# Results vs. 3.10.4

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: ced0ca9
- commit date: 2024-04-16
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 210 ms: 1.17x faster                                                     |
| chameleon      | 5.79 ms                                                     | 4.80 ms: 1.21x faster                                                    |
| docutils       | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                   |
| html5lib       | 51.0 ms                                                     | 35.8 ms: 1.43x faster                                                    |
| tornado_http   | 108 ms                                                      | 80.8 ms: 1.34x faster                                                    |
| Geometric mean | (ref)                                                       | 1.26x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|-------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 222 ms: 1.96x faster                                                     |
| async_tree_memoization  | 526 ms                                                      | 270 ms: 1.95x faster                                                     |
| async_tree_io           | 1.11 sec                                                    | 595 ms: 1.86x faster                                                     |
| async_tree_cpu_io_mixed | 638 ms                                                      | 391 ms: 1.63x faster                                                     |
| Geometric mean          | (ref)                                                       | 1.85x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 50.7 ms: 1.22x faster                                                    |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                     |
| nbody          | 71.3 ms                                                     | 70.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                       | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 79.8 ms: 1.33x faster                                                    |
| regex_dna      | 136 ms                                                      | 116 ms: 1.17x faster                                                     |
| regex_effbot   | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                    |
| regex_v8       | 15.4 ms                                                     | 18.3 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                       | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.64 ms: 1.62x faster                                                    |
| pickle_pure_python   | 270 us                                                      | 176 us: 1.53x faster                                                     |
| unpickle_pure_python | 183 us                                                      | 125 us: 1.46x faster                                                     |
| xml_etree_process    | 44.5 ms                                                     | 37.2 ms: 1.20x faster                                                    |
| tomli_loads          | 1.67 sec                                                    | 1.41 sec: 1.18x faster                                                   |
| unpickle             | 9.09 us                                                     | 8.25 us: 1.10x faster                                                    |
| xml_etree_parse      | 96.8 ms                                                     | 92.8 ms: 1.04x faster                                                    |
| xml_etree_generate   | 55.5 ms                                                     | 54.5 ms: 1.02x faster                                                    |
| xml_etree_iterparse  | 65.0 ms                                                     | 64.1 ms: 1.01x faster                                                    |
| json_loads           | 14.0 us                                                     | 13.9 us: 1.01x faster                                                    |
| pickle               | 6.85 us                                                     | 7.13 us: 1.04x slower                                                    |
| unpickle_list        | 2.71 us                                                     | 2.83 us: 1.04x slower                                                    |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                    |
| pickle_list          | 2.75 us                                                     | 3.16 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.7 ms: 1.05x faster                                                    |
| python_startup_no_site | 15.5 ms                                                     | 16.0 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.33 ms: 1.43x faster                                                    |
| django_template | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                    |
| genshi_text     | 19.8 ms                                                     | 15.9 ms: 1.25x faster                                                    |
| genshi_xml      | 41.0 ms                                                     | 33.5 ms: 1.23x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.29x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|--------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 73.9 us: 4.55x faster                                                    |
| deltablue                | 4.19 ms                                                     | 1.95 ms: 2.15x faster                                                    |
| async_tree_none          | 435 ms                                                      | 222 ms: 1.96x faster                                                     |
| async_tree_memoization   | 526 ms                                                      | 270 ms: 1.95x faster                                                     |
| async_tree_io            | 1.11 sec                                                    | 595 ms: 1.86x faster                                                     |
| raytrace                 | 273 ms                                                      | 156 ms: 1.75x faster                                                     |
| logging_silent           | 94.6 ns                                                     | 54.1 ns: 1.75x faster                                                    |
| richards_super           | 52.2 ms                                                     | 30.2 ms: 1.73x faster                                                    |
| pylint                   | 350 ms                                                      | 208 ms: 1.68x faster                                                     |
| go                       | 139 ms                                                      | 85.1 ms: 1.63x faster                                                    |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 391 ms: 1.63x faster                                                     |
| json_dumps               | 9.16 ms                                                     | 5.64 ms: 1.62x faster                                                    |
| chaos                    | 61.7 ms                                                     | 38.3 ms: 1.61x faster                                                    |
| richards                 | 42.4 ms                                                     | 26.5 ms: 1.60x faster                                                    |
| sqlglot_parse            | 1.22 ms                                                     | 760 us: 1.60x faster                                                     |
| comprehensions           | 16.5 us                                                     | 10.7 us: 1.55x faster                                                    |
| asyncio_tcp              | 732 ms                                                      | 475 ms: 1.54x faster                                                     |
| pickle_pure_python       | 270 us                                                      | 176 us: 1.53x faster                                                     |
| hexiom                   | 5.74 ms                                                     | 3.77 ms: 1.52x faster                                                    |
| sqlglot_transpile        | 1.48 ms                                                     | 971 us: 1.52x faster                                                     |
| generators               | 32.4 ms                                                     | 21.4 ms: 1.52x faster                                                    |
| scimark_lu               | 85.8 ms                                                     | 57.9 ms: 1.48x faster                                                    |
| unpickle_pure_python     | 183 us                                                      | 125 us: 1.46x faster                                                     |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.8 ms: 1.44x faster                                                    |
| mako                     | 9.03 ms                                                     | 6.33 ms: 1.43x faster                                                    |
| html5lib                 | 51.0 ms                                                     | 35.8 ms: 1.43x faster                                                    |
| pyflate                  | 409 ms                                                      | 290 ms: 1.41x faster                                                     |
| scimark_sor              | 106 ms                                                      | 76.3 ms: 1.39x faster                                                    |
| pycparser                | 930 ms                                                      | 689 ms: 1.35x faster                                                     |
| crypto_pyaes             | 62.5 ms                                                     | 46.6 ms: 1.34x faster                                                    |
| tornado_http             | 108 ms                                                      | 80.8 ms: 1.34x faster                                                    |
| regex_compile            | 106 ms                                                      | 79.8 ms: 1.33x faster                                                    |
| mypy2                    | 555 ms                                                      | 419 ms: 1.33x faster                                                     |
| deepcopy_memo            | 28.8 us                                                     | 21.8 us: 1.32x faster                                                    |
| django_template          | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                    |
| mdp                      | 1.78 sec                                                    | 1.39 sec: 1.28x faster                                                   |
| dulwich_log              | 50.5 ms                                                     | 39.5 ms: 1.28x faster                                                    |
| sympy_sum                | 107 ms                                                      | 84.5 ms: 1.27x faster                                                    |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.69 sec: 1.25x faster                                                   |
| genshi_text              | 19.8 ms                                                     | 15.9 ms: 1.25x faster                                                    |
| spectral_norm            | 77.3 ms                                                     | 62.5 ms: 1.24x faster                                                    |
| pprint_pformat           | 1.22 sec                                                    | 993 ms: 1.23x faster                                                     |
| coroutines               | 16.0 ms                                                     | 13.1 ms: 1.23x faster                                                    |
| genshi_xml               | 41.0 ms                                                     | 33.5 ms: 1.23x faster                                                    |
| float                    | 61.7 ms                                                     | 50.7 ms: 1.22x faster                                                    |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.22x faster                                                    |
| pprint_safe_repr         | 592 ms                                                      | 489 ms: 1.21x faster                                                     |
| sympy_str                | 194 ms                                                      | 161 ms: 1.21x faster                                                     |
| chameleon                | 5.79 ms                                                     | 4.80 ms: 1.21x faster                                                    |
| xml_etree_process        | 44.5 ms                                                     | 37.2 ms: 1.20x faster                                                    |
| sqlglot_optimize         | 39.8 ms                                                     | 33.4 ms: 1.19x faster                                                    |
| bench_thread_pool        | 958 us                                                      | 809 us: 1.18x faster                                                     |
| tomli_loads              | 1.67 sec                                                    | 1.41 sec: 1.18x faster                                                   |
| 2to3                     | 246 ms                                                      | 210 ms: 1.17x faster                                                     |
| regex_dna                | 136 ms                                                      | 116 ms: 1.17x faster                                                     |
| docutils                 | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                   |
| sqlglot_normalize        | 205 ms                                                      | 177 ms: 1.16x faster                                                     |
| sqlite_synth             | 1.91 us                                                     | 1.65 us: 1.16x faster                                                    |
| deepcopy                 | 255 us                                                      | 221 us: 1.16x faster                                                     |
| sympy_expand             | 314 ms                                                      | 272 ms: 1.16x faster                                                     |
| aiohttp                  | 995 us                                                      | 875 us: 1.14x faster                                                     |
| nqueens                  | 66.6 ms                                                     | 59.7 ms: 1.12x faster                                                    |
| unpickle                 | 9.09 us                                                     | 8.25 us: 1.10x faster                                                    |
| deepcopy_reduce          | 2.20 us                                                     | 2.01 us: 1.10x faster                                                    |
| regex_effbot             | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                    |
| logging_format           | 6.76 us                                                     | 6.38 us: 1.06x faster                                                    |
| python_startup           | 20.6 ms                                                     | 19.7 ms: 1.05x faster                                                    |
| meteor_contest           | 75.9 ms                                                     | 72.7 ms: 1.05x faster                                                    |
| logging_simple           | 6.22 us                                                     | 5.96 us: 1.04x faster                                                    |
| xml_etree_parse          | 96.8 ms                                                     | 92.8 ms: 1.04x faster                                                    |
| xml_etree_generate       | 55.5 ms                                                     | 54.5 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.68 ms: 1.01x faster                                                    |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                     |
| xml_etree_iterparse      | 65.0 ms                                                     | 64.1 ms: 1.01x faster                                                    |
| json_loads               | 14.0 us                                                     | 13.9 us: 1.01x faster                                                    |
| nbody                    | 71.3 ms                                                     | 70.8 ms: 1.01x faster                                                    |
| fannkuch                 | 256 ms                                                      | 257 ms: 1.01x slower                                                     |
| scimark_fft              | 187 ms                                                      | 190 ms: 1.01x slower                                                     |
| bench_mp_pool            | 62.0 ms                                                     | 63.8 ms: 1.03x slower                                                    |
| python_startup_no_site   | 15.5 ms                                                     | 16.0 ms: 1.03x slower                                                    |
| async_generators         | 222 ms                                                      | 229 ms: 1.03x slower                                                     |
| pickle                   | 6.85 us                                                     | 7.13 us: 1.04x slower                                                    |
| unpickle_list            | 2.71 us                                                     | 2.83 us: 1.04x slower                                                    |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                    |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                    |
| create_gc_cycles         | 800 us                                                      | 899 us: 1.12x slower                                                     |
| pickle_list              | 2.75 us                                                     | 3.16 us: 1.15x slower                                                    |
| regex_v8                 | 15.4 ms                                                     | 18.3 ms: 1.18x slower                                                    |
| coverage                 | 39.0 ms                                                     | 46.4 ms: 1.19x slower                                                    |
| telco                    | 3.94 ms                                                     | 5.09 ms: 1.29x slower                                                    |
| thrift                   | 617 us                                                      | 7.91 ms: 12.82x slower                                                   |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                             |

Benchmark hidden because not significant (2): json, pathlib
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240416-3.13.0a6+-ced0ca9/bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown