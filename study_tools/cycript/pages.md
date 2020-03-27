# 工具变化


## cycript

11以上不能用，cycript原作者停更了，用cyrun
通过Cydia安装“New Curses”，“readline”和“adv-cmds”
通过SSH /终端：wget http://apt.saurik.com/debs/cycript_0.9.594_iphoneos-arm.deb
wget http://www.tateu.net/repo/files/net.tateu.cycriptlistenertweak_1.0.0_iphoneos-arm.deb
wget http://www.tateu.net/repo/files/net.tateu.cyrun_1.0.5_iphoneos-arm.deb
dpkg -i cycript_0.9.594_iphoneos-arm.deb
dpkg -i net.tateu.cycriptlistenertweak_1.0.0_iphoneos-arm.deb net.tateu.cyrun_1.0.5_iphoneos-arm.deb
使用指令  cyrun -n App名称 -e 或 cyrun -n bundleID -e 
例如：cyrun -n live4iphone -e 或 cyrun -b com.tencent.live4iphone -e
将指令的 -e 改为 -d ，从App中移除(卸载)Cycript，App将被终止并自动重启。 
例如：cyrun -n live4iphone -d 或 cyrun -b com.tencent.live4iphone -d


## [用到命令](http://www.cycript.org/manual/)
```
查找
cy# choose()
通过view的nextResponder方法，可以找出它所属的视图控制器ViewController
cy# [#0x181009f0 nextResponder]
通过对象地址访问对象的成员变量
cy# #0x112f66990->_tableView
打印出当前界面的view层级
cy# UIApp.keyWindow.recursiveDescription().toString()
快捷的获取 ViewController 的方法
cy# [[[UIWindow keyWindow] rootViewController] _printHierarchy].toString()
打印对象所有属性
cy# [#0x5822600 _ivarDescription].toString()
\t_url (NSURL*): https://render.alipay.com/p/f/fd-j6lzqrgm/addressbook.html
cy# [#0x5822600 url]
展示的架构是基于layout(_autolayoutTrace)
cy# [[UIApp keyWindow] _autolayoutTrace].toString()
```
## [frida](https://github.com/3xp10it/myblog/blob/8055c9893b511278a56934793fe04eece0f80c73/_posts/2017-12-29-frida%E7%94%A8%E6%B3%95.md)

