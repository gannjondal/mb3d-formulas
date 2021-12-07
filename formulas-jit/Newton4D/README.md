# Recent JIT formulas around the implementation of the 4D Newton bulb   
For compatibility to older examples in dA, and ff.org all older formulas are available in this folder:  [/published-samples/gnj/fforg-da-3dnewton/](/published-samples/gnj/fforg-da-3dnewton/)   
   
## Current references:   
- FF org - Revisiting the 3D Newton (original introduction of the principle):   
   https://fractalforums.org/fractal-mathematics-and-new-theories/28/revisiting-the-3d-newton/1026   
- FF org - Terra Newtonia (picture thread that also contains params):   
   https://fractalforums.org/image-threads/25/terra-newtonia/3963   
- dA - Gallery Terra Newtonia (images; some with params):   
   https://www.deviantart.com/gannjondal/gallery/77446093/terra-newtonia   
   
## Formula naming:   
- `JIT` is the mandatory prefix for JIT formulas   
- `gnj` is my 3-digit identifier (for `gannjondal`)   
- `QuatPowNNewt` = (4D) Newton fractal formula using quaternion numbers, and a free power parameter of type floating point   
- `_01, _02 etc` The logic behind fractal formulas makes it not that easy (well, for me) to ensure backward compatibility.   
   I will try to keep an eye to that topic in future, so that there will not be too many of those \_xy variants.   
   Also there is not (and will not be) any formula packages that may have an own versioning.   
   Finally MB3D requires relatively short formula names (something like <24 characters; I don't recall exactly) only, so that it's not possible to have something like subversioning like \_01_01 in the most cases.   
   Hence please consider that you may not be able to use a \_02 variant within params originally written with a \_01 of the same type   
- `E` stands for "easy to use":  It is for z^n-`1`=0 only, and uses `1` as the one-and-only fix solution.   
  There will be versions with a configurable solution parameter (good for pre-transformations only) published later.   
- `C` stands for "correct multiplication of c".   
  In earlier versions of MB3D JIT formulas I did not take the effort to correctly multiply c.   
  As there is no older version for MB2 this is for compatibility across the several fractal programs.   
   
## Documentation:   
The param description has been over from the formula doc of JIT_gnj_QuatPowNNewtE_01.m3f - the variables in other formulas do slightly differ - please check the individual formulas for details, although I may improve the documentation for some older formulas later (well, I hope)...   
   
```   
SUMMARY:   
 3D Newton made from the bulb formula.   
 Normal quaternion algebra   
   
MADE BY:   
 Gannjondal   
   
PARAMETERS:   
   
 Fake_Bailout, Fake_Bailout2:   
   Default = 1   
   ORIGINAL INTENTION:   
   In some hybrids it is necessary to increase the value of 'R Bailout' on the formula window to avoid unwanted cuts.   
   In this case you may set Fake_Bailout to 'R bailout'/4 as a start value.   
   MEANWHILE:   
   It turned out that changing this value can lead to completely different structures. I don't have a simple suggestion - you may use samples that exist especially on ff.org   
   ATTENTION:   
   Changing the value of both params in parallel scales the complete object.   
   You may use the _ScaleC4d transfrom on 4Da tab as a pretransform to scale the object back.   
   Fake_Bailout - used BEFORE the transformation   
   Fake_Bailout2 - used AFTER the transformation   
   
  Fac_Theta:   
    Default = 1   
    With this param you can vary the radial angles of the potence when calculating the power of (x,y,z).   
    Hence it disturbs the power calculation, but in a very smooth way.   
    You even may try to set the param to 0.   
   
  Trans_x/y/z:   
    Parameter to set translation (forth and back)   
   
  Inversion_Factor:   
    -1 -> triplex inversion   
    +1 -> sphere inversion   
    At least this was the thought -    
	However it turned out that they are equivalent for symmetry reasons.   
    However, it's worth to play with values of |Inversion_Factor| != 1   
   
  Rot:   
    Default = 0   
    Transists between sin and cos of theta   
    1 -> sin and cos have switched their place   
   
COMMENTS, EXPLANATIONS:   
  - Meaning of the identifiers in below explanations:   
    + z stands for the variable that is visible to the fractal program, and that is used for bailout check, calculation of the distance estimation etc etc   
    + q stands for the variable that is used for the calculation of the Newton method   
   
  - Explanation of the "trick".   
    It was necessary to keep the following conditions in mind:   
    + The common DE mechanisms of MB2, and MB3D need a DIVERGENT iteration value (here z)   
    + It is of course necessary to have a variable (here q) that is used for the actual Newton iteration   
    + In MB3D (and maybe also in MB2) it is not possible to keep another triplex value than z between the iterations.   
   
    Therefore it is necessary to have a z that diverges AND it must be possible to always calculate q from z uniquely (mathematically: There must be a one-to-one relation between q, and z).   
   
    Below algorithm fullfills all above conditions - Each iteration looks like:   
    a)  Extract q[n] as q[n] = 1/z[n] + solution   
    b)  Run the Newton method calculation which provdes a new q[n+1]   
    c)  Calculate z[n+1] as z[n+1] = 1/(q[n+1]-solution), and hand it over to the fractal program   
   
    To have a classical Newton star one would need to skip the very first inversion.   
    But I decided to keep that first inversion -   
    It transforms the formula to a finite object - so to speak a Newton bulb.   
    And this object is of course much more handleable than the classical infinite star - in fact I see that as a benefit which has been introduced without any cost....   
```
