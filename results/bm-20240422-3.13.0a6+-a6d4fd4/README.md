# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [a6d4fd4](https://github.com/faster%2dcpython/cpython/commit/a6d4fd4)
- commit date: 2024-04-22T11:45:03+01:00
- commit merge base: [550483b7e6c54b2a25d4db0c4ca41bd9c1132f93](https://github.com/faster%2dcpython/cpython/commit/550483b7e6c54b2a25d4db0c4ca41bd9c1132f93)
- ref: tier1_eval_breaker

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8782756259)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.md)
- [📈time plot](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.06x faster (HPT: reliability of 91.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.md)
- [📈time plot](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.12%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.md)
- [📈time plot](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base-mem.png)
- [📄table](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.md)
- [📈time plot](bm-20240422-linux-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8782756259)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.md)
- [📈time plot](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.09x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.md)
- [📈time plot](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 77.89%, 1.00x faster at 99th %ile)
- Memory usage: 0.92x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.md)
- [📈time plot](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base-mem.png)
- [📄table](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.md)
- [📈time plot](bm-20240422-pythonperf2-x86_64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8782756259)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.md)
- [📈time plot](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.md)
- [📈time plot](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.md)
- [📈time plot](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.87%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.md)
- [📈time plot](bm-20240422-pythonperf1-amd64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.png)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8782756259)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4.json)

### vs. 3.10.4

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.md)
- [📈time plot](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- [📄table](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.md)
- [📈time plot](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.md)
- [📈time plot](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.17%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.md)
- [📈time plot](bm-20240422-pythonperf1_win32-x86-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8782756259)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.md)
- [📈time plot](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.02x faster (HPT: reliability of 84.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg
- [📄table](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.md)
- [📈time plot](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.md)
- [📈time plot](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-3.12.0.png)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base-mem.png)
- [📄table](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.md)
- [📈time plot](bm-20240422-darwin-arm64-faster%252dcpython-tier1_eval_breaker-3.13.0a6%2B-a6d4fd4-vs-base.png)

