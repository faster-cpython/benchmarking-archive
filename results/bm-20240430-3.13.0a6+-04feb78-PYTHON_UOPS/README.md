# Results

- fork: faster-cpython
- version: 3.13.0a6+
- tier 2: True
- jit: False
- commit hash: [04feb78](https://github.com/faster%2dcpython/cpython/commit/04feb78)
- commit date: 2024-04-30T10:12:32+01:00
- commit merge base: [11cbf77f9799e86603bca927a98959c7b94fff80](https://github.com/faster%2dcpython/cpython/commit/11cbf77f9799e86603bca927a98959c7b94fff80)
- ref: unify_tier_2_for_ite

## linux x86_64 (azure)

- [pystats raw](bm-20240430-azure-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-pystats.json)
- [pystats table](bm-20240430-azure-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-pystats.md)

### vs. base

- [pystats diff](bm-20240430-azure-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8892376789)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-3.10.4.md)
- [📈time plot](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-3.11.0.md)
- [📈time plot](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-3.12.0.md)
- [📈time plot](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-base-mem.png)
- [📄table](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-base.md)
- [📈time plot](bm-20240430-linux-x86_64-faster%252dcpython-unify_tier_2_for_ite-3.13.0a6%2B-04feb78-vs-base.png)

