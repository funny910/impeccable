# Fork 维护工作流

这个 Fork 用于 Trista 的 Codex 与前端 UI/UX 工作流。

## 分支职责

- `main)：只跟踪 `pbakaus/impeccable` 上游，不直接放个人定制。
- `codex-custom`：个人文档、Codex 工作流和非上游定制。
- `feature/*`：一次具体的实验或功能改动，完成后合并到 `codex-custom`。

不要把 `react-bits-demo` 复制进本仓库；它是独立的使用示例项目。

## 同步上游

在 GitHub 网页中打开本 Fork，使用文件列表上方的 **Sync fork**。

命令行同步：

```bash
git clone https://github.com/funny910/impeccable.git
cd impeccable
git remote add upstream https://github.com/pbakaus/impeccable.git
git fetch upstream
git switch main
git merge --ff-only upstream/main
git push origin main
```

如果 `main` 有本地定制，不要强行覆盖；先将本地改动移到 `codex-custom` 或 feature 分支，再同步 `main`。

## 定制原则

1. 先在 `codex-custom` 记录目的和影响面。
2. 优先修改源文件，不直接编辑生成的 provider 输出。
3. 不在 feature 分支修改版本号或写发布日志。
4. 需要提交给上游的变化，先遵守仓库的 issue-first 贡献规则。
5. 每次定制都保留最小验证命令和已知限制。
