# Results

- fork: python
- version: 3.13.0a5+
- config: T2
- commit hash: [94c9742](https://github.com/python/cpython/commit/94c9742)
- commit date: 2024-03-29T18:31:09+00:00
- commit merge base: [5d21d884b6ffa45dac50a5f9a07c41356a8478b4](https://github.com/python/cpython/commit/5d21d884b6ffa45dac50a5f9a07c41356a8478b4)
- ref: 94c97423a9c4969f8ddd

## linux x86_64 (azure)

- [pystats raw](bm-20240329-azure-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-pystats.json)
- [pystats table](bm-20240329-azure-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8485733184)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 94.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-vs-3.10.4.md)
- [📈time plot](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.17x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-vs-3.11.0.md)
- [📈time plot](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-vs-3.12.0.md)
- [📈time plot](bm-20240329-linux-x86_64-python-94c97423a9c4969f8ddd-3.13.0a5%2B-94c9742-vs-3.12.0.png)

