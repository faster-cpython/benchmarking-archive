# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [7595511](https://github.com/python/cpython/commit/7595511)
- commit date: 2024-05-01T16:47:54+00:00
- commit merge base: [6d12f4469c5f9e24809df28b19900722d52af11b](https://github.com/python/cpython/commit/6d12f4469c5f9e24809df28b19900722d52af11b)
- ref: 75955110a643875b5d09

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8914792320)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511-vs-3.11.0.md)
- [📈time plot](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6%2B-7595511-vs-3.12.0.png)

