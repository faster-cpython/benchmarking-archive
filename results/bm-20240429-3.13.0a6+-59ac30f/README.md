# Results

- fork: nineteendo
- version: 3.13.0a6+
- config: 
- commit hash: [59ac30f](https://github.com/nineteendo/cpython/commit/59ac30f)
- commit date: 2024-04-29T10:01:01+02:00
- commit merge base: [c7e7bfc4ca26bf90e0d4959e303770fbfc3a3795](https://github.com/nineteendo/cpython/commit/c7e7bfc4ca26bf90e0d4959e303770fbfc3a3795)
- ref: use_PyTuple_Pack

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8878741589)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-3.10.4.md)
- [📈time plot](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-3.11.0.md)
- [📈time plot](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-3.12.0.md)
- [📈time plot](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 85.04%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-base-mem.png)
- [📄table](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-base.md)
- [📈time plot](bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6%2B-59ac30f-vs-base.png)

