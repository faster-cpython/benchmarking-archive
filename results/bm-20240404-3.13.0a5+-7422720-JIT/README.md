# Results

- fork: brandtbucher
- version: 3.13.0a5+
- tier 2: False
- jit: True
- commit hash: [7422720](https://github.com/brandtbucher/cpython/commit/7422720)
- commit date: 2024-04-04T12:58:18-07:00
- commit merge base: [434bc593df4c0274b8afd3c1dcdc9234f469d9bf](https://github.com/brandtbucher/cpython/commit/434bc593df4c0274b8afd3c1dcdc9234f469d9bf)
- ref: stitch_exhausted

## linux x86_64 (azure)

- [pystats raw](bm-20240404-azure-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-pystats.json)
- [pystats table](bm-20240404-azure-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-pystats.md)

### vs. base

- [pystats diff](bm-20240404-azure-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.md)
- [📈time plot](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 63.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.md)
- [📈time plot](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 67.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.md)
- [📈time plot](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base-mem.png)
- [📄table](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.md)
- [📈time plot](bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 84.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 99.38%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base-mem.png)
- [📄table](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720.json)

### vs. 3.10.4

- Geometric mean: 1.05x faster (HPT: reliability of 99.20%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.82%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.md)
- [📈time plot](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x slower (HPT: reliability of 97.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.md)
- [📈time plot](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 93.16%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.md)
- [📈time plot](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base-mem.png)
- [📄table](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.md)
- [📈time plot](bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5%2B-7422720-vs-base.png)

