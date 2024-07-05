# basic short cuts
- camera view
	- 0

# walk navigation(can be used in normal view)
- enable
view.navigation.walk_navigation
- confirm
	- mouse1
- cancel
	- mouse2
- run
	- shift + w/a/s/d
- dash
	- space
- enable gravity
	- tab

# settings
- opacity outside the camera_frame
```python
from data import *

viewport.passepartout.enable = True
viewport.passepartout.value = 1	% totaly dark
```
- resolution 分辨率
```python
from output import *

resolution.x = ?
resolution.y = ?
```
- depth of the field
the range of clear scene
```python
from data import *

depth_of_field.enable = true
viewport_diplay.show.limits = true

# set the value of depth_of_field
## 1
depth_of_field.focus_distance = ?
## 2
Do(move the white_cross)
```
- blur 虚化
```python
data.depth_of_field.aperture.F_stop = ?	# the lower the value, the blurer outside the depth_of_field
```
- focal_length 焦距
```python
data.lens.focal_length = ?	# the lower the value, the larger the filed of view
```

# Motion Blur
## enable
	go to render, click Motion Blur
## setting
	shutter : control the strength of Motion Blur
	steps : control the quality

# tips
## move the camera without changing position of the focus(better do it after creating the camera)
```python
DO(create an empty object ; select it, rename it by pressing F2 ; put it near or at the focus ; select the camera)
data.depth_of_field.focus_on_object = empty_object
```
