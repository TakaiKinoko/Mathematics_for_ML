#### Rational exponent rule
* Q: Given y = x <sup>m/n</sup> where m and n are integers, compute dy/dx.
* Sol: dy/dx = (m/n)x<sup>(m/n-1)</sup>

#### derivative to non-functions

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
    * leave the equation as is and differentiate both sides:
    4y<sup>3</sup>y' + x(2yy') - 0 = 0
    * factor out y'
        (4y<sup>3</sup> + 2xy)y' = -y<sup>2</sup>
    * so the solution (**slope**) is 
        y' = - y<sup>2</sup> / (4y<sup>3</sup> + 2xy)