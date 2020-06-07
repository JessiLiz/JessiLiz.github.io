# JessiLiz.github.io
Galeria de fractales 
liz
````
import matplotlib.pyplot as plt
from PIL import Image
imgx=600
imgy=600
image=Image.new("RGB",(imgx,imgy))
image.putpixel((100,100),(255,255,255))
xa=-2
xb=2
ya=-2
yb=2
maxit=30
def f(z):
    return z**3+complex(0.2,0.3)

for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            z0=f(z)
            if abs(z)>1000:
                break
            z=z0
            r=i*8
            g=i*8
            b=i*8
            image.putpixel((x,y),(r,g,b))
image
````
![Nombre de la imagenl](https://raw.githubusercontent.com/JessiLiz/JessiLiz.github.io/master/Julia1.png)
