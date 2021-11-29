# Volumetrics

Adding a volume to the whole scene gives it a really sweet foggy / vibey effect that I love. 

## Adding volume ot the scene
- Start by adding a cube, and scale it to fit the whole scene
- Shader editor -> delete Pricinpled BSDF
- Add a Pricipled volume and connect its volume to volume of the material output
- NAME THE MATERIAL!

## Density
0.05-0.08 seems to be a sweet spot for a quite heavy foggy effect (at least in dark scenes).

## Color
A stronger color gives more contrast, which seems to match quite a few of the references I've been comparing to. A lighter color can also be cool sometimes though.

## Noise
To reach a more natural foggy effect, connect a musgrave texture's height into the volumes density. 
This creates some cool noisy volume.

## Absorption
- Add an "add shader" node
- Add a volume scatter node, low density
- Add a volume absorption node, same low density

// TODO: how does this look in a bigger scene?

## Light pattern / light throw
// TODO: learn how to procedually create light patterns in volume using image textures.
https://youtu.be/AXjE-t6dFZ8 at around 4min

## God rays
God rays comes from shining a quite strong sun lamp through a volume with a low density.

// TODO: what is volume scatter?
