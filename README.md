# LiveStreamSDK-web
- A live stream player based on qcVideo(qCloud).
- Only one parameter required: an **m3u8** url.
- Optional parameters provided to customize your player.

## QuickStart
1.Add the initializing javascript file to your html:
	<script src="//qzonestyle.gtimg.cn/open/qcloud/video/live/h5/live_connect.js" charset="utf-8"></script>;

2.Create a container element with 'id', 'width' and 'height', for example:
	<div id="video-container" style="width:750px; height: 100%"></div>

3.Add following code in your .js or <script>:
	var qcPlayer = require('/xxx/qcPlayer.es6');

	var player = qcPlayer.createPlayer('video-container',{
	    'live_url': 'http://5430.liveplay.myqcloud.com/voov/54308014404.m3u8',
	  });

  Size of player will be the same as videoContainerId

  ##Document

  



