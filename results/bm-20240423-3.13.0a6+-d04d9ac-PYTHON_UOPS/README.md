# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [d04d9ac](https://github.com/faster%2dcpython/cpython/commit/d04d9ac)
- commit date: 2024-04-23T11:39:00+01:00
- commit merge base: [a6647d16abf4dd65997865e857371673238e60bf](https://github.com/faster%2dcpython/cpython/commit/a6647d16abf4dd65997865e857371673238e60bf)
- ref: function_entry_enter

## linux x86_64 (azure)

- [pystats raw](bm-20240423-azure-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-pystats.json)
- [pystats table](bm-20240423-azure-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-pystats.md)

### vs. base

- [pystats diff](bm-20240423-azure-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8799039215)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 99.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-base-mem.png)
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-base.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-function_entry_enter-3.13.0a6%2B-d04d9ac-vs-base.png)

