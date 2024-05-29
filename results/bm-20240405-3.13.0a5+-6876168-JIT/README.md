# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [6876168](https://github.com/python/cpython/commit/6876168)
- commit date: 2024-04-05T16:21:16+02:00
- commit merge base: [abfa16b44bb9426312613893b6e193b02ee0304f](https://github.com/python/cpython/commit/abfa16b44bb9426312613893b6e193b02ee0304f)
- ref: 687616877ba540a44f82

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.md)
- [📈time plot](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 67.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.md)
- [📈time plot](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 84.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.md)
- [📈time plot](bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 93.01%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 99.50%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.md)
- [📈time plot](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x faster (HPT: reliability of 94.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.md)
- [📈time plot](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.md)
- [📈time plot](bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5%2B-6876168-vs-3.12.0.png)

