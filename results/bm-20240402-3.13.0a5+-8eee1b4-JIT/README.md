# Results

- fork: gvanrossum
- version: 3.13.0a5+
- config: JIT
- commit hash: [8eee1b4](https://github.com/gvanrossum/cpython/commit/8eee1b4)
- commit date: 2024-04-02T07:39:39-07:00
- commit merge base: [e569f9132b5bdc1c103116a020e19e3ccc20cf34](https://github.com/gvanrossum/cpython/commit/e569f9132b5bdc1c103116a020e19e3ccc20cf34)
- ref: exp_backoff

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8525964938)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-3.10.4.md)
- [📈time plot](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 81.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-3.11.0.md)
- [📈time plot](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 80.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-3.12.0.md)
- [📈time plot](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 66.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-base-mem.png)
- [📄table](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-base.md)
- [📈time plot](bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-8eee1b4-vs-base.png)

