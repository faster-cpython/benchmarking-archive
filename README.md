# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

**Key:** 📄: table, 📈: time plot, 🧠: memory plot

<!-- START table -->
[Most recent pystats on main (ec9d12b)](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-azure-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-pystats.md)

## linux aarch64 (arminc)
| date | fork/ref | hash/flags | vs. 3.10.4: | vs. 3.11.0: | vs. 3.12.0: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| [2024-05-08](results/bm-20240508-3.13.0b1-2268289) | python/v3.13.0b1 | 2268289 | 1.24x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.png) | 1.01x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.png) | 1.03x ↓<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.png) |  |
| [2024-05-07](results/bm-20240507-3.13.0a6%2B-9762122) | python/976212223541b89329d8 | 9762122 | 1.24x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-arminc-aarch64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-arminc-aarch64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-arminc-aarch64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-arminc-aarch64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.png) | 1.02x ↓<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-arminc-aarch64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-arminc-aarch64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.png) |  |
| [2024-05-04](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS) | python/999f0c512281995fb61a | 999f0c5 ️(T2) | 1.15x ↑<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.png) | 1.06x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.png) | 1.10x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.png) | 1.11x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.png)[🧠](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-arminc-aarch64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base-mem.png) |
| [2024-03-12](results/bm-20240312-3.13.0a5-076d169) | python/v3.13.0a5 | 076d169 | 1.29x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.png) | 1.05x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.png) | 1.01x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.png) |  |
| [2024-02-15](results/bm-20240215-3.13.0a4-9d34f60) | python/v3.13.0a4 | 9d34f60 | 1.29x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png) | 1.05x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png) | 1.01x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png) |  |

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.10.4: | vs. 3.11.0: | vs. 3.12.0: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| [2024-05-11](results/bm-20240511-3.14.0a0-144a6fa) | Fidget-Spinner/stackref_all | 144a6fa | 1.23x ↑<br>[📄](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-3.10.4.md)[📈](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-3.10.4.png) | 1.02x ↓<br>[📄](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-3.11.0.md)[📈](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-3.11.0.png) | 1.06x ↓<br>[📄](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-3.12.0.md)[📈](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-3.12.0.png) | 1.05x ↓<br>[📄](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-base.md)[📈](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-base.png)[🧠](results/bm-20240511-3.14.0a0-144a6fa/bm-20240511-linux-x86_64-Fidget%252dSpinner-stackref_all-3.14.0a0-144a6fa-vs-base-mem.png) |
| [2024-05-10](results/bm-20240510-3.14.0a0-ec9d12b) | python/ec9d12be9648ee60a2eb | ec9d12b | 1.29x ↑<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.10.4.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.11.0.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.11.0.png) | 1.00x ↓<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.12.0.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.12.0.png) |  |
| [2024-05-10](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL) | python/main | ec9d12b (NOGIL) | 1.17x ↓<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-3.10.4.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-3.10.4.png) | 1.44x ↓<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-3.11.0.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-3.11.0.png) | 1.45x ↓<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-3.12.0.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-3.12.0.png) | 1.49x ↓<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-base.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-base.png)[🧠](results/bm-20240510-3.14.0a0-ec9d12b-NOGIL/bm-20240510-linux-x86_64-python-main-3.14.0a0-ec9d12b-vs-base-mem.png) |
| [2024-05-10](results/bm-20240510-3.14.0a0-ec9d12b-JIT) | python/ec9d12be9648ee60a2eb | ec9d12b (JIT) | 1.29x ↑<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.10.4.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.11.0.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.11.0.png) | 1.00x ↑<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.12.0.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-3.12.0.png) | 1.00x ↑<br>[📄](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-base.md)[📈](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-base.png)[🧠](results/bm-20240510-3.14.0a0-ec9d12b-JIT/bm-20240510-linux-x86_64-python-ec9d12be9648ee60a2eb-3.14.0a0-ec9d12b-vs-base-mem.png) |
| [2024-05-10](results/bm-20240510-3.14.0a0-1973514) | faster-cpython/test_perf_jit | 1973514 | 1.29x ↑<br>[📄](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-3.10.4.md)[📈](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-3.11.0.md)[📈](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-3.11.0.png) | 1.00x ↓<br>[📄](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-3.12.0.md)[📈](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-3.12.0.png) | 1.01x ↓<br>[📄](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-base.md)[📈](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-base.png)[🧠](results/bm-20240510-3.14.0a0-1973514/bm-20240510-linux-x86_64-faster%252dcpython-test_perf_jit-3.14.0a0-1973514-vs-base-mem.png) |
| [2024-05-10](results/bm-20240510-3.14.0a0-ee3b5e3-JIT) | brandtbucher/peel | ee3b5e3 (JIT) | 1.29x ↑<br>[📄](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-3.10.4.md)[📈](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-3.11.0.md)[📈](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-3.11.0.png) | 1.00x ↑<br>[📄](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-3.12.0.md)[📈](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-3.12.0.png) | 1.00x ↓<br>[📄](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-base.md)[📈](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-base.png)[🧠](results/bm-20240510-3.14.0a0-ee3b5e3-JIT/bm-20240510-linux-x86_64-brandtbucher-peel-3.14.0a0-ee3b5e3-vs-base-mem.png) |
| [2024-05-09](results/bm-20240509-3.14.0a0-1ce3b25-JIT) | brandtbucher/hoist_partial | 1ce3b25 (JIT) | 1.28x ↑<br>[📄](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-3.10.4.md)[📈](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-3.11.0.md)[📈](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-3.11.0.png) | 1.00x ↓<br>[📄](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-3.12.0.md)[📈](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-3.12.0.png) | 1.00x ↑<br>[📄](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-base.md)[📈](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-base.png)[🧠](results/bm-20240509-3.14.0a0-1ce3b25-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist_partial-3.14.0a0-1ce3b25-vs-base-mem.png) |
| [2024-05-09](results/bm-20240509-3.14.0a0-35b5eaa) | python/35b5eaa176a5bae8a0ca | 35b5eaa | 1.30x ↑<br>[📄](results/bm-20240509-3.14.0a0-35b5eaa/bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa-vs-3.10.4.md)[📈](results/bm-20240509-3.14.0a0-35b5eaa/bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240509-3.14.0a0-35b5eaa/bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa-vs-3.11.0.md)[📈](results/bm-20240509-3.14.0a0-35b5eaa/bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa-vs-3.11.0.png) | 1.00x ↑<br>[📄](results/bm-20240509-3.14.0a0-35b5eaa/bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa-vs-3.12.0.md)[📈](results/bm-20240509-3.14.0a0-35b5eaa/bm-20240509-linux-x86_64-python-35b5eaa176a5bae8a0ca-3.14.0a0-35b5eaa-vs-3.12.0.png) |  |
| [2024-05-09](results/bm-20240509-3.14.0a0-5e272c0-JIT) | brandtbucher/hoist | 5e272c0 (JIT) | 1.29x ↑<br>[📄](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-3.10.4.md)[📈](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-3.11.0.md)[📈](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-3.11.0.png) | 1.00x ↓<br>[📄](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-3.12.0.md)[📈](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-3.12.0.png) | 1.00x ↑<br>[📄](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-base.md)[📈](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-base.png)[🧠](results/bm-20240509-3.14.0a0-5e272c0-JIT/bm-20240509-linux-x86_64-brandtbucher-hoist-3.14.0a0-5e272c0-vs-base-mem.png) |
| [2024-05-08](results/bm-20240508-3.14.0a0-bc99ede-JIT) | brandtbucher/hoist | bc99ede (JIT) | 1.29x ↑<br>[📄](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-3.10.4.md)[📈](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-3.11.0.md)[📈](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-3.11.0.png) | 1.00x ↓<br>[📄](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-3.12.0.md)[📈](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-3.12.0.png) | 1.01x ↑<br>[📄](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-base.md)[📈](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-base.png)[🧠](results/bm-20240508-3.14.0a0-bc99ede-JIT/bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede-vs-base-mem.png) |
| [2024-05-08](results/bm-20240508-3.14.0a0-0cc257c-JIT) | brandtbucher/justin_recompile | 0cc257c (JIT) | 1.24x ↑<br>[📄](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-3.10.4.md)[📈](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-3.10.4.png) | 1.02x ↓<br>[📄](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-3.11.0.md)[📈](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-3.11.0.png) | 1.05x ↓<br>[📄](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-3.12.0.md)[📈](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-3.12.0.png) | 1.04x ↓<br>[📄](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-base.md)[📈](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-base.png)[🧠](results/bm-20240508-3.14.0a0-0cc257c-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_recompile-3.14.0a0-0cc257c-vs-base-mem.png) |
| [2024-05-08](results/bm-20240508-3.14.0a0-7b0c247-JIT) | python/7b0c247f1c176e092777 | 7b0c247 (JIT) | 1.28x ↑<br>[📄](results/bm-20240508-3.14.0a0-7b0c247-JIT/bm-20240508-linux-x86_64-python-7b0c247f1c176e092777-3.14.0a0-7b0c247-vs-3.10.4.md)[📈](results/bm-20240508-3.14.0a0-7b0c247-JIT/bm-20240508-linux-x86_64-python-7b0c247f1c176e092777-3.14.0a0-7b0c247-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240508-3.14.0a0-7b0c247-JIT/bm-20240508-linux-x86_64-python-7b0c247f1c176e092777-3.14.0a0-7b0c247-vs-3.11.0.md)[📈](results/bm-20240508-3.14.0a0-7b0c247-JIT/bm-20240508-linux-x86_64-python-7b0c247f1c176e092777-3.14.0a0-7b0c247-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240508-3.14.0a0-7b0c247-JIT/bm-20240508-linux-x86_64-python-7b0c247f1c176e092777-3.14.0a0-7b0c247-vs-3.12.0.md)[📈](results/bm-20240508-3.14.0a0-7b0c247-JIT/bm-20240508-linux-x86_64-python-7b0c247f1c176e092777-3.14.0a0-7b0c247-vs-3.12.0.png) |  |
| [2024-05-08](results/bm-20240508-3.14.0a0-e63d148-JIT) | brandtbucher/justin_invalidate | e63d148 (JIT) | 1.27x ↑<br>[📄](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-3.10.4.md)[📈](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-3.10.4.png) | 1.01x ↑<br>[📄](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-3.11.0.md)[📈](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-3.12.0.md)[📈](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-3.12.0.png) | 1.01x ↓<br>[📄](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-base.md)[📈](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-base.png)[🧠](results/bm-20240508-3.14.0a0-e63d148-JIT/bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148-vs-base-mem.png) |
| [2024-05-08](results/bm-20240508-3.13.0b1-2268289) | python/v3.13.0b1 | 2268289 | 1.28x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.png) |  |
| [2024-05-07](results/bm-20240507-3.13.0a6%2B-9762122) | python/976212223541b89329d8 | 9762122 | 1.28x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-linux-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-linux-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-linux-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-linux-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-linux-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-linux-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.png) |  |
| [2024-01-17](results/bm-20240117-3.13.0a3-f009305-NOGIL) | python/v3.13.0a3 | f009305 (NOGIL) | 1.15x ↑<br>[📄](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.md)[📈](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.10.4.png) | 1.11x ↓<br>[📄](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.md)[📈](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.11.0.png) | 1.11x ↓<br>[📄](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.md)[📈](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-3.12.0.png) | 1.16x ↓<br>[📄](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-base.md)[📈](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-base.png)[🧠](results/bm-20240117-3.13.0a3-f009305-NOGIL/bm-20240117-linux-x86_64-python-v3.13.0a3-3.13.0a3-f009305-vs-base-mem.png) |
| [2023-11-22](results/bm-20231122-3.13.0a2-9c4347e-NOGIL) | python/v3.13.0a2 | 9c4347e (NOGIL) | 1.09x ↑<br>[📄](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-3.10.4.md)[📈](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-3.10.4.png) | 1.17x ↓<br>[📄](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-3.11.0.md)[📈](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-3.11.0.png) | 1.18x ↓<br>[📄](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-3.12.0.md)[📈](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-3.12.0.png) | 1.21x ↓<br>[📄](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-base.md)[📈](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-base.png)[🧠](results/bm-20231122-3.13.0a2-9c4347e-NOGIL/bm-20231122-linux-x86_64-python-v3.13.0a2-3.13.0a2-9c4347e-vs-base-mem.png) |
| [2023-10-13](results/bm-20231013-3.13.0a1-ad056f0-NOGIL) | python/v3.13.0a1 | ad056f0 (NOGIL) | 1.24x ↑<br>[📄](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-3.10.4.md)[📈](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-3.10.4.png) | 1.02x ↓<br>[📄](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-3.11.0.md)[📈](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-3.11.0.png) | 1.02x ↓<br>[📄](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-3.12.0.md)[📈](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-3.12.0.png) | 1.04x ↓<br>[📄](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-base.md)[📈](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-base.png)[🧠](results/bm-20231013-3.13.0a1-ad056f0-NOGIL/bm-20231013-linux-x86_64-python-v3.13.0a1-3.13.0a1-ad056f0-vs-base-mem.png) |

## linux x86_64 (pythonperf2)
| date | fork/ref | hash/flags | vs. 3.10.4: | vs. 3.11.0: | vs. 3.12.0: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| [2024-05-08](results/bm-20240508-3.13.0b1-2268289) | python/v3.13.0b1 | 2268289 | 1.23x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.png) | 1.04x ↓<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.png) |  |
| [2024-05-07](results/bm-20240507-3.13.0a6%2B-9762122) | python/976212223541b89329d8 | 9762122 | 1.24x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf2-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf2-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.png) | 1.04x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf2-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf2-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.png) | 1.04x ↓<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf2-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf2-x86_64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.png) |  |
| [2024-05-04](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS) | python/999f0c512281995fb61a | 999f0c5 ️(T2) | 1.08x ↑<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.png) | 1.10x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.png) | 1.18x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.png) | 1.17x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.png)[🧠](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf2-x86_64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base-mem.png) |
| [2024-03-12](results/bm-20240312-3.13.0a5-076d169) | python/v3.13.0a5 | 076d169 | 1.28x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.png) | 1.06x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.png) |  |
| [2024-02-15](results/bm-20240215-3.13.0a4-9d34f60) | python/v3.13.0a4 | 9d34f60 | 1.28x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png) | 1.06x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png) |  |

## windows amd64 (pythonperf1)
| date | fork/ref | hash/flags | vs. 3.10.4: | vs. 3.11.0: | vs. 3.12.0: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| [2024-05-08](results/bm-20240508-3.13.0b1-2268289) | python/v3.13.0b1 | 2268289 | 1.23x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.png) | 1.10x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.png) | 1.07x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.png) |  |
| [2024-05-07](results/bm-20240507-3.13.0a6%2B-9762122) | python/976212223541b89329d8 | 9762122 | 1.22x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf1-amd64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf1-amd64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.png) | 1.10x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf1-amd64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf1-amd64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.png) | 1.07x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf1-amd64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-pythonperf1-amd64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.png) |  |
| [2024-05-04](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS) | python/999f0c512281995fb61a | 999f0c5 ️(T2) | 1.10x ↑<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.png) | 1.01x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.png) | 1.03x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.png) | 1.11x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-pythonperf1-amd64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.png) |
| [2024-03-12](results/bm-20240312-3.13.0a5-076d169) | python/v3.13.0a5 | 076d169 | 1.21x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.png) | 1.08x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.png) | 1.05x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.png) |  |
| [2024-02-15](results/bm-20240215-3.13.0a4-9d34f60) | python/v3.13.0a4 | 9d34f60 | 1.20x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png) | 1.07x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png) | 1.04x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png) |  |

## windows x86 (pythonperf1_win32)
| date | fork/ref | hash/flags | vs. 3.10.4: | vs. 3.11.0: | vs. 3.12.0: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| [2024-04-27](results/bm-20240427-3.13.0a6%2B-51aefc5) | python/51aefc5bf907ddffaaf0 | 51aefc5 | 1.16x ↑<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png) | 1.27x ↑<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png) | 1.20x ↑<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png) |  |
| [2024-04-27](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS) | python/51aefc5bf907ddffaaf0 | 51aefc5 ️(T2) | 1.08x ↑<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.png) | 1.19x ↑<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.11.0.png) | 1.12x ↑<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.png) | 1.07x ↓<br>[📄](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.md)[📈](results/bm-20240427-3.13.0a6%2B-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-base.png) |
| [2024-04-26](results/bm-20240426-3.13.0a6%2B-65aa34a) | faster-cpython/tier_2_call | 65aa34a | 1.15x ↑<br>[📄](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.md)[📈](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.10.4.png) | 1.26x ↑<br>[📄](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.md)[📈](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.11.0.png) | 1.19x ↑<br>[📄](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.md)[📈](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-3.12.0.png) | 1.00x ↓<br>[📄](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.md)[📈](results/bm-20240426-3.13.0a6%2B-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%252dcpython-tier_2_call-3.13.0a6%2B-65aa34a-vs-base.png) |
| [2024-03-12](results/bm-20240312-3.13.0a5-076d169) | python/v3.13.0a5 | 076d169 | 1.18x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.png) | 1.28x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.png) | 1.21x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.png) |  |
| [2024-02-15](results/bm-20240215-3.13.0a4-9d34f60) | python/v3.13.0a4 | 9d34f60 | 1.17x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png) | 1.28x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png) | 1.21x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png) |  |

## darwin arm64 (darwin)
| date | fork/ref | hash/flags | vs. 3.10.4: | vs. 3.11.0: | vs. 3.12.0: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| [2024-05-08](results/bm-20240508-3.13.0b1-2268289) | python/v3.13.0b1 | 2268289 | 1.25x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.10.4.png) | 1.03x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.11.0.png) | 1.06x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289-vs-3.12.0.png) |  |
| [2024-05-07](results/bm-20240507-3.13.0a6%2B-9762122) | python/976212223541b89329d8 | 9762122 | 1.25x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-darwin-arm64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-darwin-arm64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.10.4.png) | 1.02x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-darwin-arm64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-darwin-arm64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.11.0.png) | 1.06x ↑<br>[📄](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-darwin-arm64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.md)[📈](results/bm-20240507-3.13.0a6%2B-9762122/bm-20240507-darwin-arm64-python-976212223541b89329d8-3.13.0a6%2B-9762122-vs-3.12.0.png) |  |
| [2024-05-04](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS) | python/999f0c512281995fb61a | 999f0c5 ️(T2) | 1.10x ↑<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.10.4.png) | 1.10x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.11.0.png) | 1.07x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-3.12.0.png) | 1.13x ↓<br>[📄](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.md)[📈](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base.png)[🧠](results/bm-20240504-3.13.0a6%2B-999f0c5-PYTHON_UOPS/bm-20240504-darwin-arm64-python-999f0c512281995fb61a-3.13.0a6%2B-999f0c5-vs-base-mem.png) |
| [2024-03-12](results/bm-20240312-3.13.0a5-076d169) | python/v3.13.0a5 | 076d169 | 1.17x ↑<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.10.4.png) | 1.04x ↓<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.11.0.png) | 1.01x ↓<br>[📄](results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.md)[📈](results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169-vs-3.12.0.png) |  |
| [2024-02-15](results/bm-20240215-3.13.0a4-9d34f60) | python/v3.13.0a4 | 9d34f60 | 1.19x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.10.4.png) | 1.03x ↓<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.11.0.png) | 1.00x ↑<br>[📄](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.md)[📈](results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60-vs-3.12.0.png) |  |


<!-- END table -->

`*` indicates that the exact same versions of pyperformance was not used.

For the results above, the "faster/slower" result is a geometric mean of each of the benchmarks. The "reliability (rel)" number is the likelihood that the change is faster or slower based on the [Hierarchical Performance Testing (HPT)](#hpt) method.  For more details, visit each individual result's README.md.

## Longitudinal results

Below are longitudinal timing results. There are also [🧠 longitudinal memory results](memory.md).

![Longitudinal speed improvement](/longitudinal.png)

![Effect of different configurations](/configs.png)

Improvement of the HPT score of key merged benchmarks, computed with `pyperf compare`.
The results have a resolution of 0.01 (1%).

- linux: Intel® Xeon® W-2255 CPU @ 3.70GHz, running Ubuntu 20.04 LTS, gcc 9.4.0
- linux2: 12th Gen Intel® Core™ i9-12900 @ 2.40 GHz, running Ubuntu 22.04 LTS, gcc 11.3.0
- linux-aarch64: ARM Neoverse N1, running Ubuntu 22.04 LTS, gcc 11.4.0
- macos: M1 arm64 Mac® Mini, running macOS 13.2.1, clang 1400.0.29.202
- windows: 12th Gen Intel® Core™ i9-12900 @ 2.40 GHz, running Windows 11 Pro (21H2, 22000.1696), MSVC v143

## Documentation

### Running benchmarks from the GitHub web UI

Visit the 🔒 [benchmark action](../../actions/workflows/benchmark.yml) and click the "Run Workflow" button.

The available parameters are:

- `fork`: The fork of CPython to benchmark.
  If benchmarking a pull request, this would normally be your GitHub username.
- `ref`: The branch, tag or commit SHA to benchmark.
  If a SHA, it must be the full SHA, since finding it by a prefix is not supported.
- `machine`: The machine to run on.
  One of `linux-amd64` (default), `windows-amd64`, `darwin-arm64` or `all`.
- `benchmark_base`: If checked, the base of the selected branch will also be benchmarked.
  The base is determined by running `git merge-base upstream/main $ref`.
- `pystats`: If checked, collect the pystats from running the benchmarks.

To watch the progress of the benchmark, select it from the 🔒 [benchmark action page](../../actions/workflows/benchmark.yml).
It may be canceled from there as well.
To show only your benchmark workflows, select your GitHub ID from the "Actor" dropdown.

When the benchmarking is complete, the results are published to this repository and will appear in the [master table](RESULTS.md).
Each set of benchmarks will have:

- The raw `.json` results from pyperformance.
- Comparisons against important reference releases, as well as the merge base of the branch if `benchmark_base` was selected.  These include
  - A markdown table produced by `pyperf compare_to`.
  - A set of "violin" plots showing the distribution of results for each benchmark.
  - A set of plots showing the memory change for each benchmark (for immediate bases only, on non-Windows platforms).

The most convenient way to get results locally is to clone this repo and `git pull` from it.

### Running benchmarks from the GitHub CLI

To automate benchmarking runs, it may be more convenient to use the [GitHub CLI](https://cli.github.com/).
Once you have `gh` installed and configured, you can run benchmarks by cloning this repository and then from inside it:

```bash
$ gh workflow run benchmark.yml -f fork=me -f ref=my_branch
```

Any of the parameters described above are available at the commandline using the `-f key=value` syntax.

### Collecting Linux perf profiling data

To collect Linux perf sampling profile data for a benchmarking run, run the `_benchmark` action and check the `perf` checkbox.

### Developer docs

The infrastructure to make all of this work is the [bench_runner
project](https://github.com/faster-cpython/bench_runner).  Look there for more
detailed developer docs.

### Details about how results are collected

The easiest way to reproduce what is here is to use the [bench_runner
project](https://github.com/faster-cpython/bench_runner) library directly, but
if you want to run parts of it in a different context or better understand how the
numbers are calculated, this section describes some of the things that the
benchmarking infrastructure does.

#### Benchmarks from pyperformance and python-macrobenchmarks

These results combine benchmarks that live in the
[pyperformance](https://github.com/python/pyperformance) and
[pyston/python-macrobenchmarks](https://github.com/pyston/python-macrobenchmarks)
projects, so running the default set from `pyperformance` will definitely
produce different results. To combine these benchmarks in the same run, clone
both repos side-by-side in the same directory and [use a manifest
file](https://github.com/faster-cpython/bench_runner/blob/main/bench_runner/templates/benchmarks.manifest)
to combine them.  This file should be passed to `pyperformance run`:

```
pyperformance run --manifest benchmarks.manifest
```

#### Different configurations

Benchmarks and stats collection can happen in three different configurations.
Here "configuration" may be a combination of both build-time and run-time flags:

- Default: A PGO build of CPython (`./configure --enable-optimizations
  --with-lto=yes`).
- Tier 2: The same build as above, but with the `PYTHON_UOPS` environment
  variable set at runtime to use the Tier 2 interpreter.
- JIT: A JIT and PGO build of CPython (`./configure --enable-optimizations
  --with-lto=yes --enable-experimental-jit`).

Information about the configuration of the run is in the `README.md` at the root
of each run directory.  The directory name will also include `PYTHON_UOPS` for
Tier 2 and `JIT` for JIT.

To reduce the number of unknown variables when comparing results, runs are
always compared against runs of the same configuration. Be aware that sometimes
the base commit on main may predate the configuration becoming available, for
example, before the JIT compiler was merged into main.  (An exception to this
rule are the weekly benchmarks of upstream main, there Tier 2 and JIT
configurations are compared against default configurations of the same commit,
but that isn't relevant for the common case of testing a pull request).

An additional sharp edge is that, by default, `pyperformance` does not pass
environment variables to the child process that actually does the work.
Therefore for a Tier 2 configuration, the `--inherit-environ=PYTHON_UOPS` flag
must be passed to `pyperformance run` when running benchmarks.

For detailed information, see how configurations affect [build time flags in the
Github Actions
configuration.](https://github.com/faster-cpython/bench_runner/blob/main/bench_runner/templates/_benchmark.src.yml).

#### Timing benchmarks

Timing benchmarks are notoriously noisy.  There are a few techniques to reduce this:

- Where available (on Linux), we use [`pyperf
  tune`](https://pyperf.readthedocs.io/en/latest/system.html) to set CPU
  affinity and other things that make the benchmarks more reproducible.  For
  this reason, we know that the benchmarks are more predictable on Linux than on
  the other platforms.
- `pyperf` has the concept of "warmup" runs, while caches are warming up and
  other things about the system are still stabilizing. These runs are excluded
  from the timing results. This is generally effective at reducing variability,
  but also may exclude real work done during optimization, for example.
- We use the Hierarchical Performance Testing (HPT) method (see below) to
  statistically reduce the effect of benchmarks that have more variability.
  This is a different method than the simple geometric mean that `pyperf` uses
  by default.  We provide both numbers in our results.

#### pystats

`pystats` are a set of counters in CPython that measure things like the number
of times each bytecode instruction is executed.  (Detailed documentation of all
of the counters should be added to CPython in the future).

Collecting `pystats` requires a special build of CPython with `pystats` enabled:
(`./configure --enable-pystats`).

`pystats` must also be enabled at runtime, either using the `-Xpystats` command
line argument or `sys._stats_on()`. `pyperformance`/`pyperf` handles this step
automatically when running on a pystats-enabled build.  Stats collection is
enabled during actual benchmarking code, and disabled while running the
"benchmarking harness" code in `pyperf` itself.  `pyperf` has the concept of
"warmup" runs, which allow things like cache lines to warmup before actually
timing benchmarks. While they aren't included in the timing benchmarks, these
warmup runs are included in pystats collection since often Tier 2/JIT traces are
created during warmup, and we don't want the stats to appear as if the traces
ran but were not created.

Any statistics collected are then dumped at exit to the `/tmp/py_stats`
directory with a random filename. Lastly, the `Tools/scripts/summarize_stats.py`
script (in the CPython repo) is used to read all of the files from
`/tmp/py_stats` and produce a human-readable markdown summary and a JSON file
with aggregate data.  Because of this design, it is imperative that:

- The `/tmp/py_stats` directory is cleared before data collection.
- No other Python processes are run that could also produce pystats data.
  Especially, this means benchmarks can not run in parallel.

For more information, see the actual code to [collect
pystats](https://github.com/faster-cpython/bench_runner/blob/main/bench_runner/templates/_pystats.src.yml).

### HPT

Hierarchical performance testing (HPT) is a method introduced in this paper:

> T. Chen, Y. Chen, Q. Guo, O. Temam, Y. Wu and W. Hu,
"Statistical performance comparisons of computers,"
IEEE International Symposium on High-Performance Comp Architecture,
New Orleans, LA, USA, 2012, pp. 1-12,
doi: 10.1109/HPCA.2012.6169043.

From the abstract:

> In traditional performance comparisons, the impact of performance variability
is usually ignored (i.e., the means of performance measurements are compared
regardless of the variability), or in the few cases where it is factored in
using parametric confidence techniques, the confidence is either erroneously
computed based on the distribution of performance measurements (with the
implicit assumption that it obeys the normal law), instead of the distribution
of sample mean of performance measurements, or too few measurements are
considered for the distribution of sample mean to be normal. …  We propose a
non-parametric Hierarchical Performance Testing (HPT) framework for
performance comparison, which is significantly more practical than standard
parametric techniques because it does not require to collect a large number of
measurements in order to achieve a normal distribution of the sample mean.

For each result, we compute a reliability score, as well as the estimated
speedup at the 90th, 95th and 99th percentile.

**The inclusion of HPT scores is considered experimental as we learn about their
usefulness for decision-making.**
