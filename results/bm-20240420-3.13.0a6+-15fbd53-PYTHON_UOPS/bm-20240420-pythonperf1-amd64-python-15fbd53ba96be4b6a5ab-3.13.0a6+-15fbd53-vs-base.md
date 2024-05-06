# Results vs. base

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 211 ms                                                                                                                 | 224 ms: 1.06x slower                                                                                                               |
| chameleon      | 4.91 ms                                                                                                                | 5.02 ms: 1.02x slower                                                                                                              |
| docutils       | 1.64 sec                                                                                                               | 1.74 sec: 1.06x slower                                                                                                             |
| html5lib       | 36.3 ms                                                                                                                | 40.5 ms: 1.12x slower                                                                                                              |
| tornado_http   | 81.8 ms                                                                                                                | 84.1 ms: 1.03x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.06x slower                                                                                                                       |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_io, async_tree_none, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| float          | 53.0 ms                                                                                                                | 57.9 ms: 1.09x slower                                                                                                              |
| nbody          | 72.4 ms                                                                                                                | 83.1 ms: 1.15x slower                                                                                                              |
| Geometric mean | (ref)                                                                                                                  | 1.08x slower                                                                                                                       |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 125 ms                                                                                                                 | 121 ms: 1.03x faster                                                                                                               |
| regex_v8       | 15.4 ms                                                                                                                | 15.2 ms: 1.01x faster                                                                                                              |
| regex_effbot   | 1.60 ms                                                                                                                | 1.59 ms: 1.01x faster                                                                                                              |
| regex_compile  | 79.7 ms                                                                                                                | 103 ms: 1.29x slower                                                                                                               |
| Geometric mean | (ref)                                                                                                                  | 1.05x slower                                                                                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|----------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 3.22 us                                                                                                                | 3.06 us: 1.05x faster                                                                                                              |
| xml_etree_parse      | 92.9 ms                                                                                                                | 90.0 ms: 1.03x faster                                                                                                              |
| json_dumps           | 5.76 ms                                                                                                                | 5.70 ms: 1.01x faster                                                                                                              |
| xml_etree_generate   | 56.2 ms                                                                                                                | 56.5 ms: 1.00x slower                                                                                                              |
| pickle_pure_python   | 183 us                                                                                                                 | 185 us: 1.01x slower                                                                                                               |
| pickle_dict          | 18.4 us                                                                                                                | 18.6 us: 1.01x slower                                                                                                              |
| json_loads           | 13.7 us                                                                                                                | 13.8 us: 1.01x slower                                                                                                              |
| xml_etree_process    | 38.2 ms                                                                                                                | 38.7 ms: 1.01x slower                                                                                                              |
| xml_etree_iterparse  | 65.0 ms                                                                                                                | 66.5 ms: 1.02x slower                                                                                                              |
| tomli_loads          | 1.42 sec                                                                                                               | 1.46 sec: 1.03x slower                                                                                                             |
| pickle               | 7.20 us                                                                                                                | 7.53 us: 1.04x slower                                                                                                              |
| unpickle_list        | 2.72 us                                                                                                                | 2.86 us: 1.05x slower                                                                                                              |
| unpickle_pure_python | 135 us                                                                                                                 | 166 us: 1.22x slower                                                                                                               |
| Geometric mean       | (ref)                                                                                                                  | 1.02x slower                                                                                                                       |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|------------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 16.9 ms                                                                                                                | 16.3 ms: 1.04x faster                                                                                                              |
| python_startup         | 20.4 ms                                                                                                                | 19.9 ms: 1.03x faster                                                                                                              |
| Geometric mean         | (ref)                                                                                                                  | 1.03x faster                                                                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|-----------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 35.0 ms                                                                                                                | 35.8 ms: 1.02x slower                                                                                                              |
| django_template | 22.4 ms                                                                                                                | 23.3 ms: 1.04x slower                                                                                                              |
| mako            | 6.46 ms                                                                                                                | 7.41 ms: 1.15x slower                                                                                                              |
| Geometric mean  | (ref)                                                                                                                  | 1.05x slower                                                                                                                       |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json | results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json |
|--------------------------|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp_ssl          | 1.72 sec                                                                                                               | 1.49 sec: 1.15x faster                                                                                                             |
| pickle_list              | 3.22 us                                                                                                                | 3.06 us: 1.05x faster                                                                                                              |
| coroutines               | 13.6 ms                                                                                                                | 13.0 ms: 1.04x faster                                                                                                              |
| python_startup_no_site   | 16.9 ms                                                                                                                | 16.3 ms: 1.04x faster                                                                                                              |
| xml_etree_parse          | 92.9 ms                                                                                                                | 90.0 ms: 1.03x faster                                                                                                              |
| richards                 | 29.5 ms                                                                                                                | 28.6 ms: 1.03x faster                                                                                                              |
| regex_dna                | 125 ms                                                                                                                 | 121 ms: 1.03x faster                                                                                                               |
| python_startup           | 20.4 ms                                                                                                                | 19.9 ms: 1.03x faster                                                                                                              |
| richards_super           | 33.2 ms                                                                                                                | 32.4 ms: 1.02x faster                                                                                                              |
| regex_v8                 | 15.4 ms                                                                                                                | 15.2 ms: 1.01x faster                                                                                                              |
| json_dumps               | 5.76 ms                                                                                                                | 5.70 ms: 1.01x faster                                                                                                              |
| regex_effbot             | 1.60 ms                                                                                                                | 1.59 ms: 1.01x faster                                                                                                              |
| logging_silent           | 57.4 ns                                                                                                                | 57.1 ns: 1.01x faster                                                                                                              |
| logging_format           | 6.47 us                                                                                                                | 6.45 us: 1.00x faster                                                                                                              |
| sqlite_synth             | 1.61 us                                                                                                                | 1.62 us: 1.00x slower                                                                                                              |
| logging_simple           | 6.03 us                                                                                                                | 6.06 us: 1.00x slower                                                                                                              |
| xml_etree_generate       | 56.2 ms                                                                                                                | 56.5 ms: 1.00x slower                                                                                                              |
| pickle_pure_python       | 183 us                                                                                                                 | 185 us: 1.01x slower                                                                                                               |
| pickle_dict              | 18.4 us                                                                                                                | 18.6 us: 1.01x slower                                                                                                              |
| json_loads               | 13.7 us                                                                                                                | 13.8 us: 1.01x slower                                                                                                              |
| typing_runtime_protocols | 74.9 us                                                                                                                | 75.7 us: 1.01x slower                                                                                                              |
| xml_etree_process        | 38.2 ms                                                                                                                | 38.7 ms: 1.01x slower                                                                                                              |
| pathlib                  | 75.4 ms                                                                                                                | 76.5 ms: 1.01x slower                                                                                                              |
| deepcopy                 | 226 us                                                                                                                 | 229 us: 1.01x slower                                                                                                               |
| bench_mp_pool            | 64.3 ms                                                                                                                | 65.2 ms: 1.01x slower                                                                                                              |
| aiohttp                  | 889 us                                                                                                                 | 907 us: 1.02x slower                                                                                                               |
| genshi_xml               | 35.0 ms                                                                                                                | 35.8 ms: 1.02x slower                                                                                                              |
| chameleon                | 4.91 ms                                                                                                                | 5.02 ms: 1.02x slower                                                                                                              |
| xml_etree_iterparse      | 65.0 ms                                                                                                                | 66.5 ms: 1.02x slower                                                                                                              |
| raytrace                 | 172 ms                                                                                                                 | 176 ms: 1.02x slower                                                                                                               |
| bench_thread_pool        | 815 us                                                                                                                 | 835 us: 1.02x slower                                                                                                               |
| meteor_contest           | 74.3 ms                                                                                                                | 76.4 ms: 1.03x slower                                                                                                              |
| tornado_http             | 81.8 ms                                                                                                                | 84.1 ms: 1.03x slower                                                                                                              |
| tomli_loads              | 1.42 sec                                                                                                               | 1.46 sec: 1.03x slower                                                                                                             |
| django_template          | 22.4 ms                                                                                                                | 23.3 ms: 1.04x slower                                                                                                              |
| pickle                   | 7.20 us                                                                                                                | 7.53 us: 1.04x slower                                                                                                              |
| unpickle_list            | 2.72 us                                                                                                                | 2.86 us: 1.05x slower                                                                                                              |
| sqlglot_normalize        | 178 ms                                                                                                                 | 187 ms: 1.05x slower                                                                                                               |
| async_generators         | 231 ms                                                                                                                 | 243 ms: 1.05x slower                                                                                                               |
| sqlglot_transpile        | 988 us                                                                                                                 | 1.04 ms: 1.06x slower                                                                                                              |
| sqlglot_parse            | 781 us                                                                                                                 | 827 us: 1.06x slower                                                                                                               |
| 2to3                     | 211 ms                                                                                                                 | 224 ms: 1.06x slower                                                                                                               |
| docutils                 | 1.64 sec                                                                                                               | 1.74 sec: 1.06x slower                                                                                                             |
| deepcopy_memo            | 23.1 us                                                                                                                | 24.8 us: 1.07x slower                                                                                                              |
| coverage                 | 45.8 ms                                                                                                                | 49.1 ms: 1.07x slower                                                                                                              |
| sqlglot_optimize         | 33.6 ms                                                                                                                | 36.6 ms: 1.09x slower                                                                                                              |
| dulwich_log              | 39.7 ms                                                                                                                | 43.4 ms: 1.09x slower                                                                                                              |
| float                    | 53.0 ms                                                                                                                | 57.9 ms: 1.09x slower                                                                                                              |
| mdp                      | 1.36 sec                                                                                                               | 1.49 sec: 1.10x slower                                                                                                             |
| pprint_safe_repr         | 494 ms                                                                                                                 | 542 ms: 1.10x slower                                                                                                               |
| json                     | 2.87 ms                                                                                                                | 3.15 ms: 1.10x slower                                                                                                              |
| sympy_integrate          | 12.6 ms                                                                                                                | 13.8 ms: 1.10x slower                                                                                                              |
| pprint_pformat           | 1.01 sec                                                                                                               | 1.11 sec: 1.10x slower                                                                                                             |
| fannkuch                 | 259 ms                                                                                                                 | 285 ms: 1.10x slower                                                                                                               |
| mypy2                    | 415 ms                                                                                                                 | 457 ms: 1.10x slower                                                                                                               |
| crypto_pyaes             | 45.7 ms                                                                                                                | 50.5 ms: 1.11x slower                                                                                                              |
| sympy_expand             | 275 ms                                                                                                                 | 304 ms: 1.11x slower                                                                                                               |
| go                       | 91.4 ms                                                                                                                | 102 ms: 1.11x slower                                                                                                               |
| sympy_sum                | 85.0 ms                                                                                                                | 94.7 ms: 1.11x slower                                                                                                              |
| html5lib                 | 36.3 ms                                                                                                                | 40.5 ms: 1.12x slower                                                                                                              |
| sympy_str                | 162 ms                                                                                                                 | 181 ms: 1.12x slower                                                                                                               |
| chaos                    | 39.8 ms                                                                                                                | 44.6 ms: 1.12x slower                                                                                                              |
| scimark_fft              | 185 ms                                                                                                                 | 208 ms: 1.12x slower                                                                                                               |
| thrift                   | 8.13 ms                                                                                                                | 9.18 ms: 1.13x slower                                                                                                              |
| mako                     | 6.46 ms                                                                                                                | 7.41 ms: 1.15x slower                                                                                                              |
| nbody                    | 72.4 ms                                                                                                                | 83.1 ms: 1.15x slower                                                                                                              |
| pyflate                  | 293 ms                                                                                                                 | 336 ms: 1.15x slower                                                                                                               |
| scimark_sor              | 79.1 ms                                                                                                                | 91.1 ms: 1.15x slower                                                                                                              |
| nqueens                  | 59.2 ms                                                                                                                | 68.6 ms: 1.16x slower                                                                                                              |
| deltablue                | 2.10 ms                                                                                                                | 2.49 ms: 1.18x slower                                                                                                              |
| scimark_sparse_mat_mult  | 2.70 ms                                                                                                                | 3.30 ms: 1.22x slower                                                                                                              |
| scimark_monte_carlo      | 42.1 ms                                                                                                                | 51.6 ms: 1.22x slower                                                                                                              |
| unpickle_pure_python     | 135 us                                                                                                                 | 166 us: 1.22x slower                                                                                                               |
| comprehensions           | 11.1 us                                                                                                                | 13.8 us: 1.24x slower                                                                                                              |
| spectral_norm            | 64.2 ms                                                                                                                | 81.7 ms: 1.27x slower                                                                                                              |
| regex_compile            | 79.7 ms                                                                                                                | 103 ms: 1.29x slower                                                                                                               |
| hexiom                   | 3.99 ms                                                                                                                | 5.24 ms: 1.31x slower                                                                                                              |
| scimark_lu               | 56.9 ms                                                                                                                | 78.3 ms: 1.38x slower                                                                                                              |
| Geometric mean           | (ref)                                                                                                                  | 1.06x slower                                                                                                                       |

Benchmark hidden because not significant (19): pycparser, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, genshi_text, async_tree_io_tg, create_gc_cycles, pidigits, generators, telco, unpickle, deepcopy_reduce, async_tree_memoization, async_tree_io, gc_traversal, async_tree_none, asyncio_tcp, async_tree_memoization_tg, async_tree_none_tg, pylint

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown