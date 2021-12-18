# Formula files utilizing projections from, and to Riemann spheres using stereographic projection   
   
The original main idea was originally to    
- map 3D to the Riemann Sphere, 
- map the sphere to the complex plane (by stereographic projection),    
- do some operations,    
- map everything back.    
   
You can find some more examples, and details at https://www.fractalforums.com/mandelbulb-3d/a-new-jit-formula/   
    
The formulas within this folder do only contain the formulas, and params from above fractalforums.com thread.   
For more recent versions see at [/formulas-jit/RiemannSphere/](/formulas-jit/RiemannSphere/).    
   
## Formulas:   
- **JIT_gnj_RiemPow2\_\*.m3f:**    
  The above mentioned complex operation is a calculation of the old 2D Mandelbrot (just up to 3 iterations due to the limitation of JIT).    
  You can find details, and param description within the formula    
- **\_JIT_gnj_RiemSimple\_\*.m3f:**    
  The complex operation is just about scaling, rotation, and translation     
- **\_JIT_gnj_RiemPowRadial\_\*.m3f:**    
  The complex operation is z(n)^Complex_Z_Power plus some rotation   
