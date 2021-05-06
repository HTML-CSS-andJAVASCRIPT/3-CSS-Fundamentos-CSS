# 2 Fundamentos CSS
# ¿Cómo funciona CSS? 

# 1. Especificidad 
Establece como de específico es un selectore para saber que estilo aplicar.
El cálculo se realiza con la siguiente fórmula:
Etiquetas y pseudoselementos 001
Clases, atributos y pseudoclases 010
Id 100
Estilos en líneas 1000
~~~css
h1.title#title{
    background-color:salmon;
}
~~~
`!important` si lo usamos quita todo los valores de especifidad porque se lo carga todo. Mala prática.
La mejor manera de hacerlo es usar siempre clases para ponerles los propiedades.
~~~css
.title{
    background-color: blue;
}
~~~
Con esta página podemos ver la calidad del CSS

https://jonassebastianohlsson.com/specificity-graph/

# 2 Cascada
Funciona siempre que la especificidad sobre el elemento sea la misma.
~~~css
.title{
    background-color: blue;
}
.title{
    background-color: red;
}
~~~
# 3 Herencia
Es la capacidad que tienen algunos elementos de heredar algunas propiedades de sus elementos contenedores (padres, abuelos, etc)
~~~html
 <a href="#">Enlace de ejemplo</a>
~~~
Por mucho que le intentemos cambiar el color del enlace en el archivo `styles.css` el enlace no hereda nada, porque tiene su estilo propio.
Habría que agregar una clase específica para el enlace.
~~~html
<a class="link" href="#">Enlace de ejemplo</a>
~~~
~~~css
.link{
    color:red;
}
~~~
Para forzar la herencia tenemos la palabra `inherit`
~~~css
.link{
    color:inherit;
}
~~~
Para que un elemento no herede tenemos la palabra `initial` que pone el elemento en el estado inicial.
~~~css
.list-item-extra{
    color:initial;
    
}
~~~

# 4 Estilos computados
Para abrir la herramientas de desarrollo, pulsando `f12`
### Estilos por defecto.
Cada explorador tienen sus propios estilos por defectos hay que tener en cuenta eso.
Se pueden normalizar los estilos.
Descargamos el archivo y lo guardamos en la carpeta `css` y lo tenemos que cargar antes del archivo `styles.css` en el `index.html`
https://necolas.github.io/normalize.css/



