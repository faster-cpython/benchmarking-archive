# Results

- fork: python
- version: 3.13.0a5+
- config: 
- commit hash: [e1eeb99](https://github.com/python/cpython/commit/e1eeb99)
- commit date: 2024-04-08T09:51:20+02:00
- commit merge base: [a453f5ef9d0b89bd00488d3814c6f0a2886342b8](https://github.com/python/cpython/commit/a453f5ef9d0b89bd00488d3814c6f0a2886342b8)
- ref: e1eeb990bd169491075e

## linux x86_64 (azure)

- [pystats raw](bm-20240408-azure-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-pystats.json)
- [pystats table](bm-20240408-azure-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8629656478)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.10.4.md)
- [📈time plot](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.11.0.md)
- [📈time plot](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.89%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.12.0.md)
- [📈time plot](bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8635769941)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.10.4.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.97%, 1.02x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.11.0.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x faster (HPT: reliability of 79.82%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.12.0.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5%2B-e1eeb99-vs-3.12.0.png)

