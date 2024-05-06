# Results

- fork: python
- version: 3.13.0a4+
- tier 2: True
- jit: False
- commit hash: [948acd6](https://github.com/python/cpython/commit/948acd6)
- commit date: 2024-02-24T18:34:45-05:00
- commit merge base: [e3dedeae7abbeda0cb3f1d872ebbb914635d64f2](https://github.com/python/cpython/commit/e3dedeae7abbeda0cb3f1d872ebbb914635d64f2)
- ref: 948acd6ed856251dc588

## linux x86_64 (azure)

- [pystats raw](bm-20240224-azure-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-pystats.json)
- [pystats table](bm-20240224-azure-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-pystats.md)

### vs. base

- [pystats diff](bm-20240224-azure-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8034015230)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: aiohttp, dask, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.md)
- [📈time plot](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.97%, 1.02x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, dask, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.md)
- [📈time plot](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 0.93x
- missing benchmarks: aiohttp, dask, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.md)
- [📈time plot](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base-mem.png)
- [📄table](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.md)
- [📈time plot](bm-20240224-linux-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8034015230)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-92-generic-x86_64-with-glibc2.35
- [raw results](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: aiohttp, dask, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.md)
- [📈time plot](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, dask, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.md)
- [📈time plot](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.15x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 0.88x
- missing benchmarks: aiohttp, dask, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.md)
- [📈time plot](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.14x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base-mem.png)
- [📄table](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.md)
- [📈time plot](bm-20240224-pythonperf2-x86_64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8034015230)
- cpu model: missing
- platform: Windows-11-10.0.22621-SP0
- [raw results](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6.json)

### vs. 3.10.4

- Geometric mean: 1.14x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.md)
- [📈time plot](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x faster (HPT: reliability of 63.62%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.md)
- [📈time plot](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x slower (HPT: reliability of 99.90%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.md)
- [📈time plot](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.md)
- [📈time plot](bm-20240224-pythonperf1-amd64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8034015230)
- cpu model: missing
- platform: Windows-11-10.0.22621-SP0
- [raw results](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6.json)

### vs. 3.10.4

- Geometric mean: 1.12x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, genshi_text, genshi_xml, html5lib, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.md)
- [📈time plot](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, genshi_text, genshi_xml, html5lib, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.md)
- [📈time plot](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.md)
- [📈time plot](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.md)
- [📈time plot](bm-20240224-pythonperf1_win32-x86-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8034015230)
- cpu model: missing
- platform: macOS-14.3-arm64-arm-64bit-Mach-O
- [raw results](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6.json)

### vs. 3.10.4

- Geometric mean: 1.09x faster (HPT: reliability of 99.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, dask, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.md)
- [📈time plot](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: aiohttp, dask, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.md)
- [📈time plot](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, dask, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.md)
- [📈time plot](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base-mem.png)
- [📄table](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.md)
- [📈time plot](bm-20240224-darwin-arm64-python-948acd6ed856251dc588-3.13.0a4%2B-948acd6-vs-base.png)

