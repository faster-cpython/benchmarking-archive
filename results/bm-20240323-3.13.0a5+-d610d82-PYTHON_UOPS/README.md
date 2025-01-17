# Results

- fork: python
- version: 3.13.0a5+
- config: T2
- commit hash: [d610d82](https://github.com/python/cpython/commit/d610d82)
- commit date: 2024-03-23T22:32:33+00:00
- commit merge base: [6c83352bfe78a7d567c8d76257df6eb91d5a7245](https://github.com/python/cpython/commit/6c83352bfe78a7d567c8d76257df6eb91d5a7245)
- ref: d610d821fd210dce63a1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8405338525)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.md)
- [📈time plot](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.md)
- [📈time plot](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.md)
- [📈time plot](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base-mem.png)
- [📄table](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.md)
- [📈time plot](bm-20240323-linux-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8405338525)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82.json)

### vs. 3.10.4

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.md)
- [📈time plot](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.md)
- [📈time plot](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.md)
- [📈time plot](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.13x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base-mem.png)
- [📄table](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.md)
- [📈time plot](bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8405338525)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.md)
- [📈time plot](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x faster (HPT: reliability of 75.35%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.md)
- [📈time plot](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 97.76%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.md)
- [📈time plot](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.md)
- [📈time plot](bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8405338525)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82.json)

### vs. 3.10.4

- Geometric mean: 1.12x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.md)
- [📈time plot](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.md)
- [📈time plot](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.md)
- [📈time plot](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.md)
- [📈time plot](bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8405338525)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.md)
- [📈time plot](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.md)
- [📈time plot](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 99.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.md)
- [📈time plot](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base-mem.png)
- [📄table](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.md)
- [📈time plot](bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5%2B-d610d82-vs-base.png)

