# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [b64de3d](https://github.com/faster%2dcpython/cpython/commit/b64de3d)
- commit date: 2024-05-03T10:51:03+01:00
- commit merge base: [f201628073f22a785a096eccb010e2f78601b60f](https://github.com/faster%2dcpython/cpython/commit/f201628073f22a785a096eccb010e2f78601b60f)
- ref: use_attributes_to_gu

## linux x86_64 (azure)

- [pystats raw](bm-20240503-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-pystats.json)
- [pystats table](bm-20240503-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-pystats.md)

### vs. base

- [pystats diff](bm-20240503-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-pystats-vs-base.md)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8941698099)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-3.10.4.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 98.45%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-3.11.0.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 90.37%, 1.00x slower at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-3.12.0.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 85.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-base-mem.png)
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-base.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-b64de3d-vs-base.png)

