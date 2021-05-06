# 3 Fundamentos CSS
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