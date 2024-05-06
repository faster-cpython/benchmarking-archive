# Results

- fork: brandtbucher
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [b8620f7](https://github.com/brandtbucher/cpython/commit/b8620f7)
- commit date: 2024-04-23T23:07:18-07:00
- commit merge base: [2e7771a03d8975ee8a9918ce754c665508c3f682](https://github.com/brandtbucher/cpython/commit/2e7771a03d8975ee8a9918ce754c665508c3f682)
- ref: justin_ghccc_cache_1

## linux x86_64 (azure)

- [pystats raw](bm-20240423-azure-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-pystats.json)
- [pystats table](bm-20240423-azure-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-pystats.md)

### vs. base

- [pystats diff](bm-20240423-azure-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8811846663)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 98.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-base-mem.png)
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-base.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6%2B-b8620f7-vs-base.png)

