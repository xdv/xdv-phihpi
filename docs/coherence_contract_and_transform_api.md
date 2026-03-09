# Coherence Contract and Transform API

## Scope

`src/phihpi_coherence.ds` and `src/phihpi_transform.ds` implement the core XDV-061 execution path.

## Coherence Window Contract

The contract token model includes:

- contract id
- provider id
- envelope id
- start logical time and duration
- stability tolerance range
- transform-set id
- capability id
- signature

`verify_coherence_contract` performs deterministic recomputation and token equality check.

## Window Enforcement

`is_execution_within_window` enforces:

- execution starts exactly at contract start
- execution end is within contract deadline

## Transform API

`transform_descriptor_token` builds the structured transform descriptor metadata.

`invoke_transform` validates in deterministic order:

1. provider attestation status
2. envelope status
3. contract active status
4. transform supported by declared transform set
5. stability tolerance compliance

`transform_result_token` returns structured result metadata only.

No raw phase vectors are exposed.
