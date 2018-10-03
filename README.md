## 我的i3配置文件

### 附上我的桌面
![my_desktop](my_desktop.png)

### 需要的工具

* i3:窗口管理器
* i3gaps:设置窗口间距
* feh:设置背景图片
* compton:终端透明
* xfce4-terminal:终端
* polybar:状态栏
* i3lock-fancy-git:锁屏

### 安装

>此处默认配置好基础系统和安装好图形化以及i3-wm

#### 1.安装字体
```
yaourt -S ttf-font-awesome
```
#### 2.安装需要的包
```
yaourt -S xfce4-terminal feh compton i3-gaps i3lock-fancy-git polybar-git
```
#### 3.配置
在文件`.xinitrc`加入如下
```
exec compton -b &
exec i3 -V >> ~/.config/i3/log/i3log-$(date +'%F-%k-%M-%S') 2>&1
```

### 遇到的问题
#### 1.依赖
依赖软件包括`alsa`,`MPD`等等,可以去[polybar的Github主页](https://github.com/jaagr/polybar)去查看相关文档。
#### 2.显示输出报错
报错内容为
```
Monitor 'eDP-1' not found or disconnected
```
这个问题需要看具体的硬件,可以查看[archlinux的xrander](https://wiki.archlinux.org/index.php/Xrandr),通过`xrander`查看自己主要适用的显示设备等等信息,然后修改i3和polybar配置文件内设备信息即可。


### 常用软件

<table>
    <tr>
        <th>功能</th>
        <th>软件</th>
    </tr>
    <tr>
        <th>浏览器</th>
        <th>Firefox, chromium</th>
    </tr>
    <tr>
        <th>输入法</th>
        <th>ibus, ibus-libpinyin</th>
    </tr>
    <tr>
        <th>程序启动</th>
        <th>rofi</th>
    </tr>
    <tr>
        <th>邮件</th>
        <th>thunderbird</th>
    </tr>
    <tr>
        <th>编辑器</th>
        <th>vim</th>
    </tr>
    <tr>
        <th>程序启动</th>
        <th>rofi</th>
    </tr>
    <tr>
        <th>音频播放</th>
        <th>vlc, mplayer</th>
    </tr>
    <tr>
        <th>office组件</th>
        <th>libreoffice, wps</th>
    </tr>
</table>
