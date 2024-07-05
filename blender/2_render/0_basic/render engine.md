# render
## render_region
	draw
		C b
	clear
		C M b
	if you can't see the box, make sure all the overlays are enabled
## Eevee
### settings
	Ambient Occlusion
		distance : set the scope of Ambient Occlusion
		Factor : set the strength of Ambient Occlusion
	Bloom
		Threshold : the higher the value is, only the very bright area will glow
		Knee : control the transition between glowing areas and non-glowing areas
		intensity : control the strength of glowing
		clamp : set the max strength
	Depth of Field
	
# color management
	goto render.color_management
		look : set contrast
		esposure : bigger the value, brighter the scene
		use curvers : set the value of red/gree/blue/... chanel

# output
## set animation out put path(necessary)
	output.output.output_path = ?
## metadata(similar to watermark)
	goto output.Metadata
	set what to burn into image
		include
	add note to the image
		click note
	burn metadata into image
		click "Burn Into Image"
## set background transparent
	render.Film.Transparent = True
	goto output.Output
		File_Format = PNG(if version < 3.4)
		Color = RGBA
## file format
	PNG
		you can see 'Compression', its value won't influence the quality , but influence desk usage and time you open it. For most time, just ignore it.

## output animation_frames(not animation)
	check colletion
	check particles system
	check render setting: for Eevee, enable Film.Overscan
	check output setting: set output.file_format = PNG
	C F12

