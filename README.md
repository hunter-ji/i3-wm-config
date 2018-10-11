## 我的i3配置文件-i3status分支

### 附上我的桌面
![my_desktop](my_desktop.png)

### 需要的工具

* i3:窗口管理器
* i3gaps:设置窗口间距
* feh:设置背景图片
* compton:终端透明
* xfce4-terminal:终端
* i3status:状态栏
* i3lock-fancy-git:锁屏

### 安装

>此处默认配置好基础系统和安装好图形化以及i3-wm

#### 1.安装字体
```
yaourt -S fft-font-awesome
```
#### 2.安装需要的包
```
yaourt -S xfce4-terminal feh compton i3-gaps i3lock-fancy-git i3status
```
#### 3.配置
在文件`.xinitrc`加入如下
```
exec compton -b &
exec i3 -V >> ~/.config/i3/log/i3log-$(date +'%F-%k-%M-%S') 2>&1
```

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
