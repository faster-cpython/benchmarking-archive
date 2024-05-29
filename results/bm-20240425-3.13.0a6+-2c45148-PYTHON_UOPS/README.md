# Results

- fork: python
- version: 3.13.0a6+
- config: T2
- commit hash: [2c45148](https://github.com/python/cpython/commit/2c45148)
- commit date: 2024-04-25T13:51:31+02:00
- commit merge base: [f180b31e7629d36265fa36f1560365358b4fd47c](https://github.com/python/cpython/commit/f180b31e7629d36265fa36f1560365358b4fd47c)
- ref: 2c451489122d539080c8

## linux x86_64 (azure)

- [pystats raw](bm-20240425-azure-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-pystats.json)
- [pystats table](bm-20240425-azure-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8859351404)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 82.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-3.10.4.md)
- [📈time plot](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.17x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-3.11.0.md)
- [📈time plot](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.20x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-3.12.0.md)
- [📈time plot](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.24x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 flaskblogging
- [🧠memory plot](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-base-mem.png)
- [📄table](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-base.md)
- [📈time plot](bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6%2B-2c45148-vs-base.png)

