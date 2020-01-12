# Purpose-Player

Purpose player 2.0.2

  this is a open source software,based on ffmpeg,play audio and video,
on Windows and Ubuntu.

  there is a directory "ffmpeg-3.1.5-src-v2.0.2",it only have two files,ffplay.c and cmdutils.c,
decompress ffmpeg-3.1.5.tar.gz,it create a directory "ffmpeg-3.1.5", use ffplay.c and cmdutils.c
in directory "ffmpeg-3.1.5-src-v2.0.2" replace ffplay.c and cmdutils.c in directory "ffmpeg-3.1.5",
and compile it like ffmpeg, copy ffplay.exe to "app" directory,then you can play meida file.

  it can display "sound river",it separate audio to 70 parts by frequency,display it like a river,
(use mouse click button "River On" and wait 3 seconds),in the bottom(red) is 20khz audio,in the up(blue)
is 20hz audio,river moves from left to right.

  it can process 2.0 channel audio and 5.1 channel audio,only display left channel(1 channel) audio.

  How to compile:
    in windows, you need install msys+mingw, in Ubuntu, every thing is ready,

    decompress yasm-1.3.0.tar.gz and run
    ./configure
    make
    sudo make install

    decompress SDL-1.2.15.src.tar.gz and run
    ./configure
    make
    sudo make install

    then goto directory "ffmpeg-3.1.5" and run (ffplay.c and cmdutils.c should already been replaced)
    ./configure
    make
    sudo make install
    copy ffplay.exe to app directory

  you can run ffplay.exe in Windows and Ubuntu 12.04 ,if your Ubuntu is 14.04 or 16.04,you need
install SDL,decompress SDL-1.2.15-1.i386.rpm,copy all file in usr/lib to /usr/lib.
(sudo cp -r ./usr/* /usr)

  In Ubuntu,if you compiled ffplay.exe, and want to run it , you need goto directory "SDL-1.2.15",
run command "sudo make uninstall"(unload develop library).



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
