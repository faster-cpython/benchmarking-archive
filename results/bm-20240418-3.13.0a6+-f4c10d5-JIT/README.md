# Results

- fork: brandtbucher
- version: 3.13.0a6+
- config: JIT
- commit hash: [f4c10d5](https://github.com/brandtbucher/cpython/commit/f4c10d5)
- commit date: 2024-04-18T10:48:35-07:00
- commit merge base: [241ed5f2cdd525de0e136d0e3ce70d5487721c10](https://github.com/brandtbucher/cpython/commit/241ed5f2cdd525de0e136d0e3ce70d5487721c10)
- ref: justin_cache

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8743424050)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-3.10.4.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 57.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-3.11.0.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 78.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-3.12.0.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-base-mem.png)
- [📄table](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-base.md)
- [📈time plot](bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6%2B-f4c10d5-vs-base.png)

