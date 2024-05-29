# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [3375282](https://github.com/python/cpython/commit/3375282)
- commit date: 2024-04-15T21:22:00+03:00
- commit merge base: [78da15406705f88ffa79dafac491fb93b373e8e9](https://github.com/python/cpython/commit/78da15406705f88ffa79dafac491fb93b373e8e9)
- ref: 3375282bb894347b73c1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8695742008)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282-vs-3.10.4.md)
- [📈time plot](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282-vs-3.11.0.md)
- [📈time plot](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282-vs-3.12.0.md)
- [📈time plot](bm-20240415-linux-x86_64-python-3375282bb894347b73c1-3.13.0a6%2B-3375282-vs-3.12.0.png)

