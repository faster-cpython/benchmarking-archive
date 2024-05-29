# Results

- fork: faster-cpython
- version: 3.13.0a3+
- config: T2
- commit hash: [7b9e10f](https://github.com/faster%2dcpython/cpython/commit/7b9e10f)
- commit date: 2024-02-08T14:11:09+00:00
- commit merge base: [17689e3c41d9f61bcd1928b24d3c50c37ceaf3f2](https://github.com/faster%2dcpython/cpython/commit/17689e3c41d9f61bcd1928b24d3c50c37ceaf3f2)
- ref: watched_dict_stats

## linux x86_64 (azure)

- [pystats raw](bm-20240208-azure-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-pystats.json)
- [pystats table](bm-20240208-azure-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-pystats.md)

### vs. base

- [pystats diff](bm-20240208-azure-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/7830914848)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f.json)

### vs. 3.10.4

- Geometric mean: 1.29x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: aiohttp, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-3.10.4.md)
- [📈time plot](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 84.73%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, django_template, djangocms, flaskblogging, genshi_text, genshi_xml, gunicorn, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
- [📄table](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-3.11.0.md)
- [📈time plot](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 99.37%, 1.00x slower at 99th %ile)
- Memory usage: 0.93x
- missing benchmarks: aiohttp, django_template, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-3.12.0.md)
- [📈time plot](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 97.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-base-mem.png)
- [📄table](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-base.md)
- [📈time plot](bm-20240208-linux-x86_64-faster%252dcpython-watched_dict_stats-3.13.0a3%2B-7b9e10f-vs-base.png)

