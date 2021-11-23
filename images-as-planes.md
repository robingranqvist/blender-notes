# Images as planes

## Enable the addon
- Go into Edit -> Preferences -> Addon, search for "images as planes"
- Enable it and save preferences

## Adding images as planes
- Shift + A to add a new object
- Select Image -> Image as plane
- Change "Material Setting" to "Emit" (TODO: Why?)
- Select your image
- Import

## Shadow invisibility

The image will cast shadows as default. This is not good (at least not if you're using it as a background image).

- Object properties -> Ray visibility -> Turn off shadows
- Boom, done.

## Rotating & scaling

The image will be really small when imported. Rotate & scale it to cover the whole background (or whatever you want it for) and MAKE SURE
to rotate it similarily to how your camera is rotated. This makes it look better for some reason.
