# Results

- fork: python
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [f201628](https://github.com/python/cpython/commit/f201628)
- commit date: 2024-05-03T00:51:43+00:00
- commit merge base: [f8290df63f1fd970dfd6bbfdc9a86341a9f97d05](https://github.com/python/cpython/commit/f8290df63f1fd970dfd6bbfdc9a86341a9f97d05)
- ref: f201628073f22a785a09

## linux x86_64 (azure)

- [pystats raw](bm-20240503-azure-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-pystats.json)
- [pystats table](bm-20240503-azure-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-pystats.md)

### vs. base

- [pystats diff](bm-20240503-azure-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8937798727)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628.json)

### vs. 3.10.4

- Geometric mean: 1.05x faster (HPT: reliability of 65.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.10.4.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.19x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.11.0.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.22x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.12.0.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.27x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 docutils, flaskblogging
- [🧠memory plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-base-mem.png)
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-base.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-base.png)

