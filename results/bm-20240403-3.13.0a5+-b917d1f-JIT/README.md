# Results

- fork: mdboom
- version: 3.13.0a5+
- tier 2: False
- jit: True
- commit hash: [b917d1f](https://github.com/mdboom/cpython/commit/b917d1f)
- commit date: 2024-04-03T20:31:44-04:00
- commit merge base: [d9cfe7e565a6e2dc15747a904736264e31a10be4](https://github.com/mdboom/cpython/commit/d9cfe7e565a6e2dc15747a904736264e31a10be4)
- ref: tier2_funcs

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8547383823)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f-vs-3.10.4.md)
- [📈time plot](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 69.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f-vs-3.11.0.md)
- [📈time plot](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 73.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f-vs-3.12.0.md)
- [📈time plot](bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-b917d1f-vs-3.12.0.png)

