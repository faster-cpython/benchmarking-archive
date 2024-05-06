# Results

- fork: mdboom
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [fa824fe](https://github.com/mdboom/cpython/commit/fa824fe)
- commit date: 2024-05-03T12:44:05-04:00
- commit merge base: [13245027526bf1b21fae6e7ca62ceec2e39fcfb7](https://github.com/mdboom/cpython/commit/13245027526bf1b21fae6e7ca62ceec2e39fcfb7)
- ref: aa_test2

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8942180003)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-3.10.4.md)
- [📈time plot](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.44%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-3.11.0.md)
- [📈time plot](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 75.08%, 1.00x faster at 99th %ile)
- Memory usage: 0.90x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: flaskblogging
- [📄table](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-3.12.0.md)
- [📈time plot](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 94.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-base-mem.png)
- [📄table](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-base.md)
- [📈time plot](bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6%2B-fa824fe-vs-base.png)

