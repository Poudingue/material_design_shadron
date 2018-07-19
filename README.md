# Material design - Shadron

This is a tool to experiment with material shading.

## Features

Allows definition of simple material parameters, no textures, only values.
It allows import of a reference image for comparison, and display negative and positive differences in two separated windows.

Diffuse models :
- Lambertian
- Max diffuse (an attempt to emulate 3dsmax diffuse model. Only works for light at latitude and longitude 0 and render with iray for now)
- Oren-Nayar

Specular models :
- Phong
- Blinn-Phong
- Max metal (an attempt to emulate 3dsmax “Metal” material. Useless for now.)
- Cook-Torrance (For now with Schlick's approximation)

## Parameters

For the material itself :

- light_latitude and longitude : Allows you to place the light with spherical coordinates.
- diff_color : Diffuse color for the material, albedo if you prefer.
- spec_color : Should stay grey for dielectrics (white for use with Cook-Torrance), can be colored for metals, with black diffuse.
- shininess : exponent for Phong and Blinn-Phong approximations. The higher the shinier.
- σ : Roughness of the material. Can be expressed as 1-glossiness, the lower the shinier. (for Oren-Nayar and Cook-Torrance models)
- IOR : Indice of refraction of the material. Used by Cook-Torrance only

For visualisation (and color picking):

- size : The width and height of windows
- γ_image : gamma correction of the reference image. Most of the time 2.2.
- γ_screen : gamma correction of your screen. Most of the time 2.2.
- diff_amplification : Amplification applied to the comparison windows.
