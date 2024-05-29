# Results

- fork: brandtbucher
- version: 3.13.0a6+
- config: JIT
- commit hash: [377ec17](https://github.com/brandtbucher/cpython/commit/377ec17)
- commit date: 2024-04-18T14:01:54-07:00
- commit merge base: [241ed5f2cdd525de0e136d0e3ce70d5487721c10](https://github.com/brandtbucher/cpython/commit/241ed5f2cdd525de0e136d0e3ce70d5487721c10)
- ref: justin_preserve_most

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8744926869)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-3.10.4.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 75.15%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-3.11.0.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 91.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-3.12.0.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 99.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-base-mem.png)
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-base.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6%2B-377ec17-vs-base.png)

