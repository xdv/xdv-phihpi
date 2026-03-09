# Envelope Isolation Constraints

## Scope

Envelope isolation is enforced in `src/phihpi_coherence.ds`.

## Overlap Detection

`windows_overlap` deterministically detects overlap between two logical windows.

## Isolation Rule

`validate_envelope_isolation` enforces:

- same envelope + overlapping window + different tenant => isolation violation
- same envelope + overlap + explicit sharing contract => allowed
- same envelope + no overlap => allowed
- different envelope ids => allowed (no alias)

## Compliance Intent

This enforces the XDV-061 boundary that envelope sharing across tenants is forbidden unless explicitly contracted.

The behavior is deterministic and replay-safe.
