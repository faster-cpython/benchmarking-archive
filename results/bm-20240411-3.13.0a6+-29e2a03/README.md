# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [29e2a03](https://github.com/faster%2dcpython/cpython/commit/29e2a03)
- commit date: 2024-04-11T11:52:28+01:00
- commit merge base: [02f1385f8ad6bf45376377c41f106b386d3a7eb0](https://github.com/faster%2dcpython/cpython/commit/02f1385f8ad6bf45376377c41f106b386d3a7eb0)
- ref: faster_trashcan

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8645603762)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-3.10.4.md)
- [📈time plot](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-3.11.0.md)
- [📈time plot](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-3.12.0.md)
- [📈time plot](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-base-mem.png)
- [📄table](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-base.md)
- [📈time plot](bm-20240411-linux-x86_64-faster%252dcpython-faster_trashcan-3.13.0a6%2B-29e2a03-vs-base.png)

