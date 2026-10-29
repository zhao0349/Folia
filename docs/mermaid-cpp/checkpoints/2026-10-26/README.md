# 历史补丁归档说明（2026-10-26）

本目录保存 2026-10-26 阶段暂停时的本地工作区补丁归档与各子任务独立候选补丁（`canonical.patch.gz` 与 `luna01.patch` ~ `luna12.patch`），仅在 Fork 仓库 `master` 分支中作为历史参考保留，不随功能分支进入上游 PR。

## 文件说明

- `canonical.patch.gz`：基于早期快照 `011e0656` 导出的 1,772 个文件变更归档（解压后为 45,641,089 字节，原始与压缩包 SHA-256 见 `manifest.json`）。
- `luna01.patch` ~ `luna12.patch`：当时 12 个并行子任务相对于 `canonical.patch.gz` 的独立增量补丁。各补丁对应的原始 SHA-256 与对比摘要记录在 `manifest.json` 中。
- `.gitattributes`：禁用本目录下补丁文件的 CRLF 自动换行转换，确保补丁字节哈希保持一致。

## 使用与选取原则

当前主开发分支 `feat/mermaid-cpp-port` 已完成 20 个图族的原生实现并通过 Windows 四配置 CI 验证。本归档中的早期补丁仅用于在需要时提取单个独立图族（如 Requirement、ER 等）的局部参考代码，请勿直接整体覆盖当前主分支已验证通过的实现。具体取舍结论见上级目录的 [`REVIEW-2026-10-28.md`](../REVIEW-2026-10-28.md)。
