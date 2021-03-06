# LiveStreamSDK-web

- A live stream player based on qcVideo(qCloud).
- Only one parameter required: an **m3u8** url.
- Optional parameters provided to customize your player.
- The player is avaliable both on desktop browsers and mobile browsers, which is implemented with Flash player on desktop and video element(H5) on mobile. 


## QuickStart

1. Add the initializing javascript files to your html:
	
		<script src="http://voovfile-10064034.cossgp.myqcloud.com/h5/qcPlayer.js"></script>

2. Create a container element with 'id', 'width' and 'height', for example:
	
		<div id="video-container" style="width:750px; height: 100%"></div>

3. Add following code to your .js:

		qcPlayer.createPlayer('video-container',{
		    'live_url': 'http://xxx/xxx/xxx.m3u8',
		  });

 > Size of the player will be the same as its container.


## Document

### Properties

#### qcPlayer.player

player object created by qcPlayer.createPlayer(containerId, option).

### Methods

#### qcPlayer.createPlayer(containerId, option)


- **containerId**: _String_. ID of the target container.

- **option**: _Object_. All of the following parameters are wrapped in this object:

	+ **live_url:** 

			Type: String.		
			
			Default: null.		
			
			Description: Required when using url mode. M3U8 url of the live stream.


	+ **live_url2:** 

			Type: String.		
			
			Default: null.		
			
			Description: Optional. Backup url of the live stream.

	
	+ **controls:** 

			Type: String.		
			
			Default: false.		
			
			Description: Optional. Player controller visibility switch.


	+ **channel_id:** 

			Type: String.		
			
			Default: null.		
			
			Description: No need when using url mode. Required when using video ID mode.


	+ **app_id:** 

			Type: String.		
			
			Default: null.		
			
			Description: No need when using url mode. Required when using video ID mode.


	+ **width:** 

			Type: Number.		
			
			Default: null.		
			
			Description: Set to container's width.

	
	+ **height:** 

			Type: Number.		
			
			Default: null.		
			
			Description: Set to container's height.

	
	+ **cache_time:** 

			Type: Number.		
			
			Default:0.3.		
			
			Description: Optional. Max cache_time before playing; Available only in Flash players on PC.

	
	+ **h5_start_patch:** 

			Type: Object.		
			
			Default: null.		
			
			Description: Optional. Video cover shown before playing. For example:		

			{
			url : img_url, 
			stretch: false //Wether stretch the cover to fill the entire player or not; default value: false
			}		

	+ **wording**:

			Type: Object.
			
			Default: Please check the details in code.
			
			Description: Optional. Can be custormized.


	+ **volume**:

			Type: Number.		
			
			Default: 0.5.		
			
			Description: Optional. Initialize volume(0 to 1). Avaliable only in Flash player.


	+ **https**:

			Type: Number.		
			
			Default: 0.		
			
			Description: Optional. HTTPS supporting switch(0: off, 1: on). 


	+ **hide_volume_tips**:

			Type: Number.
			
			Default: 0.		
			
			Description: Optional. Volume tips visibility switch(0: off, 1: on). 


	+ **WMode**:

			Type: String.		
			
			Default: window.		
			
			Description: Optional. 		

			window: do not allow other dom elements be placed over the player

			opaque: allow other dom elements be placed over the player
		

#### qcPlayer.player.resize(width, height)

- **width**: _Number_. Width of the player.
- **height**: _Number_. Height of the player.

#### qcPlayer.player.play()

Start playing video. Avaliable only in Flash player.

return: 

	200		success
	0		player has not been initialized
	-2		unknown command

#### qcPlayer.player.stop()

Stop playing video. Avaliable only in Flash player.

return: same as qcPlayer.player.play().

#### qcPlayer.player.pause()

Pause current plaing video. Avaliable only in Flash player.

return: same as qcPlayer.player.play().

#### qcPlayer.player.resume()

Continue to play puased video. Avaliable only in Flash player.

return: same as qcPlayer.player.play().