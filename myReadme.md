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
