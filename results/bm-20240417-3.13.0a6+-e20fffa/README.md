# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [e20fffa](https://github.com/faster%2dcpython/cpython/commit/e20fffa)
- commit date: 2024-04-17T14:40:16+01:00
- commit merge base: [c520bf9bdf77d43c3d5d95bd08e856759a2abc86](https://github.com/faster%2dcpython/cpython/commit/c520bf9bdf77d43c3d5d95bd08e856759a2abc86)
- ref: faster_alloc_free

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8723348356)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-3.10.4.md)
- [📈time plot](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.44%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-3.11.0.md)
- [📈time plot](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-3.12.0.md)
- [📈time plot](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 89.47%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-base-mem.png)
- [📄table](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-base.md)
- [📈time plot](bm-20240417-linux-x86_64-faster%252dcpython-faster_alloc_free-3.13.0a6%2B-e20fffa-vs-base.png)

