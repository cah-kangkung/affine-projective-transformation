# Affine Transformation

Name : Hafizhun Alim
NRM  : 1313617032

## Objectives
In this task we were asked to do affine transformation. Affine transfomation could do the following transformation simultaneously.
* Scalling
* Rotation
* Shearing
* Translation
And then we were asked to do projective transfomation which is just an affine transfomation comhine with projective/perspective warp.

## 2D Linear Transformation
Before we understand affine transformation, first we will take a look at 2D Linear transformation. A 2D point in cartesian coordinate can be denoted by a pair of value p = (x, y) or alternatively:
          
          p = [x] 
              [y]

A linear transfomation can be expressed as a Matrix M times the vector (x, y). Assuming that p' is our new vector coordinate and M is a matrix that represent all of the transformation parameters.

          p' = M(p)  or basically   p' = [a, b] @ [x]
                                         [c, d]   [y]
                               
