# How-to

```
cd board/picopi/overlay/usr/sbin
wget https://raw.githubusercontent.com/adafruit/Adafruit-Retrogame/master/retrogame
chmod 755 retrogame

wget https://raw.githubusercontent.com/dbonates/bonatopi-files/master/S32retrogame
chmod 755 S32retrogame

sed -i '/# Delay helps peripherals/i \
/usr/sbin/S32retrogame start\
' pico8

cd ../..
mkdir boot && cd boot
wget https://raw.githubusercontent.com/dbonates/bonatopi-files/master/retrogame.cfg

cd ../../../../

# na duvida: make list-defconfigs
make picopi_defconfig
make
```
