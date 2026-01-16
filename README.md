# CHANGELOG

这是一个用于集中存放多个项目变更记录（CHANGELOG）的公共仓库。

## 约定

- 每个项目一个目录，例如：`SimpleLDB/`、`hosAgent/`
- 每个版本一个文件，文件名建议：`vX.Y.Z_YYYY-MM-DD.md`
- 版本号与项目 Git tag 对齐（例如：`v0.0.14`）

> 说明：该仓库会被各项目以 Git submodule 的方式引入。

## Changelog 文件格式规范

### 模板

```markdown
# 项目名 vX.Y.Z（YYYY-MM-DD）

## 变更概览

- 主要变更点 1：简短描述
- 主要变更点 2：简短描述
- 主要变更点 3：简短描述

## 详情

### Added
- 新增功能点 1
- 新增功能点 2

### Changed
- 变更内容 1
- 变更内容 2

### Fixed
- 修复问题 1
- 修复问题 2

### Removed
- 移除内容 1

### Security
- 安全相关变更

### Performance
- 性能优化

### Documentation
- 文档更新

### UX
- 用户体验改进

### Technical
- 技术细节

## 备注

- 其他需要说明的事项
- 包含的改进内容总结

## Technical Details

- Commit: `hash` - commit message (YYYY-MM-DD HH:MM)
- Commit: `hash` - commit message (YYYY-MM-DD HH:MM)
```

### 规范说明

1. **文件命名**
   - 格式：`vX.Y.Z_YYYY-MM-DD.md`
   - 版本号遵循语义化版本规范
   - 日期为版本发布日期

2. **章节结构**
   - `变更概览`：3-5 个主要变更点的简要描述
   - `详情`：按类型分类的详细变更列表
   - `备注`：版本特别说明、注意事项等
   - `Technical Details`：包含的 commit 记录

3. **变更类型分类**
   - `Added`：新增功能
   - `Changed`：现有功能的变更
   - `Deprecated`：即将废弃的功能
   - `Removed`：已移除的功能
   - `Fixed`：问题修复
   - `Security`：安全相关变更
   - `Performance`：性能优化
   - `Documentation`：文档更新
   - `UX`：用户体验改进
   - `Technical`：技术实现细节

4. **Technical Details 格式**
   - 格式：`Commit: \`hash\` - commit message (YYYY-MM-DD HH:MM)`
   - 包含该版本的所有相关 commit
   - 按时间顺序排列
   - 即使是私人仓库也记录 commit 信息，便于内部查阅

5. **编写建议**
   - 使用清晰、简洁的语言描述变更
   - 重点突出用户可见的变更
   - 技术细节放在 Technical Details 部分
   - 遵循中文技术文档写作规范
   - 保持版本间格式一致性

## 示例

参考 [example](example/) 目录的示例文件：
- [v0.0.1](example/v0.0.1_2025-01-01.md) - 标准 changelog 模板示例

## 版本划分建议

根据 commit 类型和影响范围进行版本划分：

- **Major 版本**（X.0.0）：不兼容的 API 变更、架构重构
- **Minor 版本**（0.X.0）：新增功能、向后兼容的 API 变更
- **Patch 版本**（0.0.X）：Bug 修复、小改进、文档更新

单个 commit 可独立为一个 patch 版本，相关联的多个 commit 可合并为一个版本。

