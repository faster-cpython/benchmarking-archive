# Results

- fork: python
- version: 3.11.0b4
- config: 
- commit hash: [5a7e1e0](https://github.com/python/cpython/commit/5a7e1e0)
- commit date: 2022-07-11T16:25:22+01:00
- ref: 5a7e1e0a92622c605ab2

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0.json)

### vs. 3.10.4

- Geometric mean: 1.36x faster (HPT: reliability of 100.00%, 1.30x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, comprehensions, coverage, create_gc_cycles, dask, djangocms, gc_traversal, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- new benchmarks: mypy
- [📄table](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.md)
- [📈time plot](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, comprehensions, coverage, create_gc_cycles, dask, djangocms, gc_traversal, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- new benchmarks: mypy
- [📄table](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.md)
- [📈time plot](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 0.95x
- missing benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, comprehensions, coverage, create_gc_cycles, dask, gc_traversal, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, mypy, pylint, thrift
- [📄table](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.md)
- [📈time plot](bm-20220711-linux-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513536147)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: asyncio_tcp_ssl, asyncio_websockets, coverage, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- [📄table](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.md)
- [📈time plot](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.00x faster (HPT: reliability of 97.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp_ssl, asyncio_websockets, coverage, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- [📄table](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.md)
- [📈time plot](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 99.92%, 1.01x slower at 99th %ile)
- Memory usage: 0.90x
- missing benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp_ssl, asyncio_websockets, coverage, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.md)
- [📈time plot](bm-20220711-pythonperf2-x86_64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411326)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: asyncio_tcp_ssl, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- [📄table](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.md)
- [📈time plot](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp_ssl, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- [📄table](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.md)
- [📈time plot](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.04x slower (HPT: reliability of 99.91%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp_ssl, mypy2, richards_super, tomli_loads, typing_runtime_protocols
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.md)
- [📈time plot](bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/6961753569)
- cpu model: missing
- platform: macOS-14.1.1-arm64-arm-64bit
- [raw results](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: mypy2
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.md)
- [📈time plot](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.10.4.png)

### vs. 3.11.0

- Geometric mean: 1.01x slower (HPT: reliability of 57.18%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: mypy2
- [📄table](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.md)
- [📈time plot](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.11.0.png)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 99.73%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: mypy2
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.md)
- [📈time plot](bm-20220711-darwin-arm64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0-vs-3.12.0.png)

