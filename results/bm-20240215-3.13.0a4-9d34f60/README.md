# Results

- fork: python
- version: 3.13.0a4
- tier 2: False
- jit: False
- commit hash: [9d34f60](https://github.com/python/cpython/commit/9d34f60)
- commit date: 2024-02-15T14:38:42+01:00
- commit merge base: [b0e5c35ded6d4a16d7a021c10c99bac94250edd0](https://github.com/python/cpython/commit/b0e5c35ded6d4a16d7a021c10c99bac94250edd0)
- ref: v3.13.0a4

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9038489291)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)
- [📈time plot](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)
- [📈time plot](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 94.81%, 1.00x faster at 99th %ile)
- Memory usage: 0.88x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: flaskblogging
- [📄table](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)
- [📈time plot](bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9038489291)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)
- [📈time plot](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)
- [📈time plot](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 90.04%, 1.00x slower at 99th %ile)
- Memory usage: 0.89x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)
- [📈time plot](bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9038489291)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)
- [📈time plot](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)
- [📈time plot](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)
- [📈time plot](bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9038489291)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60.json)

### vs. 3.10.4

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)
- [📈time plot](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)
- [📈time plot](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)
- [📈time plot](bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9038489291)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 0.43x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)
- [📈time plot](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 0.44x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)
- [📈time plot](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 76.14%, 1.00x slower at 99th %ile)
- Memory usage: 0.48x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)
- [📈time plot](bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png)

