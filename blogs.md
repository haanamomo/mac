# 快捷键 

锁屏 `cmd + control + q`

截屏 `cmd + shift + 3/4/5`

截屏并复制 `cmd + control + shift + 3/4/5`

显示所有窗口 `control + ↑`

显示当前app的所有窗口 `control + ↓`

切换app `cmd + tab`

反向切换app `cmd + shift + tab`

切换tab `cmd + shift + []`

# 查看CPU型号

```sh
sysctl machdep.cpu.brand_string
```

# 语音备忘录的位置

```sh
~/Library/Application Support/com.apple.voicememos
```

# 报错the application cannot be opened

```
chmod +x SomeApp.app/Contents/MacOS/\*
```

# diskutil

* 列出所有设备：`diskutil list`
* 格式化为ExFAT：`diskutil eraseDisk ExFAT <new disk name> </dev/DiskNodeID>`

# brew

## Install

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## 防止自动更新

```
export  HOMEBREW_NO_AUTO_UPDATE=1
```

## 使用国内镜像

> [清华大学镜像使用说明](https://mirror.tuna.tsinghua.edu.cn/help/homebrew/)

```sh
cd "$(brew --repo)"
git remote set-url origin git://mirrors.ustc.edu.cn/brew.git

cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin git://mirrors.ustc.edu.cn/homebrew-core.git

brew update

echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zshrc
source ~/.zshrc
```

## 下载时开启proxy

```sh
ALL_PEOXY=socks5://localhost:1086 brew install <pkg>
```

## 检查app是否是通过brew安装的

```sh
brew list | grep vim
```

## 搜索库中的软件

```
brew search /正则表达式/
```

## 添加第三方仓库 brew tap

```sh
brew tap haanamomo/repo

brew tap  # 查看已经tap的第三方仓库
```

默认这些仓库来源于github, 实际仓库名是homebrew-repo

## brew服务管理

```sh
# 列出brew安装的, 支持brew管理的服务
brew services list

brew services start/stop/restart mysql@5.7
```

# alfred

* file search: ` `或者`'`开启文件搜索，`shift`浏览，`enter`打开
* clipboard
* snippet
* trash：打开垃圾桶

> [从零开始学习 Alfred](https://sspai.com/post/32979)

# 日历自然语言

* `control + option + space` 快速创建日历
* `cmd + 0` 打开日历
* `cmd + y` 添加日记

/w = /work 日历名英文可以直接识别首字母

at                  地点 
today/tomorrow      今天/明天
next Mon            下周一
after 10 days       10天之后
every Tue           每周二
every 2             每月2号
every 2 weeks on Tue 隔周周二
1/12-1/13           1月12日到1月13日
3pm-5:45pm          下午3点到5点45 
alert 5 min         提前五分钟提醒
todo                添加待办事项: 
due 11/27 8p      添加截止日期




      
