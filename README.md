# scripts-gl
Scripts que pueden resultar útiles para resolver ejercicios de Geometría Lineal usando Sage.

Están pensados únicamente para su uso en resolución de ejercicios y exámenes de la asignatura GL de la Facultad de Matemáticas de la Universidad Complutense de Madrid. Por ello, no se pretende que los algoritmos sean óptimos ni 100% fiables, aunque sí es recomendable que tengan una fiabilidad alta.

Cualquier error que se detecte debería ser comunicado lo antes posible.

# Cómo usarlos
Las carpetas importantes son scripts y doc. En scripts se encuentran todos los archivos con scripts disponibles. En doc se encuentra la documentación básica para ser capaz de usar dichos scripts, sin necesidad de mirar ningún tipo de código.

Si usamos la versión nueva del cuaderno de Sage, Jupyter (la del icono naranja), simplemente podremos subir los archivos .sage. Después, en el archivo que creemos para resolver los ejercicios debemos cargarlos antes de hacer nada con la instrucción <code>load("[nombre del archivo]")</code> (por ejemplo, <code>load("scripts/espacios.sage")</code>). Si queremos que se muestre "bonito" podemos activar Latex con la instrucción <code>pretty_print_default(True)</code>.

En la versión antigua no he logrado de momento subir archivos .sage, así que nos tendremos que conformar con copiar el código, pegarlo en nuestro cuaderno, ejecutarlo y, ya entonces, lo podremos utilizar. Para verlo en Latex marcar la casilla Typeset.

# Cómo participar
Si quieres subir algún script a este banco de scripts, puedes hacerlo sencillamente con un Pull-request a una rama nueva, o enviármelo, con unas ciertas condiciones.
<ol>
<li>
  Obviamente, el script debe funcionar y, si hay algún caso concreto que falla, se debe indicar en su documentación.
</li>
<li>
  Debe estar escrito como una función (o una clase con métodos) de Python. Esto es, debe recibir unos parámetros y recibir un resultado directamente.
  
<code>

    def foo(bar):
        ~ interior de la función ~
    
</code>
  
  No vale tener un cuaderno en el que sustituyes unos valores para unas variables y se va ejecutando paso a paso. De todas formas no está de más añadir, además, algo semejante si se quiere tener resultados intermedios.
</li>
<li>
  Como Python es como es, es obligatorio indentar, y toda la indentación debe ser uniforme. Así que se indentará con <b>4 espacios</b>.
</li>
<li>
  Cada función o clase debe tener justo sobre ella un comentario <code># bla bla</code> con un formato que se explciará más abajo explicando lo que hace y cómo lo hace. Esto es importante, pues en un examen se nos va a pedir algún tipo de procedimiento y debemos saber qué es lo que está haciendo la función por dentro. También debe indicar qué significa cada parámetro que recibe.
  
<code>

    # \f
    # Implentación \\
    # La función funciona así.
    #
    # Parámetros \\
    # a: vector(n) - vectorcito de entrada
    # b: recta - recta horrible con la que haremos cosas
    #
    def foo(a, b):
    
</code>

</li>
<li>
  Por simplicidad para todo el mundo, tanto el código como los comentarios deben estar todos en español (a pesar de que a mí, personalmente, me haga daño a la vista ver código en español).
</li>
</ol>

Si alguien quiere participar, pero no se ve capaz de implementar algo así, siempre me puede pedir ayuda para hacerlo.

# Formato de la documentación
En este proyecto se incluye un pequeño programa que se encarga de leer los comentarios de los archivos .sage para transformarlos en archivos .html (páginas web) que se puedan abrir con un navegador y sean más legibles que los propios comentarios en el código. Pero para que esto fucnione correctamente se necesite que los comentarios sigan unos estándares (sólo se refiere a los de documentación de las funciones; comentarios internos aclarativos pueden llevar el formato que sea).
<ul>
<li>
  Si se está documentando un archivo en general, es decir, lo que hay dentro de ese módulo, la primera línea del comentario debe ser \s. También debe haber una línea en blanco después de todo el comentario.
  
<code>
  
    # \s
    # Este archivo es muy bonito.
    # Hace cosas.
    #
    
    ~ código ~
    
</code>
  
</li>
<li>
  Para una función o método de una clase se utiliza \f y \m, respectivamente, aunque realmente no suponen ninguna diferencia real a la hora de generar la documentación.
  
<code>

    # \f
    # Esta función no hace nada.
    #
    def foo():
    
</code>
</li>
<li>
  Para una clase se utilizará \c
  
<code>
  
    # \c
    # Clase sin clase.
    #
    class clase:
    
</code>
  
</li>
</ul>
Si en el archivo .html que se genere queremos que haya algún salto de línea en un lugar concreto tenemos dos posibilidades: dejar una línea entera en blanco (pero con comentario) o escribir \\. Más o menos como en Latex.

<code>

    # Esto se verá en la primera línea.
    # Esto también.
    # 
    # Pero esto ya en la segunda. \\
    # Y esto en la tercera.
  
</code>