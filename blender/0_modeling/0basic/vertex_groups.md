# creatte vertex group
## use weigh Paint
```python
from interaction import *
from data import *

vertex_groups.add('group1')

interaction.mode_set('weight_paint')
DO(paint as you wish)

interaction.mode_set('edit_mode')
vertex_groups.assign('group1')

```