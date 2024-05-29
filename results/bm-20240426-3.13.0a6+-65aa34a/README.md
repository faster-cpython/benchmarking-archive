# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [65aa34a](https://github.com/faster%2dcpython/cpython/commit/65aa34a)
- commit date: 2024-04-26T14:52:31+01:00
- commit merge base: [2c451489122d539080c8d674b391dedc1dedcb53](https://github.com/faster%2dcpython/cpython/commit/2c451489122d539080c8d674b391dedc1dedcb53)
- ref: tier_2_call

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8849402063)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.24%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 98.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 flaskblogging
- [🧠memory plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base-mem.png)
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8849402063)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.23x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 76.65%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 83.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base-mem.png)
- [📄table](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8849402063)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 96.61%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)
- [📈time plot](bm-20240426-pythonperf1-amd64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8849402063)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a.json)

### vs. 3.10.4

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 71.74%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)
- [📈time plot](bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8849402063)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)
- [📈time plot](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x faster (HPT: reliability of 65.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)
- [📈time plot](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)
- [📈time plot](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 97.65%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base-mem.png)
- [📄table](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)
- [📈time plot](bm-20240426-darwin-arm64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png)

