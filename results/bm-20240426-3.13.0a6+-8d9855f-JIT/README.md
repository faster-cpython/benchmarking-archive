# Results

- fork: savannahostrowski
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [8d9855f](https://github.com/savannahostrowski/cpython/commit/8d9855f)
- commit date: 2024-04-26T12:04:09-07:00
- commit merge base: [3e06c7f719b99cc7f5e8889319cff4980e41d3e8](https://github.com/savannahostrowski/cpython/commit/3e06c7f719b99cc7f5e8889319cff4980e41d3e8)
- ref: llvm_18

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 92.42%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.11.0.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 90.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-base-mem.png)
- [📄table](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-base.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.11.0.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6%2B-8d9855f-vs-3.12.0.png)

