# Results

- fork: gvanrossum
- version: 3.13.0a5+
- tier 2: False
- jit: False
- commit hash: [dcee362](https://github.com/gvanrossum/cpython/commit/dcee362)
- commit date: 2024-04-03T13:17:19-07:00
- commit merge base: [c43f6a4dfaa1c1974141e2f7014a7f98ca3a3f93](https://github.com/gvanrossum/cpython/commit/c43f6a4dfaa1c1974141e2f7014a7f98ca3a3f93)
- ref: exp_backoff

## linux x86_64 (azure)

- [pystats raw](bm-20240403-azure-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-pystats.json)
- [pystats table](bm-20240403-azure-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-pystats.md)

### vs. base

- [pystats diff](bm-20240403-azure-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8545294214)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.10.4.md)
- [📈time plot](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 98.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.11.0.md)
- [📈time plot](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.12.0.md)
- [📈time plot](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-base-mem.png)
- [📄table](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-base.md)
- [📈time plot](bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-base.png)

