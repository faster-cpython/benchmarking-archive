# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [689ada7](https://github.com/python/cpython/commit/689ada7)
- commit date: 2024-04-10T20:09:25+01:00
- commit merge base: [630df37116b1c5b381984c547ef9d23792ceb464](https://github.com/python/cpython/commit/630df37116b1c5b381984c547ef9d23792ceb464)
- ref: 689ada79150f28b0053f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8656172978)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-3.10.4.md)
- [📈time plot](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-3.11.0.md)
- [📈time plot](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-3.12.0.md)
- [📈time plot](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-base-mem.png)
- [📄table](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-base.md)
- [📈time plot](bm-20240410-linux-x86_64-python-689ada79150f28b0053f-3.13.0a6%2B-689ada7-vs-base.png)

