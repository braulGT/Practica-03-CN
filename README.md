# Practica 03: Funciones de Membresia
 09/Septiembre/2022
 
 3BV11
 
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

! (/assets/images/descargar.png)
 
La funcion psigmf calcula valores de pertenencia difusos utilizando el producto de dos funciones de membresia sigmoidea.
Para y=psigmf(x,params) devuelve valores de pertenencia difusos calculados utilizando el producto de dos funciones de pertenencia. Cada funcion sigmoidea viene dada por:
