sudo su

rpi-rw

cd /tmp

git clone https://github.com/pyserial/pyserial.git

cd pyserial

python setup.py install

pistar-watchdog.service stop

systemctl stop mmdvmhost.timer

systemctl stop mmdvmhost.service

git clone https://github.com/VR2VYE/Nextion.git

cd ~/Nextion

ls

cd Nextion_G4KLX

python nextion.py NX3224T024.tft /dev/ttyUSB0 （ USB0就是你LCD所接的端口，如果不是USB就更改为你LCD所接的端口）
