# Results

- fork: Fidget-Spinner
- version: 3.13.0a6+
- config: 
- commit hash: [d59145b](https://github.com/Fidget%2dSpinner/cpython/commit/d59145b)
- commit date: 2024-04-26T20:35:27+08:00
- commit merge base: [5da0280648b5f1c5142dad39dcd1e7fd99fdf37a](https://github.com/Fidget%2dSpinner/cpython/commit/5da0280648b5f1c5142dad39dcd1e7fd99fdf37a)
- ref: tagged_evaluation_st

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8851394403)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.68%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-3.11.0.md)
- [📈time plot](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-base-mem.png)
- [📄table](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-base.md)
- [📈time plot](bm-20240426-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a6%2B-d59145b-vs-base.png)

