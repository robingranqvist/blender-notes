# Creating a simple ground plane with noise bumps

Totally straight ground planes are boring. Let's add some bumps.

### Subdivision
- Add plane
- Scale plane by clicking S -> 5
- Go into edit mode (Tab)
- Right click -> subdivide
- Open little left menu & subdivide 20-50 times

### Noise
- Add a displacement modifier
- CTRL + A -> apply scale from last step
- Click new -> go into settings for the new noise
- Change type from image to "clouds" texture
- Set depth to 0 and play around with scale

### Modifier strength
- Go back into modifiers
- Lower strenght of the modifier
- Right click plane -> Shade smooth
