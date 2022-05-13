---
title: "Draw Images"
date: 2022-05-12T17:46:39-03:00
---


Display image in ShaderToy
```
void mainImage ( out vec4 fragColor, in vec2 fragCoord )
{

    vec2 xy = fragCoord.xy / iResolution.xy; // Condensing this into oneline
     vec4 textColor = texture(iChannel0,xy); // get the pixel at the xy from iCahnnel0
    fragColor = textColor; // set the screen pixel to that color
}
```


Flash RBG over time
```
void mainImage ( out vec4 fragColor, in vec2 fragCoord )
{

    vec2 xy = fragCoord.xy / iResolution.xy; // Condensing this into oneline
     vec4 textColor = texture(iChannel0,xy); // get the pixel at the xy from iCahnnel0
    textColor.r *= abs(sin(iTime));
    textColor.g *= abs(cos(iTime));
    textColor.b  *= abs(sin(iTime) * cos(iTime));
    fragColor = textColor; // set the screen pixel to that color
}

```
