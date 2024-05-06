# Results

- fork: gvanrossum
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [ced0ca9](https://github.com/gvanrossum/cpython/commit/ced0ca9)
- commit date: 2024-04-16T14:58:21-07:00
- commit merge base: [0823f4361850145152a94e9086bede6a000d8a4a](https://github.com/gvanrossum/cpython/commit/0823f4361850145152a94e9086bede6a000d8a4a)
- ref: disable_tier2

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8713200504)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-3.10.4.md)
- [📈time plot](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-3.11.0.md)
- [📈time plot](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-3.12.0.md)
- [📈time plot](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 95.09%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-base.md)
- [📈time plot](bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-ced0ca9-vs-base.png)

