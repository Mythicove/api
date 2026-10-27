# Mythicove API

**English** | [简体中文](./README.zh-CN.md)

The OpenAPI contract repository for the Mythicove ecosystem. It is the single source of truth: the Go server (oapi-codegen) and the TypeScript client (openapi-typescript) are both generated from it.

## Conventions

- One spec file per product: specs/mirror.openapi.yaml and specs/hoard.openapi.yaml. Future products (isles, atlas, compass) follow the same pattern.
- Shared models (accounts, pagination, error responses) live in specs/common.yaml and are reused through $ref.
- The specs start at OpenAPI 3.1.
- Changing a spec changes the contract. CI generates both code ends from this repository, so generated artifacts are never hand-edited.

## Layout

- specs/: per-product OpenAPI contracts
- codegen/: generation scripts and config (to be added)

## License

Contracts and generated artifacts are [MIT](https://opensource.org/license/mit). SDK and contract assets use MIT so third-party launchers and tools can integrate without restrictions.
