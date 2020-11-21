# Monitoring wood stove

MicroPython Project to monitor my wood stove.

## Tools to install

### esp32 python tool for flashing

```
pip3 install esptool
```

### How erase esp32 device

```
esptool.py --port /dev/tty.usbserial-0001 erase_flash
```

### How flash micropython firmware for esp32

```
esptool.py --chip esp32 --port /dev/tty.usbserial-0001 write_flash -z 0x1000 MicroPython_firmware/esp32-idf4-20200902-v1.13.bin
```

### Adafruit MicroPython Tool

Utility to interact with a MicroPython board over a serial connection.

```
sudo pip3 install adafruit-ampy
```

### Get information from your device

```
ampy -p /dev/tty.usbserial-0001 ls
```

### Put python file on the device

```
ampy -p /dev/tty.usbserial-0001 put boot.py
```

Interesting websites:

- <https://boneskull.com/micropython-on-esp32-part-1/>
- <https://github.com/scientifichackers/ampy>
- <https://micropython.org/download/esp32/>

Troubleshooting:

Fix issue for:
```
ampy.pyboard.PyboardError: could not enter raw repl
```

- <https://github.com/scientifichackers/ampy/issues/19#issuecomment-317126363>