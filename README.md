# Galeria de fractales 
Jessika Lizzeth Santos Lopez 

### Conjunto de Newton:
*Para este fractal la función utilizada es f(z)=z^4-5z^2-1. Sus raices son 
![Nombre de la imagenl](https://raw.githubusercontent.com/JessiLiz/JessiLiz.github.io/master/newton.png)
*Para este fractal la función utilizada es *f(z)=z^4-5z^2-1. Sus raices son
![Nombre de la imagenl](https://github.com/JessiLiz/JessiLiz.github.io/blob/master/Newton2.png)
![Nombre de la imagenl](Newton3.png)
![Nombre de la imagenl](Newton4.png)
## Algoritmo usual:
````
import matplotlib.pyplot as plt
from PIL import Image
imgx=600
imgy=500
image=Image.new("RGB",(imgx,imgy))
xa=-1
xb=1
ya=-1
yb=1
maxit=14
h=1e-6
eps=1e-3
def f(z):
    return z**4-5*z**2-1
for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            dz=(f(z+complex(h,h))-f(z))/complex(h,h)
            z0=z-f(z)/dz
            if abs (z0-z)<eps:
                break
            z=z0
            r=i*12
            g=i*10
            b=i*15
            image.putpixel((x,y),(r,g,b))
image
````
 

