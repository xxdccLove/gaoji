

# 一、使用内测系统

## 申请内测

进入小米社区中的开发组板块，点击内测申请

进行答题，分数满足条件后可以在有名额的情况下进行内测申请

申请理由填写 `雷军！金凡！稳定版rnmtq`

## 偷渡法

### 1. 替换法偷渡

+ 下载要偷渡版本的目标卡刷包，备用
+ 进入系统更新页面，在更多中选择 下载最新完整包 
+ 进入` Download`-` downloaded_rom`目录,复制 最新完整包 的文件名，修改 目标卡刷包 文件名为 最新完整包 的文件名
+ 在系统下载至100%时，关闭网络连接，将修改过文件名的 目标卡刷包 移动到 `downloaded_rom` 文件夹中，选择替换
+ 等待系统更新完成选择重启

### 2. 模块法偷渡

> 仅限于已经解锁 BL 锁并获取 ROOT 权限的情况

+ 使用面具安装 [MIUI-Flash-Freely](https://github.com/ianchb/MIUI-Flash-Freely) 模块，或者安装[@乌堆小透明](https://www.coolapk.com/u/乌堆小透明) 的 [WooBox For MIUI](https://www.coolapk.com/apk/com.lt2333.simplicitytools) (Xposed模块) ，Lsp 勾选作用域后开启去 ota 功能，重启生效。

  ![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111735689.png)

+ 下载对应卡刷包到手机用户根目录

+ 连点 MIUI logo，点更多，然后点击手动选择安装包，开始更新

## 线刷

> 仅限于已经解锁 BL 锁的情况

+ 下载线刷包和官方刷机工具，手机进入 Fastboot 模式
+ 解压缩线刷包两次后，进行刷机



# 二、系统优化

## 1. 去广告

① 按 [查看链接](https://www.coolapk.com/feed/35142654?shareKey=OGU0NWQwYzE4N2NjNjI5Y2NjNzc~&shareUid=4161634&shareFrom=com.coolapk.market_12.3) 中方法关闭系统广告
② 到 /storage/emulated/0/Android/data/com.miui.systemAdSolution/files/ 中删除 miad 文件夹并新建 maid 文件
③安装[【爱玩机工具箱-解锁玩机新姿势】](http://www.coolapk.com/apk/com.byyoung.setting) ，在 导航-MIUI专属-高级设置-特殊服务 中移除系统广告
④使用 【李跳跳】跳过软件开屏广告

## 2. 输入法

### 1、 获取皮肤

进入森林集公众号或商店链接
[查看链接](https://shop42868965.m.youzan.com/v2/showcase/homepage?kdt_id=42676797)
购买皮肤，通过链接进行下载
(森林集大部分皮肤都可以通过商店内的折扣卷免费获得)

![](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111910506.png)



### 2、 皮肤安装

用 [MT管理器] 将下载好的皮肤文件移动到输入法皮肤文件夹中
三大输入法小米定制版主题文件夹位置
百度输入法：
/storage/emulated/0/Android/data/com.baidu.input_mi/files/skins/

![浅浅 智能深色](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111910344.png)



搜狗输入法：
/storage/emulated/0/Android/data/com.sohu.inputmethod.sogou.xiaomi/files/sogou/sga/wallpaper/
(没有 wallpaper 文件夹的需要自己创建)

![字由字在 天青](https://cdn.jsdelivr.net/gh/xxdccLove/xxdccPic/img/202208111910808.png)



讯飞输入法：
/storage/emulated/0/Android/data/com.iflytek.inputmethod.miui/files/iFlyIME/skin/theme/

### 3、注意

① 低版本的定制输入法无法使用森林集的智能深色皮肤，需要更新。建议选择 百度输入法
百度输入法小米定制版 v10.6.66.45：
[查看链接](https://wwd.lanzouq.com/i4R9y056fqib)
搜狗输入法小米定制版 v10.32.31:
[查看链接](https://wwd.lanzouq.com/iczSC056fvra)
② 定制输入法的智能助理啥的都可以关闭，都在设置里

## 3. 堆叠桌面: 

[@TAT趙](https://www.coolapk.com/u/TAT趙)

## 4. 弹幕通知：

安装弹幕通知软件，给在其他应用上层显示和读取通知的权限

## 5. 负一屏刷新问题：

核心破解安装旧版本智能助理，进入下方设置后切任务管理页面锁定任务，更新智能助理

## 6. 屏蔽系统更新更新：

 [查看链接](https://www.coolapk.com/feed/36416444?shareKey=ZDZlMmVjYTZmN2IyNjI5ZDYyMmY~&shareUid=4161634&shareFrom=com.coolapk.market_12.3)
①download文件夹下删除downloaded_rom文件夹，
②创建一个downloaded_rom文件，不要扩展名。

## 7. 隐藏状态栏图标：

 [【WooBox For MIUI】](https://www.coolapk.com/apk/com.lt2333.simplicitytools)

## 8. 内测系统通过google play安全认证:

下载 [【My Device IDs - Get device AAID, GSF ID, OAID】](https://www.coolapk.com/apk/com.github.kolacbb.ids) ，查询自己的 GSFID ，复制，点击注册到[查看链接](https://www.google.com/android/uncertified/) 完成认证。删除谷歌商店数据重新登录。就可以正常下载应用了

# 二、关于Twrp：

这里推荐 [@mi_block](https://www.coolapk.com/u/mi_block) 大佬的。个人更推荐前者

# 三、模块

救砖：[查看链接](https://wwd.lanzouq.com/iRFOt05ynebi)

A亮屏满血模块： 鹤征

第三方应用下载目录重定向：[查看链接](https://wwd.lanzouq.com/i6VUe05ynz9c)

小白条沉浸：[查看链接](https://wwd.lanzouq.com/i5xN505yo1mh)

