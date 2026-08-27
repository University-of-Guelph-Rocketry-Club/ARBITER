# ARBITER

An open-source high-altitude balloon flight simulation and validation tool designed to predict ascent, burst, descent, wind-driven trajectory, and landing location, then compare those predictions against telemetry from real HAB flights.

ARBITER is being developed by students as both a practical engineering and scientific tool and a collaborative learning project.

> The project's implementation stack has intentionally not yet been selected. Contributors will evaluate and justify suitable technologies before implementation begins.

## V1 Scope

Before the first HAB flight, V1 should support:

- Mission configuration
- Atmospheric modelling
- Balloon ascent
- Balloon expansion and burst
- Parachute descent
- Wind-driven horizontal motion
- Weather data input
- Trajectory output
- Real telemetry import
- Predicted-versus-actual flight comparison
- Error metrics

Detailed, implementation-independent requirements are in [docs/requirements.md](docs/requirements.md).

## Repository

- `docs/` contains the [requirements](docs/requirements.md), [architecture boundaries](docs/architecture.md), and [flight-validation plan](docs/flight-validation.md).
- `src/` is reserved for the eventual implementation.
- `tests/` is reserved for automated tests and validation checks.
- `tools/` is reserved for development and data-preparation utilities.
- `samples/` contains small, non-sensitive example mission, weather, and telemetry data.

See [CONTRIBUTING.md](CONTRIBUTING.md) before starting work.
