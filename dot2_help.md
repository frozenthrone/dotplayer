# 使用帮助

## 主界面介绍

## 添加订阅

订阅是托管在服务器上的m3u或者json文件(具体格式见下方的FAQ)，只要在服务器上更新了这个文件，然后在app里滑动-更新，就能保持和服务器端同步。
一般将订阅托管在github.com上， 当然用户也可以将订阅托管在其他网站或者自架的网站上。

订阅地址必须是直连的地址而不能是个网页，如果托管在github上，则会以 https://raw.githubusercontent.com 开头，因为这个域名在国内部分地区已经被墙了，在添加github上的订阅时，请挂梯子。


## 收藏夹功能


## 播放器增强

app默认调用的是系统的avplayer，只支持m3u8格式，如果用户想要看flv，ts，mkv，rtsp，rtmp等格式，则需要启用播放器增强。一般来说，播放普通的m3u8时，用系统自带的播放器即可，会比较流畅，而且有些m3u8，默认的播放器可以播放，打开播放器增强后，会无法播放。



# FAQ


## 小点播放器2和1有什么区别

1. 小点播放器2支持更多的视频格式，比如rtmp，rtsp，flv，ts等。(注意:需在设置里开启播放器增强)。
2. 小点播放器2主界面去除了1代的自定义频道添加，只保留订阅，更加方便管理。如需单独添加频道，请在收藏里添加。
3. 所有订阅的频道保存到本地数据库，每次载入列表时速度更快。
4. 电视节目单功能。(每天只需在设置里获取一次即可，注意导入数据库时间较久，请耐心等待)。
5. 小点播放器2支持视频后台播放，小点1只支持音频后台播放

## 什么是订阅
订阅是一个m3u或者json文件，保存在网络端，只需得到文件的直连链接，即可导出到小点播放器，免去在app端进行复杂的操作，管理。所有的管理都在网页端。

## 如何添加订阅
复制要添加的链接，然后点击主界面上的+号按钮，粘贴链接，确定。

## 为什么无法添加订阅
https://raw.githubusercontent.com 在国内部分地方已经被墙，所以放在github上的订阅，可能需要翻墙后才能添加订阅导入

## 如何更新订阅
在首页订阅列表里，左滑->更新

## 如何收藏/删除频道
频道图标上长按，在弹出的对话框里选择收藏或者删除

## 如何添加单独的频道
主界面上无法添加，首先点左上角红心进入收藏夹，然后再点左上角的+号添加

## 在线订阅文件的格式是什么
目前订阅文件支持2种格式 
1. m3u
2. json

### m3u格式

```json
#EXTM3U
#EXTINF:-1 tvg-logo="https://www.example.com/foo.png",频道1
https://www.example.com/channel1.m3u8
#EXTINF:-1 tvg-logo="https://www.example.com/bar.png",频道2
https://www.example.com/channel2.m3u8
```


### json格式
```json
  {
	"uuid":"64350b50-a810-4901-b86b-7a5106bdef2c",
	"title": "你的频道名字",
	"type": "tv",
	"channels": [
		{
			"name":"频道1",
	                "logo":"https://www.example.com/foo.png",
			"url": "https://www.example.com/channel1.m3u8"
		},
		{
			"name": "频道2",
	                 "logo":"https://www.example.com/bar.png",
			"url": "https://www.example.com/channel2.m3u8"
		}
	]
}
```
分成4个部分, uuid, title,type 和 channels
 
 * uuid: 不要做任何改动
 * title: 可以自定义,这个是你导入后在列表里显示的名字
 * type: 支持tv，episode，radio,省却默认tv
 	* tv:电视直播，没有播放进度条，logo显示横向
 	* episode:电影剧集，有播放进度条，logo显示纵向
 	* radio:电台，logo显示正方形
 * channels: 你所有的频道列表





		
