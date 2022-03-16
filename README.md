# pi-pico-c-blink

# build
```
cd pi-pico-c-blink
ln -s $PICO_SDK_PATH/external/pico_sdk_import.cmake .
mkdir build
cd $_
cmake ..
make -j4
```

# flash into pi-pico 
```
#cd pi-pico-c-blink/build

openocd -f interface/picoprobe.cfg -f target/rp2040.cfg -c "program blink.elf verify reset exit"
```

or just use [picoprog.sh](https://gist.github.com/hidsh/4dc19284ddea311825950b2a1be621bc)

# check the output from `puts()` in raspberry pi pico via usb-serial

```
screen /dev/tty.usbmodem142401

Hello World

Hello World

Hello World
   :

(type C-a C-\ then y to exit)
```
