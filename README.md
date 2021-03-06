# Raytracing
A simple Raytracing-Algorithm based on the article of scrathpixel extended with soft shadows. This project was developed for the university of applied science karlsruhe (germany), course of study 'computer science', subject 'computer graphics'.
Feel free to create pull requests!

## Features (already implemented)
* Spheres with transparency, emissive, reflective and surfaceColor
* Reflection
* Refraction
* Hard Shadows
* Soft Shadows
* Output in .ppm image

## Settings
You can controll the quality of the shadows and the overall result in the settings.h headerfile.
* Change the max. ray depth of all tracing
```C++
#define MAX_RAY_DEPTH 12
```
* Change the amount of shadow rays per pixel which intersects with a sphere. (0 -> no shadows, 1 -> hard shadows without noise, high value -> less noise)
```C++
#define SHADOW_RAYS 5000.0
```
* Adjust the max spread for all the shadow ray. (0 = no offset -> hard shadows with noise)
```C++
#define OFFSET_PERCENT 3.50
```
* Control how dark the shadow will be, if no shadow ray hits the emissive sphere. This increases the brightness of all shadows.
```C++
#define MIN_SHADOW_BRIGHTNESS 0.15
```
The options regarding the size of the created image, size of render blocks and number of threads the render is running in can be set as well.
* Adjust the dimensions of the created image
```C++
#define width 640
#define height 480
```
* Adjust the size of blocks that are rendered at once. These sizes have to perfectly divide width/ height.
```C++
#define BLOCK_WIDTH 40
#define BLOCK_HEIGHT 30
```
* Adjust the number of threads.
```C++
#define THREAD_COUNT 4
```


## Authors
Author of the scratchpixel.com blog, @mbpictures, @vacl.
