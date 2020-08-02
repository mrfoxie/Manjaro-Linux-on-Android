# Manjaro Linux on Android
Install Manjaro on Android using Termux

## Requirements
- Android device running arm64 architecture and minimum version of 7.0 Nougat.
- At least 5GB free storage space
- Termux
- A VNC viewer

## Quick Start
Copy this and paste it in termux and follow steps to install

```
pkg install wget && wget https://raw.githubusercontent.com/infinyte7/Manjaro-Linux-on-Android/master/manjaro.sh && chmod +x manjaro.sh && ./manjaro.sh
```
## Demo

<img src="Images/manjaro_anki_demo.gif" height="335" width="600"></img>

## Disclaimer

The software and code samples available on this page are provided "as is" without warranty of any kind, either express or implied. <br/>**Use at your own risk.**

# Steps to install Manjaro
1. Install [termux](https://play.google.com/store/apps/details?id=com.termux) and [RealVNC](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android) from play store

| Termux | RealVNC |
|----------|:-------------:|
| <img src="Images/install_termux_img.png" height="528" width="265"></img> |  <img src="Images/realvnc.jpg" height="528" width="265"></img> |

2. To install Manjaro, copy following and paste it in termux
```
pkg install wget && wget https://raw.githubusercontent.com/infinyte7/Manjaro-Linux-on-Android/master/manjaro.sh && chmod +x manjaro.sh && ./manjaro.sh
```
<img src="Images/wget_manjaro.png" height="528" width="265"></img>

3. It will install missing dependencies. (For audio)

<img src="Images/missing_packages_2.png" height="528" width="265"></img>

4. Select "Install the latest rootfs"

<img src="Images/select_chroot.png" height="528" width="265"></img>

5. Specify the installation directory

<img src="Images/select_dir.png" height="528" width="265"></img>

6. Wait for the first installation to finish

<img src="Images/first_install.png" height="528" width="265"></img>

7. Select desktop environment, select as per your requirements

<img src="Images/select_DE.png" height="528" width="265"></img>

**Size**

| xfce4   |      lxqt      |  
|----------|:-------------:|
| <img src="Images/xfce4.png" height="528" width="265"></img> |  <img src="Images/lxqt.png" height="528" width="265"></img> |

8. Select an username

 <img src="Images/username_1.png" height="528" width="265"></img>  <img src="Images/username_2.png" height="528" width="265"></img> 

9. Enter password for the username

<img src="Images/password_1.png" height="528" width="265"></img> <img src="Images/password_2.png" height="528" width="265"></img>

10. Continue to install TigerVNC

<img src="Images/VNC.png" height="528" width="265"></img>

11. Wait for setup to finish 

<img src="Images/install_finish.png" height="528" width="265"></img>

12. To run Manjaro 
```
./manjaro.sh
```
Select ```Chroot into existing rootfs```

<img src="Images/select_existing.png" height="528" width="265"></img>

13. Access it in VNC viewer android app. Run vncserver and ```Enter new password and confirm password``` at first run
```
vncserver
```
<img src="Images/vncserver.png" height="528" width="265"></img>

14. Open RealVNC app and enter following
```
Address
localhost:1

Name
manjaro
```
Enter password for the user to access it.

<img src="Images/vnc_2.png" height="528" width="265"></img>

# Install Manjaro Demo

<img src="Images/install_manjaro.gif" height="528" width="265"></img>

# Install Software
If Manjaro installed with desktop environment then continue.
## Anki
1. Run Manjaro
```
./manjaro.sh
``` 
2. Then in Manjaro, run following.
```
sudo pacman -S anki
```
It will install Anki 2.1.15-1

3. Type anki to run it
```
anki
```
Or by selecting it in desktop environment

### Demo

<img src="Images/install_anki.gif" height="528" width="260"></img>

# Some tips
1. Change ```Picture Quality``` to ```High``` in VNC viewer android app
2. Change to lower resolution inside ```Manjaro Display Settings``` for small screen devices
3. Uninstall unused programs from Manjaro to get more storage space
4. Hacker Keyboard from Play store can be used
5. ```vncserver``` may be re-run to view it in vncviewer
Inside Manjaro console
```
vncserver -kill :1
``` 
```
vncserver
```
Then open VNC viewer android app to access it.

# Faq?
### Black screen on VNC viewer?
There are many solutions for that. But in some cases reinstalling desktop environment may solve the problems.<br/>
For example: xfce4, run this to install xfce4.
```
sudo pacman -S xfce4 xfce4-goodies
```
# Credits
ItsMeKuroro<br>
[https://forum.manjaro.org](https://forum.manjaro.org/t/how-to-run-the-official-manjaro-arm-edition-on-android-with-chroot-environment/151429)