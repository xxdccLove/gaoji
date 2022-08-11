# 首先 安装驱动

不管什么机型，首先要安装驱动，一般情况下安装下面两个驱动就可以满足全机型的刷机需求，如果出现报错的情况，请检查并安装下面各个机型具体驱动

https://wwe.lanzouq.com/b01j3lk5a
密码:xxdcc



道路千万条，备份第一条。刷机不规范，半夜两行泪！

由刷机造成的任何物质损失与精神损失与本人无关！望各位安好！

# 一、小米(mi/Redmi)

1、首先，进入设置-我的设备-全部参数，连续点击7次打开开发者模式

2、进入设置-更多设置-开发者选项，打开oem解锁选项，再进入设备解锁状态，点击绑定账号与设备，看到“绑定成功”提示说明成功

3、下载并安装小米官方解锁工具后，登录你的小米账号进入软件

​	官方下载地址：http://miuirom.xiaomi.com/rom/u1106245679/5.5.224.55/miflash_unlock-5.5.224.55.zip

5、将手机关机后，按住**`音量-键`**和**`电源键`**进入Fastboot模式（兔子模式）

6、用数据线将手机与电脑连接起来，直到出现“已连接手机”的字样。点击**`解锁`**按钮，等待解锁完毕，显示解锁成功后，打开手机进入设置-更多设置-开发者选项-设备解锁状态，显示“已解锁”说明解锁成功。

---



# 二、Pixel（谷歌）

1、首先，确定你手中的Pixel版本可以解开bl锁（不是vz版），具体是否可以解锁可以参照 https://www.imei.info/

2、进入设置-关于手机，快速点击底部**`版本号`**7次进入开发者模式

3、进入设置-系统-开发者选项，找到oem解锁，打开开关，之后将手机关机

> 如果已经解锁引导程序，oem选项会变灰色并且无法操作。
>
> 如果是手机未解bl且已经确定手机是可以解锁的版本，请修改手机解锁方式为图形解锁并科学上网完成通知栏中的**`Pixel设置向导`**

4、从安卓开发网站下载Platform-Tools

官方网址：https://developer.android.google.cn/studio/releases/platform-tools

解压**`Platform-Tools.zip`**，进入对应文件夹内，按住**`Shift`**键右击，点击**`在此处打开Powershell窗口`**

5、将手机连接电脑，在关机状态下长按**`电源键`**和**`音量-键`**，在Powershell窗口内输入

```
.\fastboot devices
```



> 如果是使用wzsx150大佬制作的cmd命令脚本的话，则在代码中删除` .\`，即` fastboot devices` 下面的指令同样是这样。
>
> ![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111841264.png)

如果窗口内出现**`‘一串字符’   fastboot`**说明设备与电脑已经成功连接，如果失败，请检查驱动程序

6、在Powershell窗口内输入设备解锁指令

全机型Pixel解锁指令为：

```
.\fastboot flashing unlock
```

对于2xl这个机型，在执行完上述指令后还需要执行：

```
.\fastboot flashing unlock_critical
```

Nexus型号的解锁指令为：

```
fastboot oem unlock
```

7、输入解锁指令后，手机会亮屏并显示警告，大意为“解锁手机会清除所有数据并且会使设备不再安全”

通过**`音量+键`**和**`音量-键`**将右上角选项选择到“Unlock the Bootloader”，使用电源键进行确认



这时手机会黑屏并进行重新到该页面，这时页面会显示“unlocked”，说明解锁成功

---



# 三、LG（laogong）

> LG相关教程复制黏贴漠云大佬的855黑砖教程，各位9008请谨慎。相关资料以漠云大佬为准 https://855.lge.fun/
>
> 驱动：打开下载的QPST压缩包内的Drive文件夹，安装Qualcomm USB Driver V1.0.exe

1、下载高通工具QPST：https://qfiltool.com/category/download，

https://wwe.lanzouq.com/iRxDkze3l2f

并进行安装，安装时一路next即可。安装后QPST可能不会生成快捷方式，请到开始菜单里寻找

2、进入9008模式

+ 安装完毕后，打开QFIL，USB连接电脑，按住**`音量-键`**加**`电源键`**重启，黑屏后不要松开**`音量-键`**加**`电源键`**，狂敲**`音量+`**，观察QFIL窗口有无出现新设备,设备亮屏即为进入失败，请重新尝试

+ 等待连接成功后，上方No Port Available会显示出设备

  > 有时会显示Please select a port，此时点击右上角的Select a port选择你的设备即可
  >
  > ![image-20220129193851013](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129193851013.png)

+ 选择Flat Build

+ Select Programmer里选择下载好的LGE855 Firehose

+ Configuration-FireHose Configuration-Device Type-ufs-OK

  > Device Type默认是emmc
  >
  > ![image-20220129194007163](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194007163.png)

+ Tools-Partiton Manager-OK
+ ![image-20220129194021012](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194021012.png)

注意：每次引导失败后都必须重新进入一次9008，否则会一直卡住

3、解锁bl

+ 准备所需文件

  + G8 [工程机ABL以及配套引导(opens new window)](https://wwx.lanzoui.com/iu8Hnfuwe3e)

  + V50 [工程机ABL以及配套引导(opens new window)](https://wwx.lanzoui.com/iXqHYfuwjfg)

  + G8X&V50S [工程机ABL以及配套引导(opens new window)](https://wwx.lanzoui.com/b01015vfe)

    > [G8X&V50S解锁后指纹修复教程](https://www.coolapk.com/feed/26578393?shareKey=YmYzNzU2NmQzYWZlNjBiY2M4MTI)

+ 刷入工程机三件套

  - 列表里仔细找到abl_a，先**左键**选中

  - 右键-Partiton Manager Data-Load Image

    ![image-20220129194108613](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194108613.png)

  - 选择V500ES_abl_a.image，打开

  - 按下Raw Data Manager中右下方的Close

    ![image-20220129194141173](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194141173.png)

  - 同理再把abl_b分区刷入V500ES_abl_a.image

  - xbl_a和xbl_b分区刷入xbl_a.image

  - xbl_config_a和xbl_config_b分区刷入xbl_config_a.image

  - 全部完成后点击Close，等待下方Status中Finish Reset To EDL出现

    ![image-20220129194232585](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194232585.png)

  - 按住音量下和电源键，尝试重启进入工程机Fastboot

    > 在Android P上可能会正常开机，手动关机后按住音量下键插入数据线即可

  **日后搞机把哪个分区刷炸了，也可以强制进9008按上面刷分区的方法刷回原Kdz中的分区**

+ 解锁BootLoader

  - /* Verizon运营商版本的特殊步骤 */

  - Verizon运营商版本的特殊步骤</summary>还在为设置中找不到OEM解锁而烦恼吗，别担心，由Kamio大佬倾情提取的frp分区，为您的黑砖生活保驾护航 &gt; 其他版本请忽略，但如果你忘了打开OEM解锁，这就是补救方法。除G8以外的机型请勿刷入

  - 下载[frp备份](https://www.lanzoui.com/ictudih)

  - 解压文件，并将其移动到ADB工具根目录，输入以下命令

  + ```
    flash frp frp
    ```

  + 继续执行下方步骤

  + /* Verizon运营商版本的特殊步骤 */

  + 使用**音量键**选择Restart bootloader，按下**电源键**来**重新**进入FastBoot

    ![image-20220129194259502](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194259502.png)

  + 在ADB命令行中输入

    ```
    fastboot oem unlock
    ```

  + 然后你会看到以下界面

    ![image-20220129194332932](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194332932.png)

    > 如果显示Not allowed则说明最开始时手机的**`oem解锁`**未打开

  + 使用音量键选择UNLOCK THE BOOTLOADER，按下电源键确认，手机会自动重启并解锁BL。如果成功，那它将是这样的

  + ![image-20220129194406111](http://img.xxdcc.life/2022/01/29/22-01-29/image-20220129194406111.png)

4、退出Fastboot

> Android Q在工程机FastBoot下无法开机，需要还原原来的分区

+ 恢复原FastBoot

**这里仅提供Android Q的，Android P请自行从KDZ中解包**

- 下载G8 [原FastBoot备份(opens new window)](https://wwx.lanzoui.com/icqnuwd)
- 下载V50 [原FastBoot备份(opens new window)](https://wwx.lanzoui.com/icqo1jc)

> 请解压后再使用

- 将文件移动到[ADB工具 (opens new window)](https://www.coolapk.com/feed/24703263?shareKey=NzFmZmJiZDQ0OWE3NjAyMmJlMDg)根目录，并在ADB命令行中输入以下命令：

------

```batch
:: slot a
fastboot flash abl_a Q_abl_a.image
fastboot flash xbl_a Q_xbl_a.image
fastboot flash xbl_config_a Q_xbl_config_a.image
:: slot b
fastboot flash abl_b Q_abl_a.image
fastboot flash xbl_b Q_xbl_a.image
fastboot flash xbl_config_b Q_xbl_config_a.image
:: 格式化Data
fastboot erase userdata
```

**别复制错了/少了，一共要将三个镜像刷入6个不同的分区，请认真检查**

**然后大佬们就可以直接滚回9008备份devinfo分区，在下次BootLoader意外回锁时重新刷入来直接解锁本机**



# 四、三星（Samsung）

> 三星驱动：https://wwe.lanzouq.com/iv6fNze3ixi
>
> 不适用美版机器

1、进入设置-关于手机-软件信息，连续点击6次“编译编号”进入开发者模式

2、返回设置页面，进入“开发者选项”页面，打开**`oem解锁	`**选项

3、将数据线连接到手机与电脑，重启手机，并在开始重启时长按**`音量+键`**和**`音量-键`**不放

4、进入三星手机的ODIN模式功能选择页面，长按**`音量+`**进入解锁bl模式

> 短按`音量+`进入ODIN刷机模式
>
> 长按`音量+`进入解锁bl模式
>
> 短按`音量-`重启手机

5、短按`音量+键`解锁bl

> 短按`音量-键`重启手机

6、重新开机有黄色提示出现，说明已经解锁bl

---



# 五、一加（OnePlus）

> 一加全能工具箱地址：https://optool.daxiaamu.com/wiki_pctool
>
> 备用地址：https://cloud.xxdcc.life/s/6rIp
>
> 驱动：输入1安装驱动

1、下载完成打开一加全能工具箱

2、进入开发者模式，进入设置-系统-开发人员选项，打开oem选项以及USB调试，如果打不开oem选项，请登录谷歌账号再试
打开开发人员选项（应该都会吧）

3、连接电脑输入2，按照软件内提示操作即可解锁bl
4、开机后直接打开开发人员选项，打开usb调试，连接电脑输入3，按照软件内操作即可获取root。