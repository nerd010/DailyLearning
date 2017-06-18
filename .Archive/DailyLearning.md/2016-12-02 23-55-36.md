#2016-11-27 00:39:44
1. 最近提交到 GitHub 上的代码老是需要输入用户名和密码，找了一下原因，原来是在 `git push` 的时候用的 `https` 的方式，更换成 `ssh` 的方式就好了。命令如下：
    - `git remote rm origin`
    - `git remote add origin git@github.com:username/xxx.git` username 为你的github 用户名 xxx 为你的仓库名称
    - `git   push --set-upstream origin master`
#2016-11-27 18:55:56
2. iOS 10 使用 UNNotification 本地通知
