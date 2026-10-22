## 以后你自己更新，就这四条

bash

```bash
cd "E:\computer science\python\CS61A-Assignments"
git add -A
git commit -m "hw02 complete"
git push
```

几点说明，省得你下次又卡住：

- `cd` 到**仓库根目录**（就是 `CS61A-Assignments` 这层），不要在 `hw01` 子目录里操作。
- `git add -A` 是"把所有改动加入暂存区"。以前它会连临时文件一起吞进去，现在有 `.gitignore` 兜着，可以放心用。
- `commit -m` 后面那句是你自己的备注，随便写（你之前用的是 `lab00 complete`、`disc00 solutions` 这种小写短句）。想多行说明就用：`git commit` 不加 `-m`，会打开编辑器让你写。
- `git push` 不报错就没问题。你的凭据已经存在 Windows 凭据管理器里（`credential.helper = helper-selector`），所以**不需要**每次输账号密码。
- 想反悔某次修改还没提交：`git checkout -- 文件名`。已经 commit 了还没 push 想撤回：`git reset --soft HEAD~1`（改动会回到工作区，不会丢）。