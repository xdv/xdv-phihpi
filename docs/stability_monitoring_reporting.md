# Stability Monitoring and Reporting

## Scope

`src/phihpi_stability.ds` implements continuous stability sampling and deterministic report paths.

## Monitoring

`monitor_stability_sample` evaluates:

- envelope validity
- stability level within tolerance range
- noise index within threshold

Any violation yields deterministic `STATUS_STABILITY_BREACH`.

## Report Structure

`stability_report_token` emits deterministic structured metadata:

- envelope id
- stability level
- noise index
- integrity checksum
- logical timestamp
- signature

## Instability Handling

`instability_response` maps monitor status into deterministic actions:

- none
- rollback + release
- halt + envelope invalidation

`envelope_invalidation_token` records deterministic invalidation metadata.

`stability_event_digest` supports replay-safe event correlation.
