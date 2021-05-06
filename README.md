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

# 5 Prefijos propietarios

https://autoprefixer.github.io/

Se puede instalar el programa `prepros`. Nos genera un archivo `styles-dist.css` que contiene todos los prefijos para que la página funcione en cualquier explorador, por eso cargamos el archivo `styles-dist.css` en nuestro `index.html`. 

# 6 Box Model
![img](001.png)
### Width y height
~~~html
<div class="block">Elemento de bloque</div>
<a href="#" class="inline">Elemento de linea</a>
~~~
~~~css
.block{
    background-color: purple;
    width: 100px;
    height: 100px;
}
~~~
Con los elementos en linea no tienen ni alto ni ancho, por mucho que lo pongamos. El tamaño lo determina su contenido.
~~~css
.inline{
    background-color:lightcoral;
    color:inherit;
    width: 200px;
    height: 200px;
}
~~~