# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [f8e088d](https://github.com/python/cpython/commit/f8e088d)
- commit date: 2024-05-02T08:57:45+00:00
- commit merge base: [a6b610a94bee0e4436aee2825c14f05ec2f22f75](https://github.com/python/cpython/commit/a6b610a94bee0e4436aee2825c14f05ec2f22f75)
- ref: f8e088df2a87f613ee23

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8922611804)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d-vs-3.10.4.md)
- [📈time plot](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 99.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d-vs-3.11.0.md)
- [📈time plot](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.94%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d-vs-3.12.0.md)
- [📈time plot](bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6%2B-f8e088d-vs-3.12.0.png)

