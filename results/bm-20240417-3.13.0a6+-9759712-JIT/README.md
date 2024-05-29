# Results

- fork: brandtbucher
- version: 3.13.0a6+
- config: JIT
- commit hash: [9759712](https://github.com/brandtbucher/cpython/commit/9759712)
- commit date: 2024-04-17T16:51:34-07:00
- commit merge base: [241ed5f2cdd525de0e136d0e3ce70d5487721c10](https://github.com/brandtbucher/cpython/commit/241ed5f2cdd525de0e136d0e3ce70d5487721c10)
- ref: justin_ghccc_cache

## linux x86_64 (azure)

- [pystats raw](bm-20240417-azure-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-pystats.json)
- [pystats table](bm-20240417-azure-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-pystats.md)

### vs. base

- [pystats diff](bm-20240417-azure-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8730374393)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-3.10.4.md)
- [📈time plot](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 98.70%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-3.11.0.md)
- [📈time plot](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 97.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-3.12.0.md)
- [📈time plot](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-base-mem.png)
- [📄table](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-base.md)
- [📈time plot](bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6%2B-9759712-vs-base.png)

