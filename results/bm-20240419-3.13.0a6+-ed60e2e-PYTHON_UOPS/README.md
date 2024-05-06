# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [ed60e2e](https://github.com/faster%2dcpython/cpython/commit/ed60e2e)
- commit date: 2024-04-19T09:35:25+01:00
- commit merge base: [7e6fa5fceddc3f4721c036116c7a11533c8b23b3](https://github.com/faster%2dcpython/cpython/commit/7e6fa5fceddc3f4721c036116c7a11533c8b23b3)
- ref: move_set_ip_to_exits

## linux x86_64 (azure)

- [pystats raw](bm-20240419-azure-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-pystats.json)
- [pystats table](bm-20240419-azure-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-pystats.md)

### vs. base

- [pystats diff](bm-20240419-azure-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8750858653)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-3.10.4.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-3.11.0.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-3.12.0.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-base-mem.png)
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-base.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-move_set_ip_to_exits-3.13.0a6%2B-ed60e2e-vs-base.png)

