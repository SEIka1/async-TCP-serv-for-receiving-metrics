# Metrics Server Architecture

## Overview
High-performance asynchronous TCP server for collecting and processing metrics with:
- C++20 coroutines for lightweight concurrency
- Boost.Asio for cross-platform async I/O
- Multi-threaded processing pipeline
- Binary protocol for maximum efficiency

## Core Components

### 1. Network Layer
```mermaid
graph TD
    A[TCP Acceptor] -->|New Connection| B[Session Factory]
    B --> C[Session Pool]
    C -->|Metrics| D[Processing Queue]
