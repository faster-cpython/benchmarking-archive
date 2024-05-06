# Results

- fork: python
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [c179c0e](https://github.com/python/cpython/commit/c179c0e)
- commit date: 2024-04-17T16:42:04+01:00
- commit merge base: [ae8dfd2761e4a45afe0adada0f91f371dd121bb8](https://github.com/python/cpython/commit/ae8dfd2761e4a45afe0adada0f91f371dd121bb8)
- ref: main

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8725123884)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e.json)

### vs. 3.10.4

- Geometric mean: 1.09x faster (HPT: reliability of 96.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e-vs-3.10.4.md)
- [📈time plot](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.11x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e-vs-3.11.0.md)
- [📈time plot](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.08x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e-vs-3.12.0.md)
- [📈time plot](bm-20240417-darwin-arm64-python-main-3.13.0a6%2B-c179c0e-vs-3.12.0.png)

