# object_static, background_dynatic
## create infinite background of uniform motion匀速运动 by using 1 background if length of the background * 3 <= the number of the frames
```python	
select the background ; add key_location ; duplicate the background

while {the number of background < 3}, do the internal. Otherwise, next step
	select the copy
	move all frames backward until 2 backgrounds don't overlap
	duplicate the copy
	
do the internal for {certain chanel of each background}
	graph_editor.modifiers.add(cycles)

```

