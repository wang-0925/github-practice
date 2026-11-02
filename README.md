# github-practice

我的第一个 GitHub 练习仓库，用来熟悉提交、分支、Issue 和 Pull Request 的完整流程。

## 练习记录

- [x] 初始化本地仓库并写 README
- [x] 开一个分支，改 README，发起第一个 Pull Request
- [ ] 用 Issue 记录一个待办，并在提交里引用它
- [ ] 加一个 GitHub Actions 工作流，让它自动运行
- [ ] 用 GitHub Pages 发布一个静态页面

## 分支与 PR 流程

每次改动走一遍这个循环，不直接推到 main：

```bash
git switch -c feature/xxx      # 从 main 开新分支
# 修改文件
git add . && git commit -m "改了什么"
git push -u origin HEAD        # 推送并建立跟踪
gh pr create --fill            # 用提交信息生成 PR
gh pr merge --merge --delete-branch
```

合并后回到 main 拉取一次，本地就和远程一致了。

## 常用命令

```bash
git status          # 看当前改了什么
git add .           # 把改动放进暂存区
git commit -m "..." # 记录一次提交
git push            # 同步到 GitHub
```
