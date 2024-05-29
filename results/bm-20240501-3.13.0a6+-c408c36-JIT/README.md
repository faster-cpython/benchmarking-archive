# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [c408c36](https://github.com/python/cpython/commit/c408c36)
- commit date: 2024-05-01T17:58:22-04:00
- commit merge base: [a7711a2a4e5cf16b34fc284085da724a8c2c06dd](https://github.com/python/cpython/commit/a7711a2a4e5cf16b34fc284085da724a8c2c06dd)
- ref: c408c36e9b346f9f15a3

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8931584972)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x slower (HPT: reliability of 98.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.11.0.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 80.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-base-mem.png)
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-base.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-base.png)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8933042107)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 93.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.11.0.md)
- [📈time plot](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 95.47%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8931577407)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.md)
- [📈time plot](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 87.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.11.0.md)
- [📈time plot](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.md)
- [📈time plot](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.png)

