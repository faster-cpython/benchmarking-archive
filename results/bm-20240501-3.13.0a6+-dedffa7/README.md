# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [dedffa7](https://github.com/faster%2dcpython/cpython/commit/dedffa7)
- commit date: 2024-05-01T11:28:42+01:00
- commit merge base: [21c09d9f8195433f34b72ddfa25dd1bda3019ed7](https://github.com/faster%2dcpython/cpython/commit/21c09d9f8195433f34b72ddfa25dd1bda3019ed7)
- ref: use_attributes_to_gu

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8908365994)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 95.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-3.11.0.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.05%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-base-mem.png)
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-base.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-dedffa7-vs-base.png)

