# automatically set the background texture and the enviroment light
```python
# if render_engine = Eevee, there aren't shadows if no lights added
# if render_engine = cycles, there are shadows even if no lights added
from world import *

color.type(enviroment_texture)
color.enviroment_texture.open(path_of_hdr_img)	# you can download hdr imges at "hdrihaven.com" for free
```
