# Use Raspberry Pi GPIO with Arduino-cli

Forked from openenergymonitor/avrdude-rpi

Adding the script to arduino-cli allows the Raspberry Pi GPIO serial port to be used for flashing Arduino with the Raspberry Pi terminal. It adds DTR functionality to a spare GPIO pin so that Arduino can be serially flashed.

# Install dependencies

sudo apt-get install -y python-dev python-rpi.gpio minicom

# How to Use

1. Rename avrdude within arduino-cli directory to avrdude-original
2. Move avrdude and autoreset from this repo into the same folder as avrdude-original
3. Connect the Arduino reset pin to GPIO 18. Alternatively modify the "pin" variable in the autoreset file to chosen GPIO pin
4. Run arduino-cli as normal with target port as /dev/ttyAMA0
