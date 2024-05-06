# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [2e7771a](https://github.com/python/cpython/commit/2e7771a)
- commit date: 2024-04-23T10:20:14-07:00
- commit merge base: [0d221e9a1952949465df4e737e8d3189bdd9632a](https://github.com/python/cpython/commit/0d221e9a1952949465df4e737e8d3189bdd9632a)
- ref: 2e7771a03d8975ee8a99

## linux x86_64 (azure)

- [pystats raw](bm-20240423-azure-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-pystats.json)
- [pystats table](bm-20240423-azure-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8805734379)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 83.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 94.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-python-2e7771a03d8975ee8a99-3.13.0a6%2B-2e7771a-vs-3.12.0.png)

