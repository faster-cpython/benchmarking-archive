# Results

- fork: python
- version: 3.13.0a5+
- tier 2: False
- jit: True
- commit hash: [61e54bf](https://github.com/python/cpython/commit/61e54bf)
- commit date: 2024-03-14T16:31:47+00:00
- commit merge base: [19c3a2ff91ccf7444efadbc8f7e67269060050a2](https://github.com/python/cpython/commit/19c3a2ff91ccf7444efadbc8f7e67269060050a2)
- ref: 61e54bfcee9f08a8e09a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8294398478)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf-vs-3.10.4.md)
- [📈time plot](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x faster (HPT: reliability of 52.33%, 1.00x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf-vs-3.11.0.md)
- [📈time plot](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 86.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf-vs-3.12.0.md)
- [📈time plot](bm-20240314-linux-x86_64-python-61e54bfcee9f08a8e09a-3.13.0a5%2B-61e54bf-vs-3.12.0.png)

