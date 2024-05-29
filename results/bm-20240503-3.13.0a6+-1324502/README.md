# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [1324502](https://github.com/python/cpython/commit/1324502)
- commit date: 2024-05-03T18:00:43+02:00
- commit merge base: [9d67b72a4952766fdba803eb6eadd41dfee29dff](https://github.com/python/cpython/commit/9d67b72a4952766fdba803eb6eadd41dfee29dff)
- ref: 13245027526bf1b21fae

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8942180003)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502-vs-3.10.4.md)
- [📈time plot](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502-vs-3.11.0.md)
- [📈time plot](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 90.11%, 1.00x faster at 99th %ile)
- Memory usage: 0.90x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: flaskblogging
- [📄table](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502-vs-3.12.0.md)
- [📈time plot](bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6%2B-1324502-vs-3.12.0.png)

