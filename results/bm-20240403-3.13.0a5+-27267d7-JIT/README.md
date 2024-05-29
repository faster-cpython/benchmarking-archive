# Results

- fork: mdboom
- version: 3.13.0a5+
- config: JIT
- commit hash: [27267d7](https://github.com/mdboom/cpython/commit/27267d7)
- commit date: 2024-04-03T15:12:18-04:00
- commit merge base: [d9cfe7e565a6e2dc15747a904736264e31a10be4](https://github.com/mdboom/cpython/commit/d9cfe7e565a6e2dc15747a904736264e31a10be4)
- ref: tier2_funcs

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8544252560)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-3.10.4.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 69.46%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-3.11.0.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-3.12.0.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 91.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 unpack_sequence
- [🧠memory plot](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-base-mem.png)
- [📄table](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-base.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5%2B-27267d7-vs-base.png)

