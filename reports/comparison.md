# Memory vs No-Memory Comparison

| Metric | Memory-enabled | No-memory | Delta |
| --- | ---: | ---: | ---: |
| Evidence hit rate | 18.2% | 18.2% | +0.0% |
| Passed cases | 2/11 | 2/11 | +0 |
| Avg retrieval latency (ms) | 392.9 | 0.0 | +392.9 |
| Avg token reduction | 81.8% | 81.8% | +0.0% |

## Interpretation

Short-term cases can pass without durable memory because their evidence is still in the current thread. Cross-session, episodic and semantic cases should fail in the no-memory baseline and recover when memory retrieval is enabled.

A no-memory baseline may show near-100 percent token reduction simply because it retrieves nothing. Treat token reduction as useful only together with evidence hit rate; dropping all context is cheap but incorrect.