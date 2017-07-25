# LiveStreamSDK-web

- A live stream player based on qcVideo(qCloud).
- Only one parameter required: an **m3u8** url.
- Optional parameters provided to customize your player.


## QuickStart

1.Add the initializing javascript file to your html:
	
	<script src="//qzonestyle.gtimg.cn/open/qcloud/video/live/h5/live_connect.js" charset="utf-8"	</script>;

2.Create a container element with 'id', 'width' and 'height', for example:
	
	<div id="video-container" style="width:750px; height: 100%"></div>

3.Add following code in your .js:

	var qcPlayer = require('/xxx/qcPlayer.es6');

	var player = qcPlayer.createPlayer('video-container',{
	    'live_url': 'http://5430.liveplay.myqcloud.com/voov/54308014404.m3u8',
	  });

Size of player will be the same as its container.


## Document

### Methods

#### qcPlayer.createPlayer(containerId, option)


- containerId: _String_. ID of the target container.

- option: _Object_. All of the following optional parameters are wrapped in this object:
	+ **live_**url: 

		Type: _String_.		

		Default: null.		

		Description: Required when using url mode. M3U8 url of the live stream.


	+ **live_**url2: 

		Type: _String_.		

		Default: null.		

		Description: Optional. Backup url of the live stream.


	+ **chann**el_id: 

		Type: _String_.		

		Default: null.		

		Description: No need when using url mode. Required when using video ID mode.


	+ **app_i**d: 

		Type: _String_.		

		Default: null.		

		Description: No need when using url mode. Required when using video ID mode.


	+ **width**: 

		Type: _Number_.		

		Default: null.		

		Description: Optional. Set to container's width.

	
	+ **heigh**t: 

		Type: _Number_.		

		Default: null.		

		Description: Optional. Set to container's height.

	
	+ **cache**_time: 

		Type: _Number_.		

		Default:0.3.		

		Description: Optional. Max cache_time before playing; Available only in Flash players on PC.

	
	+ **h5_st**art_patch: 

		Type: _Object_.		

		Default: null.		

		Description: Optional. Video cover shown before playing. For example:		

			{
			url : img_url, 
			stretch: false //Wether stretch the cover to fill the entire player or not; default value: false
			}		

	+ **wordi**ng:

		Type: _Object_.

		Default: Please check the details in code.

		Description: Optional. Can be custormized.


	+ **volum**e:

		Type: _Number_.		

		Default: 0.5.		

		Description: Optional. Initialize volume(0 to 1). Avaliable only in Flash player.


	+ **https**:

		Type: _Number_.		

		Default: 0.		

		Description: Optional. HTTPS supporting switch(0: off, 1: on). 


	+ **hide_**volume_tips:

		Type: _Number_.

		Default: 0.		

		Description: Optional. Volume tips visibility switch(0: off, 1: on). 


	+ **WMode**:

		Type: _String_.		

		Default: window.		

		Description: Optional. 		

			window: do not allow other dom elements be placed over the player

			opaque: allow other dom elements be placed over the player
		

- return: A player object named 'SwfJsLink'.





