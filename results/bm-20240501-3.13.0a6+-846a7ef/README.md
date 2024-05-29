# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [846a7ef](https://github.com/faster%2dcpython/cpython/commit/846a7ef)
- commit date: 2024-05-01T21:45:37+01:00
- commit merge base: [75955110a643875b5d096b6eda06dcc6e542e171](https://github.com/faster%2dcpython/cpython/commit/75955110a643875b5d096b6eda06dcc6e542e171)
- ref: use_attributes_to_gu

## linux x86_64 (azure)

- [pystats raw](bm-20240501-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-pystats.json)
- [pystats table](bm-20240501-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8914792320)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 98.21%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-3.11.0.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-base-mem.png)
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-base.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-846a7ef-vs-base.png)

