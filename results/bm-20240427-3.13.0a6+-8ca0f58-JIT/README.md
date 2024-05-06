# Results

- fork: brandtbucher
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [8ca0f58](https://github.com/brandtbucher/cpython/commit/8ca0f58)
- commit date: 2024-04-27T18:18:41-07:00
- commit merge base: [2e7771a03d8975ee8a9918ce754c665508c3f682](https://github.com/brandtbucher/cpython/commit/2e7771a03d8975ee8a9918ce754c665508c3f682)
- ref: justin_refactor

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8864352298)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-3.10.4.md)
- [📈time plot](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 95.34%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-3.11.0.md)
- [📈time plot](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 97.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-3.12.0.md)
- [📈time plot](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-base-mem.png)
- [📄table](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-base.md)
- [📈time plot](bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6%2B-8ca0f58-vs-base.png)

