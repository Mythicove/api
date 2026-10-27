# Mythicove API

[English](./README.md) | **简体中文**

Mythicove 生态的统一 OpenAPI 契约仓库，作为单一事实源：TypeScript client 由 openapi-typescript 生成，Go server 手写并以漂移测试保证 spec 与路由一致。

## 约定

- 每个产品一个 spec 文件：specs/mirror.openapi.yaml、specs/hoard.openapi.yaml，后续的 isles、atlas、compass 同理。
- 公共模型（账号、分页、错误响应）抽到 specs/common.yaml，用 $ref 复用。
- 以 OpenAPI 3.1 起步。
- 改 spec 就是改契约：TS client 由 CI 从本仓库生成，不要手写生成物；Go 侧由漂移测试把关。

## 目录

- specs/：各产品 OpenAPI 契约
- codegen/：代码生成脚本和配置（待建）

## 许可证

契约与生成物采用 [MIT](https://opensource.org/license/mit)。SDK 和契约类资产用 MIT，第三方启动器和工具接入时没有限制。
