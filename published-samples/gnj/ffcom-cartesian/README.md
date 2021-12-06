# Data used for the ff-org thread `Bulb Mutation Games`   
   
Details see https://www.fractalforums.com/the-3d-mandelbulb/bulb-mutation-games/   
   
## Formulas:   
- JIT_gnj_BulbCartesian_02.m3f   --  Bulb of order \8 in cartesian coordinates   
- JIT_gnj_BulbCartesian_m01.m3f  --  Mutation \1:  Adding fix values to each intermediate helper variable   
- JIT_gnj_BulbCartesian_m02.m3f  --  Mutation \2:  Adding values to each of the summands, and partial powers of the intermediate factor value for x, and y calcuation   
- JIT_gnj_BulbCartesian_m03.m3f  --  Mutation \3:  Varying some *factors* on the partial powers within the summands while calculation of intermediate helper variables, and (some) while the calculation of x/y/z   
- JIT_gnj_BulbCartesian_m04.m3f  --  Mutation \4:  Adding other (wrong) power summands to some of the intermediate helper variables   
- JIT_gnj_BulbCartesian_m05.m3f  --  Mutation \5:  Similar to 3; focus is more to the numeric factors of the summands   
- JIT_gnj_BulbCartesian_m06.m3f  --  Mutation \6:  Follow up to Mutation \5 (because of the limit to \15 parameters per function)   
- JIT_gnj_BulbCartesian_m07a.m3f --  Mutation \7:  A first arbitrary combination of some of the above   
   
   
## slices.jpg:   
   
### NAMES + FORMULAS:   
   
|     Name          |    Formula  (-> Changed parameter, if the change is simple)  |   
|-------------------|--------------------------------------------------------------|   
|\01-cart-005-004f  | JIT_gnj_BulbCartesian_m07a \-\> Var13 = \-\0.2                   |   
|\02-cart-002-007l  | JIT_gnj_BulbCartesian_m02                                    |   
|\03-cart-002-009fg | JIT_gnj_BulbCartesian_m02                                    |   
|\04-cart-003-001j  | JIT_gnj_BulbCartesian_m07a \-\> Var05 = \-\0.275                 |   
|\05-cart-002-026g  | JIT_gnj_BulbCartesian_m02                                    |   
|\06-cart-012-008f  | JIT_gnj_BulbCartesian_m02 (2x) \+ Integer Power (1x)          |   
|\07-cart-008-007jk | JIT_gnj_BulbCartesian_m04                                    |   
   
   
### PARAMETERS:   
   
*Note regarding the performance:*   
 While the calculation of the shape is quite fast, post process steps can be very slow.   
 For instance:   
 For the complete \05-cart-002-026g (4800 x \3600 pt)   
 Calculation ~ \4:30 min (!)   
 Hard shadow ~ \18 min   
 Ambient Shadow (DEAO) ~ \2:30h  (SSAO is MUCH faster)   
 Reflections (enabled in the original) ~ \1:30h   
   
```   
Mandelbulb3Dv18{   
g.....V1...kG...w....2....kRHNsCcSG0.5CoiZubYK2EVLI7Ql4NlvXKgy.6d5SkzyoW9JY3vIwD   
................................5K0YkAjmtz1........A.Naa................y.2...wD   
...Uz6.....s0....2/0/....2k00...Y.....E4.....w8wX3lhOUnD/2/.......US1pAnAr1....6   
/JEnAnYD16../..........wz.................................U0.....y1...sD...../..   
.z1...kD62SBHHK6ix1..........aTTN/zniWdjTYn2N4KnDuXcedyP5ikNzsl3M0h4dBqDydPgdHCs   
GuXphXXoOYqMzKnVvrqV9QqDU....wnUG...mq1.......kD.6....sD..G.....................   
.............oAnAt1...sD....zw1...................................ErG1/E6....k1.   
.....4iSoz1.......kz6ZjsA5UL.64.Y.....8....J....S0u04.8.Uf.F....6/...sY9....SJj1   
Us3U.qFG9yDh7jyzXIGVzbCuW16.q6nzfrBh...Fbf24LNyD66gJ7KDgdz1............29.kFrA0.   
.Ub96aAIVz9.1se7Umvxz0...........IHAzjSro0..H0/bvOonzEluvBTuCfxD/........../2kpz   
aWpB.............0...................EE64pjdMR1..cYaWcuw2z18tigBvzUuz.kJFaHUR/wj   
/EU0.wzzz1...................................I4H7/UvNPcv85mLA32.yRiib1OBXdIF..XR   
SvhyaVKJN/UvNPcvXeaMNl2.ibhViXcPit3H.sSq4uC9mRbIK/UvNPcv6LrLTB3.ibhViLKSZN3H.sSq   
4uyAxxJH5/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....2..F2E.....I....w....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/nBV/..................   
................................................................................   
..........................................................UaNaNaNaNmz0..........   
........................}   
{Titel: cart-005-004f-XL-v191_05}   
```   
   
```   
Mandelbulb3Dv18{   
g.....g2...2C...w....2....U128zdtfA0.jFGRKRbVC2Es45EriF6lv9kc8d0ckqezU0o4EZucHwj   
................................7vJzaUynpz1........A./..................y.2...wD   
...Uz6....U291...I.0/....2U.I...W.....Ej.....UI1u/jcUJnD/I........US1pAnAr1....6   
/JU0LD8D16../..........wz.................................U0.....y1...sD...../..   
.z1...kDNSfKeiAiex1..........C7e31hyXLdjxPTXDAmKBuHUZe65YAxMzcPsxI0se5qDWmuUssMD   
EuH6cuf7UfSMzqOuUf/7HDqDU....w1fY1..AR7.......sD.6....sD..G.....................   
.............oAnAt1...sD....zw1...................................UNaN.E4....k1.   
.....4iSoz1.......kz2xzzz1EN.o3.Y....Q8...kJ....c0.06.2.UK.F....6/...A3.....SJ51   
Us3U.qFG9yDh7jyzXIGVzbCuW16.p6nzfrBh...Fbf24LNyD66gJ7KDgdz1............2FxzFrA0.   
.Ub96aAIVz9.1se7Umvxz0...........IHAzjSro0..dhSA5XWrzs/Fbf24LNyD..........E.2c..   
zzzz.............0...................2./8.kzzzD............8....................   
/EU0.wzzz1...................................2CcN/UvNPcveeWCNq0.yRiibHJJUk1f..XR   
SvBmx3CcN/UvNPcvQsLsUa3.ibhVi1bTV1OK.sSq4uCly3CcN/UvNPcvMwLsUa3.ibhVinqTV1OK.sSq   
4uCkz3CcN/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....2..F2E.....I....s....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/XA....................   
.....................g53iSIsud.EvFVf53iSYxfaNaNaNaNmzcNaNaNaNauj1LD8QxckJz1iSIsu   
FVfXzAQxckpX0LwjvFVf53iSoy1.....................g53iSIsuFz9..........E9mqtvbOwwD   
........................}   
{Titel: cart-002-007l-XL-v191_05}   
```   
   
```   
Mandelbulb3Dv18{   
g....U42..UHA...w....2....UI8bZW0Fw..zpMORxi1D2Enkzd96a2YwXP7ms3oA8xzKslPr8Q.WzD   
........................................kz1........A.JB.................y.2...wD   
...Uz6...........2/0/....2k00...U.....Ei.....6Qi3tRBb0oD/2/.......gK1pAnAt1....1   
/JEnAnYD16../..........wz.................................U0.....y1...sD...../..   
.z1...kDolFZd9iBmx1..........KzJxr2fLrdjgAZeBnNCHuHP4fJZymxOzslPySyorRqDPaV0iHmo   
KuHDcNPuHTrNzayP2AdjQjqDU....wne2.............kD/6....sD..G.....................   
.............oAnAt1...sD....zw1...................................UNaNsD4....k1.   
.....4iSoz1.......kzRxzzz1UO.s3.P....A4...UM....K/tR2c3.kZEF....5/...gX6....SJ52   
Ts4U.qFG9yzb2zzz4klIz9SqK16.p6nzl1Sf..kQhUXI/1yj6ocyFE0ujz1............28.kFrA0.   
.IsffaWeYzX.bjBj1PWwz0...........IXAz5Dsh0..np0CG3AszulQhUXI/1yD/..........//Amz   
W4vq.............0...................2./8.kzzzD............8....................   
/EU0.wzzz1...................................2iVN/UvNPcvee0b3a0.d9ATbHJJiaY5.AyN   
fsBmx7ySM/.Vg0jvQsLRJOA.ibhVi1bTV1OK.sSq4uCly3CcN/UvNPcvMwLsUa3.ibhVinqTV1OK.sSq   
4uCkz3CcN/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....2..F2E.....I....s....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/XA....................   
..........kkpX0LD8Qpz2iSIsuFVv.E..........UaNaNaNaNmzcNaNaNaNaujVf53iSIsOz9vFVf5   
3iSkz...........................................g53iSIsu/z1.....................   
........................}   
{Titel: cart-002-009f-XL-v191_05}   
```   
   
```   
Mandelbulb3Dv18{   
g.....g2...2C...w....2....koUvDa4Em/.rXnfwnsdM2E6Hf5jZWTAwXrRPsp.2feza5VNYA.Y3yD   
................................FLtJ9/icmz1........A./..................y.2...wD   
...Uz6....EwU0...I.0/....2kv1...T.....Ej.....cgfvTUE3YnD/I........US1pAnAr1....6   
/JEnAnQD12../2EpcNEr27ntzsvfCtBY3gyDkGdG/84klz1...........U0.....y1...sD...../..   
.z1...kD8PjK58dFjx1..........isrVvyySadj25ACcV1SBuXPGXqD0MNOzkR6Pm4cw5qD1iX7aFQx   
IuXRZpVPUmTMz4VL1pX.KaqDU.....I73/..dx1.......sD.6....sD..G.....................   
.............oAnAt1...sD....zw1....................................AAtwD4....k1.   
.....4iSoz1.......kz2xzzz1EK.I4.W....A8...kJ....H1.S6.1.UK.F....6/...EJ7....SJL0   
Us3U.qFG9yDh7jyzXIGVz9zvg16.r6nzfrBh..kuvBTuCfxD66HNL1YPWz1............2FxzFrA0.   
.Ub96aAIVz9.1se7Umvxz0...........IHAzjSro0..np0CG3Aszs/alwF.HWwj.........../2QXz   
TSYD..U3tBPI4Bjj.uqbwLs6Dz1.gFYiKRslzGEAcsTbP/2..gmirhqTQy98sB/TvUcsz..Wtonw0kyj   
2.mMxrtK./..xafV.LMYz0ELcH5Pvduj.6hPPa8Fiz9..I4H7/UvNPcv85mLA32.yRiib1OBXdIF..XR   
SvhyaVKJN/UvNPcvXeaMNl2.ibhViXcPit3H.sSq4uC9mRbIK/UvNPcv6LrLTB3.ibhViLKSZN3H.sSq   
4uyAxxJH5/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....2..F2E.....I....w....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/nBV/..................   
.....................................................cNaNaNaN4xj................   
................................................................................   
........................}   
{Titel: cart-003-001j-XL-v191_05}   
```   
   
```   
Mandelbulb3Dv18{   
g.....g2...2C...w....2....EVdUlfH1G/.5A3AAdF732EyLucEzEVaun/P7yMBcylzyj5amQPxhrD   
................................KVyIcpo9sz1........A.RVr................y.2...wD   
...Uz6....UnK3...I.0/....2UQ....e.....Ej.....s71TChj5BnD/I........US1xckpn1....U   
.JEnAnYD16../..........wz................................AU0.....y1...sD...../..   
.z1...kDw6E.GvvFHx1..........a7n/jOiKybj17yNUlWZptH994nwpP0HzwgXpcGoNdoDDyMzp2z1   
rt16kh49FbZGz0iyI1TxakoDU....w1L8...1j0...kAnAfD.6....sD..G.....................   
.............oAnAt1...sD....zw1...................................EX9gvD7....k1.   
.....4iSoz1.......kz6ZjsA5UL.64.Y.....8....J....S0u04.8.Uf.F....6/...AJ1....SJj1   
Us3U.qFG9yDh7jyzXIGVzbCuW16.q6nzfrBh...Fbf24LNyD66gJ7KDgdz1............29.kFrA0.   
.Ub96aAIVz9.1se7Umvxz0...........IHAzjSro0..H0/bvOonzEluvBTuCfxD/........../2kpz   
aWpB.............0...................EE64pjdMR1..cYaWcuw2z18tigBvzUuz.kJFaHUR/wj   
/EU0.wzzz1...................................I4H7/UvNPcv85mLA32.yRiib1OBXdIF..XR   
SvhyaVKJN/UvNPcvXeaMNl2.ibhViXcPit3H.sSq4uC9mRbIK/UvNPcv6LrLTB3.ibhViLKSZN3H.sSq   
4uyAxxJH5/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....2..F2E.....I....s....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/XA....................   
..........UaNaNaNaNmz........U.E........2.I42MZ1h6Pbz...........................   
................................................................................   
........................}   
{Titel: cart-002-026g-XL-v191_05}   
```   
   
```   
Mandelbulb3Dv18{   
g.....g2...2C...w....2....UCSzgseCq0.jZGaHDYnS1EJeRfJrocuvfL1bn7lBYgzwGa01290/xj   
................................sUNGnCyAoz1........A./..................//2...wD   
...Uz6....kHR0...I.0/....2k/2...Q.....Ej.....g7Du3CbIQnD/I........US1pAnAt1....6   
/JEnAnQD16../..........wz.................................U0.....y1...sD...../..   
.z1...kDYiHPLEQqgx1..........udDoIqOWSdjjKMxzYlQEuXo8qIr5R9NzQqin33UIEqDnRgCH85y   
Eunom9mI.G/NziveEixFrGqDU....wHYQ...Rp0.......sD.6....sD..G.....................   
.............oAnAt1...sD....zw1...................................k53i.E5....k1.   
.....4iSoz1.......kz2xzzz1UL.w3.Y....A9...kJ.....1.06.1.UK.F....6/...A3.....SJD1   
Us3U.qFG9yDh7jyzXIGVzbCuW16.p6nzfrBh...Fbf24LNyD66gJ7KDgdz1............2FxzFrA0.   
.Ub96aAIVz9.1se7Umvxz0...........IHAzjSro0..dhSA5XWrzs/Fbf24LNyD.........../2omz   
TSYD.............0...................2./8.kzzzD............8....................   
/EU0.wzzz1...................................I4H7/UvNPcv85mLA32.yRiib1OBXdIF..XR   
SvhyaVKJN/UvNPcvXeaMNl2.ibhViXcPit3H.sSq4uC9mRbIK/UvNPcv6LrLTB3.ibhViLKSZN3H.sSq   
4uyAxxJH5/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....6E2F2U.....I....s....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/XA....................   
.....................EVf53iSIE.EwbOwGrYMkyvoB742MZ1lzcNaNaNaNauj1LD8QxckJz1iSIsu   
FVfXzwGrYMEUJixjvFVf53iSoy1yHBSdPGAmzePGA6k85OuDg53iSIsuFzfFZIb.OWkezISMVOBBjXuD   
.....................2..........0....YYPoJqNZ756ExqRZ75.........................   
8.............................0E........kz9.....................................   
................................................................................   
................................}   
{Titel: cart-012-008f-XL-v191_05}   
```   
   
```   
Mandelbulb3Dv18{   
g.....g2...2C...w....2.....EDqOef/80.57hgE4QM12ECNOHVoM5ovn7KKedBOdpz0cj5Lg2CWwD   
................................IkLqA6CZnz1........A./..................y.2...wD   
...Uz6...........2/0/....2U5D...V.....Ef.....61Kpf.0ETnD/.........US1xckpp1....6   
/JEnAnAD16../..........wz.................................U0.....y1...sD...../..   
.z1...kDoe5i4M.rVx1..........yzcdgOn0pcjuUfHyhNL2u1Z3nnIALOKzsL99t2FQXpDYUfCfCf.   
3uH2B24I2lBKzOWzJ23nZapDUoAnAt1M..............sD.6....sD..G.....................   
.............oAnAt1...sD....zw1....................................yq2xD4....k1.   
.....4iSoz1.......kz6ZjsA5UL.64.Y....k7....J....S0u04A8.Uf.F....6/...AZ6....SJj1   
Us3U.qFG9yDh7jyzXIGVzbCuW16.o6nzfrBh...wQOr9PExD6AL9s6JkUz1............2CxzFrA0.   
.Ub96aAIVz9.1se7Umvxz0...........Qn7zjSro0..zMwlGfEnzEFbG7eFT5wD/........../22oz   
aWpB.............0...................EE6CtjdMR1..QFP5bvj3z18Ld91jt0tz.k4D3Gacsuj   
0EE4zzzzzbb.D0........kQ.........U7..........I4H7/UvNPcv85mLA32.yRiib1OBXdIF..XR   
SvhyaVKJN/UvNPcvXeaMNl2.ibhViXcPit3H.sSq4uC9mRbIK/UvNPcv6LrLTB3.ibhViLKSZN3H.sSq   
4uyAxxJH5/UvNPcv..EsUa3feeWCNqGQIJ36wk8EwyLsUa3f................................   
E....2..F2E.....I....g....UG7FpLbtaOT7IRg7qEV75RZBLOVtqLh/1B....................   
.....................Uf53iSIsutD..........UaNaNaNaNqzeNaNaNaNawjdkpX0LD8wy1.....   
................Vf53iSIsOzfNaNaNaNalz...........................................   
........................}   
{Titel: cart-008-007j-XL-v191_05}   
```