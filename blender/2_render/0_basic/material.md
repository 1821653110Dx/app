# type
## none metalic materials
- Metallic = 0
- modify the following to change materials
	- roughness

## metalic materials
- Metallic = 0
- transmission = 1
- change the materials
	- roughness
	- IOR
		- to set IOR, you need to know current material's IOR by surffing 
	- specular
		- the higher the specular, the clearer objects relected on its surface

# transform
```python
# transform world background img
shading.shader__type = 'World'

from input texture_coordinate
from vector import mapping

image_texture.vector = mapping.vector
mapping.vectorr = texture_coordinate.generated
DO(set the attributes of mapping)	# if render_engine = cycles, change mapping.rotation() will change directon of shadows
```

# add materials
## Applying 2 Different Materials to the Light and Dark Faces of Objects
```python
from Texture_Coordinate, Seperate_color, Mix, Diffuse_BSDF, Color_Ramp import *

Seperate_color.Mode = RGB ;
Seperate_color.Color = Texture_Coordinate.Normal ;
Seperate_color.Blue = Seperate_color.Color ;

Color_Ramp.Fac = Seperate_color.Blue ;
Color_Ramp.Color = Color_Ramp.Fac ;

# color1 = Bright color, color2 = Dark color
Mix.DataType = Color ;
Mix.BlendingMode = Mix ; 
Mix.Factor = Color_Ramp.Color ;
Mix.Ressult = Mix.Factor ;

Diffuse_BSDF.Color = Mix.Ressult ;
Diffuse_BSDF = Different_BSDF.Color ;

Material_Output.surface = Diffuse_BSDF.BSDF ;
```tip
