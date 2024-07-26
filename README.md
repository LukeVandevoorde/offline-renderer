# Offline Renderer

![endless_final_scene2_MIS_1600](https://github.com/user-attachments/assets/25c0913d-5474-4bce-91a8-d8134065943a)

Rendered at 1620x1080, 1600 samples per pixel. The scene is composed of a low poly wolf, tortoise, the Stanford bunny, and a pair of glasses in a closed room with one surface light at the top.
The glasses lenses and nose pads are smooth dielectric glass, while tortoise is rough glass. The glasses frame and wolf are metallic microfacet iron, while the bunny is microfacet gold.
The walls are all matte lambertian materials. The lenses themselves are constructed as the intersection of two icospheres and have a focal length of 1 meter.

Note that there is a wall behind the camera as well, which is reflecting light back onto the glasses, causing the concentric circles effect.

The path tracer is written in C++. It supports Lambertian, Microfacet, and Dielectric materials. Microfacet and Dielectrics use [GGX](https://www.cs.cornell.edu/~srm/publications/EGSR07-btdf.pdf) as the normal distribution function.
The path tracing algorithm uses Multiple Importance Sampling to combine the values of a surface normal ray, and a direct light sampled ray.

OpenMP is used to parallelize rendering across all cores.

The code is closed source since this was written as part of a special topics course at UCSB, but feel free to contact me if you want to talk about it

Credit to [Jakob_T_Designs](https://www.thingiverse.com/jakob_t_designs/designs) for the wolf,
[BWuckle](https://www.thingiverse.com/bwucke/designs) for the tortoise, and Stanford for the bunny
