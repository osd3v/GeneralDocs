#GRID LAYOUT

## ABSTRACT

Este modulo define un sistema basado en un grid layout, optimizada para el diseño de interfaces de usuario. En el modelo de grid layout sus items puede ser posicionados arbritrariamente en los espacios predefinidos como flexibles o fijos.

CSS: es una lenaguaje para describir el render de documentos estructurados en la pantalla, en la hoja, en el speech, etc.

## 1. Introducction

Grid layout es un nuevo modelo de layout CSS que mejora el control del dimesionamiento y posicionamiento del container y su contenido. A diferencia del flexible box layout, el cual esta orientado a un eje simple, el grid layout esta optimizado para el manejo de un 2D layout el cual permite el alineamiento deseado del contenido en las dos dimesiones. 

Adicionalmente, debido a la habilidad de posicionar explicitamente los items en el grid, Grid Layout permite una transformación transformación en el diseño de la estructura visual sin requerir cambios en el marcado(HTML). En combinación de los **media queries** y las propiedades para controlar el layout del grid container y sus items, se puede adaptar a las modificaciones por factores como orientación y espacio disponible,mientras se mantiene la estructura semantica del contenido a traves de todas las presentaciones.

Pese a que muchos layouts pueden ser expresados con Grid or Flexbox, cada uno esta especializado para determinado trabajo. Grid realiza un alinamiento en 2D, utilizando un enfoque de top-down, lo que permite superponer explicitamente los items y extendiendo sus capacidades.Flexbox se enfoca en la distribución en el espacio de un eje, utilizando el enfoque de layout bottom-up, puede utilizar un sistema de ajuste de línea basado en el tamaño de su contenido para controlar sus eje secundario, y depende de la jerarquia de marcado subyacente para construir presentaciones más complejas. Se espera que ambas herramientas se utilizen de forma complementaria.

### 1.1 Background and Motivation

A medida que las paginas web han evolucionado de documentos simples a complejas e interactivas, las técnicas del layout de los documentos, como los floats no eran no eran necesariamente los más adecuados. Utilizando una combinación de tablas y javascript o una cuidadosa medida en los elementos flotantes, los desarrolladores encontraron encontraron las soluciones para los requerimientos. Adaptar los layouts a el espacio disponible algunas veces resulta fragil o con un resultado no esperado a medida que el espacio se restringia. Como alternativa los desarrolladores de aplicaciones optaron por un layout fijo que no permite aprovechar las ventajas de cambiar el renderizado de acuerdo al espacio de la pantalla.

Las capacidades de tener un grid layout con direcciones resuelve estos problemas. Proporcinando un mecanismo para dividir el espacio disponible en un layout de columnas y filas utilizando un comportamiento predecible de las dimesiones. Asi los desarrolladores puede posicionar y dimensionar con presición los elementos de sus aplicaciones en las grid areas definidas como las intersección de estas columnas y filas. Los siguientes ejemplos ilustran como utilizar las capacidadades de adapación de los grid layout y como permite mantener una separación transparente del contenido y el estilo.

#### 1.1.1 Adapting Layouts to Available Space

Existen multiples formas de especificar las estructura del grid, las posiciones y dimensiones, cada uno esta optimizado para diferentes escenarios.

####1.1.2 Source Order Independence

​	Combinar el grid layout con media queries, permite utilizar el mismo marcado semantico, si reordenar el layout de los elementos y mantiendolo independiente del order fuente, manteniendo el layout requerido en ambas orientaciones.

## 2. Overview

Grid Layout controla la distribución del contenido mediante el uso de grid: un serie de intersecciones de lineas verticales y horizontales que crear un sistema de coordenadas con dimensiones y tamaños para los contenidos del contenedor.

CARACTERICTICAS

*  Funciones para manejar el dimensionamiento mediante pistas fijas, flexibles y basadas en el contenido.

* Diposición explicita de elementos mediante coordinadas de la cuadricula numerica, líneas de cuadricula con nombre y áreas de la cuadricula con nombre. Adicionalmente los vacios se llenan automaticamente, incluyendo el reordenamiento con orden.

* Repetición de las caracteristicas del espacio disponible y adición automatica de filas o columnas para acomodar el contenido adicional.

* Control de alineación y el espaciado con los magenes, canaletas y las propiedades de alineación.

* Permite superponer el contenido y controlar las capas con z-index.

Lo contenedores grid puede anidarse o mezclarse con los contenedores flex si es necesario para crear layouts más complejos.

### 2.1 Declaring the Grid

Los tracks(filas o columnas) de un grid son declarados and dimensionados explicitamente a través de las propiedades explicitas grid o implicitamente cuando cuando se coloca los items fuera del grid explicito. El shorthand **grid** y sus subpropiedades definen los parametros del grid.

### 2.2 Placing Items

El contenido del grid container es organizado individualmente en grid items, los cuales son ubicados de forma predefinida en areas del grid. Estos pueden ser ubicados explicitamente utilizando coordenadas  a través de los **grid-placemente properties** o implicitamente ubicados en las areas vacias utilizando **auto-placemente**.

### 2.3 Sizing the Grid

Una vez que los grid items con ubicados, el tamaño de los grid tracks es calculado, considerando el tamaño de su contenido y/o el espacio disponible especificado en la definición del grid.
La dimención y alineamiento resultante del grid container es  deacuerdo a las propiedades **align-content** y **justify-content** del grid container. 
Finalmente cada grid item es dimensionado y alineado cuando se le asigna a un grid area o cuando se especifica las propiedades sizing y alignment.

## 3. Grid Layout Concepts and Terminology

En un grid layout, el contenido del grid container es posicionado y alineado en una grid. El grid es una intersección de grid lines horizontales y verticales que dividen el grid container en espacio denominados grid areas, dentro de las cuales se ubican los grid items.

### 3.1 Grid Lines

Son lineas verticales y horizontales que divide el grid, estas estan ubicadas en cada lado de una columna o fila y se referencia a ellos mediante un indice numerico o con un nombre especificado. 

Un grid item referencia a las grid lines para determinar su posición en el gri utilizando grid placement properties.

### 3.2 Grid tracks y Cells

GRID TRACK es un termino generico para referirse a las grid columns y grid rows, es el espacio disponible entre dos grid lines adyacentes. A cada grid track se le asigna una función de dimesionamiento, que controla que el ancho y alto. Los grid track son separados por gutters.

Grid Cell es la intersección de una grid row y grid column, es la unidad minima de un grid que puede ser referenciado cuando se posiciona un grid item.

### 3.3 Grid Areas

Grid area es un concepto lógico para distribuir uno o más grid items. Una grid area consiste en una o más grid cells adyacentes. Esta delimitado por cuatro grid lines, una a cada lado del area de la grid area e incluye el tamaño de las grid tracks . Una grid area puede ser nombrado explicitamente utilizando la propiedad  **grid-template-areas** de los grid container o referenciando implicitamente por la grid lines que las delimitan. Un grid item es asignado  a un grid area utilizando la propiedad **grid-placement**.
El grid area de forma el bloque contenedor del grid item. Los grid items agregados en el mismo grid area no afectan directamente en el layout de otros. Sin embargo, un grid item que ocupa que ocupa un grid track con una funcion de dimensionamiento intrinseca puede afectar el tamaño del grid track(y la posición de los grid lines limites) y a su vez puede afectar el tamaño y posicion de otros grid items indirectamente.

## 4. Reording  and Accessibility

Grid layout permite gestionar el orden del los elementos del documento. Sin embargo, esto no sustituye el orden natural del documento fuente. Las propiedades **order** y **grid placement** no afecta el ordenamiento en medios no visuales(speech). Asimismo, el reordenamiento visual no afecta el orden secuencial de navegación por defecto(tabindex).

## 5. Grid Containers

Grid: produce que un elemento adquiera block-level de tipo caja grid-container

### 5.1 Establishing Grid Containers

Una grid container establece un nuevo contexto de tipo formato grid para su contenido. Esto es similar a establecer un contexto con formato de tipo bloque, excepto que se utiliza el grid layout en lugar un  grid block: los flotantes no se incluyen en el grid container y los padding del contenedor grid no se colapsan con los márgenes de sus contenido.

Un grid container no es un block container, y algunas propiedades se diseñaron suponiendo que el block layout no aplica en el contexto de grid layout. En particular:

* 'float' y 'clear' no afectan a un grid item. Sin embargo, la propiedad 'float' todavia afecta al **computed value** al mostrar los hijos del grid container, ya que esto sucede antes de determinarse los grid items.

* 'vertical-align' no tiene efecto en el grid item.

* los pseudo-elementos **::first-line**   y **::first-letter** no aplican a los grid containers, y los grid containers permite al formatear la primera linea o letra de sus ancestros.

Si la especificación 'display' de una elemento es 'inline-grid' y el elemento tiene posicionamiento flotante o absoluto, el computed value  del 'display' es 'grid'

###5.2 Sizing Grid Containers

Un grid container  es dimensionado utilizando las reglas de formato de contexto en el que participa:

* Como un **block-level** box en un **block formatting context**, este es dimesionado como un **block box** que establece con contexto con formato, con un  tamaño calculado 'auto' para no tener reemplazos de block boxes.

*  Como un **inline-level** box en un **inline formatting context**, este es dimesionado como un inline-level box atomico. 

En cambos casos de formato de contextos **inline** y **block**, el tamaño del bloque auto del grid container es el tamaño maximo del contenido.

El tamaño maximo del contenido del grid container es la suma del tamaño de los tracks del grid container(incluyendo lo gutters) de los ejes apropiados, cuando el grid es dimensionado con la restricción del contenido máximo. 

### 5.3 Clamping Overly Large Grids

Partiendo que la memoria es limitada, UAs puede restringirse el tamaño del grid con la definicion de un limite del UA, borrando todas las lineas fuera del limite. Si un grid item es ubicado fuera de este limite, este grid area  debe para que quede dentro del grid. 

Clamp de un grid area:

* Si el span de un grid area queda fuera del limite del grid, este span es restringido a la ultima linea del limite del grid.

* Si el grid area queda completamente fuera del limite del grid, el span será truncado a 1 y el area se reposicionará dentro del último **grid track** del grid.

## 6. Grid Items

los grid items de una grid container son los boxes representados dentro del flujos del contenido.

Cada item dentro del  flujo del grid container se convierte en un grid item, y cada texto dentro de la secuencia contigua es envuelta en un bloque anonimo. Sin embargo, si la secuencia completa de hijos de tipo texto contienen solo un espacio en blanco, este en su lugar no es renderizado.

### 6.1 Grid Items Display

un grid item establece un nuevo formato de contexto para su contenido. 

 







