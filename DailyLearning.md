#2016-11-27 00:39:44   
1. 最近提交到 GitHub 上的代码老是需要输入用户名和密码，找了一下原因，原来是在 `git push` 的时候用的 `https` 的方式，更换成 `ssh` 的方式就好了。命令如下：
    - `git remote rm origin`
    - `git remote add origin git@github.com:username/xxx.git` username 为你的 github 用户名 xxx 为你的仓库名称
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
2016-12-19 14:02:30
5. 什么是 Socket
- 它是使用标准 Unix 文件描述符（file descriptor）和其它程序通讯的方式。 -- 《C语言 Socket 简单编程指南》
6. Internet 套接字的两种类型（其实还有很多 eg: Raw Sockets)
    - Stream Sockets (流格式)  流式套接字：可靠的双向通讯的数据流。有顺序
    - Datagram Socket (数据包格式) 数据报套接字：无连接套接字
    - 所有小于 1024 的端口号都被系统保留了
7. socket() 函数
8. bind() 函数
9. listen() 函数
10. accept() 函数
11. send() 和 recv() 函数
12. sendto() 和 recvfrom() 函数
13. close() 和 shutdown() 函数
14. getpeername() 函数
15. gethostname() 函数
16. DNS: 代表域名服务（Domain Name Service）
    - 功能：你给它一个容易记忆的某个站点地址，它给你 IP 地址（然后你就可以使用 bind(), connect(), sendto() 或者其它函数） 
2016-12-25 17:28:03
## Android: Gradle: 官方解释： Gradle是一个基于Apache Ant和Apache Maven概念的项目自动化建构工具  [链接在这](http://blog.csdn.net/lee576/article/details/50673033)
2017-01-03 22:45:34   
17. `iOS 7` 之后 `UITabBarContriller` 的 `UITabBarItem` 的图标新加了 `UIImageRenderingMode: ` 的方法返回值为 `UIImage`
2017-01-06 21:16:55   
18. 多播代理 （MulticastDelegate）
19. UINavigationBar 透明设置 背景图片 设置一张空`UIImage`:  `UIImage *image = [[UIImage alloc] init];
        [self.navigationController.navigationBar setBackgroundImage:image forBarMetrics:UIBarMetricsDefault];
        // 设置导航条的样式
        self.navigationBar.barStyle = UIBarStyleBlackOpaque;`
20. `UIBarButtonItem`: `leftBarButtonItem`的 `- (instancetype)initWithCustomView:(UIView *)customView;` ; `self.navigationItem.titleView` 和 `rightBarButtonItems` 的 `rightBarButtonItems` 基本 的自定义 `navigationBar`的需求
2017-01-08 12:04:11
21. `RAC` `@weakify()` `@strongify()`
2017-01-09 23:15:00
22. iOS Sandbox 
2017-01-10 08:11:03
23. C：`switch `判断表达式应该具有整数值（包括 `char` 类型）。`case` 标签必须是整型（包括`char`）常量或者整数常量表达式（公包含整数常量表达式）。不能用变量作为`case`标签
24. C: `12.3` 默认类型为 `double`; `12.3f` 为 `float`
2017-01-11 21:52:20
25. `UIScreen` 的  `bound`, `frame`, `scale`属性
    `UIScreen` 对象包含了整个屏幕的边界矩形。当构造应用的用户界面接口时，你应该使用该对象的属性来获得推荐的矩形大小，用以构造你的程序窗口。
```
    CGRect bound = [UIScreen mainScreen].bounds; //返回的是带有状态栏的 rect
    CGRect frame = [UIScreen mainScreen].applicationFrame; //返回的是不带有状态栏的 rect
    CGFloat scale = [UIScreen mainScreen].scale; // 得到设备的自然分辨率 ，1：普通屏幕  2：视网膜屏幕  3：6p 和 7p
```
2017-01-15 22:22:39   
26. `UITableView` 的 `UITableViewDelegate`和 `UITableViewDataSource` 从 控制器中分离，在控制器中引入`dataSource`时要用属性引入，否则是无法执行 `dataSource`的方法的。
27. 如果要在分类`Category`中添加并属性，请使用`Objective-C Associated Objects ` 具体 [在这里](http://blog.leichunfeng.com/blog/2015/06/26/objective-c-associated-objects-implementation-principle/)
28. `UIButton`如果用`adjustsImageWhenHighlighted` 这个方法无法实现长按后图片有阴影的现象，那就我一定 `setHighlighted`方法。忘了方法名有没有ed 了。
29. `tableHeaderView`和`headerView`是两个不同的，前者是只有一个，后者是每个`section` 的。
2017-01-18 12:12:08   
30. 两个联合在一起使用才会出现 你想要的效果！！！内容居左并向右偏移10个单位
```
        self.nameBtn.contentHorizontalAlignment = UIControlContentHorizontalAlignmentLeft;
        self.nameBtn.contentEdgeInsets = UIEdgeInsetsMake(0, 10, 0, 0);
```
2017-01-19 23:10:02   
31. 图片平铺 保真方法：`- (UIImage *)stretchableImageWithLeftCapWidth:(NSInteger)leftCapWidth topCapHeight:(NSInteger)topCapHeight ` 
2017-01-20 18:40:46   
32. 懒加载：懒加载其实就是重写对象的 `getter` 方法，需要注意在 `getter` 方法里切勿使用 `self.xxx`，因为`self.xxx`会调用 `getter` 方法，造成死循环
2017-01-27 12:14:34   
33. SVN: `trunk`:主干，当前开发项目的主目录; `branches`: 分支目录，添加非主线功能时使用，开发测试之后，可以合并到主干项目中。`tags`: 标记目录，通常作为我现在在版本的备份。
34. `Git`是一款开源的分布式版本控制工具
35. `Git`的版本号是一个 40 位的哈希值，而`SVN`中的版本号是一个递增的整数
2017-01-30 12:55:32   
36. 隐式动画：当对于非`Root Layer`的部分属性进行修改时，默认会自动产生一些动画效果 而这些属性被称为`Animatable Properties`（可动画属性）ps: 每一个`UIView`内部都默认关联着一个`CALayer`，我们可用称这个`Layer`为`Root Layer`(根层)
37. `nonatomic` 和 `atomic` ：`atomic` 线程安全，需要消耗大量的资源； `nonatomic`：非线程安全，适合内存小的移动设备。
38. 所有属性都声明为`nonatomic`；尽量避免抢夺同一块资源；尽量将加锁、资源抢夺的业务逻辑交给服务器处理，减小移动客户端的压力。
39. 在给自定义`View` 的`xib` 文件命名时不要用控制器去掉`Controller`后的名字，因为控制器在加载时会先匹配去掉`Controller`后的名字的`xib`文件，如果没有再去找有没有全名的`xib`文件，如果没有才会创建一个空的控制器，在找`xib`文件时它，如果控制器发现有去掉`Controller`后名字的`xib`文件，但不是给自己用的时，就会崩掉。遇到这种情况可能会感觉很无厘头，所以自己在给`xib`文件命名时注意。语言不是很通顺。
2017-02-01 13:51:09   
40. 服务器的多值参数用`&`拼接
2017-02-16 19:24:11   
41. 加密：现在大多数公司的服务器都是存储的密文，不再存储明文，客户端加密后形成密文，然后上传到服务器。用户再次登陆时，服务器比对的是密文。现在如果忘记密码，只能修改，不能找回，也是这个原因。
42. 代码混淆：因为现在有反编译，所以发布之前最好进行混淆代码。
2017-02-17 09:36:46   
43. __kindof is a new feature of the Objective-C language announced by Apple, together with other new features such as Nullability Annotations and Generics. Xcode 7 is needed to use __kindof, so be sure to use that when going over through this post.
44. You need to attach your bar button item to your custom view controller, not to the navigation controller. `self.navigationItem.rightBarButtonItem = rightBtnItem;` 而不是 `self.navigationController.navigationItem.rightBarButtonItem = rightBtnItem;`
2017-03-05 16:10   
45. Docker 中的仓库，镜像，容器的理解，来一张图吧！![](https://sfault-image.b0.upaiyun.com/404/256/404256463-545a1d114c535_articlex)
46. `FROM: Ubuntu` 容器中没有 `sudo` 和 `curl` 使用命令 `apt-get -qq update` 和 `apt-get -qq -y curl`
2017-03-15 10:58:09   
47. `golang` 时间戳与字符串的转换：
    ```
    package main

import (
	"fmt"
	"time"
)
    func main () {
	//获取时间戳
	timestamp := time.Now().Unix()
	fmt.Println("time1:",timestamp)

	//格式化为字符串,tm为Time类型
	tm := time.Unix(timestamp, 0)
	fmt.Println(tm.Format("2006-01-02 03:04:05 PM"))
	fmt.Println(tm.Format("02/01/2006 15:04:05 PM"))
	
	//从字符串转为时间戳，第一个参数是格式，第二个是要转换的时间字符串
	tm2, _ := time.Parse("01/02/2006", "02/08/2015")
	fmt.Println(tm2.Unix())
}    
    ```
2017-03-16 11:31:23   
48. 什么是 `chaincode` 
    - `chaincode`（链码）是部署在 Hyperledger fabric 网络节点上，可被调用与分布式账本进行交互的一段程序代码，也即狭义范畴上的“智能合约”。链码在 VP 节点上的隔离沙盒（目前为 Docker 容器）中执行，并通过 `gRPC` 协议来被相应的 VP 节点调用和查询。
2017-03-17 15:06:02   
49. `Ubuntu` 配置 `Go` 语言的环境变量，在`/etc/profile`文件中 , `vim /etc/profile` 添加 
```
export GOROOT=/usr/lib/go
export GOPATH=$HOME/gocode
```
这两行代码。 **注**： `$GOPATH` 不是你的工作目录
2017-03-20 10:58:08   
50. [SSH原理与运用（一）：远程登录](http://www.ruanyifeng.com/blog/2011/12/ssh_remote_login.html)
51. iOS 顶层视图：可以用于添加或移除顶层对象
```
- (UIViewController *)topViewController {
    UIViewController *resultVC;
    resultVC = [self _topViewController:[[UIApplication sharedApplication].keyWindow rootViewController]];
    while (resultVC.presentedViewController) {
        resultVC = [self _topViewController:resultVC.presentedViewController];
    }
    return resultVC;
}

- (UIViewController *)_topViewController:(UIViewController *)vc {
    if ([vc isKindOfClass:[UINavigationController class]]) {
        return [self _topViewController:[(UINavigationController *)vc topViewController]];
    } else if ([vc isKindOfClass:[UITabBarController class]]) {
        return [self _topViewController:[(UITabBarController *)vc selectedViewController]];
    } else {
        return vc;
    }
    return nil;
}
```
使用方法：
```
UIViewController *topmostVC = [self topViewController];
```
 2017-03-26 13:02:08   
52. Ubuntu 16.10 修改字符编码设置
    如果出现汉字乱码的情况可以使用下面的方法去设置
第一步：`sudo vim /var/lib/locales/supported.d/en ` 添加如下内容：
```
zh_CN.GBK GBK
zh_CN.GB2312 GB2312
zh_CN. UTF-8 UTF-8
```
第二步：` sudo dpkg-reconfigure --force locales ` 强制更新设置
第三步： 在 `/etc/environment` 中添加或修改部分：
```
LANGUAGE="zh_CN:en_US:en"
LANG="zh_CN.GBK"
LC_NUMERIC="zh_CN.GBK"
LC_TIME="zh_CN.GBK"
LC_MONETARY="zh_CN.GBK"
LC_PAPER="zh_CN.GBK"
LC_IDENTIFICATION="zh_CN.GBK"
LC_NAME="zh_CN.GBK"
LC_ADDRESS="zh_CN.GBK"
LC_TELEPHONE="zh_CN.GBK"
LC_MEASUREMENT="zh_CN.GBK"
LC_CTYLE="zh_CN.GBK"
LC_ALL="zh_CN.GBK"
```
**最后重启系统**
53. `52. Ubuntu 16.10 修改字符编码设置` 不用了，找到一种新的方法来修改时区
            date tzselect
按照你要选择的时区做出选择操作，这里不详细说了。
- 查看时区的命令
```
    date -R
```
2017-05-10 15:27:33   
54. Docker CE 与 Docker EE 不同： 一个是个人版本， 一个是企业版本。 具体请参考[链接](http://blog.csdn.net/liumiaocn/article/details/60468257)
55. Ubuntu 安装 golang
Try:
```
$ sudo apt-get install golang-go
```
... but if that's too old for you, try:
```
$ sudo apt-get install golang-1.8-go
```
Or use Go's official (non-Deb) [downloads:](https://golang.org/dl/)
If you're using Ubuntu 16.04 LTS and are unable to install golang-1.8-go, then you can also use the longsleep/golang-backports PPA:
```
sudo add-apt-repository ppa:longsleep/golang-backports
sudo apt-get update
sudo apt-get install golang-go
```
**查看 Ubuntu 版本**
```
lsb_release -a
```
2017-05-15 10:25:39   
56. 绑定端口到指定接口
```
$ sudo docker run -p [([<host_interface>:[host_port]])|(<host_port>):]<container_port>[/udp] <image> <cmd>
```
![Docker 简介](https://opskumu.gitbooks.io/docker/content/chapter1.html)

2017-05-23 19:26:58   

57. docker-compose 文件 的扩展名 `.yml` `.yaml` 有什么不同
```
File extensions do not have any bearing or impact on the content of the file. You can hold YAML content in files with any extension: .yml, .yaml or indeed anything else.

The (rather sparse) YAML FAQ recommends that you use .yaml in preference to .yml, but for historic reasons many Windows programmers are still scared of using extensions with more than three characters and so opt to use .yml instead.

So, what really matters is what is inside the file, rather than what its extension is.
```

58. fabric-1.0-alpha2 `make docker` 时出现 `unrecognized import path "golang.org/x/tools/go/gcexportdata"` ,`cp: cannot stat ‘build/docker/gotools/bin/protoc-gen-go’: No such file or directory`
查看你的 golang 版本，请按要求升级到  1.7 以上。不说怎么升级了。

59. 用行动证明了自己的sha 我的天= =   Liunx 系统 树状图 直接用 `tree`命令生成就好了
### 2017-06-15 10:39:22
60. maven package 和 install 有什么区别
package 是把 jar 包 打到项目的 target 下，而 install 是把 target 下的 jar 包安装到本地仓库，供其它项目使用。
### 2017-06-19 06:57:52
61. 删除 SQL 表中某字段字符为空，Null，零长度的字符串
```
delete * from T_Nav_Team where title is null
delete * from T_Nav_Team where isnull(title) = true
delete * from T_Nav_Team where len(title)<3
select * from table where length(column) = 某个值 
```
length()是计算字符串长度的函数，不同的数据库，可能不一样。
<<<<<<< Updated upstream

### 2017-06-26 11:24:01
62. 升级 Git    
要获得最新版本的Git，你需要在Ubuntu中添加Git的维护者团队PPA（归档包）到您的软件源列表。使用以下命令添加PPA：
```
$ sudo add-apt-repository ppa:git-core/ppa
```
然后更新源列表并升级`git`：
```
$ sudo apt-get update
$ sudo apt-get install -y git
```
现在，你应该已经是最新版本，使用以下命令查看`git`版本：
```
$ git --version
```
### 2017-07-03 10:16:36
63. 今天我们也来聊聊 Mac 与服务器 ssh 无密码登录的问题   

-  编辑 `vim ~/.bash_profile`，如果你以前没新建过，那么新建它；有的话就打开修改添加。   如果是 `zsh` 的话，`vim ~/.zshrc`, 道理相同，在最后面追加就可以了。
- 添加别名： `alias 9.2="ssh root@192.168.9.2"`    !!!等号前后不能出现空格!!!
-  使配置命令生效： `bash` 下执行 `source ~/.bash_profile`，此条命令是使 `bash` 重新载入配置令刚才命令生效。 如果是 `zsh`，就 `source ~/.zshrc`

#### ssh 无密码登录
- 生成密钥：
```
#可以看到两个密钥文件：id_rsa（私钥） id_rsa.pub（公钥）
#公钥是加密，私钥是解密（不要外传私钥）
$ ssh-keygen -t rsa -C "email@example.com" 
```
- 将公钥复制到服务器
```
# 先登录到远程服务器
# 有的话添加（有的话不要删掉，因为别人可能做过免密登录），没有则新建一个就行
# 以上比较要注意的是： 公钥要放在登录服务器所用的账号的家目录下，比如你用 abc 登录# 远程服务器，就要把公钥 放到 /home/abc/.ssh/下， authorized_keys 文件也是在这个目录# 下。
cd ~/.ssh
cat -n /root/.ssh/id_rsa.pub >> authorized_keys
```

- 修改服务端 `~/.ssh` 文件夹权限为 `700`，修改 `id_rsa.pub` 的权限和 `authorized_keys`的仅限
```
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```
- 在 Mac 端 使用 `ssh-copy-id User@ip` 然后输入一次密码就可以了，以后就可以正常使用别名登录了
- - - - -
# 2017-07-06 10:43:51
安装 Java 环境
- Ubuntu 16.04
- Java 8

- 添加 PPA
```
$ sudo add-apt-repository ppa:webupd8team/java
```
- 升级并安装 installer script, 如果是 Java 9 就用 `oracle-java9-installer `
```
$ sudo apt update; sudo apt install oracle-java8-installer
```
- 查看 Java 版本
```
$ javac -version
```
- 设置 Java 环境变量
```
$ sudo apt install oracle-java8-set-default
```
=======
### 2017-06-23 14:41:11
62. git `No user exists for uid 501`
遇到一个 git 的坑，提示`No user exists for uid 501`, 重启一下终端就好了，系统有更新的话需要重启终端更新一下配置。
>>>>>>> Stashed changes

- - - - -
2017-07-10 16:54:53
64. 这里应该是要写 docker deamon 那个错误的，当时没记，现在已经忘记了......
- - - - -
2017-07-12 13:47:43
<<<<<<< Updated upstream
65. shell 脚本解决问题; [Bash 命令](https://tiswww.case.edu/php/chet/bash/bashref.html)
- - - - -
2017-07-16 12:57:40
66. ESLint 是一个插件化的 javascript 代码检测工具，它可以用于检查常见的 JavaScript 代码错误，也可以进行代码风格检查，这样我们就可以根据自己的喜好指定一套 ESLint 配置，然后应用到所编写的项目上，从而实现辅助编码规范的执行，有效控制项目代码的质量。
67. HTML表单是一个包含表单元素的区域， 表单使用<form> 标签创建。表单能够包含 <a target="_blank" title="HTML input 元素，比如文本字段、复选框、单选框、提交按钮等等。表单还可以包含<a target="_blank" title="HTML menus、<a target="_blank" title="HTML textarea、<a target="_blank" title="HTML fieldset、<a target="_blank" title="HTML legend 和 <a target="_blank" title="HTML label 元素。注意，<form >元素是块级元素，其前后会产生折行。
```
<form action="reg.ashx" method="post">
<!--表单元素在这里-->
</form>
```
68. 这两天工作中使用到了  `Node.js` 于是乎开始看代码学习。`const joi = require('joi');` joi 是 hapijs 自带的数据校验模块，他已经高度封装常用的校验功能，[如何优雅地使用 joi 对数据进行校验?](http://imweb.io/topic/572561798a0819f17b7d9d3e) 相信你会喜欢上它。
69. [`Node.js` 有两种运行模式](http://www.ruanyifeng.com/blog/2013/01/javascript_strict_mode.html)：正常模式；严格模式（`'use strict';`）。 设立『严格模式』的目的，主要有以下几个：
    - 消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为;
    - 消除代码运行的一些不安全之处，保证代码运行的安全；
    - 提高编译器效率，增加运行速度；
    - 为未来新版本的Javascript做好铺垫。

70. [`Node.js URL 模块的使用`](https://itbilu.com/nodejs/core/NJGRdjgU.html): Node.js中的URL模块，用于将URL字符串解析为对象或将对象格式化为URL字符串，该模块较为简单，共包括3个方法: 
    - URL 各部分说明
    - 将URL 字符串转换为对象：`url.parse(urlStr)[, parseQueryString][, slashesDenoteHost])`
    - 将对象格式化为URL 字符串： `url.format(urlObj)`
    - URL路径处理：`url.resolve(from, to)`

对于一个 URL 字符串，其组成部分会有所有不同，其中有些部分只有在URL字符串中存在时，对应字段才会出现在解析后对象中。以下是一个 URL 例子：
```
http://user:pass@host.com:8080/p/a/t/h?query=string#hash
```
解析后对象字段如下：

`href`: 解析前的完整原始 URL，协议名和主机名已转为小写
例如:` 'http://user:pass@host.com:8080/p/a/t/h?query=string#hash'`

`protocol`: 请求协议，小写
例如: `'http:'`

`slashes`: 协议的“：”号后是否有“/”
例如: true or false

`host`: URL主机名，包括端口信息，小写
例如:` 'host.com:8080'`

`auth`: URL中的认证信息
例如: `'user:pass'`

`hostname`: 主机名，小写
例如:` 'host.com'`

`port`: 主机的端口号
例如: `'8080'`

`pathname`: URL中路径
例如: `'/p/a/t/h'`

`search`: 查询对象，即：queryString，包括之前的问号“?”
例如: `'?query=string'`

`path`: `pathname` 和 `search` 的合集
例如:` '/p/a/t/h?query=string'`

`query`: 查询字符串中的参数部分（问号后面部分字符串），或者使用 querystring.parse() 解析后返回的对象
例如: `'query=string' or {'query':'string'}`

`hash`: 锚点部分（即：“#”及其后的部分）
例如: `'#hash'`

将URL字符串转换为对象：`url.parse(urlStr[, parseQueryString][, slashesDenoteHost])`
`url.parse()`方法用于解析URL对象，解析后返回一个JSON对象。示例如下:
```
var url = require('url');

var urlString = 'http://user:pass@host.com:8080/p/a/t/h?query=string#hash';
var result = url.parse(urlString);
console.log(result);

//输出结果如下
{ protocol: 'http:',
  slashes: true,
  auth: 'user:pass',
  host: 'host.com:8080',
  port: '8080',
  hostname: 'host.com',
  hash: '#hash',
  search: '?query=string',
  query: 'query=string',
  pathname: '/p/a/t/h',
  path: '/p/a/t/h?query=string',
  href: 'http://user:pass@host.com:8080/p/a/t/h?query=string#hash' }
```

将对象格式化为URL字符串：`url.format(urlObj)`
```
var url = require('url');

var urlObj = { protocol: 'http:',
	slashes: true,
	hostname: 'itbilu.com',
	port: 80,
	hash: '#hash',
	search: '?query=string',
	path: '/nodejs?query=string'
}
var result = url.format(urlObj);
console.log(result);

//输出结果如下
http://itbilu.com:80?query=string#hash
```

URL路径处理：url.resolve(from, to)
url.resolve()方法用于处理URL路径，也可以用于处理锚点。示例如下：
```
url.resolve('/one/two/three', 'four')         // '/one/two/four'
url.resolve('http://example.com/', '/one')    // 'http://example.com/one'
url.resolve('http://example.com/one', '/two') // 'http://example.com/two'
```
- - - - -
2017-07-17 10:48:11
71. Node.js 使用 `===` 即会判断类型，又会判断结果。
72. 箭头函数 `=>`
```
// ES5
var selected = allJobs.filter(function (job) {
    return job.isSelected();
});

//ES6
var selected = allJobs.filter(job => job.isSelected());
```
当你需要只有一个参数的函数，箭头函数的语法可以简化为 `Identifier => Expression`, 直接省略了 `function` 和 `return` 关键字，连括号和结尾的分号也同时省略了。
73. 调试 `Node.js` 使用 `node-inspector`
- - - - -
2017-07-18 10:49:02
74. Node.js 的路径问题
```
__dirname: 总是返回被执行的 js 所在文件夹的绝对路径
__filename: 总是返回被执行的 js 的绝对路径
process.cwd(): 总是返回运行 node 命令时所在的文件夹的绝对路径
```
75. `ssh-keygen` 命令:
`ssh-keygen` 命令用于为 “ssh” 生成、管理和转换认证密钥，它支持 RSA 和 DSA 两种认证密钥。 语法 ssh-keygen(选项) 选项 
- `-b`：指定密钥长度；
- `-e`：读取 openssh 的私钥或者公钥文件； 
- `-C`：添加注释； 
- `-f`：指定用来保存密钥的文件名； 
- `-i`：读取未加密的 ssh-v2 兼容的私钥/公钥文件，然后在标准输出设备上显示 openssh 兼容的私钥/公钥；
- `-l`：显示公钥文件的指纹数据； 
- `-N`：提供一个新密语； 
- `-P`：提供（旧）密语； 
- `-q`：静默模式； 
- `-t`：指定要创建的密钥类型

76. Linux Ubuntu 
`sudo npm install xxx` 出现 这样的错误信息`gyp WARN EACCES ......`
需要添加 ` --unsafe-perm` 这样来解决，如`sudo npm install --unsafe-perm --verbose -g sails`
- - - - -
2017-07-19 22:39:23      

77. 云主机 `hostname` 修改名称    
如果你经常要使用云主机而云主机的名称又太长，那应用 `hostname` 来修改吧，如果你想了解更多关于 `hostname` 命令的内容，你可以[点击这里](http://www.cnblogs.com/kerrycode/p/3595724.html)也许有不正确的地方，所以实践出真知。
### Ubuntu 
- 永久修改 `hostname` ：修改 `/etc/hostname` 文件，重启 用`uname -n` 来判断是否借点书和成功
- 临时修改：`hostname new_your_hostname`
=======
65. shell 脚本解决问题
- - - - -
2017-07-13 09:47:04
- `winston` 为 Node.js 的日志框架
>>>>>>> Stashed changes

- - - - -
2017-07-20 10:27:42
78. node.js 首先去目录下查找有没有 `index.js` 文件 ,如果没有,继续查找有没有 `default.js` 文件,接着查找有没有 `index.json`文件,最后查找有没有 `default.json` 文件.
- - - - -
2017-07-25 13:09:18
79. shell 语法 
判断文件夹是否存在 
- `-d`: 文件夹
```shell
if [ ! -d "folder"]; then
  # This is your code
fi
```

- `-f`：文件
```shell
if [! -f "file"]; then
  touch "$file"
fi
```

- `-n`: 判断一个变量是否有值
```shell
if [! -n "$var"]; then
  echo "$var is empty"
  exit 0
fi
```

- `-x`：参数判断 `$folder` 是否存在并且是否具有可执行权限
```shell
if [! -x "folder"]; then
  mkdir "$folder"
fi
```
- - - - -
80. node 模块发布到 npm 社区
在发布时版本号要符合要求：
```
版本格式：主版号.次版号.修订号，版号递增规则如下：

主版号：当你做了不相容的 API 修改，
次版号：当你做了向下相容的功能性新增，
修订号：当你做了向下相容的问题修正。
先行版号及版本编译资讯可以加到「主版号.次版号.修订号」的后面，作为延伸。
```
要修改 `package.json` 的版本号。把代码提交到 git 服务端（如果你用的是 Git的话）
`npm publish --tag 0.1.0.1` 这样
[来自这里的解释](https://github.com/npm/npm/issues/9266): make sure that you've changed the version of your application in the package.json file as well not only the version on git repo
- - - - -
81. Ubuntu 16.04 重启 mysql ：`systemctl restart mysql`
- - - - -
2017-07-29 16:24:12
82. Shell 脚本语言
BASH_SOURCE[0] 等于 BASH_SOURCE,  取得当执行的 shell 文件所在的路径及文件名。
test.sh
```
#!/bin/sh
set -e
echo "${BASH_SOURCE[0]}"
echo "${BASH_SOURCE}"
echo "$(dirname "${BASH_SOURCE[0]}" )"
DIR="$( cd "$(dirname "${BASH_SOURCE[0]}")" && pwd )"
echo $DIR
```
source ./test.sh 输出为
```
./test.sh
./test.sh
.
/root/github/banquanjia
```
- - - - -
2017-08-14 14:43:04
83. IDEA 修改类名 shift+f6 或者 鼠标右键 refactor->rename
84. idea 自定义代码模板 ：`Editor -> Live Templates -> output`, 参考 原模板

- - - - -
2017-08-15 20:00:55
85. java + maven + mongodb
[mongodb 官方文档](http://mongodb.github.io/mongo-java-driver/2.13/getting-started/installation-guide/)
```
<dependencies>
    <dependency>
        <groupId>org.mongodb</groupId>
        <artifactId>mongo-java-driver</artifactId>
        <version>2.13.2</version>
    </dependency>
</dependencies>
```
86. 国内 mongodb-driver jar 下载地址
 [国内 mongodb-driver jar 下载地址](http://central.maven.org/maven2/org/mongodb/mongo-java-driver/)

