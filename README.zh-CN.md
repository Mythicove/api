# Mythicove API

[English](./README.md) | **简体中文**

Mythicove 生态的统一 OpenAPI 契约仓库——作为 **单一事实源（single source of truth）**，同时生成 Go server（`oapi-codegen`）与 TypeScript client（`openapi-typescript`）。

## 约定

- 每个产品一个 spec 文件：`specs/mirror.openapi.yaml`、`specs/hoard.openapi.yaml`（后续 `isles`/`atlas`/`compass` 同理）。
- 公共模型（账号、分页、错误响应）抽到 `specs/common.yaml`，用 `$ref` 复用。
- 以 **OpenAPI 3.1** 起步。
- 改 spec 即改契约：两端代码由 CI 从本仓库生成，不手写生成物。

## 目录

- `specs/` — 各产品 OpenAPI 契约
- `codegen/` — 代码生成脚本 / 配置（待建）

## 许可证

契约与生成物采用 [MIT](https://opensource.org/license/mit)（SDK/契约类资产走 MIT，便于第三方启动器与工具接入）。
