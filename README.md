# Practica 03: Funciones de Membresia
 09/Septiembre/2022
 
 3BV11
 
 Aguilar Ayala José Alberto
 Gómez Trejo Braulio
 
## <sub> Objetivos <sub>
* Implementar operaciones de conjuntos difusos, utilizando MATLAB
* Implementar transformaciones de conjuntos difusos, utilizando MATLAB

# <sub> Introducción <sub>
## <sub> Conjuntos Difusos <sub>
La lógica difusa, es una lógica alternativa a la lógica clásica que pretende introducir un grado de vaguedad en las cosas que califica. En el mundo real existe mucho conocimiento no-perfecto, es decir, conocimiento vago, impreciso, incierto, ambiguo, inexacto, o probabilístico por naturaleza. Para comprender de manera clara la lógica difusa es necesario tener claro algunas definiciones.
* Variable lingüística es aquella noción o concepto que vamos a calificar de forma difusa. Por ejemplo: la altura, la edad, el error, la variación del error... Le aplicamos el adjetivo "lingüística" porque definiremos sus características mediante el lenguaje hablado.
* Universo de discurso es el rango de valores que pueden tomar los elementos que poseen la propiedad expresada por la variable lingüística. En el caso de la variable lingüística 'altura de una persona normal', sería el conjunto de valores comprendido entre 1.4 y 2.3 m.
* Valor lingüístico a las diferentes clasificaciones que efectuamos sobre la variable lingüística: en el caso de la altura, podríamos dividir el universo de discurso en los diferentes valores lingüísticos: por ejemplo bajo, mediano y alto.
* Conjunto difuso es un valor lingüístico junto a una función de pertenencia. El valor lingüístico es el “nombre” del conjunto, y la función de pertenencia se define como aquella aplicación que asocia a cada elemento del universo de discurso el grado con que pertenece al conjunto difuso. Decimos que un conjunto es nítido si su función de pertenencia toma valores en {0,1}, y difuso si toma valores en [0,1].
* Dado un conjunto difuso A, se define como alfa-corte de A, al conjunto de elementos que pertenecen al conjunto difuso A con grado mayor o igual que alfa, es decir: 
* Alfa corte estricto al conjunto de elementos con grado de pertenencia estrictamente mayor que alfa, es decir 
* Soporte de un conjunto difuso A, al conjunto nítido de elementos que tienen grado de pertenencia estrictamente mayor que 0, o sea, al alfa-corte estricto de nivel 0.

 # <sub> Problema 1<sub>
 
La funcion smf calcula valores de pertenencia difusos utilizando una funcion de membresia en forma de S basada en splines.
Para y= smf(x,params) de vuelve valores de pertenencia difusos calculados utilizando la funcion de membresia en forma de S basada en spline dada por:

$$ f(x;a,b)=
\begin{cases}
0 & x\leq a \\
2* (\frac{x-a}{b-a})^2 & a \leq x \leq \frac{a+b}{2}\\
1-2* (\frac{x-a}{b-a})^2 & \frac{a+b}{2}\leq x \leq b \\
1 & x \geq b
\end{cases}
$$
 
La funcion psigmf calcula valores de pertenencia difusos utilizando el producto de dos funciones de membresia sigmoidea.
Para y=psigmf(x,params) devuelve valores de pertenencia difusos calculados utilizando el producto de dos funciones de pertenencia. Cada funcion sigmoidea viene dada por:
$f(x;a_k,c_k)=\frac{1}{1+e^{-a_k(x-c_k)}}$

# <sub>Problema 2<sub>

Cree una función en matlab que reciba como argumentos de entrada el dominio y el rango de una función de membresía, esta función debe crear la grafica del conjunto difuso con una edición de tu preferencia (no queremos repetir los códigos para gráficar cada vez que se quiera visualizar un conjunto difuzo, como se ha visto previamente).
 
Prueba el código con las dos funciones del problema anterior, los parámetros que debes utilizar  (debes investigar) son los que se usan en el ejemplo de la práctica.
 
Se espera esta sección dos llamadas a la función con las dos gráficas respectivas. 
