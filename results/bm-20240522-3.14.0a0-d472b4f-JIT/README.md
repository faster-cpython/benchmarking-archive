# Results

- fork: python
- version: 3.14.0a0
- tier 2: False
- jit: True
- commit hash: [d472b4f](https://github.com/python/cpython/commit/d472b4f)
- commit date: 2024-05-22T08:52:36-04:00
- commit merge base: [858b9e85fcdd495947c9e892ce6e3734652c48f2](https://github.com/python/cpython/commit/858b9e85fcdd495947c9e892ce6e3734652c48f2)
- ref: d472b4f9fa4fb6061588

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9217931145)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.md)
- [📈time plot](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.md)
- [📈time plot](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: flaskblogging
- [📄table](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.md)
- [📈time plot](bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.png)

## linux x86_64 (azure)

- [pystats raw](bm-20240522-azure-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-pystats.json)
- [pystats table](bm-20240522-azure-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9217931145)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.23x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.md)
- [📈time plot](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.55%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.md)
- [📈time plot](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 98.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.md)
- [📈time plot](bm-20240522-linux-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9217931145)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.md)
- [📈time plot](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 99.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.md)
- [📈time plot](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 72.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.md)
- [📈time plot](bm-20240522-pythonperf2-x86_64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9217931145)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.md)
- [📈time plot](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.11x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- [📄table](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.md)
- [📈time plot](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.15%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.md)
- [📈time plot](bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9217931145)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.md)
- [📈time plot](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.md)
- [📈time plot](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.md)
- [📈time plot](bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9217931145)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 0.77x
- missing benchmarks: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.md)
- [📈time plot](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 57.39%, 1.00x slower at 99th %ile)
- Memory usage: 0.66x
- missing benchmarks: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.md)
- [📈time plot](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 0.68x
- missing benchmarks: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.md)
- [📈time plot](bm-20240522-darwin-arm64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f-vs-3.12.0.png)

