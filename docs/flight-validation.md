# Flight Validation

ARBITER will be checked against telemetry from real HAB flights, not just whether its output looks reasonable.

## Flight 1

**The Flight 1 prediction must be saved before launch and preserved unchanged.**

The pre-flight archive should contain:

- Mission configuration
- Weather dataset or snapshot
- Simulation output
- Software version or Git commit
- Time the prediction was generated

After launch, preserve the raw telemetry, import it into ARBITER, and compare it with the frozen prediction using the metrics in [requirements.md](requirements.md). Do not replace the archived prediction with a rerun that uses information learned after the flight.

Flight 1 can then be used to calibrate the model, investigate bad assumptions, and improve the simulator.

## Flight 2

Flight 2 should test the improved model more independently. Generate and freeze a new prediction before launch, archive the same supporting information, and compare it with Flight 2 telemetry afterward.

Keep both the original predictions and the later analysis so the results remain honest and reproducible.
