## 目录
### 修改账户名(account name)，电脑名称（full name），用户名（user name）
### Sublime Text 3 配置与插件
### Docker 与 Docker Compose
### golang


- - - - -
## Sublime Text 3 配置与插件

[MarkDown Editing](https://github.com/SublimeText-Markdown/MarkdownEditing)    
SublimeText不仅仅是能够查看和编辑 Markdown 文件，但它会视它们为格式很糟糕的纯文本。这个插件通过适当的颜色高亮和其它功能来更好地完成这些任务。关于如何在SublimeText下高效些东西可参见文章：[sublime text 2(3)下的Markdown写作](http://www.cnblogs.com/jadeboy/p/4165449.html) 抑或是前段时间写下的[追寻高效工作的一路折腾㈡](http://www.jeffjade.com/2015/08/28/2015-08-28-Write-Morkdown/)

[SideBarFolders](https://github.com/titoBouzout/SideBarFolders)
打开的文件夹都太多了? 来用这个来管理文件夹，世界原来也可以这么美好。⭐️⭐️⭐️⭐️⭐️
![SideBarFolders](https://image.nicelinks.site/sublimetext-folder.jpg)
微注：如何使用 Sublime 快速切换项目？ 使用 SideBarFolders 插件的朋友们，近期是否也发现这插件可能无法正常使用了？(至少无法重新 install 使用)。不过，没关系，Sublime Text 本身就提供了多项目管理(包括快速切换)的功能，即 ToolBar 的 Project；只须将当前项目，作为 Project 保存在本地(Project => Save Project As..)，那么即可通过 Command + Ctrl + P ( windows 是 Ctrl + Alt + P)来快速切换项目了，还能编辑，关闭，Clear，Add Floder to Project等等功能；切换项目之间，还能保留与之对应的项目所打开的标签，实在很好；具体可参见：[Projects in Sublime Text – Saving](http://www.joshuawinn.com/understanding-projects-in-sublime-text-saving-switching-etc/), [Switching, Etc](http://www.joshuawinn.com/understanding-projects-in-sublime-text-saving-switching-etc/) (update@17-02-24)。

[ColorPicker](http://weslly.github.io/ColorPicker/)
通常，如果你想使用一个颜色选择器则可能打开 Photoshop 或 GIMP。而在 Sublime Text 中，你可以使用内置的颜色选择器。安装完成后，只要按下Ctrl / Cmd + Shift + C 快捷键。

[SublimeREPL](https://github.com/wuub/SublimeREPL)
这可能是对程序员很有用的插件。SublimeREPL 允许你在 Sublime Text 中运行各种语言（NodeJS ， Python，Ruby， Scala 和 Haskell 等等）。

[Ctags插件](https://github.com/SublimeText/CTags)
有童鞋抱怨Sublime Text不能支持函数的跳转（比如像Eclipse那样，按住Control点击该方法或者对象，即可跳转到定义的地方； Alt+←即可回到原处）。其实Sublime Text也可以借助插件实现之（当然，有些情况下:Can not find defination）毕竟这个也是借助正则来匹配完成的。因此这个也就要求代码很规范。这个插件相对来讲会有些麻烦，具体的可以参见:Sublime Text ctags 的配置.

[SublimeLinter插件](https://github.com/SublimeLinter)
SublimeLinter 是前端编码利器——[Sublime Text](http://www.cnblogs.com/lhb25/archive/2012/12/28/best-tools-for-web-development-b.html) 的一款插件，用于高亮提示用户编写的代码中存在的不规范和错误的写法，支持 JavaScript、CSS、HTML、Java、PHP、Python、Ruby 等十多种开发语言。这篇文章介绍如何在 Windows 中配置 SublimeLinter 进行 JS & CSS 校验。
比如写例如像lua这样的弱语言脚本代码，有这个可以规避掉很多不该有的低级错误吧？当然这也需要你SublimeLinter安装完毕之后再安装一个SublimeLinter-lua即可。具体的使用可以参见：[借助 SublimeLinter 编写高质量的 JavaScript & CSS 代码](http://www.cnblogs.com/lhb25/archive/2013/05/02/sublimelinter-for-js-css-coding.html)

[SideBarEnhancements插件](https://github.com/titoBouzout/SideBarEnhancements)
SideBarEnhancements是一款很实用的右键菜单增强插件；在安装该插件前，在Sublime Text左侧FOLDERS栏中点击右键，只有寥寥几个简单的功能；安装了就相当于给其丰了大胸一般。⭐️⭐️⭐️⭐️
更强大的是，该插件还能让我们自定义快捷键呼出某个浏览器以预览页面！这样就不用到项目目录下寻找和拖动到特定浏览器中预览了。
安装此插件后，点击菜单栏的preferences->package setting->side bar->Key Building-User，键入以下代码：

```
[   
    { "keys": ["ctrl+shift+c"], "command": "copy_path" },
    //chrome
    { "keys": ["f2"], "command": "side_bar_files_open_with",
            "args": {
                "paths": [],
                "application": "C:\\Users\\jeffj\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe",
                "extensions":".*"
            }
     }
]
```

这里设置按Ctrl+Shift+C复制文件路径，按F2即可在Chrome浏览器预览效果(如果需要的话，也可以根据自己的需要为Firefox，Safari，IE，Opera等加上)，当然你也可以自己定义喜欢的快捷键，最后注意代码中的浏览器路径要以自己电脑里的文件路径为准。

[HTML-CSS-JS Prettify](https://github.com/victorporof/Sublime-HTMLPrettify)
一款集成了格式化（美化）html、css、js三种文件类型的插件，即便html,js写在PHP文件之内。插件依赖于nodejs，因此需要事先安装nodejs，然后才可以正常运行。插件安装完成后，快捷键ctrl+shift+H完成当前文件的美化操作。插件对html、css文件的美化不是非常满意，但还可以，后面将说明如何修改css美化脚本。本人用起来超级爽的，鉴于篇幅，就不赘述，可以参见[这篇](http://frontenddev.org/article/sublime-does-text-three-plug-ins-html-and-css-js-prettify.html)介绍。

[SublimeTmpl 快速生成文件模板](https://github.com/kairyou/SublimeTmpl)
一直都很奇怪为什么sublime text 3没有新建文件模板的功能，像html头部的DTD声明每次都要复制粘贴。用SublimeTmpl这款插件终于可以解脱了，SublimeTmpl能新建html、css、javascript、php、python、ruby六种类型的文件模板，所有的文件模板都在插件目录的templates文件夹里，可以自定义编辑文件模板。⭐️⭐️⭐️⭐️+
SublimeTmpl默认的快捷键:
```
ctrl+alt+h html
ctrl+alt+j javascript
ctrl+alt+c css
ctrl+alt+p php
ctrl+alt+r ruby
ctrl+alt+shift+p python
```

如果想要新建其他类型的文件模板的话，先自定义文件模板方在templates文件夹里，再分别打开Default (Windows).sublime-keymap、Default.sublime-commands、Main.sublime-menu、SublimeTmpl.sublime-settings这四个文件照着里面的格式自定义想要新建的类型，这里就详细介绍了，请各位自己折腾哈~

SFTP：快速编辑远程服务器文件
在Win下用Xftp 和 WinScp，被这种需要切换点击or F5刷新的手动操作蛋疼到无语；故此一遇见这SFTP，顿觉这世界都美好了许多。当然Sublime下面也有些其他同步插件，比如FtpSnyc，但是配置起来的错误提示一点都不人性化，就毫不留情的舍弃了。Sublime下有SFTP，只要Ctrl+S即可同步本地到服务器，妥妥的爽歪歪有么有？如何配置，请参见在 [Sublime Text中使用 SFTP 插件快速编辑远程服务器文件](http://blog.wpjam.com/m/sublime-text-2-sftp/);如欲使用FtpSync可参见[Sublime使用及FtpSync远程同步](http://liuwanlin.info/sublimeshi-yong-ji-ftpsyncyuan-cheng-tong-bu/)；大道至简，因简而悦；开心垒码，值得折腾。

[WakaTime](https://wakatime.com/) – 记录你的Code时间;
WakaTime可以做到精确地统计到你花在某个项目上的时间;WakaTime针对不同的IDE，拥有不同的插件，在Sublime上安装着插件，就能统计到我使用Sublime进行的所有项目的行为。可以高效管理和知晓自己code时间；并且，统计完善, 适合发朋友圈装逼（如果你喜欢的话）~
> Waka的基本设计和rescuetime类似。每个人注册完将获取一个key，装一个客户端，把key输进去（登陆是同一个道理），然后它就把本地的所有行为带个key扔给服务器来统计，一段时间之后给你个报表。不过Waka做的真的很精准，精确到每一个文件用了多少秒，每一种语言用了多少时间。
![wakatime](https://image.nicelinks.site/WakaTime.jpg)
安装和使用都很简单，请参见这里。另外一篇比较详细的文章时间都去哪了?用RescueTime和WakaTime来记录你的时间,对RescueTime和WakaTime有一个更为详细的叙述，可以一读。

[TrailingSpaces](https://packagecontrol.io/packages/TrailingSpaces): 检测并一键去除代码中多余的空格
这款插件本身倒没什么。但是如果你写前端，并处在当下这个时代，她就很有用（话说，Eslint 等工程限制级工具必须使用吧，那么项目对于空格的约定肯定是有必要的，但也会令你头疼吧？那么这款插件的作用就体现出来了）她可以自动将多余的空格标红，以示提醒。当然，如果你想一键摒除之，这也很好办，加入一点配置即可：在 Preferences / Key Bindings – User加上如下代码即可（数组内部，当然快捷键可自行约定，我这里用的是 ctrl+shift+d ）；（⭐️⭐️⭐️⭐️⭐️ For Front-End）
```
{ "keys": ["ctrl+shift+d"], "command": "delete_trailing_spaces" }
```

ConvertToUTF8 支持 GBK, BIG5, EUC-KR, EUC-JP, Shift_JIS 等编码的插件
Bracket Highlighter 用于匹配括号，引号和html标签。对于很长的代码很有用。安装好之后，不需要设置插件会自动生效

Emmet(Zen Coding)快速生成HTML代码段的插件，强大到无与伦比:可以超快速编写HTML/CSS/JS，当然这个插件还支持多种编译环境，如常见的：Eclipse/Aptana、Coda、Notepad++、Adobe Dreamweaver、TextMate等，web开发必备！！！。⭐️⭐️⭐️⭐️⭐️
jsFormat 格式化js代码，懂者自懂；强迫症Coder必备！默认快捷键Ctrl+Alt+F。
phpFormat 格式化php代码，懂者自懂；强迫症Coder必备！

[WordCount](https://github.com/titoBouzout/WordCount) 可以实时显示当前文件的字数。
[PlainTasks](https://github.com/aziz/PlainTasks) 又是一个插件顶一个软件的东东。**这个是有点用的**

## vim 配置
```
主要命令参数
      .vimrc通常用于指定vim的编辑参数和外观环境。下面列出常用的命令参数及其含义:
"打开语法高亮
syntax on

"使用配色方案
colorscheme desert

"打开文件类型检测功能
filetype on

"不同文件类型采用不同缩进
filetype indent on

"允许使用插件
filetype plugin on
filetype plugin indent on

"关闭vi模式
set nocp

"与windows共享剪贴板
set clipboard+=unnamed

"取消VI兼容，VI键盘模式不易用
set nocompatible

"显示行号, 或set number
set nu

"历史命令保存行数 
set history=100 

"当文件被外部改变时自动读取
set autoread 

"取消自动备份及产生swp文件
set nobackup
set nowb
set noswapfile

"允许使用鼠标点击定位
set mouse=a

"允许区域选择
set selection=exclusive
set selectmode=mouse,key

"高亮光标所在行
set cursorline

"取消光标闪烁
set novisualbell

"总是显示状态行
set laststatus=2

"状态栏显示当前执行的命令
set showcmd

"标尺功能，显示当前光标所在行列号
set ruler

"设置命令行高度为3
set cmdheight=3

"粘贴时保持格式
set paste

"高亮显示匹配的括号
set showmatch

"在搜索的时候忽略大小写
set ignorecase
 
"高亮被搜索的句子
set hlsearch
 
"在搜索时，输入的词句的逐字符高亮（类似firefox的搜索）
set incsearch

"继承前一行的缩进方式，特别适用于多行注释
set autoindent

"为C程序提供自动缩进
set smartindent

"使用C样式的缩进
set cindent

"制表符为4
set tabstop=4

"统一缩进为4
set softtabstop=4
set shiftwidth=4

"允许使用退格键，或set backspace=2
set backspace=eol,start,indent
set whichwrap+=<,>,h,l

"取消换行
set nowrap

"启动的时候不显示那个援助索马里儿童的提示
set shortmess=atI

"在被分割的窗口间显示空白，便于阅读
set fillchars=vert:\ ,stl:\ ,stlnc:\

"光标移动到buffer的顶部和底部时保持3行距离, 或set so=3
set scrolloff=3

"设定默认解码
set fenc=utf-8
set fencs=utf-8,usc-bom,euc-jp,gb18030,gbk,gb2312,cp936

"设定字体
set guifont=Courier_New:h11:cANSI
set guifontwide=新宋体:h11:cGB2312
 
"设定编码
set enc=utf-8
set fileencodings=ucs-bom,utf-8,chinese
set langmenu=zh_CN.UTF-8
language message zh_CN.UTF-8
source $VIMRUNTIME/delmenu.vim
source $VIMRUNTIME/menu.vim

"自动补全
filetype plugin indent on
set completeopt=longest,menu

"自动补全命令时候使用菜单式匹配列表
set wildmenu
autocmd FileType ruby,eruby set omnifunc=rubycomplete#Complete
autocmd FileType python set omnifunc=pythoncomplete#Complete
autocmd FileType javascript set omnifunc=javascriptcomplete#CompleteJS
autocmd FileType html set omnifunc=htmlcomplete#CompleteTags
autocmd FileType css set omnifunc=csscomplete#CompleteCSS
autocmd FileType xml set omnifunc=xmlcomplete#CompleteTags
autocmd FileType java set omnifunc=javacomplete#Complet

```

## Alfred workflow
- [deanishe/alfred-stackoverflow](https://github.com/deanishe/alfred-stackoverflow/releases)
- [pawelgrzybek/Alfred-github-search](https://github.com/pawelgrzybek/Alfred-github-search)
- [Kapeli/Dash-Alfred-Workflow](https://github.com/Kapeli/Dash-Alfred-Workflow)
- [bigluck/alfred2-hash](https://github.com/BigLuck/alfred2-hash)