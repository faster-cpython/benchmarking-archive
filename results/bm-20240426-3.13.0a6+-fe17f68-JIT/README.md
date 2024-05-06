# Results

- fork: savannahostrowski
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [fe17f68](https://github.com/savannahostrowski/cpython/commit/fe17f68)
- commit date: 2024-04-26T13:27:29-07:00
- commit merge base: [b43c7e1070e515b3e94043ff777ab83074234051](https://github.com/savannahostrowski/cpython/commit/b43c7e1070e515b3e94043ff777ab83074234051)
- ref: llvm_18

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 84.24%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.11.0.md)
- [📈time plot](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 90.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 97.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-base-mem.png)
- [📄table](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-base.md)
- [📈time plot](bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68.json)

### vs. 3.10.4

- Geometric mean: 1.05x faster (HPT: reliability of 97.82%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.11.0.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6%2B-fe17f68-vs-3.12.0.png)

