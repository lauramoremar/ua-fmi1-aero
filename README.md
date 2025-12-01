# Fundamentos Matemáticos de la Ingeniería 1 (Ingeniería Aeroespacial)

## Práctica con Python 25-26: Cálculo de varias variables

El objetivo de la práctica es que aprendáis a utilizar python para representar funciones o hacer cálculos en varias variables.

Para eso utilizaremos Google Colabs, una herramienta flexible, tipo "notebook", para que podamos analizar y ver paso a paso lo que vamos implementando. Trabajaremos online, por lo que no hace falta instalar nada en vuestros ordenadores.

Si no estáis familiarizados con este entorno os recomiendo ver el vídeo tutorial de 5 min que os he preparado:

| Vídeo                             | Notebook              |
| :-------------------------------- | :-------------------: |
| Introducción a Google Colabs| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/notebooks/00-plantilla-prueba.ipynb) |

La práctica consta de 4 partes: Representación de funciones, límites, continuidad y diferenciabilidad, derivación e integración.

## 1. Representación de funciones

**Tutorial:** Para aprender a representar funciones de dos variables (superficies):

| Vídeo                             | Notebook              
| :-------------------------------- | :-------------------: |
| Representación de funciones de 2 variables | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/notebooks/01-intro-representacion-funciones.ipynb) |


**Ejercicio 1:**
A continuación, realiza el siguiente ejercicio en el siguiente cuaderno en blanco. Acuérdate de guardarlo en tu google drive, porque en caso contrario, los cambios no se guardan. Cuando lo termines, descarga el archivo ejercicio1.ipynb en tu ordenador.

| Ejercicio                         | Notebook              |
| :-------------------------------- | :-------------------: |
| Ejercicio 1 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/ejercicios/ejercicio1.ipynb)  |


a. Tomando como guı́a el vı́deo anterior, representa en Python la siguiente función:
$$
f(x, y) = \frac{1}{2} \cdot e^{-\frac{x^2 + y^2}{2}}
$$

Realiza la representación en forma de rejilla (wireframe), etiquetando los ejes x, y y z. 
Los vectores x e y deberán ser equiespaciados, de 32 elementos, cuyos valores irán desde -4 hasta 4. 
Establece un grosor de lı́nea de 1.0 y asigna el color royalblue para la representación.

b. Representa la siguiente función:

$$
f(x, y) = 0.5 + \frac{\cos^2\left(\sin\left(|x^2 - y^2|\right)\right)}{(1 + 0.001(x^2 + y^2))^2}
$$

Realiza la representación en forma sólida (surface), etiquetando los ejes x, y y z. Los vectores x e y tendrán 64 elementos equiespaciados, ambos con valores desde -π/4 hasta π/4. Asigna a la representación el mapa de color plasma.



c. Representación de un hiperboloide de 1 hoja

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


d. Función definida a trozos

En una figura aparte, representa la siguiente función:

$$
f(x, y) =
\begin{cases}
\dfrac{2xy}{x^2 + y^2} & \text{si } x^2 + y^2 \neq 0 \\
0 & \text{si } x^2 + y^2 = 0
\end{cases}
$$

Evita que la representación salga deformada, ejecutando la siguiente lı́nea de código antes del plot wireframe(): nombreEjes3D.set box aspect([1,1,1])

---

## 2. Límites, continuidad y diferenciabilidad

**Ejercicio 2:**

| Ejercicio                         | Notebook             |
| :-------------------------------- | :-------------------: |
| Ejercicio 2 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/ejercicios/ejercicio2.ipynb)  |


## 3. Derivación
**Tutorial**: Para aprender a derivar con python:

| Video                             | Notebook              |
| :-------------------------------- | :-------------------: |
| Derivación dos variables | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/notebooks/02-calculo-derivadas-parciales-gradiente.ipynb) |

**Ejercicio 3:**


| Ejercicio                         | Notebook              |
| :-------------------------------- | :-------------------: |
| Ejercicio 3 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/ejercicios/ejercicio3.ipynb)  |

## 4. Integración
**Tutorial**: Para aprender a hacer integrales múltiples:

|  Vídeo                            | Notebook              |
| :-------------------------------- | :-------------------: |
| Tutorial 03 - Cálculo integrales múltiples| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/notebooks/03-calculo-integrales-multiples.ipynb) |

**Ejercicio 4:**


| Ejercicio                         | Notebook             |
| :-------------------------------- | :-------------------: |
| Ejercicio 4 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lauramoremar/ua-fmi1-aero/blob/main/lessons/25-26/ejercicios/ejercicio4.ipynb)  |


## Entrega de la práctica
La práctica se podrá realizar individualmente o por parejas y se entregará a través del panel de Evaluación del UACloud, hasta las 23:59 del **16 de diciembre de 2025**. Constará de un archivo comprimido (zip o rar) que incluirá una carpeta con los scripts de los ejercicios. Es importante comentar todo elcódigo de la práctica.

