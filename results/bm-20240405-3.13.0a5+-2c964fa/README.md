# Results

- fork: faster-cpython
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [2c964fa](https://github.com/faster%2dcpython/cpython/commit/2c964fa)
- commit date: 2024-04-05T11:59:35+01:00
- commit merge base: [85843348c5f0b8c2f973e8bc586475e69af19cd2](https://github.com/faster%2dcpython/cpython/commit/85843348c5f0b8c2f973e8bc586475e69af19cd2)
- ref: specialize_binary_op

## linux x86_64 (azure)

- [pystats raw](bm-20240405-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-pystats.json)
- [pystats table](bm-20240405-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-pystats.md)

### vs. base

- [pystats diff](bm-20240405-azure-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571916364)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.10.4.md)
- [📈time plot](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.11.0.md)
- [📈time plot](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.12.0.md)
- [📈time plot](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-base-mem.png)
- [📄table](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-base.md)
- [📈time plot](bm-20240405-linux-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8576567006)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.11.0.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 65.60%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 95.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-base-mem.png)
- [📄table](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-base.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-faster%252dcpython-specialize_binary_op-3.13.0a5%2B-2c964fa-vs-base.png)

