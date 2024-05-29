# Results

- fork: Fidget-Spinner
- version: 3.13.0a5+
- config: T2
- commit hash: [577e8e3](https://github.com/Fidget%2dSpinner/cpython/commit/577e8e3)
- commit date: 2024-04-07T02:11:32+08:00
- commit merge base: [62aeb0ee69b06091396398de56dcb755ca3b9dc9](https://github.com/Fidget%2dSpinner/cpython/commit/62aeb0ee69b06091396398de56dcb755ca3b9dc9)
- ref: int_constant_propaga

## linux x86_64 (azure)

- [pystats raw](bm-20240407-azure-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-pystats.json)
- [pystats table](bm-20240407-azure-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-pystats.md)

### vs. base

- [pystats diff](bm-20240407-azure-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8725220170)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3.json)

### vs. 3.10.4

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-3.10.4.md)
- [📈time plot](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-3.11.0.md)
- [📈time plot](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-3.12.0.md)
- [📈time plot](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-base-mem.png)
- [📄table](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-base.md)
- [📈time plot](bm-20240407-linux-x86_64-Fidget%252dSpinner-int_constant_propaga-3.13.0a5%2B-577e8e3-vs-base.png)

