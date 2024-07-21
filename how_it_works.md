# Ubuntu-Studio-Bitwig-Widows-VST


Please note its my second languages so there could grammatical errors.

## 1. Ubuntu Studio 24.04 LTS iso download
Download Ubuntu Studio
https://ubuntustudio.org/download/
Flash the iso to usb stick and install Ubuntu-Studio on your disk.


## 2. Ubdate Ubuntu Studio 24.04 LTS
update the system


## 3. Install wine staging + windows vst plugin
install wine staging
https://wiki.winehq.org/Ubuntu

downlaod + install gorangrooves drums studio standard v 2
https://library.gorangrooves.com/virtual-instruments/handy-drums-studio-standard-v2/
download the tiral exe from website with creat a account
install the exe with wine you only need to install the vst3, demo samples and midi files
with that done we can go to step 4 to install yabridge


## 4. Install yabridge
offical github site installer


https://github.com/robbert-vdh/yabridge

---
fast installer

downlaod the yabridge-x.x.x.tar.gz
https://github.com/robbert-vdh/yabridge/releases


open terminal where you stored the file
typ than tar -C ~/.local/share -xavf yabridge-x.y.z.tar.gz
``` js
tar -C ~/.local/share -xavf yabridge-
```


go to location from yaybrige
``` js
cd ~/.local/share/yabridge/
```
than add location for VST from wine
``` js
./yabridgectl add ~/.wine/drive_c/Program\ Files/Common\ Files/VST3/
```
uname = username from u currently session
is that not working you can go over /home/uname/.wine/drive_c/Program\ Files/Common\ Files/VST3/

sync the plugins
``` js
./yabridgectl sync
```

uname = username from u currently session
- normally the plugins will stored under ~/.vst3 or /home/uname/.vst3
- remember that for setup the path in bitwig
- check the plugins over Dolphin you can activ the hidden folders/files with press ctrl + h

## 5. Install bitwig beta or the stable

For me i continue in beta.

!!!Important do not install the flatpak version!!!
When you install the flatpak version the yabdridgectl will not working. I found the info in the README file from yabdridge.

Download bitwig over website
https://www.bitwig.com

``` js
chmod +x bitwig-studio-5.x-beta-x.deb
```
``` js
sudo apt install ./bitwig-studio-5.x-beta-x.deb
```
if something wrong with the installer you can try to run
``` js
sudo apt --fix-broken install
```
than install the package again with
``` js
sudo apt install ./bitwig-studio-5.x-beta-x.deb
```
This steps works for me well. I hope that helps somebody.
