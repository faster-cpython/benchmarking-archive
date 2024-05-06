# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [5da0280](https://github.com/python/cpython/commit/5da0280)
- commit date: 2024-04-25T08:53:29-07:00
- commit merge base: [cce5ae60821ceb7f72cec0ed48f7350c6a63fdc9](https://github.com/python/cpython/commit/cce5ae60821ceb7f72cec0ed48f7350c6a63fdc9)
- ref: 5da0280648b5f1c5142d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8851394403)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280-vs-3.10.4.md)
- [📈time plot](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 96.08%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280-vs-3.11.0.md)
- [📈time plot](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.86%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280-vs-3.12.0.md)
- [📈time plot](bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6%2B-5da0280-vs-3.12.0.png)

