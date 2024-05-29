# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [c43f6a4](https://github.com/python/cpython/commit/c43f6a4)
- commit date: 2024-04-03T18:17:51+00:00
- commit merge base: [1c434688866db79082def4f9ef572b85d85908c8](https://github.com/python/cpython/commit/1c434688866db79082def4f9ef572b85d85908c8)
- ref: c43f6a4dfaa1c1974141

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8545305709)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.10.4.md)
- [📈time plot](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x faster (HPT: reliability of 97.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.11.0.md)
- [📈time plot](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.12.0.md)
- [📈time plot](bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5%2B-c43f6a4-vs-3.12.0.png)

