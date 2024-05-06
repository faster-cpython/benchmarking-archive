# Results

- fork: brandtbucher
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [6e8e3d5](https://github.com/brandtbucher/cpython/commit/6e8e3d5)
- commit date: 2024-05-02T15:03:30-07:00
- commit merge base: [c408c36e9b346f9f15a34e98a5596f311df65efa](https://github.com/brandtbucher/cpython/commit/c408c36e9b346f9f15a34e98a5596f311df65efa)
- ref: justin_trampolines

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8931584972)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.10.4.md)
- [📈time plot](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x slower (HPT: reliability of 97.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.11.0.md)
- [📈time plot](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.12.0.md)
- [📈time plot](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 97.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-base-mem.png)
- [📄table](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-base.md)
- [📈time plot](bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8931577407)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.10.4.md)
- [📈time plot](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 61.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.11.0.md)
- [📈time plot](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.12.0.md)
- [📈time plot](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-base-mem.png)
- [📄table](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-base.md)
- [📈time plot](bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6%2B-6e8e3d5-vs-base.png)

