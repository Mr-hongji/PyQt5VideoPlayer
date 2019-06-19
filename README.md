由于个人的博客系统中的在线不放视频功能需要播放不同格式的视频文件，但是目前的H5播放器只支持MP4, WebM, 和 Ogg不能满足需要，所以自己使用了Pyqt5开发了一个简单的多格式的视频播放器，通过使用URL Protocol 方式来通过web页面调用本地应用程序的方式播放在线多格式的视频文件。

Python 3.x

pip install pyqt5

# PyQt5VideoPlayer
基于PyQt5的视频播放器(暂不支持全屏和窗口最大化)

pyqt5官方文档：
https://www.riverbankcomputing.com/static/Docs/PyQt5/api/qtwidgets/qaction.html


安装 LAVFilters-0.74.1-Installer.exe程序做解码器，即可支持avi、MP4、flv、rmvb等视频格式

运行：
  Python pyqt5.py ‘视频路径’

如图：
![image](https://github.com/Mr-hongji/PyQt5VideoPlayer/blob/master/images/videoplayer.jpg)
