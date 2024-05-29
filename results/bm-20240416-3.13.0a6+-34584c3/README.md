# Results

- fork: gvanrossum
- version: 3.13.0a6+
- config: 
- commit hash: [34584c3](https://github.com/gvanrossum/cpython/commit/34584c3)
- commit date: 2024-04-16T14:34:48-07:00
- commit merge base: [acf69e09c66f8473399fabab36b81f56496528a6](https://github.com/gvanrossum/cpython/commit/acf69e09c66f8473399fabab36b81f56496528a6)
- ref: call_stat_inc

## linux x86_64 (azure)

- [pystats raw](bm-20240416-azure-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-pystats.json)
- [pystats table](bm-20240416-azure-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-pystats.md)

### vs. base

- [pystats diff](bm-20240416-azure-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8713010520)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-3.10.4.md)
- [📈time plot](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-3.11.0.md)
- [📈time plot](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-3.12.0.md)
- [📈time plot](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 96.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-base-mem.png)
- [📄table](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-base.md)
- [📈time plot](bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6%2B-34584c3-vs-base.png)

