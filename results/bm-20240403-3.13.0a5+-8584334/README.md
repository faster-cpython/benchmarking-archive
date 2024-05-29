# Results

- fork: python
- version: 3.13.0a5+
- config: 
- commit hash: [8584334](https://github.com/python/cpython/commit/8584334)
- commit date: 2024-04-03T20:13:32-07:00
- commit merge base: [b4fe02f595fcb9f78261920a268ef614821ec195](https://github.com/python/cpython/commit/b4fe02f595fcb9f78261920a268ef614821ec195)
- ref: 85843348c5f0b8c2f973

## linux x86_64 (azure)

- [pystats raw](bm-20240403-azure-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-pystats.json)
- [pystats table](bm-20240403-azure-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571916364)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.10.4.md)
- [📈time plot](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.11.0.md)
- [📈time plot](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.12.0.md)
- [📈time plot](bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8576567006)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.10.4.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.11.0.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 87.22%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.12.0.md)
- [📈time plot](bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5%2B-8584334-vs-3.12.0.png)

