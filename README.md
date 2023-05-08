Git 仓库两个分支之间如果出现多条合并基线（merge-base），
会造成 pull request 代码评审差异比较不符合预期，会引入
其他分支文件。

检查两个分支（如 master 和 topic）是否有多条 merge base，使用如下命令：

    git merge-base --all master topic

如果输出多个提交ID，说明有多个 merge-bases，会在 pull request 差异比较时，
显示多余文件。

