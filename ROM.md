# 刷机

## Huawei Mate MT1-U06

  准备好boot.img、system.img、recovery.img、cust.img：
  ```shell
  adb reboot bootloader
  fastboot flash boot boot.img
  fastboot flash recovery recovery.img
  fastboot flash system system.img
  fastboot flash cust cust.img
  fastboot reboot
  adb wait-for-device
  adb reboot recovery
  ```