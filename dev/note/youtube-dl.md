查看所有格式：
youtube-dl -F <link/videoID>

指定格式：
youtube-dl -f <link/videoID>

全局代理：
youtube-dl --proxy <IP:Port>

获取频道所有视频ID
youtube-dl --get-id <channelID>

批量下载视频
youtube-dl -a <idTxT>

下载频道所有视频
youtube-dl --download-archive <IDTxT> <ChannelLink> 

<eg:>
youtube-dl --download-archive .\Archive.txt https://www.youtube.com/channel/UCEickjZj99-JJIU8_IJ7J-Q -f mp4 --proxy 127.0.0.1:7890
 
下载播放列表
youtube-dl --yes-playlist <listID>

