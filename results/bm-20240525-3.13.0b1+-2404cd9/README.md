# Results

- fork: python
- version: 3.13.0b1+
- config: 
- commit hash: [2404cd9](https://github.com/python/cpython/commit/2404cd9)
- commit date: 2024-05-25T17:30:57+00:00
- ref: 2404cd94603bc585e617

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9319142252)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.md)
- [📈time plot](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.86%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.md)
- [📈time plot](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 92.27%, 1.00x faster at 99th %ile)
- Memory usage: 0.92x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: flaskblogging
- [📄table](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.md)
- [📈time plot](bm-20240525-arminc-aarch64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.png)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9319142252)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.md)
- [📈time plot](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 95.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.md)
- [📈time plot](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.03%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.md)
- [📈time plot](bm-20240525-linux-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9319142252)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.md)
- [📈time plot](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.md)
- [📈time plot](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 75.85%, 1.00x slower at 99th %ile)
- Memory usage: 0.93x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.md)
- [📈time plot](bm-20240525-pythonperf2-x86_64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9319142252)
- cpu model: missing
- platform: macOS-14.5-arm64-arm-64bit-Mach-O
- [raw results](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 0.80x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.md)
- [📈time plot](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.52%, 1.00x faster at 99th %ile)
- Memory usage: 0.73x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.md)
- [📈time plot](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 0.71x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.md)
- [📈time plot](bm-20240525-darwin-arm64-python-2404cd94603bc585e617-3.13.0b1%2B-2404cd9-vs-3.12.0.png)

