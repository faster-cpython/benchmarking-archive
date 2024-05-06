# Results vs. 3.10.4

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: e83be54
- commit date: 2024-04-15
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 211 ms: 1.16x faster                                                     |
| chameleon      | 5.79 ms                                                     | 4.83 ms: 1.20x faster                                                    |
| docutils       | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                   |
| html5lib       | 51.0 ms                                                     | 37.4 ms: 1.37x faster                                                    |
| tornado_http   | 108 ms                                                      | 82.1 ms: 1.32x faster                                                    |
| Geometric mean | (ref)                                                       | 1.24x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 273 ms: 1.93x faster                                                     |
| async_tree_none         | 435 ms                                                      | 227 ms: 1.92x faster                                                     |
| async_tree_io           | 1.11 sec                                                    | 602 ms: 1.84x faster                                                     |
| async_tree_cpu_io_mixed | 638 ms                                                      | 397 ms: 1.60x faster                                                     |
| Geometric mean          | (ref)                                                       | 1.82x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 50.9 ms: 1.21x faster                                                    |
| nbody          | 71.3 ms                                                     | 68.5 ms: 1.04x faster                                                    |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                       | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 78.9 ms: 1.34x faster                                                    |
| regex_dna      | 136 ms                                                      | 117 ms: 1.17x faster                                                     |
| regex_effbot   | 1.66 ms                                                     | 1.56 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                       | 1.14x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.65 ms: 1.62x faster                                                    |
| pickle_pure_python   | 270 us                                                      | 180 us: 1.50x faster                                                     |
| unpickle_pure_python | 183 us                                                      | 128 us: 1.43x faster                                                     |
| xml_etree_process    | 44.5 ms                                                     | 37.6 ms: 1.18x faster                                                    |
| tomli_loads          | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                   |
| unpickle             | 9.09 us                                                     | 8.40 us: 1.08x faster                                                    |
| xml_etree_parse      | 96.8 ms                                                     | 92.8 ms: 1.04x faster                                                    |
| json_loads           | 14.0 us                                                     | 13.5 us: 1.04x faster                                                    |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.6 ms: 1.02x faster                                                    |
| xml_etree_generate   | 55.5 ms                                                     | 54.8 ms: 1.01x faster                                                    |
| unpickle_list        | 2.71 us                                                     | 2.83 us: 1.04x slower                                                    |
| pickle_dict          | 17.2 us                                                     | 18.4 us: 1.07x slower                                                    |
| pickle               | 6.85 us                                                     | 7.37 us: 1.08x slower                                                    |
| pickle_list          | 2.75 us                                                     | 3.08 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.8 ms: 1.04x faster                                                    |
| python_startup_no_site | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.34 ms: 1.43x faster                                                    |
| django_template | 28.9 ms                                                     | 23.6 ms: 1.22x faster                                                    |
| genshi_xml      | 41.0 ms                                                     | 34.4 ms: 1.19x faster                                                    |
| genshi_text     | 19.8 ms                                                     | 16.8 ms: 1.18x faster                                                    |
| Geometric mean  | (ref)                                                       | 1.25x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|--------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 75.5 us: 4.45x faster                                                    |
| deltablue                | 4.19 ms                                                     | 2.06 ms: 2.03x faster                                                    |
| async_tree_memoization   | 526 ms                                                      | 273 ms: 1.93x faster                                                     |
| async_tree_none          | 435 ms                                                      | 227 ms: 1.92x faster                                                     |
| async_tree_io            | 1.11 sec                                                    | 602 ms: 1.84x faster                                                     |
| pylint                   | 350 ms                                                      | 210 ms: 1.67x faster                                                     |
| logging_silent           | 94.6 ns                                                     | 56.8 ns: 1.67x faster                                                    |
| raytrace                 | 273 ms                                                      | 164 ms: 1.66x faster                                                     |
| json_dumps               | 9.16 ms                                                     | 5.65 ms: 1.62x faster                                                    |
| chaos                    | 61.7 ms                                                     | 38.1 ms: 1.62x faster                                                    |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 397 ms: 1.60x faster                                                     |
| scimark_lu               | 85.8 ms                                                     | 53.8 ms: 1.59x faster                                                    |
| sqlglot_parse            | 1.22 ms                                                     | 764 us: 1.59x faster                                                     |
| richards_super           | 52.2 ms                                                     | 33.3 ms: 1.57x faster                                                    |
| comprehensions           | 16.5 us                                                     | 10.6 us: 1.56x faster                                                    |
| generators               | 32.4 ms                                                     | 20.9 ms: 1.55x faster                                                    |
| asyncio_tcp              | 732 ms                                                      | 476 ms: 1.54x faster                                                     |
| go                       | 139 ms                                                      | 90.8 ms: 1.53x faster                                                    |
| hexiom                   | 5.74 ms                                                     | 3.79 ms: 1.51x faster                                                    |
| sqlglot_transpile        | 1.48 ms                                                     | 979 us: 1.51x faster                                                     |
| pickle_pure_python       | 270 us                                                      | 180 us: 1.50x faster                                                     |
| scimark_sor              | 106 ms                                                      | 72.0 ms: 1.47x faster                                                    |
| richards                 | 42.4 ms                                                     | 29.3 ms: 1.45x faster                                                    |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.9 ms: 1.43x faster                                                    |
| unpickle_pure_python     | 183 us                                                      | 128 us: 1.43x faster                                                     |
| pyflate                  | 409 ms                                                      | 286 ms: 1.43x faster                                                     |
| mako                     | 9.03 ms                                                     | 6.34 ms: 1.43x faster                                                    |
| crypto_pyaes             | 62.5 ms                                                     | 44.5 ms: 1.41x faster                                                    |
| html5lib                 | 51.0 ms                                                     | 37.4 ms: 1.37x faster                                                    |
| regex_compile            | 106 ms                                                      | 78.9 ms: 1.34x faster                                                    |
| deepcopy_memo            | 28.8 us                                                     | 21.7 us: 1.32x faster                                                    |
| tornado_http             | 108 ms                                                      | 82.1 ms: 1.32x faster                                                    |
| mypy2                    | 555 ms                                                      | 424 ms: 1.31x faster                                                     |
| mdp                      | 1.78 sec                                                    | 1.39 sec: 1.28x faster                                                   |
| spectral_norm            | 77.3 ms                                                     | 60.9 ms: 1.27x faster                                                    |
| sympy_sum                | 107 ms                                                      | 84.5 ms: 1.27x faster                                                    |
| dulwich_log              | 50.5 ms                                                     | 39.9 ms: 1.26x faster                                                    |
| pycparser                | 930 ms                                                      | 753 ms: 1.24x faster                                                     |
| django_template          | 28.9 ms                                                     | 23.6 ms: 1.22x faster                                                    |
| pprint_pformat           | 1.22 sec                                                    | 996 ms: 1.22x faster                                                     |
| sympy_integrate          | 15.3 ms                                                     | 12.5 ms: 1.22x faster                                                    |
| pprint_safe_repr         | 592 ms                                                      | 489 ms: 1.21x faster                                                     |
| float                    | 61.7 ms                                                     | 50.9 ms: 1.21x faster                                                    |
| sympy_str                | 194 ms                                                      | 161 ms: 1.20x faster                                                     |
| coroutines               | 16.0 ms                                                     | 13.3 ms: 1.20x faster                                                    |
| chameleon                | 5.79 ms                                                     | 4.83 ms: 1.20x faster                                                    |
| genshi_xml               | 41.0 ms                                                     | 34.4 ms: 1.19x faster                                                    |
| bench_thread_pool        | 958 us                                                      | 807 us: 1.19x faster                                                     |
| xml_etree_process        | 44.5 ms                                                     | 37.6 ms: 1.18x faster                                                    |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.79 sec: 1.18x faster                                                   |
| genshi_text              | 19.8 ms                                                     | 16.8 ms: 1.18x faster                                                    |
| tomli_loads              | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                   |
| regex_dna                | 136 ms                                                      | 117 ms: 1.17x faster                                                     |
| 2to3                     | 246 ms                                                      | 211 ms: 1.16x faster                                                     |
| docutils                 | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                   |
| sqlite_synth             | 1.91 us                                                     | 1.66 us: 1.15x faster                                                    |
| sqlglot_optimize         | 39.8 ms                                                     | 34.7 ms: 1.15x faster                                                    |
| sympy_expand             | 314 ms                                                      | 275 ms: 1.14x faster                                                     |
| deepcopy                 | 255 us                                                      | 226 us: 1.13x faster                                                     |
| nqueens                  | 66.6 ms                                                     | 58.9 ms: 1.13x faster                                                    |
| aiohttp                  | 995 us                                                      | 885 us: 1.12x faster                                                     |
| sqlglot_normalize        | 205 ms                                                      | 185 ms: 1.11x faster                                                     |
| deepcopy_reduce          | 2.20 us                                                     | 2.02 us: 1.09x faster                                                    |
| unpickle                 | 9.09 us                                                     | 8.40 us: 1.08x faster                                                    |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.55 ms: 1.07x faster                                                    |
| regex_effbot             | 1.66 ms                                                     | 1.56 ms: 1.06x faster                                                    |
| logging_format           | 6.76 us                                                     | 6.46 us: 1.05x faster                                                    |
| xml_etree_parse          | 96.8 ms                                                     | 92.8 ms: 1.04x faster                                                    |
| nbody                    | 71.3 ms                                                     | 68.5 ms: 1.04x faster                                                    |
| logging_simple           | 6.22 us                                                     | 5.98 us: 1.04x faster                                                    |
| json_loads               | 14.0 us                                                     | 13.5 us: 1.04x faster                                                    |
| python_startup           | 20.6 ms                                                     | 19.8 ms: 1.04x faster                                                    |
| fannkuch                 | 256 ms                                                      | 247 ms: 1.04x faster                                                     |
| scimark_fft              | 187 ms                                                      | 182 ms: 1.03x faster                                                     |
| meteor_contest           | 75.9 ms                                                     | 74.2 ms: 1.02x faster                                                    |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.6 ms: 1.02x faster                                                    |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                     |
| xml_etree_generate       | 55.5 ms                                                     | 54.8 ms: 1.01x faster                                                    |
| pathlib                  | 75.7 ms                                                     | 76.2 ms: 1.01x slower                                                    |
| bench_mp_pool            | 62.0 ms                                                     | 63.7 ms: 1.03x slower                                                    |
| unpickle_list            | 2.71 us                                                     | 2.83 us: 1.04x slower                                                    |
| python_startup_no_site   | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                                    |
| async_generators         | 222 ms                                                      | 235 ms: 1.06x slower                                                     |
| pickle_dict              | 17.2 us                                                     | 18.4 us: 1.07x slower                                                    |
| pickle                   | 6.85 us                                                     | 7.37 us: 1.08x slower                                                    |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                    |
| create_gc_cycles         | 800 us                                                      | 895 us: 1.12x slower                                                     |
| pickle_list              | 2.75 us                                                     | 3.08 us: 1.12x slower                                                    |
| coverage                 | 39.0 ms                                                     | 46.0 ms: 1.18x slower                                                    |
| telco                    | 3.94 ms                                                     | 5.10 ms: 1.29x slower                                                    |
| thrift                   | 617 us                                                      | 7.84 ms: 12.70x slower                                                   |
| Geometric mean           | (ref)                                                       | 1.21x faster                                                             |

Benchmark hidden because not significant (2): regex_v8, json
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240415-3.13.0a6+-e83be54/bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown