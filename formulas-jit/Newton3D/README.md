# Recent JIT formulas around the implementation of the 3D Newton bulb   
For compatibility to older examples in dA, and ff.org all older formulas are available in this folder: [/published-samples/gnj/fforg-da-3dnewton/](/published-samples/gnj/fforg-da-3dnewton/)   
   
## Current references:   
- FF org - Revisiting the 3D Newton (original introduction of the principle):   
   https://fractalforums.org/fractal-mathematics-and-new-theories/28/revisiting-the-3d-newton/1026   
- FF org - Terra Newtonia (picture thread that also contains params):   
   https://fractalforums.org/image-threads/25/terra-newtonia/3963   
- dA - Gallery Terra Newtonia (images; some with params):   
   https://www.deviantart.com/gannjondal/gallery/77446093/terra-newtonia   
   
## Formula naming:   
- `JIT` is the mandatory prefix for JIT formulas.   
- `gnj` is my 3-digit identifier (for `gannjondal`). Other developers may introduce their own acronyms.   
- `RealPowNewt` = (3D) Newton fractal formula using triplex numbers, and a free power parameter of type floating point   
- `Pow3Newton` = (3D) Newton fractal formula using triplex numbers for z^`3` ONLY which uses cartesian coordinates.   
   Hence it avoids sin/cos/atan/power etc, and should hence be faster than the RealPow versions.     
   
**One-character identifiers:**   
- `E` stands for _easy to use_:  It is for z^n-`1`=0 only, and uses `1` as the one-and-only fix solution.   
- `P` stands for _pretransform_:  The formula _can_ be used as stand-alone formula.   
   However different values of a solution of the Newton-Raphson method, as well as the `c` in `z^n+c` don't introduce anything new (at least not without much on effort), and makes configuration difficult.   
   Nevertheless the older varaiants that allow these settings are still useful mainly as pretransforms:  The combination of inversion, and power allow to introduce great variations of distortions.     
- `C` stands for _correct multiplication of c_:   
  In earlier versions of MB3D JIT formulas I did not take the effort to correctly multiply c.   
    
**Numbering/Versioning:**     
- `_##`:  The number at the end is just the version:   
  The logic behind fractal formulas makes it not that easy (well, for me) to ensure backward compatibility.   
  Therefore it's most useful to keep old versions somehow, other than usual in software development.   
  Also there is not (and will not be) any formula packages that may have an own versioning.   
  Finally MB3D requires relatively short formula names (something like <24 characters; I don't recall the exact value) only, so that it's not possible to have something like subversioning like \_01_01 in the most cases.   
  Hence please consider that you may not be able to use a \_02 variant within params originally written with a \_01 of the same type.   
  
  I will try to keep an eye to that topic in future, so that there will not be too many of those \_xy variants.   
  If someone should find development rules, and best bractices on how to guarantee backwards compatibility in JIT development I would be happy to take them into account.    
        
## Documentation:   
The param description has been over from the formula doc of gnj_RealPowNewtE_01.m3f - the variables in other formulas do slightly differ - please check the individual formulas for details, although I may improve the documentation for some older formulas later (well, I hope)...   
   
```   
SUMMARY:   
 3D Newton made from the bulb formula.   
 Normal triplex algebra where   
 1/q^n ":=" q^(-n)   
   
MADE BY:   
 Gannjondal   
   
PARAMETERS:   
 Power_:   
   Default = 3   
   The power of the polynom   
    (x,y,z)^power - c = 0   
   to be solved   
   
 Fake_Bailout, Fake_Bailout2:   
   Default = 1 / 1   
   ORIGINAL INTENTION:   
   In some hybrids it is necessary to increase the value of 'R Bailout' on the formula window to avoid unwanted cuts.   
   In this case you may set Fake_Bailout to 'R bailout'/4 as a start value.   
   MEANWHILE:   
   It turned out that changing this value can lead to completely different structures.   
   I don't have a simple suggestion - you may use samples that exist especially on ff.org   
   ATTENTION:   
   Changing the value of both params in parallel scales the complete object.   
   You may use the _Scaling transfrom on 3Da tab as a pretransform to scale the object back.   
   Fake_Bailout - used BEFORE the transformation   
   Fake_Bailout2 - used AFTER the transformation   
   
  Fac_Phi, Fac_Theta:   
    Default = 1 for both   
    With this params you can vary the radial angles of the potence when calculating the power of (x,y,z).   
    Hence it disturbs the power calculation, but in a very smooth way.   
    You even may try to set one of the params to 0.   
   
  Trans_x/y/z:   
    Parameter to set translation (forth and back)   
   
  Inversion_Factor:   
    -1 -> triplex inversion   
    +1 -> sphere inversion   
    At least this was the thought -    
	However it turned out that they are equivalent for symmetry reasons.   
    However, it's worth to play with values of |Inversion_Factor| != 1   
   
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
