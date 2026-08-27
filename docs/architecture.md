# Architecture

ARBITER does not have a concrete software architecture yet. The team should choose one only after discussing the requirements and comparing suitable technologies.

Whatever stack is selected, the project should maintain these conceptual boundaries:

```text
User Interface / CLI / Other Client
              |
              v
       Simulation Interface
              |
       +------+------+
       |             |
       v             v
Physics/Models    Weather/Data
       |
       v
Simulation Results
       |
       +--> Visualization
       +--> Export
       +--> Flight comparison
```

This diagram describes separation of responsibilities, not a required folder layout, programming style, framework, or deployment model. The simulation should be usable independently of any particular client, while weather and other external data should cross clear boundaries.

## Technology Selection

The team should evaluate candidate stacks based on:

- Accessibility for intermediate computer science and engineering students
- Cross-platform requirements
- Numerical and scientific ecosystem
- Testing support
- Visualization capabilities
- Maintainability
- Performance needs
- Packaging and deployment complexity
- Quality of documentation
- How much contributors can learn from the stack

The decision and its reasoning should be recorded before implementation begins. This document does not recommend a winner.
