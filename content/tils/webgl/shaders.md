---
title: "Intro to Shaders"
date: 2022-05-12T17:46:39-03:00
---


## Terms
- fragCoord -- Pixels x,y,z value

Using the fragCoord lets make half the screen black
and the other half red
```
void mainImage( out vec4 fragColor, in vec2 fragCoord)
{
  vec2 xy = fragCoord.xy; // we obtain our coordinates for the current pixel
  vec4 solidRed = vec4(0,0.0,0.0,1.0); // this is actully black right now
  if (xy.x > 300.0) {
    // Arbitrary number, we don't know how big our screen is
    solidRed.r = 1.0; // set its red component to 1.0
  }
  fragColor = solidRed;
}
```

For any `vec4` you can access its components via obj.x, obj.y, obj.z and obj.w etc.
Its helpful to rename them so when other people look at your code they will understand that `obj` represents a color.



Shader toy passes use uniforms which are variables which are passed from the CPU to the GPU
````
void mainImage( out vec4 fragColor, in vec2 fragCoord)
{
    vec2 xy = fragCoord.xy; // we obtain our coordinates for the current pixel

    xy.x = xy.x / iResolution.x; // we divide the coordinates by the screen size
    xy.y = xy.y / iResolution.y;

    // Now x is 0 for the left leftmost pixel, and is 1 for the rightmost pixel

    vec4 solidRed = vec4(0,0.0,0.0,1.0); // this is actully black right now
    if (xy.x > 0.5) {
      // Arbitrary number, we don't know how big our screen is
      solidRed.r = 1.0; // set its red component to 1.0
    }
    fragColor = solidRed;
   }
   ```


   ## From Split to Gradiant

   turning this into a gradiant should be, our color values go from 0 to 1, and our coordinates now go from 0 to 1 as well

   ```
   void mainImage( out vec4 fragColor, in vec2 fragCoord)
{
    vec2 xy = fragCoord.xy; // we obtain our coordinates for the current pixel

    xy.x = xy.x / iResolution.x; // we divide the coordinates by the screen size
    xy.y = xy.y / iResolution.y;

    // Now x is 0 for the left leftmost pixel, and is 1 for the rightmost pixel

    vec4 solidRed = vec4(0,0.0,0.0,1.0); // this is actully black right now

      // Arbitrary number, we don't know how big our screen is
      solidRed.r = xy.x; // set its red component to normalized x value

    fragColor = solidRed;
   }
   ```
