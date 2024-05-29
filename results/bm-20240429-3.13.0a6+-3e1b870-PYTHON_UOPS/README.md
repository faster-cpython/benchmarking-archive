# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: T2
- commit hash: [3e1b870](https://github.com/faster%2dcpython/cpython/commit/3e1b870)
- commit date: 2024-04-29T08:37:40+01:00
- commit merge base: [ab6eda0ee59587e84cb417dd84452b9c6845434c](https://github.com/faster%2dcpython/cpython/commit/ab6eda0ee59587e84cb417dd84452b9c6845434c)
- ref: tier_2_yield_value

## linux x86_64 (azure)

- [pystats raw](bm-20240429-azure-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-pystats.json)
- [pystats table](bm-20240429-azure-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-pystats.md)

### vs. base

- [pystats diff](bm-20240429-azure-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8875103345)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 51.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-3.10.4.md)
- [📈time plot](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.18x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-3.11.0.md)
- [📈time plot](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.21x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-3.12.0.md)
- [📈time plot](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-base-mem.png)
- [📄table](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-base.md)
- [📈time plot](bm-20240429-linux-x86_64-faster%252dcpython-tier_2_yield_value-3.13.0a6%2B-3e1b870-vs-base.png)

