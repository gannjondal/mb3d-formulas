# Formulas, and samples created for the two available formula packages on dA - Pack 2   
   
Details see https://www.deviantart.com/gannjondal/art/JIT-Formula-Pack-and-Samples-2-of-2-594738839   
   
## Formula list:   
- **JIT_AmazingSquare_02.m3f**   
  JIT variant of the known Amazing Box / Tglad folding for lerning purposes.   
  The only tiny difference is that all single parameters gets squared before the folding.   
   
- **JIT_gnj_TwoRealPower_02.m3f**   
  Simply a sum of two (potentially different) powes of triplex numbers.   
    
- **\_JIT_gnj_Exp_02.m3f**   
  A exponential of a triplex number   
  Not easy to use, but it can show (locally) some nice forms, and distortions   
  See http://www.fractalforums.com/theory/triplex-algebra/60/ for details   
      
- **\_JIT_gnj_LoziExt1_02.m3f**   
  A mathematically useless 3D 'extension' of the 2D Lozi attrcator.   
  Quite fast - for all those who love acute angles ;-)   
       
- **JIT_gnj_VolterraLotka_02.m3f**   
  Another old strange Attractor called Volterra Lotka.    
  Just try it out; probably best with non-triplex formulas   
      
- **\_JIT_gnj_RiemSimple_01.m3f / \_JIT_gnj_RiemPowRadial_01.m3f / \_JIT_gnj_RiemPow2_03.m3f / \_JIT_gnj_RiemPow2_04.m3f / JIT_gnj_RiemPow2_05.m3f**   
   My as of now most elaborated formulas. I think I don't promise too much if I say that you can (with some exercise)   a new world of shapes.   
   The explanation would be too long for here. Please have a look to the info section of the formula.   
      
**Just a few hints:**   
   + I would recommend to start with a combination of \_JIT_gnj_RiemSimple_01 in position 1 and IntegerPower in position 2 - and change the values starting with Complex_...   
     The most simple start would be to change Complex_MultAll_x. With increasing (positive) values > 1 you shift all details of the bulb more and more to the north pole of the bulb, and with values down to 0 you shift them to the south pole....   
   + Generally best to be used in combination with formulas of the bulb type (like Integer Power).    
   + NumComplexOps (if available) must be 1, 2, or 3 (integers). The higher the values the more details.   
   + SquaredRBackward must be 0, or 1. Switching on (value = 1) reduces the number of details dramatically.    
   + Be careful with AddCAtEnd - small changes can change the picture dramatically   
   + The formulas \_JIT_gnj_RiemSimple_01 and ...RiemPow2... are faster than \_JIT_gnj_RiemPowRadial_01 because they avoid any trigonometric functions.   
   + Ah, and for all who like maths:  The formulas are interpreting sphere coordinates as a Riemann sphere, map them to the complex plane using spherical projection, make some operations there, and go the way back.
