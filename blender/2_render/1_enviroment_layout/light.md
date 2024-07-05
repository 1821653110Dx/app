# shadow
## Eevee
### quality
- render setting
```python
from render.Eevee.shadows import *

# set quality of sunlight
cascade_size = ?

# set quality of other lights
cube_size = ?

# further improve quality(better enable it in final render only)
high_bit_depth = True
```
- data setting
```python
from data import *

# for sunlight, the same as other lights
sun.shadow.contact_shadows = True
sun.shadow.cascade_shadow_map.fade = ?	# define softness of transition of shadows when the zoom changes
sun.shadows.cascade_shadow_map.max_distance = ?	# define which distance the shadows begin to be not intact
sun.shadow.cascade_shadow_map.distribution = ? # distribution up, nearby shadow better, shadow in the distance worse
```
### set the influence disance of non_sun_light(> distance the shadow won't be generated)
```python
# take spot_light as an example
spot.custom_distance = True
spot.custom_distance.disance = ?
```

### problems
if occur some problems, you can adjust
```python
from data import *

# for sunlight, the same as other lights
shadow.bias = ?
shadow.contact_shadows.distance = ?
shadow.contact_shadows.biaas = ?
shadow.contact_shadows.thickness = ?
```

# lights
## Eevee
### method
- show the volume of the lights/create fog
```python
DO(add a 'cube', move it to where the light is, adjust its size)
DO(create a material for the cube)
material[the_material].surface(Remove)
material[the_material].volume(Principled_Volumed)
Do(adujust the density, color and so on)

# adjust at which distance the samples begin to be generated and at which distance samples won't been generated
render.render_Engine(Eevee).volumematrics.start = ?
render.render_Engine(Eevee).volumematrics.end = ?

# set the quality of the fog
render.render_Engine(Eevee).volumematrics.samples = ?	# the bigger the better;set the number of layers of the fog
render.render_Engine(Eevee).volumematrics.the_size = ?	# the smaller the better; set the quality of each layer

# set the distribution of samples
render.render_Engine(Eevee).volumematrics.distribution = ?	# higher the value is, the more of these samples will be distributed closer to the camera ; lower the value is, the more of them are evenly distributed across [start, end]
```
- enable the light of non_sun pass through the object
```python
# take spot as an example
from data.light.spot import *

shadow.clip_start = ?	# increase the value; clip_start used to set at which distance the light can be obstructed
```
- 

# tips
- make several lights share same data
	- C l, object_data

