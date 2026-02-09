# flush bootloader step
adafruit-nrfutil --verbose dfu serial \
    --package xiao_nrf52840_ble_bootloader-0.10.0_s140_7.3.0.zip
    -p /dev/cu.usbmodem14401 \
    -b 115200 \
    --singlebank \
    --touch 1200

刷新完毕后，Volume 会出现一个 XIAO-BOOT 的 USB drive，将 ZMK 固件 cp 进去即可
左手刷完毕后会，macOS 会出现弹窗，右手刷完则不会出现
