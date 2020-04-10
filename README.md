## 我的i3配置文件-i3status分支

不同的状态栏：[*polybar*](https://github.com/Kuari/i3-wm-config) *i3status*

语言 ：*中文* [*English*](https://github.com/Kuari/i3-wm-config/tree/i3status/en)

<br />

## 截图

![my_desktop](my_desktop.png)

<br />

## 安装

>此处默认配置好基础系统和安装好图形化以及i3-wm

### 需要的软件

* *i3-wm* : 窗口管理器
* *i3gaps* : 设置窗口间距
* *feh* : 设置背景图片
* *compton* : 终端透明
* *xfce4-terminal* : 终端
* *i3status* : 状态栏
* *i3lock-fancy-git* : 锁屏

#### 1.安装字体
```bash
yaourt -S fft-font-awesome
```
#### 2.安装需要的包
```bash
yaourt -S xfce4-terminal feh compton i3-gaps i3lock-fancy-git i3status
```
#### 3.配置
在文件`.xinitrc`加入如下
```bash
exec compton -b &
exec i3 -V >> ~/.config/i3/log/i3log-$(date +'%F-%k-%M-%S') 2>&1
```

将`.i3status.conf`文件移动到`/home/$USER`下来

```bash
mv .i3status.conf ~
```

<br />

## 快捷键

#### 基础

| 功能                           | 按键                     | 备注             |
| ------------------------------ | ------------------------ | ---------------- |
| 向上/下/左/右移动              | $mod+k/j/h/l             |                  |
| 切换分区                       | $mod+1/2/3/4/5/6/7/8/9/0 |                  |
| 移动窗口到目标分区             | $mod+Shift+1/2/3/.../0   |                  |
| 关闭i3-wm                      | $mod+Shift+e             |                  |
| 关闭窗口                       | $mod+q                   |                  |
| 移动窗口到上/下/左/右侧        | $mod+Shift+k/j/h/l       |                  |
| 更改布局为横向/竖向            | $mod+h/v                 |                  |
| 窗口全屏/取消全屏              | $mod+f                   |                  |
| 隐藏窗口                       | $mod+-                   |                  |
| 切换显示隐藏窗口（为浮动状态） | $mod+Shift+-             |                  |
| 浮动窗口取消浮动               | $mod+Shift+space         |                  |
| 调高音量5%                     | $mod+F3                  |                  |
| 调低音量5%                     | $mod+F2                  |                  |
| 打开/关闭声音                  | $mod+F1                  |                  |
| 锁屏                           | $mod+F12                 | 需要安装i3-fancy |

#### 软件

* 此处需要安装相应的软件才可实现

| 功能                      | 按键         | 备注               |
| ------------------------- | ------------ | ------------------ |
| 终端                      | $mod+enter   | 用的xfce4-terminal |
| firefox                   | $mod+Shift+f |                    |
| chromium                  | $mod+Shift+g |                    |
| slack                     | $mod+Shift+k |                    |
| steam                     | $mod+Shift+s |                    |
| thunderbird               | $mod+Ctrl+t  |                    |
| blueberry                 | $mod+Shift+b |                    |
| virtualbox中的win10虚拟机 | $mod+Shift+v |                    |
| ...                       | ...          | ...                |

<br />

## 自定义配置

### 1. 配置快捷键

```bash
bindsym $mod+<快捷键> exec <shell>
```

* 软件

需要确保软件已安装，且使用软件自带的启动命令

```bash
bindsym $mod+Shift+f exec firefox
```

* 运行脚本

```bash
 bindsym $mod+Shift+s exec bash ~/example.sh
```

* virtualbox虚拟机

此处为直接打开一个名为“win10”的虚拟机

```bash
bindsym $mod+Shift+v exec VBoxManage startvm "win10" --type gui
```

### 2. 配置背景图

```bash
exec_always --no-startup-id feh --bg-scale "/home/kuari/Picture/girl.png"
```

<br />

## 常用软件

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
        <th>音频播放</th>
        <th>vlc, mplayer</th>
    </tr>
    <tr>
        <th>office组件</th>
        <th>libreoffice, wps</th>
    </tr>
</table>