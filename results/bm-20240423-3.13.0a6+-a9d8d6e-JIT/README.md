# Results

- fork: brandtbucher
- version: 3.13.0a6+
- config: JIT
- commit hash: [a9d8d6e](https://github.com/brandtbucher/cpython/commit/a9d8d6e)
- commit date: 2024-04-23T18:19:34-07:00
- commit merge base: [2e7771a03d8975ee8a9918ce754c665508c3f682](https://github.com/brandtbucher/cpython/commit/2e7771a03d8975ee8a9918ce754c665508c3f682)
- ref: justin_ghccc_cache_3

## linux x86_64 (azure)

- [pystats raw](bm-20240423-azure-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-pystats.json)
- [pystats table](bm-20240423-azure-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-pystats.md)

### vs. base

- [pystats diff](bm-20240423-azure-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8811775881)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 98.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 98.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-base-mem.png)
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-base.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6%2B-a9d8d6e-vs-base.png)

