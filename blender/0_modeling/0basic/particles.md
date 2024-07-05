# short cut
- hide particle_systems of several objects at the same time
	- M mouse 1

# emitter
## set particle as certain object
```python
from particles.render.emitter import *

render_as = object ;
object.instance_object = certain_object
```

## make particles have different size
```python
from particles.render.emitter import *

render.scale_random = ?
```

## make particles move randomly
```python
from particles.emitter.physics.forces import brownian
```

## starting velocity
```python
from particles.emitter.velocity import *
```

## let particles rotate after collion or effectors
```python
from particles.emitter import *

particles.emitter.rotation = True
particles.emitter.rotation.dynamic = True
```

## set weight of force received
```python
from particles.emitter.field_weights import *

# select the collection of field_weights, which will effect particles
effector_collection =  ?

# set the weight of gravity on all forces, which is not included in the collection of field_weights
field_weights.gravity = ?


# set the weight of all field_weights on all forces
field_weights.all = ?

# set the weight of wind on all field_weights
field_weights.wind = ?
```

# Hair
## set particle as certain object
```python
from particles.render.hair import *

render.render_as = object 
object.instance_object = certain_object
```
## Arrange particles 
- along the normal
```python
from particles.render.hair import *

object.object_rotation = True
```
- along global_z, and make particles rotate along the axis
```python
from particles.render.hair import *

advanced = True
rotation = True

rotation.orientation_axis = global_z

rotation.phase = ?
```
## set the density and length of particles
```python
from particles.render.hair import *

# set density of particles
vertex_groups.density = ?

# set length of particles
vertex_groups.length = ?
```

# meshes collided
# killed particles 
```python
from physics import *
from sympy import *

certain_object = symbols('certain_object')

Collison.add(certain_object)

Collison.particles.kill_particles = True
```
# stick particles
```pythhon
from physics import *
Collison.particles.stickinness =
```
# be passed through
```python
from physics import *
Collison.particles.permeability = 
```
# minize $v_z$ after colliding
```python
from physics import *
Collison.particles.damping = UP
```
# minimize the $v_{xy}$ 
```
from physics import *
Collison.particles.friction =

Collison.particles.randomize = 	 # set random fritcion
```

# tips
## particles to object
```python
# transform
EMITTER.modifiers.particle_system.make_instances_real()

# remove corresponding particle_system
particles.particle_system.remove(corresponding_particle_sysyem)

# if  want every object independent, then
DO(select one object)
S_l.object_data()
object.relations.make_single_user.object_and_data(selected_objects)
```

# warn
- every time you change something of your particles system, remember to 'particles.emitter.cache.bake()'

# problems
## there is something wrong with rendered particle animation
- S leftarrow
- particles.emitter.emission.number = random_number
## if there are no particle_animation in the rendered animation
```python
# if emiter
particles.emitter.cache.bake()
```
## for particles_animation, if there is nothing changed after you changed something of particles_system
```python
particles.emitter.cache.delete_bake()
```
## if emiter is missing but particles is exsisted after baking
```pytthon
particle.emitter.render.show_emitter = True
```
## if particles are missing but emiter is existed after baking
```python
particles.particle_system.camera_icon =True
```
