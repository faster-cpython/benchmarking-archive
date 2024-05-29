# Results

- fork: python
- version: 3.13.0a6+
- config: T2
- commit hash: [acf69e0](https://github.com/python/cpython/commit/acf69e0)
- commit date: 2024-04-16T14:27:18+01:00
- commit merge base: [c053d52edd1e05ccc339e380b705749a3240d645](https://github.com/python/cpython/commit/c053d52edd1e05ccc339e380b705749a3240d645)
- ref: acf69e09c66f8473399f

## linux x86_64 (azure)

- [pystats raw](bm-20240416-azure-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-pystats.json)
- [pystats table](bm-20240416-azure-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-pystats.md)

### vs. base

- [pystats diff](bm-20240416-azure-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8726738428)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 82.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.10.4.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.17x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.11.0.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.12.0.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.25x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-base-mem.png)
- [📄table](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-base.md)
- [📈time plot](bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6%2B-acf69e0-vs-base.png)

