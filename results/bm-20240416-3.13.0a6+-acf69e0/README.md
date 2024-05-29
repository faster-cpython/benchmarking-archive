# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [acf69e0](https://github.com/python/cpython/commit/acf69e0)
- commit date: 2024-04-16T14:27:18+01:00
- commit merge base: [c053d52edd1e05ccc339e380b705749a3240d645](https://github.com/python/cpython/commit/c053d52edd1e05ccc339e380b705749a3240d645)
- ref: acf69e09c66f8473399f

## linux x86_64 (azure)

- [pystats raw](bm-20240416-azure-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-pystats.json)
- [pystats table](bm-20240416-azure-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8713010520)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.10.4.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.11.0.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.12.0.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.12.0.png)

