# CM311-1a-CoreELEC
适用于**魔百和CM311-1a**的CoreELEC打包脚本，开启蓝牙，增加蓝牙遥控器支持，改了一下LED指示灯

在 [KryptonLee/e900v22c-CoreELEC](https://github.com/KryptonLee/e900v22c-CoreELEC.git) 的基础上进行了修改

`common-files/{advancedsettings.xml,backspace.xml,e900v22c.rc_keymap,fs-resize,rc_maps.cfg}` 来自于 [KryptonLee/e900v22c-CoreELEC](https://github.com/KryptonLee/e900v22c-CoreELEC.git)

`common-files/bt-remote.hwdb` 为蓝牙遥控器按键文件

`common-files/ccm311-1a.dtb` 是盒子的dtb文件，由于CM311-1a没有wifi,dtb中删除了关于wifi部分

用法 (Ubuntu 20.04 LTS)
```
sudo apt-get update -y
sudo apt-get install -y make gcc git texinfo gzip squashfs-tools
```

```
cd ~

git clone https://github.com/alahei/CM311-1a-CoreELEC.git
cd CM311-1a-CoreELEC
sh build.sh
```
有可能需要输入sudo密码
