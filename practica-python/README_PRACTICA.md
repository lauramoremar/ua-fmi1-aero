# Práctica con Python 25-26: Cálculo de varias variables

El objetivo de la práctica es que aprendáis a utilizar python para representar funciones o hacer cálculos en varias variables.

Para eso utilizaremos Google Colab, una herramienta flexible, tipo "notebook", para que podamos analizar y ver paso a paso lo que vamos implementando. Trabajaremos online, por lo que no hace falta instalar nada en vuestros ordenadores.

Para una introducción rápida en el entorno de Google Colabs os recomiendo que miréis el siguiente vídeo.

| Vídeo                             | Notebook              |
| :-------------------------------- | :-------------------: |
| [Introducción a Google Colab](https://drive.google.com/file/d/1wLqaivUCHKDoiBYiL6xWvGG_cZqqb-Di/view?usp=sharing)| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/notebooks/00-que-es-colab.ipynb) |

La práctica consta de 4 partes: Representación de funciones, límites, continuidad y diferenciabilidad, derivación e integración.

## 1. Representación de funciones


### Tutorial

En el siguiente vídeo se explica como representar funciones de dos variables utilizando distintos comandos de python, de forma que podáis representar cualquier superficie que necesitéis.

| Vídeo                             | Notebook              
| :-------------------------------- | :-------------------: |
| [Representación de funciones de 2 variables](https://drive.google.com/file/d/1wLqaivUCHKDoiBYiL6xWvGG_cZqqb-Di/view?usp=drive_link) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/notebooks/01-intro-representacion-funciones.ipynb) |



### Ejercicio 1
A continuación, realiza el siguiente ejercicio usando la siguiente plantilla. Acuérdate de guardarlo en tu google drive, porque en caso contrario, los cambios no se guardan. Cuando lo termines, descarga el archivo ejercicio1.ipynb en tu ordenador para luego adjuntarlo a tu práctica.

| Ejercicio                         | Notebook              |
| :-------------------------------- | :-------------------: |
| Ejercicio 1 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/ejercicios/ejercicio1.ipynb)  |


#### a) Tomando como guı́a el vı́deo anterior, representa en Python la siguiente función:

$$
f(x, y) = \frac{1}{2} \cdot e^{-\frac{x^2 + y^2}{2}}
$$

Realiza la representación en forma de rejilla (wireframe), etiquetando los ejes x, y y z. 
Los vectores x e y deberán ser equiespaciados, de 32 elementos, cuyos valores irán desde -4 hasta 4. 
Establece un grosor de lı́nea de 1.0 y asigna el color royalblue para la representación.

#### b) Representa la siguiente función:

$$
f(x, y) = 0.5 + \frac{\cos^2\left(\sin\left(|x^2 - y^2|\right)\right)}{(1 + 0.001(x^2 + y^2))^2}
$$

Realiza la representación en forma sólida (surface), etiquetando los ejes x, y y z. Los vectores x e y tendrán 64 elementos equiespaciados, ambos con valores desde -π/4 hasta π/4. Asigna a la representación el mapa de color plasma.


#### c) Representación de un hiperboloide de 1 hoja

Representa un hiperboloide de 1 hoja con ecuaciones paramétricas:

$$
\begin{cases}
x = a\sqrt{1 + u^2} \cdot \cos(v) \\
y = b\sqrt{1 + u^2} \cdot \sin(v) \\
z = c \cdot u
\end{cases}
$$

con $0 \leq v \leq 2\pi$, $u \in \mathbb{R}$.

- $a = b = c = 1$
- $u$: vector equiespaciado de 50 elementos, desde $-5$ hasta $5$
- $v$: vector equiespaciado de 25 elementos, desde $0$ hasta $2\pi$

- La representación será en forma de rejilla, con un grosor de lı́nea de
0.75. 
- Elige un color de tu preferencia, a partir de la siguiente lista:

https://matplotlib.org/stable/gallery/color/named_colors.html

- **Para evitar deformación,** ejecutar antes de `plot.wireframe()`:
  ```python
  nombreEjes3D.set_box_aspect([1, 1, 1])
  ```


#### d) Función definida a trozos

En una figura aparte, representa la siguiente función:

$$
f(x, y) =
\begin{cases}
\dfrac{2xy}{x^2 + y^2} & \text{si } x^2 + y^2 \neq 0 \\
0 & \text{si } x^2 + y^2 = 0
\end{cases}
$$

Evita que la representación salga deformada, ejecutando la siguiente lı́nea de código antes del plot wireframe(): nombreEjes3D.set box aspect([1,1,1])


## 2. Límites, continuidad y diferenciabilidad

### **Ejercicio 2:**

Este archivo solo debe incluir las respuestas escritas a los siguientes apartados mediante comentarios:

| Ejercicio                         | Notebook             |
| :-------------------------------- | :-------------------: |
| Ejercicio 2 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/ejercicios/ejercicio2.ipynb)  |


#### a) Análisis de continuidad y diferenciabilidad

Observa la gráfica que has obtenido en el **Ejercicio 1 a.**. Mirando solamente la gráfica:

1- ¿Podrías decir si la función $f(x, y)$ es continua en el punto $(0, 0)$?

2- ¿Y diferenciable en $(0, 0)$?

3- Observa ahora la expresión de esta función: 
$$
f(x, y) = \frac{1}{2} \cdot e^{-\frac{x^2 + y^2}{2}}
$$  

¿Es continua en todo $\mathbb{R}^2$?

Justifica todas las respuestas.


#### b) Cálculo del límite gráficamente

Estudiando solo la gráfica del **Ejercicio 1 a.** y sin realizar ningún cálculo:

1-  ¿Sabrías decir cuánto vale?  
   $$\lim_{(x,y)\rightarrow(0,0)} f(x, y)$$

2- ¿Por qué?



#### c) Verificación del límite

Verifica que tu respuesta es correcta calculando el límite doble:

- Opción 1: Wolfram Alpha
Introduce la siguiente línea en [Wolfram Alpha](https://www.wolframalpha.com/):
```
limit of (1/2)*e^(-(x^2+y^2)/2) as (x,y)->(0,0)
```

- Opción 2: Python

```python
import sympy as sp

# Definir variables
x, y = sp.symbols('x y')
f = (1/2) * sp.exp(-(x**2 + y**2)/2)

# Calcular el límite
limite = sp.limit(f, (x, y), (0, 0))
print(f"El límite cuando (x,y)->(0,0) es: {limite}")
```


#### d) Análisis de la función del Ejercicio 1 b.

Estudiando la gráfica del **Ejercicio 1 b.** y sin realizar ningún cálculo, responde a las siguientes preguntas (justificando las respuestas):

Sea 

$$f(x, y) = 0.5 + \frac{\cos^2\left(\sin\left(|x^2 - y^2|\right)\right)}{(1 + 0.001(x^2 + y^2))^2}$$

1. ¿Cuánto vale $f(0, 0)$?
2. ¿Qué valor tiene $\lim\limits_{(x,y)\rightarrow(0,0)} f(x, y)$?
3. ¿Es $f(x, y)$ es continua en el punto $(0, 0)$?




**Notas importantes:**
- Este archivo debe contener **solo comentarios** con las respuestas, no código ejecutable.
- Las respuestas deben basarse en la observación de las gráficas generadas en el Ejercicio 1.
- Para cálculos numéricos o simbólicos, puedes usar SymPy (como se muestra arriba) o verificar en Wolfram Alpha.


## 3. Derivación
### Tutorial

En el siguiente vídeo veréis los comandos básicos que permiten calcular derivadas parciales y el gradiente de una función de varias variables.

| Video                             | Notebook              |
| :-------------------------------- | :-------------------: |
| Derivación dos variables | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/notebooks/02-calculo-derivadas-parciales-gradiente.ipynb) |

### **Ejercicio 3**

Utiliza la plantilla del Notebook de Google Colab para escribir el código que permita resolver los siguientes apartados:


| Ejercicio                         | Notebook              |
| :-------------------------------- | :-------------------: |
| Ejercicio 3 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/ejercicios/ejercicio3.ipynb)  |


#### a) Cálculo de derivadas parciales

Calcula en Python las derivadas parciales:

$$\frac{\partial f}{\partial x}, \quad \frac{\partial f}{\partial y}, \quad \frac{\partial^{2}f}{\partial x^{2}}, \quad \frac{\partial^{2}f}{\partial y^{2}}, \quad \frac{\partial^{2}f}{\partial x\partial y}, \quad \frac{\partial^{3}f}{\partial x^{3}}$$

donde:

$$f(x,y)=\arctan(x+y)+\arccos(x)$$

**Nota:**  
- $\arctan(x)$ equivale a: `sym.atan(x)`  
- $\arccos(x)$ equivale a: `sym.acos(x)`

Imprime los resultados de estos cálculos por consola.


#### b) Cálculo del gradiente

Siendo:

$$f(x,y)=\sqrt[5]{x^{2}+y^{2}}+\ln(x+1)\cdot\ln(y+1)$$

calcula e imprime por consola el gradiente de la función en el punto $(0,1)$.

**Nota:**  
- $\sqrt[5]{x}$ equivale a: `sym.root(x,n)`  
- $\ln(x)$ equivale a: `sym.log(x)`



## 4. Integración
### **Tutorial**

En el siguiente vídeo se explica cómo calcular integrales triples usando comandos de python de la librería sympy,

|  Vídeo                            | Notebook              |
| :-------------------------------- | :-------------------: |
| Cálculo integrales múltiples| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/notebooks/03-calculo-integrales-multiples.ipynb) |

### **Ejercicio 4**

A continuación, realiza los apartados del ejercicio 4 siguiendo la siguiente plantilla de Google Colab. recuerda siempre hacer una copia en tu google drive y, una vez hecho, descargarlo en tu ordenador para entregarlo.


| Ejercicio                         | Notebook             |
| :-------------------------------- | :-------------------: |
| Ejercicio 4 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/practica-python/25-26/ejercicios/ejercicio4.ipynb)  |


#### a) Integrales dobles

Calcula e imprime por consola las siguientes integrales dobles, respetando los órdenes de integración:

1. $$\int_{0}^{2}\int_{y-2}^{\sqrt{36-9y^{2}}}2x^{2}y\,dx\,dy$$

2. $$\int_{\pi/2}^{\pi}\int_{1}^{\sqrt{2}}(r^{2}\cos^{2}\theta+3r^{3}\sin\theta)\,dr\,d\theta$$

### b) Integrales triples

Calcula e imprime por consola las siguientes integrales triples, respetando los órdenes de integración:

1. $$\int_{0}^{1}\int_{0}^{2x}\int_{0}^{2x-y}e^{x}(3y-z)\,dz\,dy\,dx$$

**Atención:** El orden de integración es $dz\,dy\,dx$ (el enunciado original tenía $dx\,dy\,dx$, lo cual es un error tipográfico).

2. $$\int_{0}^{\pi}\int_{0}^{2\pi}\int_{0}^{a}\rho^{2}\sin\phi\,d\rho\,d\theta\,d\phi$$

**Nota:** Esta integral está en coordenadas esféricas.



## Entrega de la práctica
La práctica se podrá realizar individualmente o por parejas y se entregará a través del panel de Evaluación del UACloud, hasta las 23:59 del **16 de diciembre de 2025**. Constará de un archivo comprimido (zip o rar) que incluirá una carpeta con los scripts de los ejercicios. Es importante comentar todo elcódigo de la práctica.

