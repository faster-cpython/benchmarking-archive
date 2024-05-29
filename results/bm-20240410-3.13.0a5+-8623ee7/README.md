# Results

- fork: faster-cpython
- version: 3.13.0a5+
- config: 
- commit hash: [8623ee7](https://github.com/faster%2dcpython/cpython/commit/8623ee7)
- commit date: 2024-04-10T12:34:30+01:00
- commit merge base: [e1eeb990bd169491075eeaea31481a4a96bdecbb](https://github.com/faster%2dcpython/cpython/commit/e1eeb990bd169491075eeaea31481a4a96bdecbb)
- ref: call_complex_paramet

## linux x86_64 (azure)

- [pystats raw](bm-20240410-azure-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-pystats.json)
- [pystats table](bm-20240410-azure-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-pystats.md)

### vs. base

- [pystats diff](bm-20240410-azure-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-pystats-vs-base.md)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8630568784)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-3.10.4.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-3.11.0.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.00x slower (HPT: reliability of 66.29%, 1.00x slower at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-3.12.0.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-base-mem.png)
- [📄table](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-base.md)
- [📈time plot](bm-20240410-pythonperf2-x86_64-faster%252dcpython-call_complex_paramet-3.13.0a5%2B-8623ee7-vs-base.png)

