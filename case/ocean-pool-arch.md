# Case - Ocean Pool Arch

This is a fairly minimalistic render, featuring a pool in a room, looking out into the oceanic distance through an arch. There's also a little plant
in the corner, courtesy of Blenderkit (free 3D assets).

![arch-pool-ocean-final-render](https://user-images.githubusercontent.com/54509721/143142597-0c430015-c0db-493b-9487-7f6376ee77ee.png)

## The room

- Add a simple cube
- Go into edit mode and select all verticies of one side
- Remove them by CTRL + X -> Faces
- Add a solidify modifier to the cube and thicken to taste

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

## The pool

### The outer ring 

- Add a circle
- Scale to taste
- (What did I do here? Can't remember)
- Add a solidify modifier and thicken to taste
- Add a bevel modifier and bevel to taste

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
