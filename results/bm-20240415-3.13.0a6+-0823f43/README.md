# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [0823f43](https://github.com/python/cpython/commit/0823f43)
- commit date: 2024-04-15T10:08:21-05:00
- commit merge base: [10f1a2687a080f07bc128e185c854586207f08cf](https://github.com/python/cpython/commit/10f1a2687a080f07bc128e185c854586207f08cf)
- ref: 0823f4361850145152a9

## linux x86_64 (azure)

- [pystats raw](bm-20240415-azure-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-pystats.json)
- [pystats table](bm-20240415-azure-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8694420849)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.10.4.md)
- [📈time plot](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.54%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.11.0.md)
- [📈time plot](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.93%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.12.0.md)
- [📈time plot](bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8695202898)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.10.4.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.11.0.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.12.0.md)
- [📈time plot](bm-20240415-pythonperf1-amd64-python-0823f4361850145152a9-3.13.0a6%2B-0823f43-vs-3.12.0.png)

