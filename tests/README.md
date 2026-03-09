# XDV PHIHPI Tests

Deterministic tests and fixtures for `xdv-phihpi`.

## Covered Behaviors

- Coherence contract validation and transform invocation path.
- Stability monitoring/report token emission and instability response.
- Envelope overlap and cross-tenant isolation constraints.

## Entrypoints

- `xdv-phihpi/src/phihpi_tests.ds` : core behavior checks.
- `xdv-phihpi/tests/phihpi_e2e.ds` : aggregate test entrypoint.

## Run

```bash
dust check xdv-phihpi/src
dust check xdv-phihpi/tests/phihpi_e2e.ds
```
