# Results

- fork: python
- version: 3.13.0a6+
- config: T2
- commit hash: [a6647d1](https://github.com/python/cpython/commit/a6647d1)
- commit date: 2024-04-22T13:34:06+01:00
- commit merge base: [ceb6038b053c403bed3ca3a8bd17b7e3fc9aab7d](https://github.com/python/cpython/commit/ceb6038b053c403bed3ca3a8bd17b7e3fc9aab7d)
- ref: a6647d16abf4dd659978

## linux x86_64 (azure)

- [pystats raw](bm-20240422-azure-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-pystats.json)
- [pystats table](bm-20240422-azure-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8796929662)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-vs-3.10.4.md)
- [📈time plot](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-vs-3.11.0.md)
- [📈time plot](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-vs-3.12.0.md)
- [📈time plot](bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6%2B-a6647d1-vs-3.12.0.png)

