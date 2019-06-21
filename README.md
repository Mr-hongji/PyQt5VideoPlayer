# PyQt5VideoPlayer
由于个人的博客系统中在线播放视频功能需要播放不同格式的视频文件，但是目前的H5播放器只支持MP4, WebM, 和 Ogg不能满足需要，如果把所有的视频格式都做统一的转码处理这种方式又太耗时间，所以决定使用了Pyqt5开发了一个简单的多格式的视频播放器，通过使用URL Protocol 方式来通过web页面调用本地应用程序的方式播放在线多格式的视频文件。
* **暂不支持全屏和窗口最大化**
* 安装 LAVFilters-0.74.1-Installer.exe程序做解码器，即可支持avi、MP4、flv、rmvb等视频格式（必须）
* [**pyqt5官方文档**](https://www.riverbankcomputing.com/static/Docs/PyQt5/api/qtwidgets/qaction.html)
* **DevRequird:**

        ➣  Python 3.x
        ➣  pip install pyqt5

* **Run .py File：**

        ➣  Python pyqt5.py ‘视频路径’    
      例：
            python pyqt5.py d:/123.avi
            python pyqt5.py http://127.0.0.1/12345.mp4   （视频地址是 HTTP 的时候，视频名称最好设置为数字，其他字符会导致视频无法播放，原因暂时未知）
* **MakEexeFileRequird:**

        ➣   pip install pywin32
        ➣  pip install pyinstaller
        ➣  打开 cmd, 切换到该项目的根目录下运行： pyinstaller -F -w -i images/favicon.ico pyqt5.py
      会在目录下生成__pycache__、build、dist三个目录，目录结构如图：
     
      ➣  把所用到的图片文件images目录复制到dist目录下
      ➣  运行 dist下的 exe文件，ok。
      
      
![image](https://github.com/Mr-hongji/PyQt5VideoPlayer/blob/master/images/pyinstaller_ok.png)
![image](https://github.com/Mr-hongji/PyQt5VideoPlayer/blob/master/images/pyinstaller_ok_1.png)


     
*** Protocol Url使用：**

     ➣  打开目录下的 videoPlayer.reg 文件， 修改EXE的放置路径：
      ![image](https://github.com/Mr-hongji/PyQt5VideoPlayer/blob/master/images/registerFile.png)
     ➣  双击运行.reg文件， 弹出是否继续提示框，选择 “是”，后提示注册完成。
     ➣  HTML页面中的使用：`<a href="videoPlayer://http://127.0.0.1/3.mp4">videoPlayer 测试</a>`

如图：
![image](https://github.com/Mr-hongji/PyQt5VideoPlayer/blob/master/images/videoplayer.jpg)
