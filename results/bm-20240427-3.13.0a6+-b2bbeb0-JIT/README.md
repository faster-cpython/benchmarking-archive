# Results

- fork: savannahostrowski
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [b2bbeb0](https://github.com/savannahostrowski/cpython/commit/b2bbeb0)
- commit date: 2024-04-27T11:36:18-07:00
- commit merge base: [51aefc5bf907ddffaaf083ded0de773adcdf08c8](https://github.com/savannahostrowski/cpython/commit/51aefc5bf907ddffaaf083ded0de773adcdf08c8)
- ref: llvm_18

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0-vs-3.10.4.md)
- [📈time plot](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 75.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0-vs-3.11.0.md)
- [📈time plot](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0-vs-3.12.0.md)
- [📈time plot](bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6%2B-b2bbeb0-vs-3.12.0.png)

