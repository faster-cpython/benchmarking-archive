# Results vs. base

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.01x faster
- HPT reliability: 96.36%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 210 ms                                                                                                                 | 218 ms: 1.04x slower                                                                                                       |
| chameleon      | 5.01 ms                                                                                                                | 4.67 ms: 1.07x faster                                                                                                      |
| docutils       | 1.64 sec                                                                                                               | 1.68 sec: 1.03x slower                                                                                                     |
| html5lib       | 36.2 ms                                                                                                                | 36.0 ms: 1.01x faster                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.00x faster                                                                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| async_tree_none  | 224 ms                                                                                                                 | 219 ms: 1.03x faster                                                                                                       |
| async_tree_io_tg | 620 ms                                                                                                                 | 607 ms: 1.02x faster                                                                                                       |
| Geometric mean   | (ref)                                                                                                                  | 1.02x faster                                                                                                               |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| nbody          | 70.2 ms                                                                                                                | 58.3 ms: 1.21x faster                                                                                                      |
| float          | 51.6 ms                                                                                                                | 46.7 ms: 1.11x faster                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.10x faster                                                                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 16.0 ms                                                                                                                | 15.0 ms: 1.07x faster                                                                                                      |
| regex_dna      | 122 ms                                                                                                                 | 120 ms: 1.01x faster                                                                                                       |
| regex_compile  | 79.8 ms                                                                                                                | 86.8 ms: 1.09x slower                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.00x slower                                                                                                               |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 1.41 sec                                                                                                               | 1.18 sec: 1.19x faster                                                                                                     |
| pickle_pure_python   | 179 us                                                                                                                 | 171 us: 1.05x faster                                                                                                       |
| xml_etree_iterparse  | 64.0 ms                                                                                                                | 60.9 ms: 1.05x faster                                                                                                      |
| unpickle_pure_python | 129 us                                                                                                                 | 123 us: 1.05x faster                                                                                                       |
| xml_etree_generate   | 55.3 ms                                                                                                                | 53.0 ms: 1.04x faster                                                                                                      |
| unpickle_list        | 2.80 us                                                                                                                | 2.74 us: 1.02x faster                                                                                                      |
| json_dumps           | 5.64 ms                                                                                                                | 5.52 ms: 1.02x faster                                                                                                      |
| xml_etree_process    | 37.7 ms                                                                                                                | 37.0 ms: 1.02x faster                                                                                                      |
| xml_etree_parse      | 91.2 ms                                                                                                                | 90.0 ms: 1.01x faster                                                                                                      |
| pickle               | 7.14 us                                                                                                                | 7.23 us: 1.01x slower                                                                                                      |
| unpickle             | 8.36 us                                                                                                                | 8.80 us: 1.05x slower                                                                                                      |
| Geometric mean       | (ref)                                                                                                                  | 1.03x faster                                                                                                               |

Benchmark hidden because not significant (3): pickle_list, pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|------------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 17.0 ms                                                                                                                | 17.8 ms: 1.05x slower                                                                                                      |
| python_startup         | 20.3 ms                                                                                                                | 21.4 ms: 1.06x slower                                                                                                      |
| Geometric mean         | (ref)                                                                                                                  | 1.05x slower                                                                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|----------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| mako           | 6.38 ms                                                                                                                | 5.72 ms: 1.12x faster                                                                                                      |
| genshi_text    | 16.5 ms                                                                                                                | 15.5 ms: 1.07x faster                                                                                                      |
| Geometric mean | (ref)                                                                                                                  | 1.07x faster                                                                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json | results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json |
|--------------------------|:----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------:|
| spectral_norm            | 63.3 ms                                                                                                                | 51.3 ms: 1.23x faster                                                                                                      |
| nbody                    | 70.2 ms                                                                                                                | 58.3 ms: 1.21x faster                                                                                                      |
| tomli_loads              | 1.41 sec                                                                                                               | 1.18 sec: 1.19x faster                                                                                                     |
| scimark_sparse_mat_mult  | 2.66 ms                                                                                                                | 2.27 ms: 1.17x faster                                                                                                      |
| fannkuch                 | 257 ms                                                                                                                 | 226 ms: 1.14x faster                                                                                                       |
| scimark_fft              | 185 ms                                                                                                                 | 165 ms: 1.12x faster                                                                                                       |
| mako                     | 6.38 ms                                                                                                                | 5.72 ms: 1.12x faster                                                                                                      |
| float                    | 51.6 ms                                                                                                                | 46.7 ms: 1.11x faster                                                                                                      |
| generators               | 21.7 ms                                                                                                                | 19.8 ms: 1.10x faster                                                                                                      |
| pyflate                  | 289 ms                                                                                                                 | 269 ms: 1.07x faster                                                                                                       |
| chameleon                | 5.01 ms                                                                                                                | 4.67 ms: 1.07x faster                                                                                                      |
| regex_v8                 | 16.0 ms                                                                                                                | 15.0 ms: 1.07x faster                                                                                                      |
| genshi_text              | 16.5 ms                                                                                                                | 15.5 ms: 1.07x faster                                                                                                      |
| pprint_pformat           | 1.00 sec                                                                                                               | 943 ms: 1.06x faster                                                                                                       |
| deepcopy_memo            | 22.3 us                                                                                                                | 21.0 us: 1.06x faster                                                                                                      |
| richards_super           | 32.3 ms                                                                                                                | 30.6 ms: 1.06x faster                                                                                                      |
| scimark_monte_carlo      | 40.6 ms                                                                                                                | 38.5 ms: 1.05x faster                                                                                                      |
| pickle_pure_python       | 179 us                                                                                                                 | 171 us: 1.05x faster                                                                                                       |
| xml_etree_iterparse      | 64.0 ms                                                                                                                | 60.9 ms: 1.05x faster                                                                                                      |
| richards                 | 28.3 ms                                                                                                                | 27.0 ms: 1.05x faster                                                                                                      |
| telco                    | 5.05 ms                                                                                                                | 4.83 ms: 1.05x faster                                                                                                      |
| unpickle_pure_python     | 129 us                                                                                                                 | 123 us: 1.05x faster                                                                                                       |
| pprint_safe_repr         | 491 ms                                                                                                                 | 470 ms: 1.04x faster                                                                                                       |
| xml_etree_generate       | 55.3 ms                                                                                                                | 53.0 ms: 1.04x faster                                                                                                      |
| deepcopy_reduce          | 2.02 us                                                                                                                | 1.94 us: 1.04x faster                                                                                                      |
| typing_runtime_protocols | 73.8 us                                                                                                                | 71.1 us: 1.04x faster                                                                                                      |
| sqlite_synth             | 1.64 us                                                                                                                | 1.58 us: 1.04x faster                                                                                                      |
| logging_simple           | 5.98 us                                                                                                                | 5.77 us: 1.04x faster                                                                                                      |
| crypto_pyaes             | 45.7 ms                                                                                                                | 44.3 ms: 1.03x faster                                                                                                      |
| logging_silent           | 56.8 ns                                                                                                                | 54.9 ns: 1.03x faster                                                                                                      |
| async_tree_none          | 224 ms                                                                                                                 | 219 ms: 1.03x faster                                                                                                       |
| bench_thread_pool        | 811 us                                                                                                                 | 791 us: 1.03x faster                                                                                                       |
| logging_format           | 6.42 us                                                                                                                | 6.26 us: 1.02x faster                                                                                                      |
| unpickle_list            | 2.80 us                                                                                                                | 2.74 us: 1.02x faster                                                                                                      |
| async_tree_io_tg         | 620 ms                                                                                                                 | 607 ms: 1.02x faster                                                                                                       |
| json_dumps               | 5.64 ms                                                                                                                | 5.52 ms: 1.02x faster                                                                                                      |
| xml_etree_process        | 37.7 ms                                                                                                                | 37.0 ms: 1.02x faster                                                                                                      |
| deepcopy                 | 222 us                                                                                                                 | 218 us: 1.02x faster                                                                                                       |
| meteor_contest           | 72.8 ms                                                                                                                | 71.7 ms: 1.02x faster                                                                                                      |
| xml_etree_parse          | 91.2 ms                                                                                                                | 90.0 ms: 1.01x faster                                                                                                      |
| coroutines               | 13.2 ms                                                                                                                | 13.0 ms: 1.01x faster                                                                                                      |
| create_gc_cycles         | 895 us                                                                                                                 | 884 us: 1.01x faster                                                                                                       |
| regex_dna                | 122 ms                                                                                                                 | 120 ms: 1.01x faster                                                                                                       |
| chaos                    | 39.2 ms                                                                                                                | 38.9 ms: 1.01x faster                                                                                                      |
| html5lib                 | 36.2 ms                                                                                                                | 36.0 ms: 1.01x faster                                                                                                      |
| pathlib                  | 75.2 ms                                                                                                                | 74.8 ms: 1.01x faster                                                                                                      |
| dulwich_log              | 40.3 ms                                                                                                                | 40.5 ms: 1.01x slower                                                                                                      |
| sqlglot_parse            | 776 us                                                                                                                 | 783 us: 1.01x slower                                                                                                       |
| coverage                 | 46.0 ms                                                                                                                | 46.4 ms: 1.01x slower                                                                                                      |
| pickle                   | 7.14 us                                                                                                                | 7.23 us: 1.01x slower                                                                                                      |
| sqlglot_transpile        | 982 us                                                                                                                 | 995 us: 1.01x slower                                                                                                       |
| aiohttp                  | 885 us                                                                                                                 | 898 us: 1.01x slower                                                                                                       |
| go                       | 90.0 ms                                                                                                                | 91.8 ms: 1.02x slower                                                                                                      |
| sqlglot_optimize         | 34.0 ms                                                                                                                | 34.7 ms: 1.02x slower                                                                                                      |
| async_generators         | 235 ms                                                                                                                 | 240 ms: 1.02x slower                                                                                                       |
| docutils                 | 1.64 sec                                                                                                               | 1.68 sec: 1.03x slower                                                                                                     |
| mdp                      | 1.49 sec                                                                                                               | 1.53 sec: 1.03x slower                                                                                                     |
| raytrace                 | 165 ms                                                                                                                 | 170 ms: 1.03x slower                                                                                                       |
| sympy_sum                | 85.4 ms                                                                                                                | 88.3 ms: 1.03x slower                                                                                                      |
| sympy_str                | 163 ms                                                                                                                 | 168 ms: 1.03x slower                                                                                                       |
| pylint                   | 188 ms                                                                                                                 | 194 ms: 1.04x slower                                                                                                       |
| 2to3                     | 210 ms                                                                                                                 | 218 ms: 1.04x slower                                                                                                       |
| sympy_expand             | 274 ms                                                                                                                 | 286 ms: 1.04x slower                                                                                                       |
| bench_mp_pool            | 64.2 ms                                                                                                                | 67.2 ms: 1.05x slower                                                                                                      |
| python_startup_no_site   | 17.0 ms                                                                                                                | 17.8 ms: 1.05x slower                                                                                                      |
| unpickle                 | 8.36 us                                                                                                                | 8.80 us: 1.05x slower                                                                                                      |
| python_startup           | 20.3 ms                                                                                                                | 21.4 ms: 1.06x slower                                                                                                      |
| sympy_integrate          | 12.6 ms                                                                                                                | 13.3 ms: 1.06x slower                                                                                                      |
| mypy2                    | 418 ms                                                                                                                 | 447 ms: 1.07x slower                                                                                                       |
| deltablue                | 2.04 ms                                                                                                                | 2.20 ms: 1.08x slower                                                                                                      |
| scimark_sor              | 76.6 ms                                                                                                                | 83.1 ms: 1.08x slower                                                                                                      |
| regex_compile            | 79.8 ms                                                                                                                | 86.8 ms: 1.09x slower                                                                                                      |
| thrift                   | 8.03 ms                                                                                                                | 8.76 ms: 1.09x slower                                                                                                      |
| hexiom                   | 3.87 ms                                                                                                                | 4.45 ms: 1.15x slower                                                                                                      |
| scimark_lu               | 57.0 ms                                                                                                                | 73.2 ms: 1.29x slower                                                                                                      |
| Geometric mean           | (ref)                                                                                                                  | 1.01x faster                                                                                                               |

Benchmark hidden because not significant (21): asyncio_tcp_ssl, pycparser, async_tree_none_tg, genshi_xml, async_tree_memoization, async_tree_io, async_tree_memoization_tg, pickle_list, asyncio_tcp, comprehensions, nqueens, async_tree_cpu_io_mixed, gc_traversal, sqlglot_normalize, pidigits, pickle_dict, async_tree_cpu_io_mixed_tg, regex_effbot, json_loads, tornado_http, json

# HPT report

- Reliability score: 96.36% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown