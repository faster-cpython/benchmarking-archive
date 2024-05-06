# Results

- fork: python
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [1e4a4c4](https://github.com/python/cpython/commit/1e4a4c4)
- commit date: 2024-04-19T09:25:08-07:00
- commit merge base: [8d4a244f1516dcde23becc2a273d30c202237598](https://github.com/python/cpython/commit/8d4a244f1516dcde23becc2a273d30c202237598)
- ref: main

## linux x86_64 (azure)

- [pystats raw](bm-20240419-azure-x86_64-python-main-3.13.0a6%2B-1e4a4c4-pystats.json)
- [pystats table](bm-20240419-azure-x86_64-python-main-3.13.0a6%2B-1e4a4c4-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8756629900)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4-vs-3.10.4.md)
- [📈time plot](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4-vs-3.11.0.md)
- [📈time plot](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4-vs-3.12.0.md)
- [📈time plot](bm-20240419-linux-x86_64-python-main-3.13.0a6%2B-1e4a4c4-vs-3.12.0.png)

