## 小点播放器2和1有什么区别
1. 小点播放器2去除了1代的自定义频道添加，只保留订阅，更加方便管理。
2. 所有订阅的频道保存到本地数据库，每次打开列表时速度更快
3. 电视节目单功能


## 小点播放器支持什么视频格式 
主要用来播放m3u8，当然也支持其他格式，如mp4等,只支持http，不支持p2p，rtmp，rtsp
  
## 什么是订阅
订阅是一个m3u或者json文件，保存在网络端，只需得到文件的直连链接，即可导出到小点播放器，免去在app端进行复杂的操作，管理。所有的管理都在网页端。

## 怎么添加订阅
复制要添加的链接，然后点击左右角+号按钮，粘贴链接，确定。

## 怎么更新订阅
在首页订阅列表里，左滑-》更新

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





		
