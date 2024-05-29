# Results

- fork: python
- version: 3.13.0a6+
- config: T2
- commit hash: [ab6eda0](https://github.com/python/cpython/commit/ab6eda0)
- commit date: 2024-04-29T07:54:05+01:00
- commit merge base: [aa8f6d2708bce1462544d2e2cae05a2595ffd9ec](https://github.com/python/cpython/commit/aa8f6d2708bce1462544d2e2cae05a2595ffd9ec)
- ref: ab6eda0ee59587e84cb4

## linux x86_64 (azure)

- [pystats raw](bm-20240429-azure-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-pystats.json)
- [pystats table](bm-20240429-azure-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8875103345)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 50.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-vs-3.10.4.md)
- [📈time plot](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.18x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-vs-3.11.0.md)
- [📈time plot](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-vs-3.12.0.md)
- [📈time plot](bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6%2B-ab6eda0-vs-3.12.0.png)

