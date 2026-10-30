# Skills

独立安装、独立维护的 Codex Skills 集合。

## 组件

- [ea](docs/ea/README.md)：Engineering Analysis 开发草稿，固化 PRD 之后、Spec/Plan 之前的核心工程思路。

- [codex-window](skills/codex-window/SKILL.md)：定时刷新 codex 5h 额度, 创建或联动调整三个每日定时任务，间隔为 5 小时 5 分钟。

## 安装指定组件

从本地仓库安装到 Codex 用户级目录：

```bash
npx skills add ./ --skill codex-window --agent codex --global
npx skills add ./ --skill ea --agent codex --global
```

在仓库目录中执行。只安装指定 Skill，不会安装其他组件。

发布到 GitHub 后，将 `./` 替换为实际的 `owner/repo`。

## 使用

```text
用 $codex-window 设置开始时间为 09:00
```

默认时区 Asia/Shanghai，三个时间为 09:00、14:05、19:10。修改开始时间会同步更新三个任务。

每个组件放在 `skills/<name>/SKILL.md`，目录名和 frontmatter 中的 name 保持一致。
