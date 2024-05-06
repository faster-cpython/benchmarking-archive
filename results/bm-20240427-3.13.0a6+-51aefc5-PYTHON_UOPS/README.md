# Results

- fork: python
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [51aefc5](https://github.com/python/cpython/commit/51aefc5)
- commit date: 2024-04-27T11:36:06+01:00
- commit merge base: [c57326f48729f5cd7ddf7e2b38c4fd06d0962a41](https://github.com/python/cpython/commit/c57326f48729f5cd7ddf7e2b38c4fd06d0962a41)
- ref: 51aefc5bf907ddffaaf0

## linux x86_64 (azure)

- [pystats raw](bm-20240427-azure-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-pystats.json)
- [pystats table](bm-20240427-azure-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-pystats.md)

### vs. base

- [pystats diff](bm-20240427-azure-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base-mem.png)
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.14x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x slower (HPT: reliability of 99.96%, 1.02x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.93x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.14x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base-mem.png)
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x slower (HPT: reliability of 64.92%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.92%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.12x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.12x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 99.97%, 1.01x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base-mem.png)
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

