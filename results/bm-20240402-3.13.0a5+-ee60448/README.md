# Results

- fork: mdboom
- version: 3.13.0a5+
- config: 
- commit hash: [ee60448](https://github.com/mdboom/cpython/commit/ee60448)
- commit date: 2024-04-02T14:25:50-04:00
- commit merge base: [027fa2eccf39ddccdf7b416d16601277a7112054](https://github.com/mdboom/cpython/commit/027fa2eccf39ddccdf7b416d16601277a7112054)
- ref: tier2_pystats_misses

## linux x86_64 (azure)

- [pystats raw](bm-20240402-azure-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-pystats.json)
- [pystats table](bm-20240402-azure-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8529041631)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448.json)

### vs. 3.10.4

- Geometric mean: 1.36x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.10.4.md)
- [📈time plot](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 99.89%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.11.0.md)
- [📈time plot](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.12.0.md)
- [📈time plot](bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.12.0.png)

