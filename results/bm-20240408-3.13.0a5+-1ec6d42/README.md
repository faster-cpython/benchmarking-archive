# Results

- fork: faster-cpython
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [1ec6d42](https://github.com/faster%2dcpython/cpython/commit/1ec6d42)
- commit date: 2024-04-08T10:38:09+01:00
- commit merge base: [e1eeb990bd169491075eeaea31481a4a96bdecbb](https://github.com/faster%2dcpython/cpython/commit/e1eeb990bd169491075eeaea31481a4a96bdecbb)
- ref: specialize_load_attr

## linux x86_64 (azure)

- [pystats raw](bm-20240408-azure-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-pystats.json)
- [pystats table](bm-20240408-azure-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-pystats.md)

### vs. base

- [pystats diff](bm-20240408-azure-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8597901566)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-3.10.4.md)
- [📈time plot](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 95.27%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-3.11.0.md)
- [📈time plot](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.78%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-3.12.0.md)
- [📈time plot](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 85.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-base-mem.png)
- [📄table](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-base.md)
- [📈time plot](bm-20240408-linux-x86_64-faster%252dcpython-specialize_load_attr-3.13.0a5%2B-1ec6d42-vs-base.png)

