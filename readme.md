To do the quantization of the texture, we need to bake out some maps:

1. Create b/w map where you want the strokes to have a directional aspect. E.g: bake out curvature map
2. Use the image_gradient OSL shader to calculate the image gradient (rate of change), bake that out
3. Use the directional_scatter OSL shader to scatter bitmaps