#2016-11-27 00:39:44
1. 最近提交到 GitHub 上的代码老是需要输入用户名和密码，找了一下原因，原来是在 `git push` 的时候用的 `https` 的方式，更换成 `ssh` 的方式就好了。命令如下：
    - `git remote rm origin`
    - `git remote add origin git@github.com:username/xxx.git` username 为你的github 用户名 xxx 为你的仓库名称
    - `git   push --set-upstream origin master`
#2016-11-27 18:55:56
2. iOS 10 使用 UNNotification 本地通知
#2016-12-02 23:56:34
3.  NSArray
    - `removeObject:` 会枚举数组，向每一个对象发送`isEqual:`消息。`isEqual:`的作用是判断当前对象和传入对象所饮食的数据是否相等（返回`YES`或`NO`）。不同的类可以根据自身情况覆盖`isEqual:`并实现相应的逻辑。
    - `removeObjectIdenticalTo:`方法不会比较对象所包含的数据，只会比较指向对象的指针。因此，该方法只会移除数组所保存的那些和传入对象指针完全相同的指针。
#2016-12-05 11:37:57
4.  Simulated Metrics
- 可以用来预览用户界面的各种外观效果