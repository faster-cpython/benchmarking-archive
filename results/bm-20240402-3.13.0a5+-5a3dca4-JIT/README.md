# Results

- fork: brandtbucher
- version: 3.13.0a5+
- config: JIT
- commit hash: [5a3dca4](https://github.com/brandtbucher/cpython/commit/5a3dca4)
- commit date: 2024-04-02T12:48:25-07:00
- commit merge base: [05e0b67a43c5c1778dc2643c8b7c12864e135999](https://github.com/brandtbucher/cpython/commit/05e0b67a43c5c1778dc2643c8b7c12864e135999)
- ref: stitch_exhausted

## linux x86_64 (azure)

- [pystats raw](bm-20240402-azure-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-pystats.json)
- [pystats table](bm-20240402-azure-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-pystats.md)

### vs. base

- [pystats diff](bm-20240402-azure-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8528815369)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.md)
- [📈time plot](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 51.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.md)
- [📈time plot](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 63.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.md)
- [📈time plot](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base-mem.png)
- [📄table](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.md)
- [📈time plot](bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8528815369)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x faster (HPT: reliability of 55.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x slower (HPT: reliability of 99.96%, 1.01x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base-mem.png)
- [📄table](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8528815369)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.md)
- [📈time plot](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.md)
- [📈time plot](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.md)
- [📈time plot](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.92%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.md)
- [📈time plot](bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8528815369)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4.json)

### vs. 3.10.4

- Geometric mean: 1.04x faster (HPT: reliability of 99.57%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.md)
- [📈time plot](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.md)
- [📈time plot](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.md)
- [📈time plot](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.md)
- [📈time plot](bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8528815369)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.md)
- [📈time plot](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x slower (HPT: reliability of 99.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.md)
- [📈time plot](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 86.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.md)
- [📈time plot](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base-mem.png)
- [📄table](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.md)
- [📈time plot](bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-5a3dca4-vs-base.png)

