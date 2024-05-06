# Results

- fork: python
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [bfc57d4](https://github.com/python/cpython/commit/bfc57d4)
- commit date: 2024-03-29T18:58:08-04:00
- commit merge base: [05e0b67a43c5c1778dc2643c8b7c12864e135999](https://github.com/python/cpython/commit/05e0b67a43c5c1778dc2643c8b7c12864e135999)
- ref: bfc57d43d8766120ba0c

## linux x86_64 (azure)

- [pystats raw](bm-20240329-azure-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-pystats.json)
- [pystats table](bm-20240329-azure-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.36x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.23x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 72.43%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.12x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.31x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x faster (HPT: reliability of 92.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

