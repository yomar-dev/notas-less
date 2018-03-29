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




### Enlaces de interes ###

[Documentación Oficial de LESS](http://lesscss.org/)