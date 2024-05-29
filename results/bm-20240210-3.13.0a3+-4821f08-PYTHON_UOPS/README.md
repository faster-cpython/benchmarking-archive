# Results

- fork: python
- version: 3.13.0a3+
- config: T2
- commit hash: [4821f08](https://github.com/python/cpython/commit/4821f08)
- commit date: 2024-02-10T15:59:23-07:00
- commit merge base: [b70a68fbd6b72a25b5ef430603e39c9e40f40d29](https://github.com/python/cpython/commit/b70a68fbd6b72a25b5ef430603e39c9e40f40d29)
- ref: 4821f08674e290a396d2

## linux x86_64 (azure)

- [pystats raw](bm-20240210-azure-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-pystats.json)
- [pystats table](bm-20240210-azure-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-pystats.md)

### vs. base

- [pystats diff](bm-20240210-azure-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7858199173)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: aiohttp, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.md)
- [📈time plot](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 98.80%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.md)
- [📈time plot](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.93x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.md)
- [📈time plot](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base-mem.png)
- [📄table](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.md)
- [📈time plot](bm-20240210-linux-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7858199173)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-92-generic-x86_64-with-glibc2.35
- [raw results](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.md)
- [📈time plot](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x slower (HPT: reliability of 93.66%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.md)
- [📈time plot](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 0.88x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.md)
- [📈time plot](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base-mem.png)
- [📄table](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.md)
- [📈time plot](bm-20240210-pythonperf2-x86_64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7858199173)
- cpu model: missing
- platform: Windows-11-10.0.22621-SP0
- [raw results](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.md)
- [📈time plot](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.md)
- [📈time plot](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 99.87%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.md)
- [📈time plot](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.md)
- [📈time plot](bm-20240210-pythonperf1-amd64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7858199173)
- cpu model: missing
- platform: Windows-11-10.0.22621-SP0
- [raw results](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08.json)

### vs. 3.10.4

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, dulwich_log, flaskblogging, genshi_text, genshi_xml, html5lib, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.md)
- [📈time plot](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, dulwich_log, flaskblogging, genshi_text, genshi_xml, html5lib, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.md)
- [📈time plot](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.md)
- [📈time plot](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.md)
- [📈time plot](bm-20240210-pythonperf1_win32-x86-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7858199173)
- cpu model: missing
- platform: macOS-14.3-arm64-arm-64bit-Mach-O
- [raw results](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.md)
- [📈time plot](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.md)
- [📈time plot](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.md)
- [📈time plot](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base-mem.png)
- [📄table](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.md)
- [📈time plot](bm-20240210-darwin-arm64-python-4821f08674e290a396d2-3.13.0a3%2B-4821f08-vs-base.png)

