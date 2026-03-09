# Provider Attestation and Capabilities

## Scope

`src/phihpi_provider.ds` defines provider registration, attestation, and capability declaration semantics.

## Registration Requirements

Registration validates presence and compatibility of:

- provider id
- firmware hash
- coherence capability
- stability range
- supported transform set
- envelope capacity
- phase resolution
- hardware interface id
- post-quantum signature
- logical timestamp

## Attestation

`attestation_token` and `verify_attestation` provide deterministic identity verification.

## Capability Declaration

`provider_capability_token` models immutable capability metadata during active contracts.

This supports deterministic pre-checks before coherence contract issuance and transform invocation.
