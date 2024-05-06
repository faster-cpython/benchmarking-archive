# Results

- fork: python
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [c43f6a4](https://github.com/python/cpython/commit/c43f6a4)
- commit date: 2024-04-03T18:17:51+00:00
- commit merge base: [1c434688866db79082def4f9ef572b85d85908c8](https://github.com/python/cpython/commit/1c434688866db79082def4f9ef572b85d85908c8)
- ref: c43f6a4dfaa1c1974141

## linux x86_64 (azure)

- [pystats raw](bm-20240403-azure-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-pystats.json)
- [pystats table](bm-20240403-azure-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8545294214)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.10.4.md)
- [📈time plot](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.11.0.md)
- [📈time plot](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.12.0.md)
- [📈time plot](bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.12.0.png)

