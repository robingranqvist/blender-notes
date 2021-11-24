# Sand dunes

Instructions for fully procedual sand dunes.

## Base

- Add a plane
- Go into edit mode and add subdivisions (or a subdivision modifier -> simple -> using adaptive subdivisions)
- Go into shader editor -> New material
- Change color to whatever sandy color you want


## Displacements

- Go into Material -> Settings -> Surface -> Displacement & bump
- Shader editor -> add a Voronoi texture node
- Add a displacement node
- Connect distance into height & displacement into displacement on the output
- Change the scale settings on the displacement node
- Change scale on voronoi texture (you could also use node wrangler to mapping node)
- Add a Mix RGB node -> connect into voronoi vector
- Add a Noise texture -> connect into mix RGB color 2
- Change factor on Mix RGB node
- Change voronoi to Smooth F1

## More detail

For more surface details, add a new Noise texture into a new Mix RGB node, and mix voronoi & noise into displacement node
Increase scale of noise, and reduce factor on mix node -> more noisy detail
Use node wrangler to scale the noise down

DONE.
