# Purpose-Player

小戴媒体播放器  2.0.2

 
是一个开源软件,全媒体,包括视频,音频,跨平台(WindowsXP/Vista/7,Ubuntu).
 
解压ffmpeg-3.1.5.tar到某个目录, 然后用这里的源代码,就是两个文件 ffplay.c 和 cmdutils.c ,替换掉ffmpeg-3.1.5
里的 ffplay.c 和 cmdutils.c 就行了,按照原来一样的方法编译,然后把ffplay.exe拷贝到app目录.
 
可以显示声音河流,把声音按照频率分成70段,象显示一条河流一样显示出来,
(点击窗口右下角的"River On",等待3秒钟),最下面的(红色)是20KHz,最上面的(蓝色)是20Hz,河流从左向右流动,

能显示2.0声道的媒体文件,新版本同时能显示5.1声道电影文件(只提取左声道一个声道的声音),
可以更清晰的显示声音河流.
 
编译方法如下：
(如果是Windows平台，需要先安装msys+mingw,如果是Ubuntu可以直接编译。)
 
把 yasm-1.3.0.tar 展开
在 yasm-1.3.0 目录下运行：
./configure
make
sudo make install
 
把 SDL-1.2.15.src.tar 展开
在 SDL-1.2.15 目录下运行：
./configure
make
sudo make install
 
把 ffmpeg-3.1.5 展开(替换掉ffmpeg-3.1.5目录里的 ffplay.c 和 cmdutils.c )
在 ffmpeg-3.1.5 目录下运行：
./configure
make
sudo make install
把ffplay拷贝到App目录.
 
Windows Ubuntu 12.04 可以直接运行,或者用命令行运行(有更多提示，显示媒体信息).
Ubuntu 14.04 16.04下面需要安装SDL运行时库,解压SDL-1.2.15-1.i386.rpm ,把 usr/lib 下面
所有文件拷贝到/usr/lib

(在命令行运行 sudo cp -r ./usr/* /usr)

如果你在 Ubuntu 刚刚编译了ffplay,需要在 SDL-1.2.15 目录下运行sudo make uninstall.(把开发库卸载)
