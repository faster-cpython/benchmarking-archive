# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [c7e7bfc](https://github.com/python/cpython/commit/c7e7bfc)
- commit date: 2024-04-29T08:58:57+02:00
- commit merge base: [ab6eda0ee59587e84cb417dd84452b9c6845434c](https://github.com/python/cpython/commit/ab6eda0ee59587e84cb417dd84452b9c6845434c)
- ref: c7e7bfc4ca26bf90e0d4

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8878741589)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc-vs-3.10.4.md)
- [📈time plot](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.86%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc-vs-3.11.0.md)
- [📈time plot](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc-vs-3.12.0.md)
- [📈time plot](bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6%2B-c7e7bfc-vs-3.12.0.png)

