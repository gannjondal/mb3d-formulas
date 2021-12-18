# Formula files utilizing projections from, and to Riemann spheres    

## Variant 1:  Using stereographic projection   
The original main idea was originally to    
- map 3D to the Riemann Sphere,   
- map the sphere then to the complex plane (by stereographic projection),   
- do some operations on complex plane,   
- map everything back.    
   
You can find some more examples at https://www.fractalforums.com/mandelbulb-3d/a-new-jit-formula/   
   
## Formulas:   
- **Jit_gnj_RiemannPower2_\*.m3f:**   
  Implements variant 1.   
  The above mentioned complex operation is a calculation of the old 2D Mandelbrot (just up to 3 iterations due to the limitation of JIT).   
  You can find details, and param description within the formula.   
  ![Sample image:] (./RiemPower2Sample.jpg)   