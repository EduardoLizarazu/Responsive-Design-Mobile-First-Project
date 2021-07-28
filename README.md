# Responsive Design Mobile First

## Setup inicial

### Arquitectura inicial
La arquitectura web se puede definir como la forma en que las páginas de un sitio web están estructuradas y enlazadas entre sí _(de manera lógica y coherente)_. Una arquitectura web ideal ayuda a los usuarios y a los motores de búsqueda a encontrar fácilmente lo que están buscando en un sitio web.

**Arquitectura inicial del proyecto**

[Batabit figma](https://www.figma.com/file/sMmlQaZldfDcLERYYWe6h4/Bata-Bit?node-id=44%3A594)

Entonences analizamos primero el diseño que nos paso el diseñador y vamos viendo como separarlo para ir formando el layout.

- Header
- 4 Section
- Footer
```
<body>  
	<header></header>  
	<main>  
		<section></section>  
		<section></section>  
		<section></section>  
		<section></section>  
	</main>  
	<footer></footer>  
</body>
```

## Assets
Los assets son todos los  **recursos estáticos**  que utilizaremos en nuestro proyecto, tales como:
* Imágenes  
* Logotipos/Isotipos (Si el logotipo y el nombre de la empresa/marca se encuentran en elementos separados, es preferible descargarlos agrupados)
* Iconos

**PRO TIP:** podemos descargar varios assets simultáneamente. Solo debemos seleccionar varios elementos, presionando CTRL + Clic sobre el elemento, y luego presionamos Export seleccionamos el formato, ¡y Listo! nuestros assets se descargaran en un archivo .zip

Clasificamos los assets según el tipo de recurso (imagen, ícono, etc…), además es recomendble que sigamos un estándar para nombrar nuestros archivos (nombre corto, desciptivo, en minúsculas, sin espacios).
Finalmente la estructura de carpetas de nuestro proyecto debería quedar de esta forma:
```
- assets 
	- icons 
		- img 
			- bitcon.svg 
			- logo.svg 
- index.html
```
## Agregando estilos tips
1. **Posicionamiento (Display)** --> static, absolute, relative, fixed.
2. **Modelo de caja (Box model)** --> margin, border, padding, content, width, height.
3. **Tipografia** --> tipos, tamaños de fuente, etc.
4. **Estilos visuales** --> box-shadow, border-radius, gradient, etc.
5. **Otros** --> reglas CSS y más.

## Implementando BEM
No es necesario ponerle clase a todas las etiquetas. Solo a aquellas etiquetas que creemos que se **repetiran en el mismo bloque.** Ya que despues podemos llamarlo en CSS con combinadores desendientes. De esta forma nos queda un HTML mas limpio.

[Metodologia BEM](https://en.bem.info/methodology/quick-start/)

[Metodologia BEM Stylecheat](https://9elements.com/bem-cheat-sheet/)

## Imagen background
Una buena practiva cuando usamos:
```
background-image: url();
```
Una buena practica es añadirle el siguiente codigo:
```
background-image: url();
background-size: cover;
background-position: center;
background-repeat: no-repeat;
```
### Background-size
Background-size sirve bastante para manejar de que manera queremos que se vea la imagen en el fondo.

Cover por ejemplo, para que la imagen cubra todo el espacio según el tamaño del contenedor.

**Imagen con cover:**

![enter image description here](https://static.platzi.com/media/user_upload/Captura%20de%20pantalla%202020-10-26%20221335-02d64ad3-d0ab-4649-860b-2a06460064e5.jpg)

Contain para que la imagen se ajuste dentre del tamaño del contenedor.
**Imagen con contain**

![enter image description here](https://static.platzi.com/media/user_upload/Captura%20de%20pantalla%202020-10-26%20221434-9169541a-a4d2-4e18-837f-c1812e9beae1.jpg)

### Background-position
```
background-position: center;
```
Sirve para posicionar una imgen en el centro de su contenedor y siempre este en el centro.

[play with background-position](https://www.w3schools.com/cssref/playit.asp?filename=playcss_background-position)

## Seccion de Beneficios
### Position: absolute y relative
Cada vez que usemos **Position: absolute** es recomendable ponerle **Position: relative** al contedor padre. Pues **absolute** buscara tomara como referencia al padre con **relative** mas cercano. Entonces para evitar comportamientos extraños ponemos **relative** al contenedor padre y **delimitar su movimiento.**
### Posicionamiento en el centro
**Ponemos calc(50% -20px).**  El 50% es para que el contenido este el centro, pero el elemento (icono) mantiene su propia dimencion. Entonces el -20px es para quitarle la propia dimencion del elemento insertado.

## Overflow
Es cuando hay desvordamiento del contenido porque el contenedor no crece. **El contenido es mas grande que el height de su padre (contenedor),** entonces empieza como a salirse del mismo. 
Para resolver este problema que tuvimos en el card 4 pusimos ```min-height: 150px;``` esto para que esto sea lo minimo que pueda medir, pero dando le chace para que siga creciendo.

## Overflow-x
La propiedad de CSS overflow-x establece lo que se muestra cuando el contenido desborda los bordes izquierdo y derecho de un elemento a nivel de bloque. Puede que no sea nada, una barra de desplazamiento o el contenido adicional.
## Overflow-behavior
La propiedad de css overscroll-behabior establece lo que hace un navegador cuando alcanza el límite de un área de desplazamiento. Es una abreviatura de overscroll-behavior-x y overscroll-behavior-y.
## Scroll-snap-type
```scroll-snap-type: x proximity```
La propiedad CSS scroll-snap-type establece qué tan estrictamente se aplican los puntos de snap en el contenedor de desplazamiento en caso de que haya uno.
## Scroll-snap-align: center
Lo use para que se **centrara el scroll** en los contenedores y no quedara a la mitad.
## Gap
Lo use para separar los contenedores, aunque este aun no es valido en algunos navegadores.
## Otros datos
Usamos ```vertical-align: text-bottom;``` para alinear el texto que se vio afectado por icono. Esto ocurrio en
> .plan-card--ca span
> .plan-card--price span

Tambien use ```overscroll-behavier-x: contain;```

## Google Lighthouse
Es una herramienta automatizada de código abierto para medir la calidad de las páginas web. Se puede ejecutar en cualquier página web, pública o que requiera autenticación. Google Lighthouse audita el rendimiento, la accesibilidad y la optimización de motores de búsqueda de páginas web.
