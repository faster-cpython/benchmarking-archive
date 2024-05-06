# Results

- fork: faster-cpython
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [8069375](https://github.com/faster%2dcpython/cpython/commit/8069375)
- commit date: 2024-04-02T11:55:26+01:00
- commit merge base: [9dae05ee59eeba0e67af2a46f2a2907c9f8d7e4a](https://github.com/faster%2dcpython/cpython/commit/9dae05ee59eeba0e67af2a46f2a2907c9f8d7e4a)
- ref: interpreter_reentry_

## linux x86_64 (azure)

- [pystats raw](bm-20240402-azure-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-pystats.json)
- [pystats table](bm-20240402-azure-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8521632576)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375.json)

### vs. 3.10.4

- Geometric mean: 1.36x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-vs-3.10.4.md)
- [📈time plot](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-vs-3.11.0.md)
- [📈time plot](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-vs-3.12.0.md)
- [📈time plot](bm-20240402-linux-x86_64-faster%252dcpython-interpreter_reentry_-3.13.0a5%2B-8069375-vs-3.12.0.png)

