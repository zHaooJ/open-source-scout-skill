# 发布到代码托管仓库

[返回首页](../README.md)

这份目录已经按“仓库根目录就是 Skill 目录”的方式组织。项目仓库为 [zHaooJ/open-source-scout](https://github.com/zHaooJ/open-source-scout)。以下说明用于维护发布包，或发布你自己的 Fork。

## 仓库资料建议

| 字段 | 建议内容 |
| --- | --- |
| Repository name | `open-source-scout` |
| 中文介绍 | 用渐进选择题澄清需求，发现并核验开源项目，给出可追溯的比较与选型建议。 |
| English description | A Codex skill for guided requirements, open-source project discovery, evidence checks, and practical comparisons. |
| Topics | `codex`、`agent-skills`、`open-source`、`project-discovery`、`developer-tools` |
| 首页 | 默认展示根目录 `README.md`，从中链接到 `README.en.md` |
| License | 当前包采用 MIT，见根目录 `LICENSE` |

## 放入哪些内容？

将本目录内的文件作为仓库根目录内容提交，包括 `.github/` 和 `.gitignore`。上传后应能直接访问根目录 `SKILL.md` 和 `README.md`，无需再进入一层 `open-source-scout/`。

发布的是 Skill 本身及说明，不包括本机的 `work/`、研究缓存、聊天记录、凭据或外层生成的 ZIP。需要下载包时，可以把 ZIP 放到仓库的 Release 附件中。

## 发布步骤

1. 在选定平台建立仓库，使用上述名称或你自己的名称。
2. 将这个目录的内容提交到仓库根目录；目录内已经有 README 和 MIT 许可，避免用平台模板重复生成。
3. 查看网页上中英文首页、相对链接、Mermaid 流程图和目录结构。
4. 按 README 的安装步骤检查下载后的目录是否能作为 Skill 使用。
5. 需要正式版本时，再创建与你采用的版本号一致的 tag 和 Release，并更新 `CHANGELOG.md`。

中英文首页已包含本仓库地址和克隆命令。发布你自己的 Fork 时，按实际目标调整这些入口；相对文档链接通常不需要调整。只有实际创建了 tag 和 Release，才将对应内容记为正式发布版本。

## 发布时核对

- 名称仍为 `open-source-scout`，目录名、`SKILL.md` 的 `name` 和调用提示一致。
- 确认 MIT 是你准备采用的许可；若改用其他许可，同步 `LICENSE`、中英文首页及徽章。
- 当前版权声明使用 `Open Source Scout contributors`；如需标注实际个人或组织，使用你有权声明的名称。
- 设计参考链接保留，外部项目的许可没有被本仓库的 MIT 许可替代。
- 演示案例仍明确标注为示意，没有包装成实时检索或运行测试。
- 没有将某个宿主的未验证兼容性写成已支持。

GitHub 支持本包使用的 Markdown 表格和 Mermaid 代码块。其他托管平台若不渲染 Mermaid，读者仍可阅读流程图下面的文字说明。
