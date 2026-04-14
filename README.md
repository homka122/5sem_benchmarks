# Benchmark: Influence of Grouping on Performance

This project evaluates the impact of grouping strategies (RSM and Automata) on execution time and RAM usage when building graph structures.

## Experiment Description

### Parameters

- **Depth**: Context depth (1 or 2)
- **Number of contexts**: 10, 20, 30 (small) or 50, 100 (large)
- **Graphs**:
  - **Small**: `collections`, `cornerCases`, `generalJava`, `basic`
  - **Large**: `com_fasterxml_jackson`, `org_apache_jackrabbit`, `org_jivesoftware_openfire`, `reactor`

### Grouping Strategies

- No grouping
- RSM only
- Automata only
- RSM + Automata

### Measured Metrics

- **Execution time** (seconds)
- **RAM usage** (KB)

## Results

### Depth 1 — Small Graphs (10 contexts)

![Time: Depth 1, Small Graphs, 10 contexts](plots/time_depth1_10_small.png)

![RAM: Depth 1, Small Graphs, 10 contexts](plots/ram_depth1_10_small.png)

### Depth 1 — Large Graphs (10 contexts)

![Time: Depth 1, Large Graphs, 10 contexts](plots/time_depth1_10_large.png)

![RAM: Depth 1, Large Graphs, 10 contexts](plots/ram_depth1_10_large.png)

### Depth 1 — Small Graphs (50 contexts)

![Time: Depth 1, Small Graphs, 50 contexts](plots/time_depth1_50_small.png)

![RAM: Depth 1, Small Graphs, 50 contexts](plots/ram_depth1_50_small.png)

### Depth 1 — Large Graphs (50 contexts)

![Time: Depth 1, Large Graphs, 50 contexts](plots/time_depth1_50_large.png)

![RAM: Depth 1, Large Graphs, 50 contexts](plots/ram_depth1_50_large.png)

### Depth 2 — Small Graphs (all contexts)

![Time: Depth 2, Small Graphs](plots/time_depth2_all_small.png)

![RAM: Depth 2, Small Graphs](plots/ram_depth2_all_small.png)

## Key Findings

1. **RSM + Automata** provides the best performance in most cases (marked in green)
2. The speedup ratio (×N) shows improvement compared to the worst strategy
3. Larger contexts (50, 100) generally show more significant benefits from grouping
4. RAM usage follows similar patterns to execution time