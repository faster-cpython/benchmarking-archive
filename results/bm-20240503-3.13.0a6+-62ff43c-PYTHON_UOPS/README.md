# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [62ff43c](https://github.com/faster%2dcpython/cpython/commit/62ff43c)
- commit date: 2024-05-03T11:38:25+01:00
- commit merge base: [f201628073f22a785a096eccb010e2f78601b60f](https://github.com/faster%2dcpython/cpython/commit/f201628073f22a785a096eccb010e2f78601b60f)
- ref: tier_2_call

## linux x86_64 (azure)

- [pystats raw](bm-20240503-azure-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-pystats.json)
- [pystats table](bm-20240503-azure-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-pystats.md)

### vs. base

- [pystats diff](bm-20240503-azure-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8937798727)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c.json)

### vs. 3.10.4

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-3.10.4.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-3.11.0.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.11x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-3.12.0.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-base-mem.png)
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-base.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-62ff43c-vs-base.png)

