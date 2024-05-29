# Results

- fork: faster-cpython
- version: 3.13.0a5+
- config: 
- commit hash: [e985127](https://github.com/faster%2dcpython/cpython/commit/e985127)
- commit date: 2024-04-10T19:10:27+01:00
- commit merge base: [e1eeb990bd169491075eeaea31481a4a96bdecbb](https://github.com/faster%2dcpython/cpython/commit/e1eeb990bd169491075eeaea31481a4a96bdecbb)
- ref: call_cmethod

## linux x86_64 (azure)

- [pystats raw](bm-20240410-azure-x86_64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-pystats.json)
- [pystats table](bm-20240410-azure-x86_64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-pystats.md)

### vs. base

- [pystats diff](bm-20240410-azure-x86_64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-pystats-vs-base.md)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8635912720)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-vs-3.10.4.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-vs-3.11.0.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-vs-3.12.0.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-faster%252dcpython-call_cmethod-3.13.0a5%2B-e985127-vs-3.12.0.png)

