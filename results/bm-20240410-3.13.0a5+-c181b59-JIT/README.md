# Results

- fork: mdboom
- version: 3.13.0a5+
- tier 2: False
- jit: True
- commit hash: [c181b59](https://github.com/mdboom/cpython/commit/c181b59)
- commit date: 2024-04-10T11:29:00-04:00
- commit merge base: [687616877ba540a44f82ff764b5f13d36c0f3910](https://github.com/mdboom/cpython/commit/687616877ba540a44f82ff764b5f13d36c0f3910)
- ref: tier2_func_simple_fr

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8633884683)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.md)
- [📈time plot](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 50.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.md)
- [📈time plot](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 84.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.md)
- [📈time plot](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 99.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base-mem.png)
- [📄table](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.md)
- [📈time plot](bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8633884683)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 85.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 99.70%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base-mem.png)
- [📄table](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8633884683)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 95.97%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.md)
- [📈time plot](bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8633884683)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.md)
- [📈time plot](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.md)
- [📈time plot](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.md)
- [📈time plot](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.md)
- [📈time plot](bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8633884683)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.md)
- [📈time plot](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x faster (HPT: reliability of 97.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.md)
- [📈time plot](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.md)
- [📈time plot](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base-mem.png)
- [📄table](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.md)
- [📈time plot](bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5%2B-c181b59-vs-base.png)

