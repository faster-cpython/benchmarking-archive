# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [630df37](https://github.com/python/cpython/commit/630df37)
- commit date: 2024-04-10T18:17:18+01:00
- commit merge base: [6bc0b33a91713ee62fd1860d28b19cb620c45971](https://github.com/python/cpython/commit/6bc0b33a91713ee62fd1860d28b19cb620c45971)
- ref: 630df37116b1c5b38198

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8656172978)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37-vs-3.10.4.md)
- [📈time plot](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.04%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37-vs-3.11.0.md)
- [📈time plot](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37-vs-3.12.0.md)
- [📈time plot](bm-20240410-linux-x86_64-python-630df37116b1c5b38198-3.13.0a6%2B-630df37-vs-3.12.0.png)

