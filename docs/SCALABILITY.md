# Scalability baseline

Scale the application based on measured demand and real workloads. Avoid distributed components until profiling shows a bottleneck.

## Priorities
- Profile the most-used workflows and address measured bottlenecks before adding replicas.
- Bound request/input size, concurrency, retries, queue depth, connection pools, and external service timeouts.
- Paginate long lists, avoid unbounded history reads, and optimize measured database queries.
- Keep service instances stateless where possible and externalize shared state before horizontal scaling.
- Add structured logs, request IDs, metrics, health/readiness checks, graceful shutdown, and tested rollback procedures for hosted services.
- Protect secrets and personal data; keep sensitive values out of logs.
- Add automated build, unit, integration, dependency/security, and deployment smoke tests appropriate to the repository's stack.

## Load validation
Test normal, peak, burst, and dependency-failure scenarios with representative data. Measure throughput, p95/p99 latency, error rates, CPU/memory, database wait time, queue lag, and cost where applicable.

## Release gates
- [ ] Authorization/data isolation and negative paths are tested where applicable.
- [ ] Retried mutations are bounded and idempotent where needed.
- [ ] Persistent data backup/restore and rollback are validated.
- [ ] Capacity assumptions and measured load-test results are recorded.

This is a planning checklist, not evidence of completed load testing or production scaling.