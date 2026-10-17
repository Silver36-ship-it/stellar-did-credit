# Event Indexing Guide

Soroban contract events provide indexers and data feeders with updates about
on-chain state. Events consist of a topic vector and a data payload.

## Credit Oracle Events

### `IdentityOracleUpdated`

- **Topic:** `[Symbol("IdentityOracleUpdated")]`
- **Data:** `identity_oracle_id: Address`
- **Emitted when:** The admin sets or updates the identity-oracle contract ID
  on the credit oracle via `set_identity_oracle`.
- **Indexer action:** Update the cached identity-oracle contract address.
