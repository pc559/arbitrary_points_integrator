Code to generate integration weights for given sample points, using a second-order Legendre polynomial expansion for each segment [x<sub>i-1</sub>, x<sub>i+1</sub>].
If the number of points is even, the final segment [x<sub>N-1</sub>, x<sub>N</sub>] is dealt with using a first-order expansion.
Once the weights have been calculated for a given set of points, the integral of any sufficiently smooth function (f) over those points (xs) is simply:

integral = np.dot(weights, f(xs))

giving a cheap way of integrating many functions over the same fixed set of sample points.

Also includes code to generate integration weights using the same method for functions integrated against an oscillatory weight function, giving a cheap way of integrating many functions over the same fixed set of sample points, against the same e<sup>iwx</sup> weight function.
