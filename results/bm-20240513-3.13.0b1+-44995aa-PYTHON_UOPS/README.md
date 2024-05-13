# Results

- fork: python
- version: 3.13.0b1+
- tier 2: True
- jit: False
- commit hash: [44995aa](https://github.com/python/cpython/commit/44995aa)
- commit date: 2024-05-13T11:56:26+00:00
- commit merge base: [2268289a47c6e3c9a220b53697f9480ec390466f](https://github.com/python/cpython/commit/2268289a47c6e3c9a220b53697f9480ec390466f)
- ref: 44995aab499b09a550de

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9063827501)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa.json)

### vs. 3.10.4

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.10.4.md)
- [📈time plot](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.11.0.md)
- [📈time plot](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.18x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.12.0.md)
- [📈time plot](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.14x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-base-mem.png)
- [📄table](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-base.md)
- [📈time plot](bm-20240513-pythonperf2-x86_64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9063827501)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa.json)

### vs. 3.10.4

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 0.74x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.10.4.md)
- [📈time plot](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.61x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.11.0.md)
- [📈time plot](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.07x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 0.64x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.12.0.md)
- [📈time plot](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.13x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: 🔴 sqlglot_normalize
- [🧠memory plot](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-base-mem.png)
- [📄table](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-base.md)
- [📈time plot](bm-20240513-darwin-arm64-python-44995aab499b09a550de-3.13.0b1%2B-44995aa-vs-base.png)

