![](https://github.com/zpelgrims/directionalscatter/blob/master/wip_001.png?raw=true)
![](https://github.com/zpelgrims/directionalscatter/blob/master/wip_001_expl.jpg?raw=true)

To do the quantization of the texture, we need to bake out some maps:

1. Create b/w map where you want the strokes to have a directional aspect. E.g: bake out curvature map
2. Use the image_gradient OSL shader to calculate the image gradient (rate of change), bake that out
3. Use the directional_scatter OSL shader to scatter bitmaps


// would be way better if i can remove the baking steps:
// look into:
//  https://github.com/mmp/pbrt-v3/blob/7095acfd8331cdefb03fe0bcae32c2fc9bd95980/src/core/texture.cpp#L93
//  https://graphics.stanford.edu/papers/trd/trd_jpg.pdf
//  https://computergraphics.stackexchange.com/questions/5939/ray-tracing-partial-derivatives-for-texture-lookup
