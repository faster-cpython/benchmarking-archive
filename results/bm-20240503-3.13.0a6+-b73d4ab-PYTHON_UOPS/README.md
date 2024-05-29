# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: T2
- commit hash: [b73d4ab](https://github.com/faster%2dcpython/cpython/commit/b73d4ab)
- commit date: 2024-05-03T20:15:47+01:00
- commit merge base: [f201628073f22a785a096eccb010e2f78601b60f](https://github.com/faster%2dcpython/cpython/commit/f201628073f22a785a096eccb010e2f78601b60f)
- ref: dynamic_underflow

## linux x86_64 (azure)

- [pystats raw](bm-20240503-azure-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-pystats.json)
- [pystats table](bm-20240503-azure-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-pystats.md)

### vs. base

- [pystats diff](bm-20240503-azure-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-pystats-vs-base.md)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8943839715)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 92.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: 2to3, docutils, genshi_text, genshi_xml, html5lib, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-vs-3.10.4.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: 2to3, docutils, genshi_text, genshi_xml, html5lib, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-vs-3.11.0.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 0.92x
- missing benchmarks: 2to3, docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, pylint, thrift
- [📄table](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-vs-3.12.0.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-faster%252dcpython-dynamic_underflow-3.13.0a6%2B-b73d4ab-vs-3.12.0.png)

