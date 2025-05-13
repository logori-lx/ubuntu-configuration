# Clash

# ubuntu下clash配置

### clash安装

首先需要先下载clash ，直接下载代码即可，rar文件就是clash压缩包

下载完成后，修改appimage的可执行权限

![mage1.png](https://p.sda1.dev/24/66a0dd4a442e2c804a33514abe399aec/image1.png)

![image2.png](https://p.sda1.dev/24/c009f684de050fc7e3863467ae9e8dec/image2.png)

修改完成后，点击Appimage文件即可运行

### 配置桌面快捷方式

根据下面代码创建clash.desktop

```bash
[Desktop Entry]
Encoding=UTF-8
Type=Application
#App name
Name=Clash
#App Icon file path
Icon=/home/xxx/Pictures/clash.jpeg
#whether boot with a terminal opened
Terminal=false
#AppImage desktop file path
Exec=/home/xxx/Desktop/clash-verge_1.6.2_amd64.AppImage
```

注意将Exec的路径修改成AppImage所在的路径，Icon应用图标的话可以自己在网上找一张图片，放在Icon对应的路径下

将.desktop文件拷贝到/usr/share/applications/目录下，并给予可执行权限

```bash
#将/path/to/.desktop 改成.desktop所在路径
sudo cp /path/to/.desktop /usr/share/applications/clash.desktop
sudo chmod +x /usr/share/applications/clash.desktop
```

即可在桌面找到clash

![image3.png](https://p.sda1.dev/24/61052cc9d38a5a627feaae5f14b73369/image3.png)

右键 Add to Favourites即可添加到侧边栏

![image4.png](https://p.sda1.dev/24/2bcf2ab1dc46bc5137a8400dfd15fea3/image4.png)

![image5.png](https://p.sda1.dev/24/1d0d420bdea767c61832ca82c5b5f1d2/image5.png)

### 配置开机自启动

将.desktop拷贝到~/.config/autostart即可

```bash
sudo cp ./clash.desktop ~/.config/autostart
sudo chmod +x ~/.config/autostart/clash.desktop
```
