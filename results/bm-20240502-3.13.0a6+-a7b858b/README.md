# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [a7b858b](https://github.com/faster%2dcpython/cpython/commit/a7b858b)
- commit date: 2024-05-02T11:45:50+01:00
- commit merge base: [f8e088df2a87f613ee23ea4f6787f87d9196b9de](https://github.com/faster%2dcpython/cpython/commit/f8e088df2a87f613ee23ea4f6787f87d9196b9de)
- ref: use_attributes_to_gu

## linux x86_64 (azure)

- [pystats raw](bm-20240502-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-pystats.json)
- [pystats table](bm-20240502-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8922611804)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-3.10.4.md)
- [📈time plot](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 96.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-3.11.0.md)
- [📈time plot](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.94%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-3.12.0.md)
- [📈time plot](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 62.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-base-mem.png)
- [📄table](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-base.md)
- [📈time plot](bm-20240502-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-a7b858b-vs-base.png)

