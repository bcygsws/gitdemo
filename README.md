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

## 区分远程仓库的 https 和 SSH 的地址

-   SSH 方式，不需要频繁切换账号，每一个账号对应一套公钥和私钥（公钥和私钥文件均存放于/.ssh 下），在/.ssh 文件下设置有私钥文件 id_rsa,在 github 账号上添加了 SSH Key(字符串从 id_rsa.pub 公钥文件中获取)
-   HTTPS 方式，多账号时，需要切换(win10 系统凭证管理器中会记忆存储一些账号，切换账号时，需要在凭证管理器中删除旧的账号信息)
