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

## 相关知识

### 路线图
- **boot.img**是什么？结构？是否可以自己制作？怎么做？
  > 我想刷入一个自己编译的AOSP生成的ROM

- **recovery.img**是什么？结构？是否可以自己制作？怎么做？
  > 同上

- **system.img**是什么？结构？是否可以自己制作？怎么做？
  > 同上

- **cust.img**是什么？结构？是否可以自己制作？怎么做？
  > 同上

- `fastboot flash`命令是干什么？
  > 了解刷机过程

- 是否可能刷入一个AOSP源码编译出来的ROM？
  > 如果可以，那么就可以放到手机上调试，而不用放到模拟器里面，模拟器太慢

- `adb reboot bootloader`是干什么？
  > 了解刷机过程

- `adb reboot recovery`是干什么？
  > 了解刷机过程

- **twrp**是啥？
  > 这个好像是个做recovery镜像项目，了解一下他们