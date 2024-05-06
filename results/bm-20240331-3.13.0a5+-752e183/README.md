# Results

- fork: python
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [752e183](https://github.com/python/cpython/commit/752e183)
- commit date: 2024-03-31T19:14:48+01:00
- commit merge base: [bfc57d43d8766120ba0c8f3f6d7b2ac681a81d8a](https://github.com/python/cpython/commit/bfc57d43d8766120ba0c8f3f6d7b2ac681a81d8a)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8500212475)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-3.10.4.md)
- [📈time plot](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-3.11.0.md)
- [📈time plot](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-3.12.0.md)
- [📈time plot](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-base-mem.png)
- [📄table](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-base.md)
- [📈time plot](bm-20240331-linux-x86_64-python-main-3.13.0a5%2B-752e183-vs-base.png)

