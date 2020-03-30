# Affine Transformation

Name : Hafizhun Alim
NRM  : 1313617032

## Objectives
In this task we were asked to do affine transformation. Affine transfomation could do the following transformation simultaneously.
* Scalling
* Rotation
* Shearing
* Translation
And then we were asked to do projective transfomation which is just an affine transfomation combine with projective/perspective warp.

## 2D Linear Transformation
Before we understand affine transformation, first we will take a look at 2D Linear transformation. A 2D point in cartesian coordinate can be denoted by a pair of value p = (x, y) or alternatively:

asdasdasdasdasdasdasdasds
       p = [x] 
           [y]

How can we do transformation? Well the simple equation would be p' = T(p). Since linear transfomation can be expressed as a Matrix, now our equation would be Matrix M times the vector (x, y). Assuming that p' is our new vector coordinate and M is a matrix that represent all of the transformation parameters.

       p' = M(p)  or basically   [x'] = [a, b] @ [x]
                                 [y']   [c, d]   [y]
                               
#### Scalling
We do scalling by simply multyply our x and y by a scallar.

       x' = x * sx   or   [x'] = [sx, b] @ [x]
       y' = y * sy        [y']   [c, sy]   [y]
       
#### Rotation
For rotation there would be an angel asociate with it called, theta.

       x' = x cos(θ) - y sin(θ)   or   [x'] = [cos(θ), -sin(θ)] @ [x]
       y' = x sin(θ) + y cos(θ)        [y']   [sin(θ),  cos(θ)]   [y]
       
#### Shearing
The matrix reprsentaion for shearing would be.

       [x'] = [1, hs] @ [x]
       [y']   [vs, 1]   [y]
       
#### Translation
Lets look at translation. A translation done to a point would be as simple as
        
       x' = x + tx  or  ?
       y' = y + ty
       
Notice that it can no longer be expressed by matrix M times the vector, thus translation is not a linear transformation because
       
       [x'] = [a, b] @ [x]   this would translate to   x' = ax + by
       [y']   [c, d]   [y]                             y' = cx + dy
       
It is almost imposible in this linear transformation that we can generate equation that matches with our translation equation. So how do we solve this?

#### Homogeneous Coordinates
The answer is homogeneous coordinates. Homogeneous coordinates in 2D space is basically a way to represent 2D coordinates with 3 vector. To write homogeneous coordinates we simply add the third coordinate in our vector called w. Hence our new coordinate will look like this

            [x]
        p = [y]    =>   p = [x/w]
            [w]             [y/w]

We could fill variable w with anything but it is usually 1 or 0 where homogeneouse points whose w = 0 are called points of infinity. 
So now that we have our new coordinate system, lets see what we will get from this.


* Translation 

        [x'] = [1, 0, tx] @ [x]        x' = x + tx 
        [y'] = [0, 1, ty]   [y]   =>   y' = y + ty
        [w'] = [0, 0,  1]   [1]        w' = 1
       
It matches our equation! hooray!
Now for the rest of our transformation

* Scalling

[x'] = [1, 0, tx] @ [x]
[y'] = [0, 1, ty]   [y]
[w'] = [0, 0,  1]   [1]

* Rotation

[x'] = [x cos(θ), -y sin(θ), 0] @ [x]
[y'] = [x sin(θ), y cos(θ),  0]   [y]
[w'] = [0,        0,         1]   [1]
       

       
       
       
       
       
       
       
       
       
       
