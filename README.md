 # AIOps Assessment - Basic AIOps Monitoring & Event Processing

## 1. AIOps Scenario
This project demonstrates an operational monitoring workflow for application services. High metric utilization (CPU/Memory) and log error spikes are continuously analyzed to generate actionable anomaly events.

## 2. Operational Data & Observations
- **Metrics:** Fields like `cpu_usage` and `memory_usage` reflect operational load. Spikes above normal operating ranges represent abnormal metric behavior.
- **Logs:** Log level entries (e.g., `ERROR`, `CRITICAL`) indicate application failure states.
- **Timestamps:** Standard ISO timestamps correlate metric spikes with corresponding log error instances.

## 3. Anomaly Findings & Event Flow
- Detected metric threshold breaches and error log entries.
- Triggered anomaly events from `EventProducer` to `EventTopic`.
- Received and processed events via `EventConsumer` to reach final AIOps pipeline output.

## 4. Troubleshooting & Corrections
- **Issue:** `ModuleNotFoundError` during test execution due to path resolution conflicts.
- **Fix:** Refactored module imports in `tests/test_aiops_pipeline.py` and executed tests using `PYTHONPATH=src pytest`.

## 5. Reproduction Steps
To verify and run this pipeline:
1. Open terminal in the project root.
2. Execute test suite:
   ```bash
   PYTHONPATH=src pytest