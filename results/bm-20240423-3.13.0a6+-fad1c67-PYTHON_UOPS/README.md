# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: T2
- commit hash: [fad1c67](https://github.com/faster%2dcpython/cpython/commit/fad1c67)
- commit date: 2024-04-23T13:50:24+01:00
- commit merge base: [a6647d16abf4dd65997865e857371673238e60bf](https://github.com/faster%2dcpython/cpython/commit/a6647d16abf4dd65997865e857371673238e60bf)
- ref: return_gen_tier_2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8800798173)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.03x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-base-mem.png)
- [📄table](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-base.md)
- [📈time plot](bm-20240423-linux-x86_64-faster%252dcpython-return_gen_tier_2-3.13.0a6%2B-fad1c67-vs-base.png)

