# Results

- fork: python
- version: 3.13.0a5+
- tier 2: False
- jit: True
- commit hash: [027fa2e](https://github.com/python/cpython/commit/027fa2e)
- commit date: 2024-04-02T10:45:00-04:00
- commit merge base: [954d616b4c8cd091214aa3b8ea886bcf9067243a](https://github.com/python/cpython/commit/954d616b4c8cd091214aa3b8ea886bcf9067243a)
- ref: 027fa2eccf39ddccdf7b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8559937355)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.10.4.md)
- [📈time plot](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 63.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.11.0.md)
- [📈time plot](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 92.16%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.12.0.md)
- [📈time plot](bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8556788888)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.10.4.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 73.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.11.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.79%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.12.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5%2B-027fa2e-vs-3.12.0.png)

