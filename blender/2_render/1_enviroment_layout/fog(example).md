# Eevee
```python
DO(add a 'cube', move it to where the light is, adjust its size)
DO(create a material for the cube)
object.viewport_display.diplay_as = 'Wire'

material[the_material].surface(Remove)
material[the_material].volume(Principled_Volume)
Do(adujust the density, color and so on)

# adjust at which distance the fog begin to be shown and at which distance the fog begin to be disappear
render.render_Engine(Eevee).volumematrics.start = ?
render.render_Engine(Eevee).volumematrics.end = ?

# set the quality of the fog
render.render_Engine(Eevee).volumematrics.samples = ?	# the bigger the better;set the number of layers of the fog
render.render_Engine(Eevee).volumematrics.the_size = ?	# the smaller the better; set the quality of each layer

# set the distribution of layers
render.render_Engine(Eevee).volumematrics.distribution = ?	# if = 0, at any distance the quality of the fog are equal; if > 0, the bigger, the better when close the fog
```