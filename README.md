# Cool-Retro-Term-For-Windows-2023-
Credit to https://gist.github.com/h3r/2d5dcb2f64cf34b6f7fdad85c57c1a45, https://tvc-16.science/cool-retro-term-wsl2.html, and Specifics https://gist.github.com/specifics.

1. Enable the Windows Developer mode:
 - Press the **windows** key  > type **"Windows update and settings"** > hit Enter
 - **Click** on **"For Developers"** tab on the left panel
 - **Choose** "Developer mode"
  
  ![](https://i.imgur.com/80C1sq3.png)

 - Press **windows** key > type **"Power Shell"** > right click > click on **"Run as Administrator"** and paste:
  ```bash
  Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
  ```

2. Install a distro of your choice. I used Ubuntu on my system. (Try 20.04.6 LTS if you need compatibility with qt5)
![](https://i.imgur.com/4BvQ6X2.png)


3. Verify that yout VMP and WSL is on: **windows key** > enter **Windows feature** > **Turn Windows features on or off** then
![](https://i.imgur.com/9EWeM0T.png)


Note: That some people may have to enable virtualizaion in their UEFI/BIOS (https://support.microsoft.com/en-us/windows/enable-virtualization-on-windows-11-pcs-c5578302-6e43-4b4b-a449-8ced115f58e1)
   
4. Install **Windows Subsystem for Linux** (WSL)
![](https://i.imgur.com/Z8OWOId.png)

  
5. Run your distro terminal environment and make your username and pasword.

6. Exit and run WSL (**WIN+R**, then **"wsl"**, then **"OK"**)

![](https://i.imgur.com/eut7drb.png)

   
8. Once the WSL terminal is loaded run the following commands (Use **CTRL+SHIFT+V** to paste)
   
```bash
cd /mnt/c/users/WINDOWS-USERNAME-HERE
sudo apt-get install git
sudo apt-get update
sudo apt-get upgrade
sudo apt install build-essential qmlscene qt5-qmake qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools qtdeclarative5-dev qml-module-qtquick-controls2 qml-module-qtgraphicaleffects qml-module-qtquick-dialogs qml-module-qtquick-localstorage qml-module-qtquick-window2 qml-module-qt-labs-settings qml-module-qt-labs-folderlistmodel qtquickcontrols2-5-dev
strip --remove-section=.note.ABI-tag /usr/lib/x86_64-linux-gnu/libQt5Core.so.5
```

For Ubuntu latest ed.:
```bash
sudo apt install libfuse2
```

Or for Ubuntu versions < 22.04:
```bash
sudo apt-get install fuse libfuse2
```

Then:
```bash
wget https://github.com/Swordfish90/cool-retro-term/releases/download/1.1.1/Cool-Retro-Term-1.1.1-x86_64.AppImage
chmod a+x Cool-Retro-Term-1.1.1-x86_64.AppImage
./Cool-Retro-Term-1.1.1-x86_64.AppImage
```
