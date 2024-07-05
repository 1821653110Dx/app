# navigation
## walk/fly
- enable/diable
	- S ~ / click
- walk
	- w a s d
- fly up/down
	- e, q
- jump
	- v
- run / sneak潜行
	- S/M
- teleport 瞬间转移
	- space
- change speed
	- roll mouse 3
- enable gravity
	- g
# object mode
## select overlapped objects
S M mouse1
## loaction
- let object always move on th face
	- enable snap(S Tab)
	- select 'face project'
	- enable 'align rotation to target' 'backface culling', both of which subodinate to target selection
	- enable 'move', 'rotate'
> if result not satisfying, set global to local, try again

## edit geometric center
	C .
## combine objects
	C j

## flip
	C m <axis>

##  cp a certain attributes of last object
> scale, location, rotation...
> need enable add-on : copy attributes menu

	C c, chose the option

## curve
- line >> tube
	- data-geometry-bevel-round, set depth

# edit mode
## selection
- proportional editing = o
	-  if affect the connected parts only, select 'connected only'
- brush c
- select the non-manifold非流体几何
	- select-select_all_by_trait-non_manifold

## baisc edit
- connect verticles
	- J
- rip$\tiny 撕裂$ vertices/edges
	- v
- 1line -> 2 lines
	- bevel
- flatten edge
	- in x-z: s y 0
- subdivide
	- setlect the top and bottom edges, mouse 2, subdivide
	![36f261ed5c759cbb6967aad15c237777.png](../../../../_resources/36f261ed5c759cbb6967aad15c237777.png)
	- subdivid, C S b
	![c2d681b081c25abec7307e99bda92692.png](../../../../_resources/c2d681b081c25abec7307e99bda92692.png)
- fill
	- normal : f
	- triangular face : M f
	- C f, grid fill
		- ![fceff7fdf0c4b0405330aef3a990e176.png](../../../../_resources/fceff7fdf0c4b0405330aef3a990e176.png)
- rm overlaped faces/edges
	- rm verticles
- make closed edges round
	- M S s
- normal
	- flip : M n
	- reevaluate : S n(used to fix normal orientation)
- extrude
	- quick extrude = mouse 2
	- menu = M e
> with subdivision modifiers enabled, if you want to extrude less rouned parts, you can extrude twice
- bevel
	- adjust "Shape" in BEVEL panel at the bottom left corner
	![c2ea4b0e9778cb9c31fd211956f31288.png](../../../../_resources/c2ea4b0e9778cb9c31fd211956f31288.png)
## cut off
- create a surface
- swicth cut orientation : switch nornal direction
- select the surface and object to  cutoff, enable bool-tool, use difference

## hole
- create a closed skecth: create a plane, rm its vertexes, enable Snap(face project), add vertex by C mouse2, F
- extrude the sketch
- use bool  tool

- ##### sketch on a plane
  
  - add a plane
    
  - use knife to sketch on the plane
    
  - delete faces and useless edges
    
- ##### project edges to an object
  
  - F3 knife-project

## problems
- If mirror operation doesn't work, aplly scale

