> 本文教程取自 [Magisk中文网](https://magiskcn.com/)

# Root

1、系统是纯净官方系统（如果不是，建议刷一次完整包）

2、手机下载安装：[MT管理器](https://www.coolapk.com/apk/bin.mt.plus)

3、手机下载安装：[Magisk](https://magiskcn.com/magisk-download)

4、下载系统完整包：[magiskcn.com/get-miui](https://magiskcn.com/get-miui)（其他品牌请自行到官网下载）

5、打开**MT管理器**，找到我们下载好的系统包，点开zip包，长按 **boot.img** 提取出来到 **Dowmload** 目录
（小米手机系统包默认下载的位置：**Download/dowmloaded_rom**）

（如果系统包里面没有**boot.img**，只有**payload.bin**，请参考这个教程提取：[magiskcn.com/payload-boot](https://magiskcn.com/payload-boot)）

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111759715.png)

6、打开Magisk【安装 – 选择并修补一个文件 – 弹窗文件管理窗口（找到刚刚提取的**boot.img**）- 开始】

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111800217.png)

7、修补结束，会生成一个名字为（**magisk_patched-版本号_随机字符.img**）的文件（每次生成的随机字符都不一样，使用的时候请输入生成的名字）

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111800101.png)



8、手机连接到电脑，把**boot.img**和（**magisk_patched-2X000_xxxxx.img**）两个文件复制到电脑

9、下载FastBoot：https://mrzzoxo.lanzouw.com/iMbPYz63p6f
（解压出来，把**magisk_patched-2X000_xxxxx.img**复制到fastboot目录里）

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111800232.png)



10、打开bat文件（**打开CMD命令行.bat**）把手机重启到BootLoader模式（**重启+音量-键**）然后输入下面的命令

```
fastboot flash boot 面具文件
```

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111801200.png)



11、出现下面这三行代码，就是成功刷入了。

```
Sending 'boot' (131072 KB) OKAY [ 3.049s]
Writing 'boot'             OKAY [ 0.587s]
Finished. Total time: 4.582s
```

12、重启手机（开机有震动基本没问题了）耐心等手机开机。（显示Magisk的版本，就是刷好了的）

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111801370.png)

(A/B）(Ramdisk）(SAR）
这是手机分区，老款手机会显示“否”。新出的手机一般都显示“是”。不影响使用。

# 还原 Boot

如果刷模块不兼容或者其他骚操作导致卡米的话，可以把我们前面提取的boot.img通过fastboot刷回去，恢复原系统，一般都能正常开机！
boot.img保留一份在电脑，避免出问题了可以自救下！还原boot指令

```
fastboot flash boot boot.img
```

后期系统更新，直接下载全量完整包升级，然后重复上面的步骤就可以继续愉快的使用Magisk了！

# [payload提取boot文件（payload.bin解包boot.img）](https://magiskcn.com/payload-boot)

1.在电脑下载系统包（全量包）小米参考：https://magiskcn.com/get-miui（其他品牌请自行到官网下载）

2.下载Payload解包工具：https://mrzzoxo.lanzouw.com/iR65zpaueyd

3.解压系统包（只需要payload.bin文件）

4.复制解压出来的【payload.bin】文件到Payload解包工具的payload_input文件夹

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111802764.png)



5.打开【payload_dumper.exe】执行解包（文件越大，解包时间越长）

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111803947.png)



6.打开payload_output文件夹就可以看到我们解好的包了

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111803798.png)



# [AB分区保留面具升级系统（不丢面具升级系统）](https://magiskcn.com/ab-magisk-update)

> 如果是跨安卓版本升级的，一定要先升级，再重新刷面具！

0、先确认是不是AB分区

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111753078.png)

1、下载最新完整包 – 进度跑完 – 不重启

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111752640.png)

2、打开Magisk – 安装 – 安装到未使用的槽位（OTA后） – 重启

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111752148.png)