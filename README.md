# Clash

# ubuntu下clash配置

### clash安装

首先需要先下载clash ，可以通过这个[链接](https://github.com/logori-lx/ubuntu-configuration/blob/main/clash-verge_1.6.2_amd64.AppImage)下载

下载完成后，修改appimage的可执行权限

![image.png](attachment:ea48769a-9bb9-4781-8e4d-9cfd3c46768f:image.png)

![image.png](attachment:d9f364e4-3f18-42b8-8dc3-43a42b5df319:image.png)

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

![image.png](attachment:7981968e-e941-4bd2-a55c-d5935a60021b:image.png)

右键 Add to Favourites即可添加到侧边栏

![image.png](attachment:688c256e-3b56-4692-a4b5-90abae30f30f:image.png)

![image.png](attachment:cda91ac0-48e8-4dd8-bd83-182b920e35f0:image.png)

### 配置开机自启动

将.desktop拷贝到~/.config/autostart即可

```bash
sudo cp ./clash.desktop ~/.config/autostart
sudo chmod +x ~/.config/autostart/clash.desktop
```