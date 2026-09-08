# 验证状态

本文件只记录实际完成的检查，不将示例当成测试。

- 已完成：原始 Skill 结构校验、资源相对引用检查、本机全局安装入口检查。
- 已完成：使用 Skills CLI 在独立临时项目中从本地发布包安装，成功发现一个 Skill；安装后与发布包逐文件比较一致。
- 已完成：从公开 GitHub 仓库通过 `npx -y skills add time-dealer/adaptive-learning -a codex -y` 安装到独立临时项目；全部 9 个 Skill 资源文件与发布包一致（不计本机 Finder 生成且未发布的 .DS_Store）。
- 已完成：临时项目限定 `-a codex` 卸载后公共入口仍在；随后执行 `npx -y skills remove adaptive-learning -y`，公共入口已删除，独立学习目录的测试记录仍在。单宿主卸载与完整卸载的范围不同。
- 已完成：GitHub 首页文本、表格及 Mermaid 流程图渲染检查。
- 尚未单独实测：Skills CLI 的全局 `-g --all` 安装路径；以上公开安装与卸载验证使用项目范围，未改动使用者现有全局 Skill。
- 尚未验证：完整多轮教学、新会话恢复、不同宿主的图示／交互行为、长期学习效果。

维护者本地运行 `quick_validate.py` 需要 `PyYAML`。如果报 `ModuleNotFoundError: No module named 'yaml'`，说明校验环境缺依赖，不代表 Skill 无法安装或运行。维护环境设置见 [维护者验证环境](maintainer-validation.md)。

行为验证应至少覆盖首次问诊、短问答、用户跳过、开放作品反馈、纠错以及保存后恢复。执行者不提前读取评分预期；真实个人档案不作为公开测试材料。
