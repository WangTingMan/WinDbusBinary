# Welcome to usb DBUS on Windows OS!
DBUS an IPC communication method.
Here is the official website: https://www.freedesktop.org/wiki/Software/dbus/
You can use this repo to use dbus on windows!
# How to use
1. Copy dbus-1.dll into your system dll dir or other dir then the process which use
   DBUS can find it and load it.
2. Create a shortcut for dbus-daemon.exe and put the shortcut into desktop
3. Modify the shortcut you created by step 2. Modify the target command line like this:
   xxx\dbus-daemon.exe --config-file=system.conf
4. Just start the dbus-daemon.exe!
# Test with QT
There are some DBUS example in QT project. You can run them to test dbus on windows.
Use qdbusviewer.exe, maybe you will find that somethins wrong with the org.freedesktop.DBUs,
however, that issue will not have any impact with the DBUS usage.


# 在Windows上面使用DBUS
DBUS是一种进程间远程调用的机制。
官方网站是： https://www.freedesktop.org/wiki/Software/dbus/
通过这里提供的DBUS Windows移植版本，你可以在windows上面开发dbus程序啦！
# 如何使用
1. 复制dbus-1.dll到你的计算机的系统目录中，以便使用DBUS的程序可以找到它并且加载它。部分DBUS程序是动态从系统中加载该dll
   的，因此请需要注意系统加载dll的搜索路径。
2. 在桌面上创建dbus-daemon.exe的快捷方式
3. 修改步骤2创建的快捷方式，在该快捷方式上右键，在“目标”栏位中填写：xxx\dbus-daemon.exe --config-file=system.conf
   注意，xxx指的是dbus-daemon.exe所在的文件夹。
4. 开始运行dbus-daemon.exe吧!
# 在QT中测试
QT中有很多DBUS的示例程序，可以使用它们来测试DBUS通信。
不过使用qdbusviewer.exe，你会发现浏览org.freedesktop.DBUs的DBUS接口时，会报一部分错误，不过这并不影响你实际的DBUS通信
开发哦！