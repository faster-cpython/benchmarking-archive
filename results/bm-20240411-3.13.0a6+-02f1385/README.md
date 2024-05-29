# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [02f1385](https://github.com/python/cpython/commit/02f1385)
- commit date: 2024-04-11T08:37:01+01:00
- commit merge base: [993c3cca16ed00a0bfe467f7f26ac4f5f6dfb24c](https://github.com/python/cpython/commit/993c3cca16ed00a0bfe467f7f26ac4f5f6dfb24c)
- ref: 02f1385f8ad6bf453763

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8645603762)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385-vs-3.10.4.md)
- [📈time plot](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 96.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385-vs-3.11.0.md)
- [📈time plot](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385-vs-3.12.0.md)
- [📈time plot](bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6%2B-02f1385-vs-3.12.0.png)

