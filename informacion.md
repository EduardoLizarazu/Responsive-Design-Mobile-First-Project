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
**1. Posicionamiento (Display)** --> static, absolute, relative, fixed.
**2.  Modelo de caja (Box model)** --> margin, border, padding, content, width, height.
**3. Tipografia** --> tipos, tamaños de fuente, etc.
**4. Estilos visuales** --> box-shadow, border-radius, gradient, etc.
**5. Otros** --> reglas CSS y más.

## Implementando BEM
No es necesario ponerle clase a todas las etiquetas. Solo a aquellas etiquetas que creemos que se **repetiran en el mismo bloque.** Ya que despues podemos llamarlo en CSS con combinadores desendientes. De esta forma nos queda un HTML mas limpio.
[Metodologia BEM](https://en.bem.info/methodology/quick-start/)
[Metodologia BEM Stylecheat](https://9elements.com/bem-cheat-sheet/)
