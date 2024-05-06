# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [2584082](https://github.com/python/cpython/commit/2584082)
- commit date: 2024-04-23T17:38:33+00:00
- commit merge base: [2e7771a03d8975ee8a9918ce754c665508c3f682](https://github.com/python/cpython/commit/2e7771a03d8975ee8a9918ce754c665508c3f682)
- ref: 258408239a4fe8a14919

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8805805986)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 98.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6%2B-2584082-vs-3.12.0.png)

