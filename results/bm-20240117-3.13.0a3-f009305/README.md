# Results

- fork: python
- version: 3.13.0a3
- tier 2: False
- jit: False
- commit hash: [f009305](https://github.com/python/cpython/commit/f009305)
- commit date: 2024-01-17T13:14:40+01:00
- commit merge base: [b204c4beb44c1a9013f8da16984c9129374ed8c5](https://github.com/python/cpython/commit/b204c4beb44c1a9013f8da16984c9129374ed8c5)
- ref: v3.13.0a3

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8975028102)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.md)
- [📈time plot](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.09%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.md)
- [📈time plot](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 99.11%, 1.00x faster at 99th %ile)
- Memory usage: 0.93x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.md)
- [📈time plot](bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8975028102)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.md)
- [📈time plot](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 99.93%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.md)
- [📈time plot](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 96.41%, 1.00x slower at 99th %ile)
- Memory usage: 0.89x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.md)
- [📈time plot](bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8975028102)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit
- [raw results](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305.json)

### vs. 3.10.4

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.md)
- [📈time plot](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.md)
- [📈time plot](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 86.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.md)
- [📈time plot](bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.png)

