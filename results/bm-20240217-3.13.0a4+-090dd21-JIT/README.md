# Results

- fork: python
- version: 3.13.0a4+
- config: JIT
- commit hash: [090dd21](https://github.com/python/cpython/commit/090dd21)
- commit date: 2024-02-17T23:18:30+02:00
- commit merge base: [aba37d451fabb44a7f478958ba117ae5b6ea54c0](https://github.com/python/cpython/commit/aba37d451fabb44a7f478958ba117ae5b6ea54c0)
- ref: 090dd21ab9379d6a2a69

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7945075940)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.md)
- [📈time plot](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 97.27%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.md)
- [📈time plot](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 96.12%, 1.00x faster at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.md)
- [📈time plot](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base-mem.png)
- [📄table](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.md)
- [📈time plot](bm-20240217-linux-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7945075940)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-92-generic-x86_64-with-glibc2.35
- [raw results](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.md)
- [📈time plot](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 91.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.md)
- [📈time plot](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.92x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.md)
- [📈time plot](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base-mem.png)
- [📄table](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.md)
- [📈time plot](bm-20240217-pythonperf2-x86_64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7945075940)
- cpu model: missing
- platform: Windows-11-10.0.22621-SP0
- [raw results](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.md)
- [📈time plot](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.md)
- [📈time plot](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.md)
- [📈time plot](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 60.44%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.md)
- [📈time plot](bm-20240217-pythonperf1-amd64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7945075940)
- cpu model: missing
- platform: Windows-11-10.0.22621-SP0
- [raw results](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21.json)

### vs. 3.10.4

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, dulwich_log, flaskblogging, genshi_text, genshi_xml, html5lib, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.md)
- [📈time plot](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, dulwich_log, flaskblogging, genshi_text, genshi_xml, html5lib, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.md)
- [📈time plot](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.md)
- [📈time plot](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.md)
- [📈time plot](bm-20240217-pythonperf1_win32-x86-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7945075940)
- cpu model: missing
- platform: macOS-14.3-arm64-arm-64bit-Mach-O
- [raw results](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.md)
- [📈time plot](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.md)
- [📈time plot](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 77.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.md)
- [📈time plot](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 92.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base-mem.png)
- [📄table](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.md)
- [📈time plot](bm-20240217-darwin-arm64-python-090dd21ab9379d6a2a69-3.13.0a4%2B-090dd21-vs-base.png)

