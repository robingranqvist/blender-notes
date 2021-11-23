# Render engine
These are some typical settings for renders using Cycles on Concierge render cloud rendering system.

## Samples
Render properties -> Sampling.
For lighter scenes (strong sun lights, hdri's etc.), use somewhere between 200-400. Could probably boost a bit if using cloud rendering.
Darker scenes with volumetrics needs a lot more. Up to 2k-3k samples. Still a bit of noise on really dark renders, but looks kinda nice.
Volumetrics need higher sample count!

## Adaptive sampling
Render properties -> Sampling -> Adaptive sampling.
Just turn it on. Seems to cut the render time a bit.

## Reduce light bounces
Render properties -> Light paths -> Max bounces (Cycles).
Use light bounces between 2-4. More isn't needed. Cuts render time A LOT.

## Tile size
Performace -> Tiles.
Use whatever depending on local or cloud render.

## Area light portals
Object data properties -> Portal.
Lower noise for area lights.

## Object instancing
Don't duplicate identical objects! ALT + D to make them share object data. 99% less memory usage.
Share object data by CTRL + L -> Object data (on other instances of the same object).

## Adaptive subdivision
Higher poly count on foreground objects.
Subdivision modifier -> Adaptive subdivision (Experimental feature).

## Local renders
Use GPU with or without optix denoising.

// Todo: Learn about settings for glass / metallic materials.
