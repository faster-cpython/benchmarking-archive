# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [51aefc5](https://github.com/python/cpython/commit/51aefc5)
- commit date: 2024-04-27T11:36:06+01:00
- commit merge base: [c57326f48729f5cd7ddf7e2b38c4fd06d0962a41](https://github.com/python/cpython/commit/c57326f48729f5cd7ddf7e2b38c4fd06d0962a41)
- ref: 51aefc5bf907ddffaaf0

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 69.49%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 89.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 99.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base-mem.png)
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 88.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 98.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base-mem.png)
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png)

