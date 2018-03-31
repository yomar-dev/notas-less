# Notas Less #


### Importar archivos ###

Para importar archivos debemos hacerlo con la clausula **@import**, seguido se la ruta del archivo, luego el nombre del archivo y por ultimo la extensión de dicho archivo.

*Ejemplo:* <br>

`@import "base/_tipografia.less";`


### Variables ###

Las variables se declaran con **@** seguido del nombre.

*Ejemplo:* <br>

~~~
@color-h1: #333;
@color-p: #1e1e1e;
~~~


### Anidaciones ###

Nos permite incluir estilos de un elemento dentro de otro.

*Ejemplo:* <br>

**Entrada:**

~~~
p{
	color: #333;

	a{
		color: skyblue;
		font-weight: bold;

		&:hover{
			background-color: #222;
			cursor: pointer;			
		}
	}
}
~~~

**Salida:**

~~~
p {
  color: #333;
}

p a {
  color: skyblue;
  font-weight: bold;
}

p a:hover {
  background-color: #222;
  cursor: pointer;
}
~~~


### Mixins ###

Son un conjunto de propiedades CSS agrupadas. Esto nos permite utilizar el grupo en sí y no repetir mil veces las mismas propiedades.

*Ejemplo:* <br>

**Entrada:**

~~~
.max-width(){
	max-width: 1024px;
	margin-left: auto;
	margin-right: auto;
}

.section{
	.max-width;
}

.container{
	.max-width;
}
~~~

**Salida:**

~~~
.section {
  max-width: 1024px;
  margin-left: auto;
  margin-right: auto;
}
.container {
  max-width: 1024px;
  margin-left: auto;
  margin-right: auto;
}
~~~


### Mixins Paramétricos ###

Son aquellos que reciben paramétros.

*Ejemplo:* <br>

**Entrada:**

~~~
.border-radius(@radius) {
	-webkit-border-radius: @radius;
	-moz-border-radius: @radius;
	border-radius: @radius;
}
 
.sidebar {
	.border-radius(4px);
}
~~~

**Salida:**

~~~
.sidebar {
  -webkit-border-radius: 4px;
  -moz-border-radius: 4px;
  border-radius: 4px;
}
~~~




### Enlaces de interes ###

[Documentación Oficial de LESS](http://lesscss.org/)