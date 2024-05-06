# Results

- fork: gvanrossum
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [8cb71dd](https://github.com/gvanrossum/cpython/commit/8cb71dd)
- commit date: 2024-04-26T17:09:45-07:00
- commit merge base: [b43c7e1070e515b3e94043ff777ab83074234051](https://github.com/gvanrossum/cpython/commit/b43c7e1070e515b3e94043ff777ab83074234051)
- ref: tier2_flag

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8855851495)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-3.11.0.md)
- [📈time plot](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 98.95%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-base-mem.png)
- [📄table](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-base.md)
- [📈time plot](bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6%2B-8cb71dd-vs-base.png)

