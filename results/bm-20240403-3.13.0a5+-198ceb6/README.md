# Results

- fork: faster-cpython
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [198ceb6](https://github.com/faster%2dcpython/cpython/commit/198ceb6)
- commit date: 2024-04-03T10:34:08+01:00
- commit merge base: [bf82f77957a31c3731b4ec470c406f5708ca9ba3](https://github.com/faster%2dcpython/cpython/commit/bf82f77957a31c3731b4ec470c406f5708ca9ba3)
- ref: specialize_binary_op

## linux x86_64 (azure)

- [pystats raw](bm-20240403-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-pystats.json)
- [pystats table](bm-20240403-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8536600011)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-vs-3.10.4.md)
- [📈time plot](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 97.05%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-vs-3.11.0.md)
- [📈time plot](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 98.60%, 1.00x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-vs-3.12.0.md)
- [📈time plot](bm-20240403-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-198ceb6-vs-3.12.0.png)

