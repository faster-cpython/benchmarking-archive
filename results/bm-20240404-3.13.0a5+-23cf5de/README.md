# Results

- fork: faster-cpython
- version: 3.13.0a5+
- config: 
- commit hash: [23cf5de](https://github.com/faster%2dcpython/cpython/commit/23cf5de)
- commit date: 2024-04-04T12:38:32+01:00
- commit merge base: [85843348c5f0b8c2f973e8bc586475e69af19cd2](https://github.com/faster%2dcpython/cpython/commit/85843348c5f0b8c2f973e8bc586475e69af19cd2)
- ref: specialize_binary_op

## linux x86_64 (azure)

- [pystats raw](bm-20240404-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-pystats.json)
- [pystats table](bm-20240404-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-pystats.md)

### vs. base

- [pystats diff](bm-20240404-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8553994929)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-3.10.4.md)
- [📈time plot](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 81.33%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-3.11.0.md)
- [📈time plot](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 94.97%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-3.12.0.md)
- [📈time plot](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-base-mem.png)
- [📄table](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-base.md)
- [📈time plot](bm-20240404-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-23cf5de-vs-base.png)

