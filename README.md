# Metrics Server [![CI Status](https://github.com/SEIka1/async-TCP-serv-for-receiving-metrics/actions/workflows/build.yml/badge.svg)](https://github.com/SEIka1/async-TCP-serv-for-receiving-metrics/actions)

Modern C++20 TCP server for high-frequency metrics collection.

## Features
- ⚡ Async I/O with coroutines (Boost.Asio)
- 📊 Binary protocol for maximum throughput
- 🔒 Built-in data validation and recovery

## Quick Start
```bash
# Build (requires Boost 1.82+)
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --parallel

# Run
./build/server --config config.yaml
