# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [7819b1c](https://github.com/faster%2dcpython/cpython/commit/7819b1c)
- commit date: 2024-05-03T15:10:44+01:00
- commit merge base: [f201628073f22a785a096eccb010e2f78601b60f](https://github.com/faster%2dcpython/cpython/commit/f201628073f22a785a096eccb010e2f78601b60f)
- ref: tier_2_call

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8941340909)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-3.10.4.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 98.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-3.11.0.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-3.12.0.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 89.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-base-mem.png)
- [📄table](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-base.md)
- [📈time plot](bm-20240503-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-7819b1c-vs-base.png)

