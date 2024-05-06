# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 280cb86
- commit date: 2024-04-25
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                                       |
| chameleon      | 7.11 ms                                                                | 6.94 ms: 1.02x faster                                                      |
| docutils       | 2.91 sec                                                               | 2.92 sec: 1.00x slower                                                     |
| html5lib       | 68.8 ms                                                                | 68.2 ms: 1.01x faster                                                      |
| tornado_http   | 95.9 ms                                                                | 95.3 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 90.4 ms                                                                | 75.3 ms: 1.20x faster                                                      |
| float          | 77.2 ms                                                                | 72.6 ms: 1.06x faster                                                      |
| pidigits       | 189 ms                                                                 | 193 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                                 | 140 ms: 1.01x faster                                                       |
| regex_v8       | 25.2 ms                                                                | 25.5 ms: 1.01x slower                                                      |
| regex_effbot   | 3.67 ms                                                                | 3.76 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.03 sec                                                               | 1.90 sec: 1.07x faster                                                     |
| unpickle_pure_python | 237 us                                                                 | 223 us: 1.06x faster                                                       |
| unpickle             | 15.5 us                                                                | 15.1 us: 1.03x faster                                                      |
| xml_etree_parse      | 152 ms                                                                 | 148 ms: 1.02x faster                                                       |
| xml_etree_iterparse  | 104 ms                                                                 | 102 ms: 1.02x faster                                                       |
| pickle               | 11.6 us                                                                | 11.5 us: 1.01x faster                                                      |
| xml_etree_generate   | 87.3 ms                                                                | 86.7 ms: 1.01x faster                                                      |
| pickle_pure_python   | 308 us                                                                 | 306 us: 1.01x faster                                                       |
| json_loads           | 27.3 us                                                                | 27.6 us: 1.01x slower                                                      |
| pickle_dict          | 34.0 us                                                                | 34.6 us: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (4): xml_etree_process, unpickle_list, pickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| python_startup_no_site | 7.57 ms                                                                | 7.71 ms: 1.02x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.0 ms: 1.08x faster                                                      |
| django_template | 36.4 ms                                                                | 35.9 ms: 1.01x faster                                                      |
| genshi_xml      | 53.7 ms                                                                | 54.2 ms: 1.01x slower                                                      |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6+-2e7771a | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody                    | 90.4 ms                                                                | 75.3 ms: 1.20x faster                                                      |
| spectral_norm            | 114 ms                                                                 | 99.7 ms: 1.14x faster                                                      |
| scimark_sparse_mat_mult  | 4.96 ms                                                                | 4.38 ms: 1.13x faster                                                      |
| scimark_monte_carlo      | 70.0 ms                                                                | 61.9 ms: 1.13x faster                                                      |
| fannkuch                 | 386 ms                                                                 | 345 ms: 1.12x faster                                                       |
| scimark_fft              | 344 ms                                                                 | 308 ms: 1.12x faster                                                       |
| crypto_pyaes             | 73.3 ms                                                                | 67.7 ms: 1.08x faster                                                      |
| mako                     | 10.8 ms                                                                | 10.0 ms: 1.08x faster                                                      |
| hexiom                   | 6.88 ms                                                                | 6.40 ms: 1.07x faster                                                      |
| pyflate                  | 463 ms                                                                 | 432 ms: 1.07x faster                                                       |
| tomli_loads              | 2.03 sec                                                               | 1.90 sec: 1.07x faster                                                     |
| chaos                    | 63.4 ms                                                                | 59.3 ms: 1.07x faster                                                      |
| float                    | 77.2 ms                                                                | 72.6 ms: 1.06x faster                                                      |
| unpickle_pure_python     | 237 us                                                                 | 223 us: 1.06x faster                                                       |
| go                       | 155 ms                                                                 | 147 ms: 1.06x faster                                                       |
| logging_silent           | 108 ns                                                                 | 102 ns: 1.06x faster                                                       |
| pprint_safe_repr         | 763 ms                                                                 | 724 ms: 1.05x faster                                                       |
| scimark_lu               | 132 ms                                                                 | 125 ms: 1.05x faster                                                       |
| scimark_sor              | 134 ms                                                                 | 128 ms: 1.05x faster                                                       |
| pprint_pformat           | 1.55 sec                                                               | 1.48 sec: 1.04x faster                                                     |
| nqueens                  | 89.8 ms                                                                | 86.0 ms: 1.04x faster                                                      |
| richards                 | 43.7 ms                                                                | 41.9 ms: 1.04x faster                                                      |
| comprehensions           | 17.7 us                                                                | 17.1 us: 1.03x faster                                                      |
| deltablue                | 3.73 ms                                                                | 3.63 ms: 1.03x faster                                                      |
| richards_super           | 49.4 ms                                                                | 48.0 ms: 1.03x faster                                                      |
| unpickle                 | 15.5 us                                                                | 15.1 us: 1.03x faster                                                      |
| chameleon                | 7.11 ms                                                                | 6.94 ms: 1.02x faster                                                      |
| pycparser                | 1.19 sec                                                               | 1.16 sec: 1.02x faster                                                     |
| xml_etree_parse          | 152 ms                                                                 | 148 ms: 1.02x faster                                                       |
| telco                    | 8.73 ms                                                                | 8.57 ms: 1.02x faster                                                      |
| xml_etree_iterparse      | 104 ms                                                                 | 102 ms: 1.02x faster                                                       |
| sqlite_synth             | 2.86 us                                                                | 2.82 us: 1.02x faster                                                      |
| sympy_sum                | 168 ms                                                                 | 166 ms: 1.01x faster                                                       |
| sqlglot_transpile        | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                                      |
| django_template          | 36.4 ms                                                                | 35.9 ms: 1.01x faster                                                      |
| generators               | 30.3 ms                                                                | 29.9 ms: 1.01x faster                                                      |
| meteor_contest           | 111 ms                                                                 | 109 ms: 1.01x faster                                                       |
| sympy_str                | 295 ms                                                                 | 291 ms: 1.01x faster                                                       |
| sqlglot_parse            | 1.32 ms                                                                | 1.31 ms: 1.01x faster                                                      |
| typing_runtime_protocols | 117 us                                                                 | 116 us: 1.01x faster                                                       |
| sympy_integrate          | 22.0 ms                                                                | 21.8 ms: 1.01x faster                                                      |
| regex_compile            | 141 ms                                                                 | 140 ms: 1.01x faster                                                       |
| html5lib                 | 68.8 ms                                                                | 68.2 ms: 1.01x faster                                                      |
| sqlglot_optimize         | 57.2 ms                                                                | 56.7 ms: 1.01x faster                                                      |
| 2to3                     | 277 ms                                                                 | 275 ms: 1.01x faster                                                       |
| raytrace                 | 273 ms                                                                 | 271 ms: 1.01x faster                                                       |
| pickle                   | 11.6 us                                                                | 11.5 us: 1.01x faster                                                      |
| xml_etree_generate       | 87.3 ms                                                                | 86.7 ms: 1.01x faster                                                      |
| thrift                   | 823 us                                                                 | 817 us: 1.01x faster                                                       |
| tornado_http             | 95.9 ms                                                                | 95.3 ms: 1.01x faster                                                      |
| dulwich_log              | 69.3 ms                                                                | 68.8 ms: 1.01x faster                                                      |
| pickle_pure_python       | 308 us                                                                 | 306 us: 1.01x faster                                                       |
| deepcopy_reduce          | 3.22 us                                                                | 3.21 us: 1.01x faster                                                      |
| create_gc_cycles         | 1.77 ms                                                                | 1.76 ms: 1.00x faster                                                      |
| mdp                      | 2.68 sec                                                               | 2.69 sec: 1.00x slower                                                     |
| docutils                 | 2.91 sec                                                               | 2.92 sec: 1.00x slower                                                     |
| deepcopy                 | 361 us                                                                 | 363 us: 1.01x slower                                                       |
| coverage                 | 96.7 ms                                                                | 97.2 ms: 1.01x slower                                                      |
| async_generators         | 462 ms                                                                 | 466 ms: 1.01x slower                                                       |
| genshi_xml               | 53.7 ms                                                                | 54.2 ms: 1.01x slower                                                      |
| regex_v8                 | 25.2 ms                                                                | 25.5 ms: 1.01x slower                                                      |
| json_loads               | 27.3 us                                                                | 27.6 us: 1.01x slower                                                      |
| coroutines               | 22.6 ms                                                                | 22.8 ms: 1.01x slower                                                      |
| gc_traversal             | 4.01 ms                                                                | 4.06 ms: 1.01x slower                                                      |
| asyncio_tcp              | 509 ms                                                                 | 516 ms: 1.01x slower                                                       |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                      |
| pickle_dict              | 34.0 us                                                                | 34.6 us: 1.02x slower                                                      |
| python_startup_no_site   | 7.57 ms                                                                | 7.71 ms: 1.02x slower                                                      |
| pidigits                 | 189 ms                                                                 | 193 ms: 1.02x slower                                                       |
| regex_effbot             | 3.67 ms                                                                | 3.76 ms: 1.02x slower                                                      |
| pathlib                  | 17.6 ms                                                                | 18.1 ms: 1.03x slower                                                      |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (30): async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, dask, async_tree_cpu_io_mixed, pylint, mypy2, xml_etree_process, genshi_text, gunicorn, async_tree_io, unpickle_list, asyncio_websockets, async_tree_memoization, pickle_list, sqlglot_normalize, regex_dna, sympy_expand, bench_thread_pool, asyncio_tcp_ssl, deepcopy_memo, logging_simple, aiohttp, bench_mp_pool, json_dumps, djangocms, logging_format, json

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x