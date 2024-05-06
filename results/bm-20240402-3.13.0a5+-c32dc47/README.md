# Results

- fork: python
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [c32dc47](https://github.com/python/cpython/commit/c32dc47)
- commit date: 2024-04-02T11:59:21+01:00
- commit merge base: [c97d3af2391e62ef456ef2365d48ab9b8cdbe27b](https://github.com/python/cpython/commit/c97d3af2391e62ef456ef2365d48ab9b8cdbe27b)
- ref: main

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8521671266)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.23x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47-vs-3.10.4.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47-vs-3.11.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 94.64%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47-vs-3.12.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5%2B-c32dc47-vs-3.12.0.png)

