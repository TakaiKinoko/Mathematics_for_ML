#### Rational exponent rule
* Q: Given y = x <sup>m/n</sup> where m and n are integers, compute dy/dx.
* Sol: dy/dx = (m/n)x<sup>(m/n-1)</sup>

#### derivative to non-functions (slope of tangent to circle)

x<sup>2</sup> + y<sup>2</sup> = 1

* step 1: use the operator d/dx on both sides
    d/dx (x<sup>2</sup> + y<sup>2</sup>) = d/dx 1
* step 2: simplify and use sum rule
    d/dx x<sup>2</sup> + d/dx y<sup>2</sup> = 0
* step 3: use basic rule on x<sup>2</sup> and chain rule on y<sup>2</sup>
    2x + 2y dy/dx = 0
* step 4: simplify
    dy/dx = - x/y

#### explicit v.s. implicit 
y<sup>4</sup> + xy<sup>2</sup> - 2 = 0

* explicit: 
    * treat the equation as a function on y<sup>2</sup>
    * solve y<sup>2</sup> inside the quadratic equation
    * take square root of both side will get y
* implicit: 
    * y is an implicit expression of x, thus we can use the chain rule.
    * leave the equation as is and differentiate both sides:
    4y<sup>3</sup>y' + x(2yy') - 0 = 0
    * factor out y'
        (4y<sup>3</sup> + 2xy)y' = -y<sup>2</sup>
    * so the solution (**slope**) is 
        y' = - y<sup>2</sup> / (4y<sup>3</sup> + 2xy)
    * this is not a complete solution though, it doesn't tell what y is in terms of x. 
        * when x = 1 it's easy to see that y = 1, we can plug both into the implicit formula for y'.
        * but when x = 2, there's no easy way to see what the solution of y is thus we're stuck with the explict formula to find y. 
    
#### another implicit example
What's the slope of the tangent line to the curve y<sup>3</sup> + x<sup>3</sup> = 3xy at the point (4/3, 2/3)? 
* it's hard to find y in terms of x
* (d/dx) (y<sup>3</sup> + x<sup>3</sup>) = d/dx 3xy
* 3y<sup>2</sup> * dy/dx + 3 x<sup>2</sup> = 3y + 3x(dy/dx)
* this is a linear equation in a sense, relatively easy to solve
* dy/dx(3y<sup>2</sup> - 3x) = 3y - 3x<sup>2</sup>
* dy/dx = (y-x<sup>2</sup>)/ (y<sup>2</sup> - x)
* now because we already have a point (4/3, 2/3), just plug it into the equation above.

## use of implicit differentiation
e.g. finding the derivative of inverse functions
* given y = f(x), g(x) = x, then g(f(x)) = x, g=f<sup>-1<sup>, f=g<sup>-1<sup>
* plot f and f<sup>-1</sup> on the same graph: reflect f across y = x

#### implicit differentiation allows us to find the derivative of any inverse function provided we know the derivative of the function
* ex: y = tan<sup>-1</sup>x [this is just arctan x]


#### natual log properties
* ln(x<sub>1</sub>x<sub>2</sub>) = lnx<sub>1</sub> + lnx<sub>2</sub>

* ln 1 = 0
* ln e = 1

#### derivatives of logarithms
use implicit differentiation (to find the derivatives of ANY **inverse functions**)

* w = ln x ==> e<sup>w</sup> = x 
* ==> d/dx e<sup>w</sup> = d/dx x = 1
* ==> (d/dw e<sup>w</sup>)(dw/dx) = 1
* ==> e<sup>w</sup> dw/dx = 1
* ==> dw/dx = 1/e<sup>w</sup> = 1/x 

#### derivatives of a^x
d/dx a<sup>x</sup> = M(a)a<sup>x</sup>

* to differentiate any exponential: two methods
    1.  d/dx a<sup>x</sup> = ?
        * use base e 
        * => a<sup>x</sup> = (e<sup>x ln a</sup>)
        * => (ln a)e<sup>x ln a</sup> (chain rule, see ln a as a constant)
        * => (ln a)a<sup>x</sup>
        So the magic number **M(a)** is ln a
    1. use logarithmic differentiation
        sometimes when dealing with d/dx u= ?, it's easier to compute d/dx ln u.
        * e.g. 
            * d/dx a<sup>x</sup> = ?
            * u = a<sup>x</sup>
            * ln u = x ln a
            * (ln u)' = ln a 
            * u' = u ln a
            * d/dx a<sup>x</sup> = (ln a) a<sup>x</sup>
