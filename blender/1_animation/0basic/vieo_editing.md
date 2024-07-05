# join images into video
	add-image/sequence, select images, then add image strip
	goto output,
		set
			Resolution
			Frame Rate
			Frame start, end
		
		go to output
			set 
				path
				file fomat = FFmpeg Video
			goto encoding
				set containner
			goto video
				set output quality = high quality
	C F12
