

 
## Q:what video format does this app support

  A: this app is designed to play m3u8 file, but also supporting other format like mp4 ,etc. Only support http ,not p2p,rtmp,rtsp
  Q:that is the subscription file format

  A: subscription file supports txt ,m3u, and json.

### for txt file
```
ch1,https://www.example.com/channel1.m3u8
ch2,https://www.example.com/channel2.m3u8
```

### for m3u file
```json
#EXTM3U
#EXTINF:-1  tvg-logo="https://www.example.com/foo.png", ch1
https://www.example.com/channel1.m3u8
#EXTINF:-1 tvg-logo="https://www.example.com/bar.png" ,ch2
https://www.example.com/channel2.m3u8
```

### for json file
```json
  {
	"uuid":"64350b50-a810-4901-b86b-7a5106bdef2c",
	"title": "you subscription file name",
	"channels": [
		{
			"name":"ch1",
	   		"logo":"https://www.example.com/foo.png",
			"url": "https://www.example.com/channel1.m3u8"
		},
		{
			"name": "ch2",
	                "logo":"https://www.example.com/bar.png",
			"url": "https://www.example.com/channel2.m3u8"
		}
	]
}
```
the file contains three part, uuid,title and channels

  * uuid: don't change it
  * title: change it to your own name
  * channels: your channels list here

  put this file on the web(like github),get the direct link(very important!) and paste it. That's all you need to do.
  
