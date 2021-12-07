# Formulas, and samples for the Mandelbulb3D program

## Intention, notes:
**This repository is mainly intended to publish formulas (currently JIT formulas only), and related samples for the program Mandelbulb3D (MB3D, M3D).**   
    
Please find MB3D at https://github.com/thargor6/mb3d   
   
Originally these `ABC-formulas` repositories were mainly intended to publish my own formulas, and related samples for the several fractal programs I use.   
This was mainly since I found that I need a central place for my formulas rather to have them scattered across the fractal forums, deviantart etc.   
Also I made the experience in earlier days in Ultrafractal that versioning 'by hand' is really a nightmare - I know, that should be self-eveident for any 'real' developer, but I don't see me as true developer, and hence I felt into that trap...   

However, while thinking about the way to build such a central repository I came to the conlusion that I would like to follow more the common open source approach, and to publish the formulas in a way that everyone can contribute.   
Therefore - Please feel free to contribute, ask for changes / corrections / improvements, to add your comments, and questions etc.   
    
In any case this repostiory is currently **not** thought to be included into the official MB3D distribution.   
If there would be a real active development of MB3D I would talk with the program author to establish such a central repository.   
But as of now the current maintainer says that there is no further active development planned.   
   
**Nevertheless I want to encourage you to share own .m3f formulas (be it JIT, or ASM) here as well.**   
   
**Formula naming:**  The current idea is to identify the original formula author by a specific prefix (in my case JIT_gnj_).    
The prefix JIT_ is necessary by MB3D program design to identify JIT formulas (other prefixes may work, but with slight limitations).   
The style to use \3-digit name identifiers to identify formula authors comes from Ultrafractal (and is used to a certain extend also in MB3D JITs spread over the web).   

## Usage of JIT / .m3f formulas:
To use JIT formulas you need MB3D >= 1.90 .   
To get the files included into your MB3D place the .m3f files into the configured formula directory (usually \\M3Formulas\\) of your MB3D installation, and (re-)start your MB3D.    
Afterwards you will see the tab you had configured using the .DEoption parameter in the formula.   
More hints regarding the development of JIT formulas can be found at [published-samples/gnj/da-jittutorial](published-samples/gnj/da-jittutorial)   

## Folders:   
- The folder [formulas-jit](formulas-jit) contains JIT .m3f files (and potentially sample data) independent from any publishing elsewhere.   
  Any possible development will happen here.   
     
  The folder contains several subfolders related to several mathematical ideas etc:   
  - **AmazingXYZ:**  AmazingBox, AmazingSurf and variations
  - **Attractors:**  Classical attractors
  - **BasicFunctionsTo3D:**  Any pure mathematical function in triplex algebra
  - **Bulb3D:**  Anything around fractals of polynomic functions (like, but not restricted to z=z^k+c) using triplex algebra
  - **Bulb4DNonQuat:**  Anything around fractals of polynomic functions (like, but not restricted to z=z^k+c) using 4D numbers (but not quaternions)
  - **Bulb4DQuaternion:**  Anything around fractals of polynomic functions (like, but not restricted to z=z^k+c) using quaternions numbers
  - **Diverse**
  - **Extended2DMandel:**  Approaches to "extend" the traditional 2D Mandelbrot formula (and similar formulas) without raising it to higher-dimensional numbers.
  - **Mixtures**
  - **Newton3D:**  Newton fractal in triplex algebra
  - **Newton4D:**  Newton fractal using quaternions etc
  - **Proprietary:**  Anything specific from one's own idea kitchen which should not simply land up under `Diverse`
  - **RiemannSphere:**  Anything related to the idea to do a kind of 2D calculation using Riemann spheres, and spherical projection to the surface (and back)
  - **Simplex**
  
- The folder [published-samples](published-samples) will contain JIT .m3f formulas, and other related data published elsewhere (currently at fractalforums.org, fractalforums.com, and deviantart.com).    
  The files will not be changed (beyond any possible improvements of non-functional parts like documentation etc).   
  Even corrections would result in new files for compatibility with the existing threads.   

## Disclaimer:
The formulas have been tested on my box (Windows 7/10 with older Intel processors -mainly i7/4930, and i5/4440-) - and sometimes nowhere else.    
I have heard that some users of Linux/Wine had some difficulties with JIT formulas - but please feel free to test.   
Also I never have heard about results on a Mac.   
But I neither have the capacity, nor the intention to test the somewhere else than on my normal boxes.   
Hence I cannot provide any warranty for this code. -    
Please however do not hesitate to share your experiences, or to add code that helps to run it on other hardware, or OS.   
As of now I'm publishing all of my formulas under the LGPL license (see the according license file if you really should like that stuff)...   
   
My formulas need MB3D \>=1.90 to run - they cannot run independently (in fact JIT formulas are written in a proprietary language).   
Of course this program is using own disclaimers, and licenses.   
Hence please check the according notes in the MB3D repository if needed.
