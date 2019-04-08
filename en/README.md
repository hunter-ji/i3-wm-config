## My i3 configuration file

Different status bars：[*polybar*](https://github.com/Kuari/i3-wm-config) *i3status*

Language ：*中文* [*English*](https://github.com/Kuari/i3-wm-config/tree/i3status/en)



### Screenshot

![my_desktop](../my_desktop.png)



### Required software

* *i3-wm* : window manager
* *i3gaps* : set window spacing
* *feh* : set background image
* *compton* : terminal transparency
* *xfce4-terminal* : terminal
* *i3status* : status bar
* *i3lock-fancy-git* : lock screen



### Installation

>The base system is configured by default and the graphical and i3-wm are installed.

#### 1.Install font
```bash
yaourt -S fft-font-awesome
```
#### 2.Install the required package
```bash
yaourt -S xfce4-terminal feh compton i3-gaps i3lock-fancy-git i3status
```
#### 3.Configuration
In the file `.xinitrc` is added as follows
```bash
exec compton -b &
exec i3 -V >> ~/.config/i3/log/i3log-$(date +'%F-%k-%M-%S') 2>&1
```

Move the `.i3status.conf` file to `/home/$USER`

```bash
mv .i3status.conf ~
```



### Most used software

<table>
    <tr>
        <th>features</th>
        <th>software</th>
    </tr>
    <tr>
        <th>Browser</th>
        <th>Firefox, chromium</th>
    </tr>
    <tr>
        <th>Input</th>
        <th>ibus, ibus-libpinyin</th>
    </tr>
    <tr>
        <th>Program startup</th>
        <th>rofi</th>
    </tr>
    <tr>
        <th>Mail</th>
        <th>thunderbird</th>
    </tr>
    <tr>
        <th>Editor</th>
        <th>vim</th>
    </tr>
    <tr>
        <th>Audio Player</th>
        <th>vlc, mplayer</th>
    </tr>
    <tr>
        <th>Office component</th>
        <th>libreoffice, wps</th>
    </tr>
</table>