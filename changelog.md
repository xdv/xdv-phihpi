# Changelog

## 0.1.1 - XDV-061 PHIHPI Core Implementation

- Implemented XDV-061 contract constants and validators in `src/phihpi_contracts.ds`.
- Implemented provider registration/attestation and capability declaration in `src/phihpi_provider.ds`.
- Implemented coherence window contract verification and envelope isolation checks in `src/phihpi_coherence.ds`.
- Implemented transform descriptor/invocation/result API in `src/phihpi_transform.ds`.
- Implemented stability monitoring/reporting and instability response in `src/phihpi_stability.ds`.
- Added behavior tests in `src/phihpi_tests.ds`.
- Added aggregate test entrypoint `tests/phihpi_e2e.ds`.
- Updated README and docs for delivered XDV-061 behavior.

## 0.1.0 - Initial Skeleton

- Created project scaffold for XDV Phi Hardware Provider Interface.
- Added State.toml, README.md, and docs/test placeholders.
- Imported LICENSE from xdv-os/LICENSE.
