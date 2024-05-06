# Results vs. 3.10.4

- fork: python
- ref: 7e6fa5fceddc3f4721c0
- machine: linux-x86_64
- commit hash: 7e6fa5f
- commit date: 2024-04-19
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 301 ms: 1.16x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.58 ms: 1.28x faster                                                  |
| docutils       | 3.30 sec                                               | 3.08 sec: 1.07x faster                                                 |
| html5lib       | 88.9 ms                                                | 71.9 ms: 1.24x faster                                                  |
| tornado_http   | 136 ms                                                 | 103 ms: 1.33x faster                                                   |
| Geometric mean | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 379 ms: 1.92x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 979 ms: 1.81x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 506 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 637 ms: 1.60x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.76x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 117 ms                                                 | 89.3 ms: 1.31x faster                                                  |
| nbody          | 154 ms                                                 | 121 ms: 1.27x faster                                                   |
| pidigits       | 191 ms                                                 | 191 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                  |
| regex_compile  | 188 ms                                                 | 179 ms: 1.05x faster                                                   |
| regex_effbot   | 3.63 ms                                                | 3.54 ms: 1.02x faster                                                  |
| regex_dna      | 227 ms                                                 | 222 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 316 us: 1.53x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 63.9 ms: 1.24x faster                                                  |
| tomli_loads          | 3.14 sec                                               | 2.55 sec: 1.23x faster                                                 |
| unpickle_pure_python | 331 us                                                 | 286 us: 1.15x faster                                                   |
| json_loads           | 31.2 us                                                | 27.3 us: 1.14x faster                                                  |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| xml_etree_generate   | 99.4 ms                                                | 93.0 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 112 ms: 1.03x faster                                                   |
| unpickle_list        | 5.20 us                                                | 5.10 us: 1.02x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.37 us: 1.06x slower                                                  |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                  |
| pickle               | 10.7 us                                                | 12.2 us: 1.14x slower                                                  |
| pickle_dict          | 29.6 us                                                | 36.1 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 26.2 ms: 1.21x faster                                                  |
| mako            | 16.3 ms                                                | 13.5 ms: 1.21x faster                                                  |
| django_template | 48.2 ms                                                | 40.8 ms: 1.18x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 59.7 ms: 1.11x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.18x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 119 us: 4.58x faster                                                   |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                  |
| deltablue                | 7.91 ms                                                | 4.10 ms: 1.93x faster                                                  |
| async_tree_none          | 728 ms                                                 | 379 ms: 1.92x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 979 ms: 1.81x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 516 ms: 1.79x faster                                                   |
| logging_silent           | 190 ns                                                 | 107 ns: 1.78x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 506 ms: 1.72x faster                                                   |
| pylint                   | 551 ms                                                 | 344 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 637 ms: 1.60x faster                                                   |
| raytrace                 | 507 ms                                                 | 322 ms: 1.57x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 316 us: 1.53x faster                                                   |
| richards_super           | 94.7 ms                                                | 62.4 ms: 1.52x faster                                                  |
| chaos                    | 115 ms                                                 | 78.5 ms: 1.47x faster                                                  |
| scimark_sor              | 220 ms                                                 | 151 ms: 1.45x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.50 ms: 1.44x faster                                                  |
| richards                 | 79.3 ms                                                | 55.9 ms: 1.42x faster                                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.82 ms: 1.41x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 91.6 ms: 1.40x faster                                                  |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                 |
| scimark_monte_carlo      | 118 ms                                                 | 88.8 ms: 1.33x faster                                                  |
| tornado_http             | 136 ms                                                 | 103 ms: 1.33x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| float                    | 117 ms                                                 | 89.3 ms: 1.31x faster                                                  |
| go                       | 240 ms                                                 | 185 ms: 1.30x faster                                                   |
| logging_simple           | 8.30 us                                                | 6.41 us: 1.29x faster                                                  |
| logging_format           | 9.09 us                                                | 7.05 us: 1.29x faster                                                  |
| deepcopy_memo            | 58.5 us                                                | 45.5 us: 1.28x faster                                                  |
| thrift                   | 1.07 ms                                                | 838 us: 1.28x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.58 ms: 1.28x faster                                                  |
| nbody                    | 154 ms                                                 | 121 ms: 1.27x faster                                                   |
| deepcopy                 | 479 us                                                 | 380 us: 1.26x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.35 us: 1.24x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 63.9 ms: 1.24x faster                                                  |
| html5lib                 | 88.9 ms                                                | 71.9 ms: 1.24x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.28 sec: 1.24x faster                                                 |
| tomli_loads              | 3.14 sec                                               | 2.55 sec: 1.23x faster                                                 |
| comprehensions           | 28.8 us                                                | 23.5 us: 1.22x faster                                                  |
| genshi_text              | 31.8 ms                                                | 26.2 ms: 1.21x faster                                                  |
| mako                     | 16.3 ms                                                | 13.5 ms: 1.21x faster                                                  |
| pyflate                  | 716 ms                                                 | 600 ms: 1.19x faster                                                   |
| djangocms                | 38.4 us                                                | 32.4 us: 1.19x faster                                                  |
| django_template          | 48.2 ms                                                | 40.8 ms: 1.18x faster                                                  |
| spectral_norm            | 170 ms                                                 | 144 ms: 1.18x faster                                                   |
| aiohttp                  | 1.44 ms                                                | 1.24 ms: 1.16x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 123 ms: 1.16x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                                  |
| 2to3                     | 348 ms                                                 | 301 ms: 1.16x faster                                                   |
| dask                     | 441 ms                                                 | 381 ms: 1.16x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 286 us: 1.15x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 73.4 ms: 1.15x faster                                                  |
| json_loads               | 31.2 us                                                | 27.3 us: 1.14x faster                                                  |
| pathlib                  | 20.5 ms                                                | 18.2 ms: 1.13x faster                                                  |
| bench_thread_pool        | 986 us                                                 | 884 us: 1.12x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 23.2 ms: 1.11x faster                                                  |
| sympy_sum                | 196 ms                                                 | 177 ms: 1.11x faster                                                   |
| json                     | 5.69 ms                                                | 5.12 ms: 1.11x faster                                                  |
| mypy2                    | 894 ms                                                 | 806 ms: 1.11x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 59.7 ms: 1.11x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 63.2 ms: 1.09x faster                                                  |
| hexiom                   | 10.4 ms                                                | 9.55 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.98 ms: 1.08x faster                                                  |
| sympy_str                | 346 ms                                                 | 322 ms: 1.08x faster                                                   |
| docutils                 | 3.30 sec                                               | 3.08 sec: 1.07x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 93.0 ms: 1.07x faster                                                  |
| scimark_lu               | 176 ms                                                 | 166 ms: 1.06x faster                                                   |
| fannkuch                 | 532 ms                                                 | 502 ms: 1.06x faster                                                   |
| sympy_expand             | 566 ms                                                 | 536 ms: 1.05x faster                                                   |
| regex_compile            | 188 ms                                                 | 179 ms: 1.05x faster                                                   |
| pprint_safe_repr         | 1.02 sec                                               | 966 ms: 1.05x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 2.01 sec: 1.05x faster                                                 |
| scimark_fft              | 466 ms                                                 | 445 ms: 1.05x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 112 ms: 1.03x faster                                                   |
| regex_effbot             | 3.63 ms                                                | 3.54 ms: 1.02x faster                                                  |
| regex_dna                | 227 ms                                                 | 222 ms: 1.02x faster                                                   |
| unpickle_list            | 5.20 us                                                | 5.10 us: 1.02x faster                                                  |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| pidigits                 | 191 ms                                                 | 191 ms: 1.00x slower                                                   |
| meteor_contest           | 120 ms                                                 | 120 ms: 1.00x slower                                                   |
| sqlite_synth             | 3.02 us                                                | 3.05 us: 1.01x slower                                                  |
| nqueens                  | 106 ms                                                 | 107 ms: 1.01x slower                                                   |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.02x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 3.76 ms: 1.04x slower                                                  |
| mdp                      | 2.85 sec                                               | 2.99 sec: 1.05x slower                                                 |
| async_generators         | 444 ms                                                 | 468 ms: 1.05x slower                                                   |
| pickle_list              | 5.08 us                                                | 5.37 us: 1.06x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                  |
| pickle                   | 10.7 us                                                | 12.2 us: 1.14x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                  |
| pickle_dict              | 29.6 us                                                | 36.1 us: 1.22x slower                                                  |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.23x slower                                                  |
| telco                    | 7.27 ms                                                | 9.19 ms: 1.27x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.21x faster                                                           |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240419-3.13.0a6+-7e6fa5f-PYTHON_UOPS/bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.11x