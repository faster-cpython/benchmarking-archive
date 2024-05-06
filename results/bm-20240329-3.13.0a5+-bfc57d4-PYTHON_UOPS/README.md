# Results

- fork: python
- version: 3.13.0a5+
- tier 2: True
- jit: False
- commit hash: [bfc57d4](https://github.com/python/cpython/commit/bfc57d4)
- commit date: 2024-03-29T18:58:08-04:00
- commit merge base: [05e0b67a43c5c1778dc2643c8b7c12864e135999](https://github.com/python/cpython/commit/05e0b67a43c5c1778dc2643c8b7c12864e135999)
- ref: bfc57d43d8766120ba0c

## linux x86_64 (azure)

- [pystats raw](bm-20240329-azure-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-pystats.json)
- [pystats table](bm-20240329-azure-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-pystats.md)

### vs. base

- [pystats diff](bm-20240329-azure-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.11x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.16x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base-mem.png)
- [📄table](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.md)
- [📈time plot](bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.14x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.15x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base-mem.png)
- [📄table](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.md)
- [📈time plot](bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 66.40%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.90%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.11x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.md)
- [📈time plot](bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8494215798)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4.json)

### vs. 3.10.4

- Geometric mean: 1.12x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base-mem.png)
- [📄table](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.md)
- [📈time plot](bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5%2B-bfc57d4-vs-base.png)

