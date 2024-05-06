# Results

- fork: python
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [7e6fa5f](https://github.com/python/cpython/commit/7e6fa5f)
- commit date: 2024-04-19T09:26:42+01:00
- commit merge base: [d3bd6b5f3f48731715e21fe132b8e65a4e5f6ce8](https://github.com/python/cpython/commit/d3bd6b5f3f48731715e21fe132b8e65a4e5f6ce8)
- ref: 7e6fa5fceddc3f4721c0

## linux x86_64 (azure)

- [pystats raw](bm-20240419-azure-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-pystats.json)
- [pystats table](bm-20240419-azure-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8750858653)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-vs-3.10.4.md)
- [📈time plot](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-vs-3.11.0.md)
- [📈time plot](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-vs-3.12.0.md)
- [📈time plot](bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6%2B-7e6fa5f-vs-3.12.0.png)

