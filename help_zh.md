
## 问:支持什么样的视频格式 
  答: 本播放器主要用来播放m3u8，当然也支持其他格式，如mp4等,只支持http，不支持p2p，rtmp，rtsp
## 问:订阅文件的格式是什么
 A: 订阅文件支持三种格式 txt ,m3u,json.
### txt文本格式

```json
频道1,https://www.example.com/channel1.m3u8
频道2,https://www.example.com/channel2.m3u8
```
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
分成3个部分, uuid, title和 channels
 
 * uuid: 不要做任何改动
 * title: 可以自定义,这个是你导入后在列表里显示的名字
 * channels: 你所有的频道列表

  将json文件放到网络上，比如github，然后获取直链的网址，在添加订阅里粘贴保存即可。

