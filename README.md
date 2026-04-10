# XDV Phi Hardware Provider Interface

Version: 0.1.0
Status: active
Language: Dust Programming Language (DPL)

## Specification Alignment

Primary specification: XDV-061 in `xdv-spec`.

Implemented focus for this milestone:

1. Coherence window contract and transform API flow.
2. Stability monitoring and report emission.
3. Envelope isolation validation constraints.

## Purpose

Phi-domain hardware provider boundary for contract-bound coherence execution.

## Modules

- `src/phihpi_contracts.ds`
  Normative constants and validators for provider identity, transform sets, contract windows, stability tolerance, and error mapping.

- `src/phihpi_provider.ds`
  Provider registration, capability declaration tokenization, attestation token generation, and verification.

- `src/phihpi_coherence.ds`
  Coherence window contract tokenization/verification, execution-window enforcement, overlap detection, and envelope isolation checks.

- `src/phihpi_transform.ds`
  Transform descriptor construction, invocation validation path, and structured transform result/event tokenization.

- `src/phihpi_stability.ds`
  Continuous stability sample evaluation, report tokenization, instability response, and event digest path.

- `src/phihpi_tests.ds`
  Behavioral tests for coherence+transform API, stability monitoring/reporting, and envelope isolation constraints.

- `src/main.ds`
  Startup validation, smoke flows, and self-test entrypoints.

## Design Notes

- No transform runs without active coherence contract validation.
- Transform compatibility is checked against declared transform set.
- Stability monitoring enforces tolerance and noise thresholds.
- Envelope aliasing/overlap across tenants requires explicit sharing contract.
- Report/event tokens are deterministic for replay-equivalent behavior.

## Build

```bash
dust check xdv-phihpi/src
```

## Test

```bash
dust check xdv-phihpi/src/phihpi_tests.ds
dust check xdv-phihpi/tests/phihpi_e2e.ds
```

## Integration Contracts

- Preserve deterministic contract/transform/report ordering.
- Keep envelope isolation checks in transform path.
- Emit structured stability/error metadata only (no raw phase state).
- Enforce contract expiration and instability response deterministically.
