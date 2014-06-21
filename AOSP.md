# AOSP

## repo
- 将工作区的源码切换到 android-1.6_r1.5:
  
  ```shell
  repo init -b android-1.6_r1.5
  repo sync
  ```

## 编译android-1.6_r1.5

### 环境
- Debian 7.2
- git 1.7
- JDK 5

  ```shell
  wget https://myown-android-s3c2410.googlecode.com/files/jdk-1_5_0_22-linux-i586.bin
  chmod a+x jdk-1_5_0_22-linux-i586.bin
  ./jdk-1_5_0_22-linux-i586.bin
  mv jdk1.5.0_22/ /usr/lib/jvm/
  rm /etc/alternatives/java
  ln -s /usr/lib/jvm/jdk1.5.0_22/jre/bin/java /etc/alternatives/java
  rm /etc/alternatives/javac
  ln -s /usr/lib/jvm/jdk1.5.0_22/bin/javac /etc/alternatives/javac
  ```

- bison 2.5

  ```shell
  apt-get install bison
  ```

- zlib1g-dev

  ```shell
  apt-get install zlib1g-dev
  ```

- zip 3.0

  ```shell
  apt-get install zip
  ```

- flex 2.5

  ```shell
  apt-get install flex
  ```

- libncurses5-dev 5.9-10

  ```shell
  apt-get install libncurses5-dev
  ```

- gperf 3.0

  ```bash
  apt-get install gperf
  ```

- gcc 4.4

  ```bash
  apt-get install gcc-4.4
  update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.4 40
  ```

- g++ 4.4

  ```bash
  apt-get install g++-4.4
  update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.4 40
  ```


### make时遇到的问题
- > make: *** [out/host/linux-x86/obj/EXECUTABLES/aapt_intermediates/AaptAssets.o] Error 1
  
  修改`frameworks/base/tools/aapt/Android.mk`：

  ```Makefile
  LOCAL_CFLAGS += -Wno-format-y2k
  ```
  改为
  ```Makefile
  LOCAL_CFLAGS += -Wno-format-y2k -fpermissive
  ```

  [参考][1]

- > make: *** [out/host/linux-x86/obj/STATIC_LIBRARIES/libutils_intermediates/AssetManager.o] Error 1
  
  修改`frameworks/base/libs/utils/Android.mk`：

  ```Makefile
  LOCAL_CFLAGS += -DLIBUTILS_NATIVE=1 $(TOOL_CFLAGS)
  ```
  
  改为
  
  ```Makefile
  ...
  LOCAL_CFLAGS += -DLIBUTILS_NATIVE=1 $(TOOL_CFLAGS) -fpermissive
  ```

  [参考][1]


- > make: *** [out/host/linux-x86/obj/EXECUTABLES/grxmlcompile_intermediates/grxmlcompile.o] Error 1

  ```shell
  cd external/srec
  wget "https://github.com/CyanogenMod/android_external_srec/commit/4d7ae7b79eda47e489669fbbe1f91ec501d42fb2.diff"
  patch -p1 < 4d7ae7b79eda47e489669fbbe1f91ec501d42fb2.diff
  rm -f 4d7ae7b79eda47e489669fbbe1f91ec501d42fb2.diff
  cd ../..
  ```

  [参考][1]


- > make: *** [out/host/linux-x86/obj/EXECUTABLES/adb_intermediates/adb] Error 1
  
  ```shell
  apt-get install libncurses5-dev
  ```

  [参考][2]

- > make: *** [out/host/linux-x86/obj/EXECUTABLES/bb2sym_intermediates/trace_reader.o] Error 1

  修改`development/emulator/qtools/trace_reader.cpp`:

  ```cpp
  char *end = rindex(mmap_path, '@');
  if (end == NULL)
    return NULL;
  char *start = rindex(mmap_path, '/');
  ```

  改为

  ```cpp
  const char *end = rindex(mmap_path, '@');
  if (end == NULL)
    return NULL;
  const char *start = rindex(mmap_path, '/');
  ```

  [参考1][3]
  [参考2][4]

- > development/emulator/qtools/dmtrace.cpp:166:35: error: invalid conversion from ‘const char*’ to ‘char*’ [-fpermissive]
  > development/emulator/qtools/dmtrace.cpp:183:34: error: invalid conversion from ‘const char*’ to ‘char*’ [-fpermissive]
  > make: *** [out/host/linux-x86/obj/EXECUTABLES/q2dm_intermediates/dmtrace.o] Error 1

  方法同上。有点区别的地方是，这次是将等号右边强制类型转换为`(char *)`。

- > make: *** [out/target/product/generic/obj/SHARED_LIBRARIES/libwebcore_intermediates/WebCore/HTMLNames.cpp] Error 255

  降gcc/g++版本:

  ```bash
  apt-get install gcc-4.4
  apt-get install g++-4.4
  update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.4 40
  update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.4 40
  ```

  [参考][5]





[1]: http://blog.csdn.net/yiyaaixuexi/article/details/8330645
[2]: http://blog.csdn.net/peter_hucq/article/details/6665237
[3]: http://xxj050.appspot.com/?p=19001
[4]: http://blog.csdn.net/milo103/article/details/5060085
[5]: http://s90304a123.pixnet.net/blog/post/43192291-android%E7%B7%A8%E8%AD%AF%E9%8C%AF%E8%AA%A4%3Aunknown-parameter-a-interfacename-for-ta