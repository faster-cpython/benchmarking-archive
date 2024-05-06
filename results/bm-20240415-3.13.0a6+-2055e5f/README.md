# Results

- fork: gvanrossum
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [2055e5f](https://github.com/gvanrossum/cpython/commit/2055e5f)
- commit date: 2024-04-15T11:27:16-07:00
- commit merge base: [0823f4361850145152a94e9086bede6a000d8a4a](https://github.com/gvanrossum/cpython/commit/0823f4361850145152a94e9086bede6a000d8a4a)
- ref: disable_tier2

## linux x86_64 (azure)

- [pystats raw](bm-20240415-azure-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-pystats.json)
- [pystats table](bm-20240415-azure-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-pystats.md)

### vs. base

- [pystats diff](bm-20240415-azure-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8694420849)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f.json)

### vs. 3.10.4

- Geometric mean: 1.36x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.10.4.md)
- [📈time plot](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.11.0.md)
- [📈time plot](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.12.0.md)
- [📈time plot](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-base-mem.png)
- [📄table](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-base.md)
- [📈time plot](bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8695202898)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.10.4.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.11.0.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.12.0.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-base.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6%2B-2055e5f-vs-base.png)

