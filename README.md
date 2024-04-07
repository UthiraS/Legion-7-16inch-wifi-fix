# Legion-7-16inch-wifi-fix
Fix for WIFI adapter on uthira-Legion-7-16IRX9 for Ubuntu 20.04

**Remove** any random things you tried like the following one:

`sudo apt remove rtw89-dkms`

else you may get random errors like this,

_2.008814] kernel: rtw89_8852ce 0000:72:00.0: failed to register hw
[    2.008827] kernel: rtw89_8852ce 0000:72:00.0: failed to register core hw
[    2.008836] kernel: rtw89_8852ce 0000:72:00.0: failed to register core
[    2.056359] kernel: rtw89_8852ce: probe of 0000:72:00.0 failed with error -22_

**Next**, 
1. `git clone https://github.com/lwfinger/rtw89`
2. `git checkout 6dc944`
3. goto the folder
4. `make clean`
5. `make`
6. `sudo make install`
7. sudo reboot now to check if wifi adapter shows up

**If no**
1. Look for some rtw8852c* file in /lib/firmware/rtw89
2. If not, goto http://security.ubuntu.com/ubuntu/pool/main/l/linux-firmware/
3. Download linux-firmware_20240202.git36777504-0ubuntu1_amd64.deb
4. Double click the file. If it already exists, remove the existing one and install it in software center
5. I didnot place any config at this location - /etc/modprobe.d/<dev_name>.conf

Now the wifi adapter should show up





