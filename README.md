# Mythicove API

**English** | [简体中文](./README.zh-CN.md)

Unified OpenAPI contract repository for the Mythicove ecosystem — the **single source of truth** that generates both the Go server (`oapi-codegen`) and the TypeScript client (`openapi-typescript`).

## Conventions

- One spec file per product: `specs/mirror.openapi.yaml`, `specs/hoard.openapi.yaml` (future `isles`/`atlas`/`compass` follow the same pattern).
- Shared models (accounts, pagination, error responses) live in `specs/common.yaml`, reused via `$ref`.
- Starting from **OpenAPI 3.1**.
- Changing the spec means changing the contract: code on both ends is generated from this repository by CI — never hand-edit generated artifacts.

## Layout

- `specs/` — per-product OpenAPI contracts
- `codegen/` — code generation scripts / config (to be added)

## License

Contracts and generated artifacts are [MIT](https://opensource.org/license/mit) — SDK/contract assets use MIT so third-party launchers and tools can integrate easily.
