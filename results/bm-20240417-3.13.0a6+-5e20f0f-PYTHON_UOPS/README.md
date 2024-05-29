# Results

- fork: gvanrossum
- version: 3.13.0a6+
- config: T2
- commit hash: [5e20f0f](https://github.com/gvanrossum/cpython/commit/5e20f0f)
- commit date: 2024-04-17T10:42:20-07:00
- commit merge base: [acf69e09c66f8473399fabab36b81f56496528a6](https://github.com/gvanrossum/cpython/commit/acf69e09c66f8473399fabab36b81f56496528a6)
- ref: call_stat_inc

## linux x86_64 (azure)

- [pystats raw](bm-20240417-azure-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-pystats.json)
- [pystats table](bm-20240417-azure-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-pystats.md)

### vs. base

- [pystats diff](bm-20240417-azure-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8726738428)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 88.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-3.10.4.md)
- [📈time plot](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.16x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-3.11.0.md)
- [📈time plot](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.20x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-3.12.0.md)
- [📈time plot](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-base-mem.png)
- [📄table](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-base.md)
- [📈time plot](bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-5e20f0f-vs-base.png)

