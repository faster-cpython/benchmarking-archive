# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [9654daf](https://github.com/python/cpython/commit/9654daf)
- commit date: 2024-03-26T13:26:45+02:00
- commit merge base: [8bef34f625e21886b1c64544c060e19ee2e229bf](https://github.com/python/cpython/commit/8bef34f625e21886b1c64544c060e19ee2e229bf)
- ref: 9654daf793b534b44a83

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8738548223)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf-vs-3.10.4.md)
- [📈time plot](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 65.47%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf-vs-3.11.0.md)
- [📈time plot](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 71.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf-vs-3.12.0.md)
- [📈time plot](bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5%2B-9654daf-vs-3.12.0.png)

