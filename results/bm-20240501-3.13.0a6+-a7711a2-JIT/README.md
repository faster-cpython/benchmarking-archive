# Results

- fork: python
- version: 3.13.0a6+
- tier 2: False
- jit: True
- commit hash: [a7711a2](https://github.com/python/cpython/commit/a7711a2)
- commit date: 2024-05-01T22:44:55+01:00
- commit merge base: [424438b11ec90110054f720bfa6ea67d644cc2ec](https://github.com/python/cpython/commit/424438b11ec90110054f720bfa6ea67d644cc2ec)
- ref: main

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8915475261)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2-vs-3.10.4.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x slower (HPT: reliability of 97.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2-vs-3.11.0.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2-vs-3.12.0.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-main-3.13.0a6%2B-a7711a2-vs-3.12.0.png)

