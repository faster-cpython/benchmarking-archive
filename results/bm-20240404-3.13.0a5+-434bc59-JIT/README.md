# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [434bc59](https://github.com/python/cpython/commit/434bc59)
- commit date: 2024-04-04T12:26:07-07:00
- commit merge base: [42205143f8b3211d1392f1d9f2cf6717bdaa5b47](https://github.com/python/cpython/commit/42205143f8b3211d1392f1d9f2cf6717bdaa5b47)
- ref: 434bc593df4c0274b8af

## linux x86_64 (azure)

- [pystats raw](bm-20240404-azure-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-pystats.json)
- [pystats table](bm-20240404-azure-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.md)
- [📈time plot](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 73.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.md)
- [📈time plot](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 94.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.md)
- [📈time plot](bm-20240404-linux-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 87.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 98.14%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8560816817)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.md)
- [📈time plot](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x faster (HPT: reliability of 98.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.md)
- [📈time plot](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 98.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.md)
- [📈time plot](bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5%2B-434bc59-vs-3.12.0.png)

