# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [b43c7e1](https://github.com/python/cpython/commit/b43c7e1)
- commit date: 2024-04-26T21:23:30+01:00
- commit merge base: [5a90de0d4cbc151a6deea36a27eb81b192410e56](https://github.com/python/cpython/commit/5a90de0d4cbc151a6deea36a27eb81b192410e56)
- ref: b43c7e1070e515b3e940

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8882561058)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 50.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-3.11.0.md)
- [📈time plot](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 87.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-base-mem.png)
- [📄table](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-base.md)
- [📈time plot](bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6%2B-b43c7e1-vs-base.png)

