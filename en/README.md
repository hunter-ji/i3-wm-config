## My i3 configuration file

Different status bars：  **polybar** [**i3status**](https://github.com/Kuari/i3-wm-config/tree/i3status)

Language :  [*中文*](https://github.com/Kuari/i3-wm-config) *English*



### Screenshot

![my_desktop](../my_desktop.png)

### Required software

* *i3-wm* : window manager
* *i3gaps* : set window spacing
* *feh* : set background image
* *compton* : terminal transparency
* *xfce4-terminal* : terminal
* *polybar* : status bar
* *i3lock-fancy-git* : lock screen



### Installation

>The base system is configured by default and the graphical and i3-wm are installed.

#### 1.Install font
```
yaourt -S ttf-font-awesome
```
#### 2.Install the required package
```
yaourt -S xfce4-terminal feh compton i3-gaps i3lock-fancy-git polybar-git
```
#### 3.Configuration
In the file `.xinitrc` is added as follows
```
exec compton -b &
exec i3 -V >> ~/.config/i3/log/i3log-$(date +'%F-%k-%M-%S') 2>&1
```



### Problems encountered

#### 1.other software dependencies
Dependent software including `alsa`, `MPD`, etc., can go to [polybar's Github](https://github.com/jaagr/polybar) home page to view related documents.

#### 2.debugging
```
cd .config/polybar
bash launch.sh
```
Execute this command to debug and view its error. In addition to viewing the error here, according to the above configuration, i3 will output the log to `~/.config/i3/log/` after startup, you can directly view the log.

#### 3.display output error
The error message is
```
Monitor 'eDP-1' not found or disconnected
```
This problem needs to look at the specific hardware, you can view the [archlinux的xrander](https://wiki.archlinux.org/index.php/Xrandr), view the main display device and other information through xrander, and then modify the device information in the i3 and polybar configuration files.




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


