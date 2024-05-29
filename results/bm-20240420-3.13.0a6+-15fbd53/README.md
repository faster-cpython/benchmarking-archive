# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [15fbd53](https://github.com/python/cpython/commit/15fbd53)
- commit date: 2024-04-20T17:46:52+01:00
- commit merge base: [d8f350309ded3130c43f0d2809dcb8ec13112320](https://github.com/python/cpython/commit/d8f350309ded3130c43f0d2809dcb8ec13112320)
- ref: 15fbd53ba96be4b6a5ab

## linux x86_64 (azure)

- [pystats raw](bm-20240420-azure-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-pystats.json)
- [pystats table](bm-20240420-azure-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.23x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 80.95%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x faster (HPT: reliability of 59.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.png)

