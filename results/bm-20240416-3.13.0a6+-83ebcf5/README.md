# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [83ebcf5](https://github.com/faster%2dcpython/cpython/commit/83ebcf5)
- commit date: 2024-04-16T18:20:36+01:00
- commit merge base: [c520bf9bdf77d43c3d5d95bd08e856759a2abc86](https://github.com/faster%2dcpython/cpython/commit/c520bf9bdf77d43c3d5d95bd08e856759a2abc86)
- ref: faster_alloc_free

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8710019120)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-3.10.4.md)
- [📈time plot](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 96.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-3.11.0.md)
- [📈time plot](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.43%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-3.12.0.md)
- [📈time plot](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-base-mem.png)
- [📄table](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-base.md)
- [📈time plot](bm-20240416-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-83ebcf5-vs-base.png)

