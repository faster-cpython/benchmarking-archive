# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [262fb91](https://github.com/python/cpython/commit/262fb91)
- commit date: 2024-03-27T17:38:19+00:00
- commit merge base: [74c8568d07719529b874897598d8b3bc25ff0434](https://github.com/python/cpython/commit/74c8568d07719529b874897598d8b3bc25ff0434)
- ref: 262fb911ab7df8e890eb

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8474043440)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91-vs-3.10.4.md)
- [📈time plot](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.04x faster (HPT: reliability of 77.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91-vs-3.11.0.md)
- [📈time plot](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 82.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91-vs-3.12.0.md)
- [📈time plot](bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5%2B-262fb91-vs-3.12.0.png)

