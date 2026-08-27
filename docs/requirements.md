# V1 Requirements

These requirements describe what ARBITER needs to do before the first HAB flight. They are intentionally independent of programming language, framework, and application architecture.

## Mission Inputs

V1 must accept enough information to describe:

- Launch location
- Launch time
- Payload mass
- Balloon properties
- Lifting gas
- Free lift or fill information
- Parachute properties

Inputs should be clear enough that another contributor can understand and repeat a run.

## Physical Simulation

V1 must model:

- Atmospheric pressure
- Atmospheric temperature
- Atmospheric density
- Buoyancy
- Balloon ascent
- Balloon expansion
- Balloon burst
- Parachute descent
- Wind-driven horizontal movement

The level of detail can grow over time, but each model must state its assumptions and expected range of use.

## Simulation Outputs

V1 must produce:

- Latitude and longitude throughout the simulated flight
- Altitude versus time
- Vertical velocity versus time
- Predicted burst altitude and location
- Predicted landing location
- Predicted flight duration

## Data Workflows

V1 must support:

- Importing weather data
- Exporting simulation results in a machine-readable format
- Importing real HAB telemetry
- Comparing a prediction against actual flight data

The weather data used for each prediction must be saved with enough context to reproduce the run later.

## Comparison Metrics

At minimum, predicted-versus-actual comparison must include:

- Landing error
- Burst-altitude error
- Burst-time error
- Total flight-time error
- Altitude root mean square error (RMSE)
- Horizontal trajectory error

Metric definitions, coordinate assumptions, time alignment, and handling of missing telemetry must be documented before results are presented.

## Engineering Requirements

- Simulation logic must be independent from the user interface.
- Identical input and weather data should produce reproducible results.
- SI units should be used internally.
- Major physical models and assumptions must be documented.
- Important mathematical behaviour must be automatically testable.
- Simulation results must be exportable in a machine-readable format.
- Weather data used for a prediction must be preserved so the run can be reproduced.
- The architecture should allow individual components to evolve without rewriting the entire project.
- External data sources should be isolated behind clear interfaces or boundaries.
- The project should prioritize understandable code over unnecessary abstraction.

These requirements do not prescribe object-oriented, functional, entity-component, client-server, desktop, web, or any other implementation style.
