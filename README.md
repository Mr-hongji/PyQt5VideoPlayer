

# PyQt5VideoPlayer

由于个人的博客系统中在线播放视频功能需要播放不同格式的视频文件，但是目前的H5播放器只支持MP4, WebM, 和 Ogg不能满足需要，如果把所有的视频格式都做统一的转码处理这种方式又太耗时间，所以决定使用了Pyqt5开发了一个简单的多格式的视频播放器，通过使用URL Protocol 方式来通过web页面调用本地应用程序的方式播放在线多格式的视频文件。


Requird:
      Python 3.x

      pip install pyqt5
      
MakEexeFileRequird:

     1、 pip install pywin32
      
     2、pip install pyinstaller
      
      
      3、打开 cmd, 切换到该项目的根目录下运行： pyinstaller -F -w -i images/favicon.ico pyqt5.py
      会在目录下生成__pycache__、build、dist三个目录
      
      4、把所用到的图片文件images目录复制到dist目录下
      
      5、运行 dist下的 exe文件，ok。
      

基于PyQt5的视频播放器(暂不支持全屏和窗口最大化)

pyqt5官方文档：
https://www.riverbankcomputing.com/static/Docs/PyQt5/api/qtwidgets/qaction.html


安装 LAVFilters-0.74.1-Installer.exe程序做解码器，即可支持avi、MP4、flv、rmvb等视频格式

运行：
  Python pyqt5.py ‘视频路径’    
  
  例：
  
    python pyqt5.py d:/123.avi
    
    python pyqt5.py http://127.0.0.1/12345.mp4   （视频地址是 HTTP 的时候，视频名称最好设置为数字，其他字符会导致视频无法播放，原因暂时未知）

如图：
![image](https://github.com/Mr-hongji/PyQt5VideoPlayer/blob/master/images/videoplayer.jpg)
