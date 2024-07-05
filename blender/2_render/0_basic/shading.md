# shade_editor
## short cut
- disconnect node
	- C mouse2 
- rm panel
	- C x
- copy color
	- C c

## panel
- the left side of the panel is for input, and the right side is for output

# viewport shading
## modify the direction of studio_lights
modify 'rotation'

## modify the strenght of studio_lights
modify 'strenght' 

## modify the brightness of background
modify 'world opacity'

## want the preview more real
- 1
```python
shading.lighting.scene_lights = True	# enable the user_created_light
shading.lighting.scene_world = True		# enable the studio_lights
```
- 2
```python 
Material.settings.Screen_Space_Reflection = True
```
- 3 
```python
import render.eevee

ambient Occlusion = True
bloom = True
screen_space_reflections = True
screen_space_reflections.reflection = True
```
# render shading
## Eevee
### want the preview more real
- let objects relect the lights of their own material colors
```python
S_a.light_probe.irradiance_volume
do(put it to the objects, change the size{bigger than the objects})

# if want auto_bake
bakerender.eevee.indirect_lighting.bake_indirect_lighting()
render.eevee.indirect_lighting.auto_bake = True

# if want pre_bake bakerender.eevee.indirect_lighting.bake_indirect_lighting()

```
- goto viewport_shading.want_the_preview_more_real

# problems
	 shading of an area is conspicious显眼
	 	expand area of the corresponsing meshs