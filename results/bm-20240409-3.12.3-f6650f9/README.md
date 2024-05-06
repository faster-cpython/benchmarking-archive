# Results

- fork: python
- version: 3.12.3
- tier 2: False
- jit: False
- commit hash: [f6650f9](https://github.com/python/cpython/commit/f6650f9)
- commit date: 2024-04-09T10:09:14+02:00
- ref: v3.12.3

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8665231790)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.md)
- [📈time plot](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 96.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, unpack_sequence
- [📄table](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.md)
- [📈time plot](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.md)
- [📈time plot](bm-20240409-linux-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8665231790)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.md)
- [📈time plot](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, unpack_sequence
- [📄table](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.md)
- [📈time plot](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.md)
- [📈time plot](bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8665231790)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.md)
- [📈time plot](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging, unpack_sequence
- [📄table](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.md)
- [📈time plot](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.md)
- [📈time plot](bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8665231790)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9.json)

### vs. 3.10.4

- Geometric mean: 1.01x faster (HPT: reliability of 71.82%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.md)
- [📈time plot](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging, unpack_sequence
- [📄table](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.md)
- [📈time plot](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 99.38%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.md)
- [📈time plot](bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8665231790)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit
- [raw results](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: flaskblogging, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.md)
- [📈time plot](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.98%, 1.01x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: flaskblogging, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.md)
- [📈time plot](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 87.63%, 1.00x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.md)
- [📈time plot](bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9-vs-3.12.0.png)

