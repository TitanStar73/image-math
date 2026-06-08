# Image Math

What if you could do math on an image?

I was inspired by [3Blue1Brown's video](https://www.youtube.com/watch?v=ldxFjLJ3rVY) where he took the logarithm of a [Droste](https://en.wikipedia.org/wiki/Droste_effect) art piece to convert it into an [Escher-style](https://en.wikipedia.org/wiki/Print_Gallery_(M._C._Escher)) artwork. 

Every point on an image is corresponded with a complex number in the complex plane. Applying a function on every point on an initial image gives a new complex number, cooresponding to its position in the new image.

I was able to recreate [Escher's effect](https://en.wikipedia.org/wiki/Print_Gallery_%28M._C._Escher%29) and more!

---

Jump forward to:
1.   [Applying your own function](#applying-your-own-functions)
2.  [Creating your own Escher-style images](#creating-an-escher-style-image)

## Some cool effects I got:
| Inv-Function | 3B1B's image | My Droste Image | Rings
| :---: | :---: | :---: | :---:
| **Original**<br>Click any image<br>for higher quality | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/raw/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/raw/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/raw/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/raw/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/raw/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/raw/droste_test2.png" height="121" width="121" /></a>
| Escher Effect | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/escher/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/escher/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/escher/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/escher/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/escher/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/escher/droste_test2.png" height="121" width="121" /></a>
| Rotate<br>$f(z)=iz$ | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/rotate/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/rotate/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/rotate/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/rotate/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/rotate/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/rotate/droste_test2.png" height="121" width="121" /></a>
| Zoom to corner<br>$f(z)=\frac{z+2+2i}{3}$ | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/zoom_into_corner/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/zoom_into_corner/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/zoom_into_corner/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/zoom_into_corner/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/zoom_into_corner/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/zoom_into_corner/droste_test2.png" height="121" width="121" /></a>
| Kaleidoscope<br>$f(z)=z^6$ | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/kaleidoscope/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/kaleidoscope/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/kaleidoscope/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/kaleidoscope/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/kaleidoscope/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/kaleidoscope/droste_test2.png" height="121" width="121" /></a>
| Kaleidoscope <br> (Try any polynomial :D)<br>$f(z) = z^3 + 3z^2$ | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/assymetrical_kaleidoscope/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/assymetrical_kaleidoscope/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/assymetrical_kaleidoscope/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/assymetrical_kaleidoscope/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/assymetrical_kaleidoscope/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/assymetrical_kaleidoscope/droste_test2.png" height="121" width="121" /></a>
| Logarithm <br> $f(z) = e^z$ | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/logarithm/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/logarithm/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/logarithm/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/logarithm/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/logarithm/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/logarithm/droste_test2.png" height="121" width="121" /></a>
| Inverse <br> $f(z) = 1/z$ | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/inverse/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/inverse/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/inverse/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/inverse/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/inverse/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/inverse/droste_test2.png" height="121" width="121" /></a>
| [Weierstrass Elliptical function](https://en.wikipedia.org/wiki/Weierstrass_elliptic_function) | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/weierstrass/3b1b.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/weierstrass/3b1b.png" height="121" width="121"/></a> | <a href="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/weierstrass/droste_test.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/weierstrass/droste_test.png" height="121" width="121" /></a> | <a href ="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/weierstrass/droste_test2.png" target="_blank" rel="noopener noreferrer"><img src="https://raw.githubusercontent.com/TitanStar73/image-math/refs/heads/main/assets/weierstrass/droste_test2.png" height="121" width="121" /></a>



## Applying your own functions:
1. Create the [inverse of your function](https://en.wikipedia.org/wiki/Inverse_function). e.g. if $f(x) = e^x$, the inverse function is $g(x) = log(x)$
2. Create the function in using [numpy](https://github.com/numpy/numpy).
    ```python
    def f(z):
        return np.log(x) # i.e. log(x)
    ```
3. Add the ```@image_function``` decorator.
    ```python
    @image_function
    def my_image_function(z):
        return np.log(x)
    ```
4. Done! Use your function like this:
    ```python
    my_image_function("input.png", "output.png", zoom = 1.0, output_scale = 1.0)
    ```
    -   ```zoom```: Change this to zoom-in/out the output.
    -   ```output_scale```: Output resolution w.r.t input image. Smaller number makes rendering much faster, but loses quality.


## Creating an Escher-style Image:
1. Start with a [Droste](https://en.wikipedia.org/wiki/Droste_effect) image.
2. Find the *singularity* of the image, (where all the recursive images meet), generally the center of the image. Find the position w.r.t the center of the image [(0,0) = center; (1,1) = top right corner]
3. Create the escher function:
    ```python 
    scale = 16 #Size of smaller image wrt the larger one.
    center = (0,0) #Center point, (0,0) by default
    subject = (-0.8,-0.8) #Subject of drawing, cannot be center
    esch = escher_function(scale, center,subject)```
4. Create the final image:
    ```python
    input_filename = "droste.png" # Input filename
    output_filename = "escher.png" # Output
    zoom = 1.8 # Used to zoom-in/out the output image.
    res = 1.0 # Set to a low number (e.g. 0.2) for faster rendering and testing, but lower output quality. 1.0 is the maximum quality.

    esch(input_filename, output_filename, zoom, res)

    ```
