# Results

- fork: mdboom
- version: 3.13.0a6+
- tier 2: False
- jit: False
- commit hash: [73d6faa](https://github.com/mdboom/cpython/commit/73d6faa)
- commit date: 2024-04-23T15:01:44-04:00
- commit merge base: [258408239a4fe8a14919d81b73a16e2cfa374050](https://github.com/mdboom/cpython/commit/258408239a4fe8a14919d81b73a16e2cfa374050)
- ref: aa_test_apr_2024

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8805805986)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 97.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-3.11.0.md)
- [📈time plot](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-base-mem.png)
- [📄table](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-base.md)
- [📈time plot](bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6%2B-73d6faa-vs-base.png)

