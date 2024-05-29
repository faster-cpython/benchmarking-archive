# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: T2
- commit hash: [65aa34a](https://github.com/faster%2dcpython/cpython/commit/65aa34a)
- commit date: 2024-04-26T14:52:31+01:00
- commit merge base: [2c451489122d539080c8d674b391dedc1dedcb53](https://github.com/faster%2dcpython/cpython/commit/2c451489122d539080c8d674b391dedc1dedcb53)
- ref: tier_2_call

## linux x86_64 (azure)

- [pystats raw](bm-20240426-azure-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-pystats.json)
- [pystats table](bm-20240426-azure-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-pystats.md)

### vs. base

- [pystats diff](bm-20240426-azure-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8859351404)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: docutils, flaskblogging, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: docutils, flaskblogging, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: docutils, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, thrift
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 docutils, mypy2, pylint
- [🧠memory plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base-mem.png)
- [📄table](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)
- [📈time plot](bm-20240426-linux-x86_64-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png)

