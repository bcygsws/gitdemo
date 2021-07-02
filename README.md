# gitdemo

## git 提交冲突的解决方案

### 冲突产生原因

-   不同的程序员修改了同一个远程仓库中的同一块代码

## 冲突的解决

-   首先操作的那个程序员 A，可以将修改正常提交到远程仓库
-   之后，操作的程序员 B,修改代码，add-commit-push 过程中，会报错如下：! [rejected] master -> master (non-fast-forward)
    hint: its remote counterpart. Integrate the remote changes (e.g.
    hint: 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.
-   程序员 B 必须首先手动解决冲突，而后再走一遍：add-commit-push 才能推送成功
