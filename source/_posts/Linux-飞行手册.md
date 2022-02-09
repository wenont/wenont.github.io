---

title: Linux 飞行手册
date: 2022-02-07 23:29:25
categories:
  - 技术
tags:
  - linux

---

使用的是 Pop_OS，基于 Ubuntu 的发行版。基本讲一些应用安装说明和 trobleshooting

 <!--more--> 
## 文字处理

### GoldenDict
用了很多年的字典软件
`sudo apt-get install goldendict`

将 internal player 改为 Qt Multimedia

~~“警告：内置播放器：ao_open_live()调用失败：无法打开设备：alsa，...”~~

~~推荐使用 mpv player 或者 vlc player，（需提前安装）。~~

~~外置播放其设置输入：mpv 或 cvlc ，保存即可。~~

### Notion

Notion 没有 Linux 桌面端应用，只能使用网页版。

- 将 Notion 网页添加到应用中：
  
  Chrome 打开 Notion 网页 > 右上角菜单 > More tools > Create shortcut..
  
  桌面上会产生一个 Notion 的 .desktop 快捷方式，在桌面打开终端：
  
  `sudo mv XXX.desktop /usr/share/applications`

### Obsidian

knowledge base

### Mark text

[https://github.com/marktext/marktext](https://github.com/marktext/marktext)

Markdown editor

### LaTeX - TeXlive

`sudo apt-get install texlive-full`

### ibus-rime

`sudo apt-get install ibus-rime`

按 F4 切换 Rime 内置输入法，切换半角/全角

[https://github.com/rime/home/wiki/RimeWithIBus](https://github.com/rime/home/wiki/RimeWithIBus)

[https://github.com/rime/ibus-rime](https://github.com/rime/ibus-rime)

```yaml
# ~/.config/ibus/rime/luna_pinyin_simp.custom.yaml

menu:
  page_size: 9
patch:
  "style/display_tray_icon": true
  "style/horizontal": true
```

```yaml
# ~/.config/ibus/rime/ibus_rime.yaml

style:
   horizontal: true
```

### ~~Typora~~

1.0.0 版本开始收费了，弃用

`sudo apt-get install typora`



---



## 编程

### Anaconda 3

`conda —version`

`conda 4.10.3`

- 安装位置：`/opt/anaconda3`

- 安装后 Anaconda Navigator 出现界面缩放尺寸过小的问题。
  
  解决方案：
  
  (In Terminal) `anaconda-navigator`
  
  Go to File > Preferences, and check “Enable High DPI Scaling”
  
  [https://askubuntu.com/questions/1252036/zoom-and-anaconda-navigator-have-weird-scaling](https://askubuntu.com/questions/1252036/zoom-and-anaconda-navigator-have-weird-scaling)

### Node.js

[https://github.com/nodejs/help/wiki/Installation](https://github.com/nodejs/help/wiki/Installation)

为了将 `Node,js` 命令添加到默认路经，使用软链接将 `node`, `npm`, 和 `npx` 放入 `usr/bin/` 中:
```bash
sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/node /usr/bin/node

sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/npm /usr/bin/npm

sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/npx /usr/bin/npx

# 如果下载了 Angular 和 Hexo 的包：
sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/ng /usr/bin/ng

sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/hexo /usr/bin/hexo
```

### VS Code

---

## 工具类

### Onedriver (Currently used)

[https://github.com/jstaf/onedriver](https://github.com/jstaf/onedriver)

**install CLI**

[https://software.opensuse.org/download.html?project=home%3Ajstaf&package=onedriver](https://software.opensuse.org/download.html?project=home%3Ajstaf&package=onedriver)

### Zoom

[https://zoom.us/download#client_4meeting](https://zoom.us/download#client_4meeting)

### Discord

### rclone for Onedrive (with bugs)

[https://www.linuxuprising.com/2018/07/how-to-mount-onedrive-in-linux-using.html](https://www.linuxuprising.com/2018/07/how-to-mount-onedrive-in-linux-using.html)

[https://rclone.org/downloads/](https://rclone.org/downloads/)

## 其它

### Pop OS: systemd-boot can’t detect Windows

[Pop OS: systemd-boot can't detect Windows](https://unix.stackexchange.com/questions/610779/pop-os-systemd-boot-cant-detect-windows)

### Wechat - deepin-wine version wechat client

[https://www.jianshu.com/p/ecbd320c7ff5](https://www.jianshu.com/p/ecbd320c7ff5)

[https://github.com/zq1997/deepin-wine](https://github.com/zq1997/deepin-wine)

**高分辨率缩放问题**

[https://github.com/wszqkzqk/deepin-wine-ubuntu/issues/45](https://github.com/wszqkzqk/deepin-wine-ubuntu/issues/45)

**注意，deepin-wine的位置应该在：**

`/home/username/.deepinwine/deepin-wine6-stable/bin/wine`

**输入字体是小方块 问题** 

[link](https://blog.csdn.net/qq_37624415/article/details/82228572?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.channel_param&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.channel_param)

**manjaro 版**

[https://oscarcx.com/tech/manjaro-xfce-setup.html](https://oscarcx.com/tech/manjaro-xfce-setup.html)

### Qv2ray - v2ray client

[https://tmtsub.cc/link/4MEpzkcZECiwHHge?sub=3](https://tmtsub.cc/link/4MEpzkcZECiwHHge?sub=3)

## 外观

### dracula theme

[https://draculatheme.com](https://draculatheme.com/)

### Pimp terminal

[https://drasite.com/blog/Pimp%20my%20terminal](https://drasite.com/blog/Pimp%20my%20terminal)

### gnome-tweaks

[https://www.opendesktop.org/p/1297346](https://www.opendesktop.org/p/1297346)

### plank - a dock application

[https://draculatheme.com/plank](https://draculatheme.com/plank)

### Flat Remix Blue - Linux Theme

[https://www.gnome-look.org/p/1214931/](https://www.gnome-look.org/p/1214931/)

### Panel Transparency - gnome extension

[https://extensions.gnome.org/extension/1011/dynamic-panel-transparency/](https://extensions.gnome.org/extension/1011/dynamic-panel-transparency/)

[http://us.archive.ubuntu.com/ubuntu/](http://us.archive.ubuntu.com/ubuntu/)

### Blur my shell - gnome extension

[https://extensions.gnome.org/extension/3193/blur-my-shell/#](https://extensions.gnome.org/extension/3193/blur-my-shell/#)

### Fcitx 5

[https://github.com/hosxy/Fcitx5-Material-Color](https://github.com/hosxy/Fcitx5-Material-Color)