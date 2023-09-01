# Ganache vs Anvil Benchmarks for Forking Polygon

## Introduction

In this repo you will find the comparison done through [flood](https://github.com/paradigmxyz/flood) for comparing performance / reliability of forking through ganache vs anvil

## Results

![latencies](./benchmarks/eth_call/figures/latencies.png)
![success_rate](./benchmarks/eth_call/figures/success_rate.png)
![throughput](./benchmarks/eth_call/figures/throughput.png)

## Methodology

```
flood eth_call anvil=localhost:3000 ganache=localhost:8545 -o ./fork-benchmarks/benchmarks/eth_call -d 3 --rates 1 4 16 64
```

## Considerations

My Dockerfiles may have not been optimized, and Ganache kept crashing during the benchmark, so I just ran them locally on my machine so I could get these results.
