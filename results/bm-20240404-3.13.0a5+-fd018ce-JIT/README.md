# Results

- fork: mdboom
- version: 3.13.0a5+
- config: JIT
- commit hash: [fd018ce](https://github.com/mdboom/cpython/commit/fd018ce)
- commit date: 2024-04-04T09:48:17-04:00
- commit merge base: [d9cfe7e565a6e2dc15747a904736264e31a10be4](https://github.com/mdboom/cpython/commit/d9cfe7e565a6e2dc15747a904736264e31a10be4)
- ref: all_above_350

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8556443564)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 68.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-3.11.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.97%, 1.01x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 91.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 unpack_sequence
- [🧠memory plot](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-base-mem.png)
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-base.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5%2B-fd018ce-vs-base.png)

