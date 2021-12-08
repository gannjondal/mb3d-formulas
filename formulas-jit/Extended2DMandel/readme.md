# Non-standard approaches to extend known 2D fractals to 3D, or 4D

## Extensions, and variations of the official formula Mandel4DBiC

**Formula names:**   
`JIT_gnj_BiMand*.m3f`   
   
**Idea:**   
The idea is simple:  A 4-dimensional space can be seen as two flat planes, orthogonal to each other.   
When you now take two 2d Mandelbrot sets, each living in one of the plans and put it to a fractal program then --- something interesting may be shown.   
This (and nothing else) is done by the original `Mandel4DBiC`.   
And indeed it is possible to get something interesting with some tricks (hybridisation).   
   
However, the formula becomes much more interesting, and easier to be used if you allow to have the two Mandelbrot sets interacting with each other.    
You can get for instance filigree, and twisting threads meandring through the space - symmetrical enough to not be confusing, but irregular enough to form beautiful structures.   
The idea may sound somehow primitive - however I really like the results....   
   
**Implementation:**   
The implementation is rather simple as well - within `JIT_gnj_BiMand_03.m3f` the mixture part looks like:   
```
   x := tmpx + mxz*tmpz + mxw*tmpw + cx;   
   y := tmpy + myw*tmpw + myz*tmpz + cy;   
   z := tmpz + mzx*tmpx + mzy*tmpy + cz;   
   w := tmpw + mwy*tmpy + mwx*tmpx + cw;   
```   
where (x, y), and (z, w) span the two planes, and `tmp*` are the respective temporary variables.   
The variables `m[target][source]` are the configurable parameters.   
Of course, the `c*` variables follow the usual conventions for escape time fractals.   
