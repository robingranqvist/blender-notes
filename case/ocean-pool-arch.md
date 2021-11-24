# Case - Ocean Pool Arch

This is a fairly minimalistic render, featuring a pool in a room, looking out into the oceanic distance through an arch. There's also a little plant
in the corner, courtesy of Blenderkit (free 3D assets).

- Engine: Cycles
- Resolution: 1080 x 1350
- Samples: 700 for final render
- Max light bounces: 3
- Adaptive sampling
- No denoising
- No post-processing

![arch-pool-ocean-final-render](https://user-images.githubusercontent.com/54509721/143142597-0c430015-c0db-493b-9487-7f6376ee77ee.png)

## The room

- Add a simple cube
- Go into edit mode and select all verticies of one side
- Remove them by CTRL + X -> Faces
- Add a solidify modifier to the cube and thicken to taste

### The room - material

- The material is a simple colored "default" material with high roughness
- There's a barely noticable voronoi texture sent through a bump node to the material. Scale of 0.001 and strenght of 0.01.

## The arch

Modelling is hard, and even such a simple shape as this one was hard for me to create. Luckily there's all kinds of tutorials out there.
I used [this technique](https://www.reddit.com/r/blender/comments/g37t1n/blender_secrets_how_to_make_an_arch) provided by a Reddit user.

- Add a cube
- Scale it on the X or Y-axis
- Add around 15-20 loop cuts by pressing CTRL + R
- Navigate to one of the "exact axis views" (one of the colorful buttons in the top right of the viewport)
- Press F3 and search for the "warp tool"
- Change the warp angle to 180 degrees
- Extrude the bottom vertices of both "legs" of the arch
- Select all vertices of the front of the arch and press CTRL + F. This fills them up
- Remove the leftover vertices (on the back side)
- Add a solidify modifier and thicken it up to taste

This was very uncesssary. //TODO: Learn a new way to create arches.

The room has a boolean modifier applied, which cuts out the arch shape out of the wall. The arch is then hidden in the render (and viewport).

## The pool

### The outer ring 

- Add a circle
- Scale to taste
- (What did I do here? Can't remember)
- Add a solidify modifier and thicken to taste
- Add a bevel modifier and bevel to taste
- The material is a slightly more metallic version of the same material as the room.

### The water

- Add a cylinder
- Scale to taste and place inside the outer pool ring

For the water material, I used a material from the free addon Blenderkit. Couldn't be bothered learning to create just as good water for this project.

## The outside ocean

- Add a cube
- Scale to taste, fill the frame outside
- Add the same watermaterial, but modify scale and color to look more "oceany" (size of noise waves, darker color)

## The sky

The sky is a free image from Unsplash, imported as a plane with shadows removed. Looks great. It's then placed behind the "ocean" and scaled to fill the frame.

## The plant

As mentioned above, the plant is a free asset from the Blenderkit addon.

## Lighting

### Outside light

The whole scene is being lit by an evening HDRI from Polyhaven. It's rotated to light up the room straight from the outside in through the arch. It's 
set to a strenght of 0.5, and is complemented by a white sun light, also at a strenght of 0.5. Both are rotated to light from (almost) the same angle.

### Inside light

There are three main lights inside the room; two point lights and one area light.

- Point lights: 10 w, radius of 1 meter and a slight light blue color.
- Area light: 50 w, radius of 3 x 1.5 and a strong pink color.

#### Point lights

The point lights are placed above the arch, giving an almost reverse vignette kinda look at the top left and right of the scene. 
These are used to give the top of the room a bit of light. 

#### Area light

The area light is probably my biggest takeaway from this render. It gives the room a much brighter feeling, but the color compliments the whole room-color so well. 
It was actually colored by mistake, but immediately gave the render a nicer vibe. Definitely gonna keep use colored lights for scenes like this.

## Improvements

- Could probably be a bit more light inside the room
- Figure out how to add more subdivisions to the arch. It's a bit clanky as of now.
- Water could be more lightblueish, aka. pool-waterish
- Show more of the thicknes of the arch. How? Hmm, maybe a slighly different angle of the shot?
- Figure out how to create, place & scatter some winding plants around the arch opening
- Softer light. How? Maybe use the integrated sky texture instead of HDRI & sun light
- The outside is more of a day-feeling instead of an evening-feeling, even if the latter was intended at the start.

## Good things :)

- I like the chill vibe
- Figured out how to use weird colored lights together with the color of the room
- I kinda like the lighting overall
- Finally figured out arches
