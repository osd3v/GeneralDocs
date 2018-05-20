#HTML - ESPECIFICACIÓN

Hyper Text Markup Language

W3C [World Wide Web Consortium]

HTML fue inicialmente diseñado como un lenguage para describir semanticamente documentos cientificos. Sin embargo, se fue adoptando nuevas funcionalidades para describir otro tipo de documentos e incluso aplicaciónes.

* Web IDL

* HTTP

* XML

* Unicode

* Character encondings

* Javascript

* CSS

  HTML tiene como uno de sus soportes las API del DOM.

  las APIs de HTML y el DOM están diseñadas de forma que ningún script puede detectar la ejecución simultanea de otros scripts, evitando las complejidades del multihilo.

  Extensiones

  arreglo de mecanismos para agregar sematica

  * class : atributo para extender y crear elementos propios. 
    * data-*="" : incluir data para script en linea, por el lado del cliente / servidor. Estos elementos no son manipulados por los navegadores y permite que los scripts incluir datos en elementos HTML que la secuencia de comando puede luego buscar y procesar.

    * <meta name="" content="">  : mecanismo para incluir metadata (metadata names)

    * rel="" mecanismo para anotar links con singnificado especifico(link types)

    * <script type="">: mecanismo para customizar un tipo, para manejarlo en linea o en los scripts del servidor.

    * Adicionalmente se puede extener las APIs utilizando el mecanismo de prototipos de javascript. Esto es ampliamente utilizando en los scripts de las bibliotecas, para las instancias.

#HTML y XML

 La especificaciòn define un lenguage abstracto para describir documentos y aplicaciones, y otras APIs para interactuar con la representación de recursos en memoria que utilzia el lenguage.
La representación de elementos es conocida como DOM [Document Object Model] - html

Existen varias sintaxis que se puede utilizar para trasmitir los recursos en este lenaguaje abstracto.

1. HTML sintaxis, formato sugerido, es más compatible con los Web browser legados [text/html]
2. XHTML sintaxis, aplicación de XML [application/xhtml-xml]



### Introducción

el documento HTML consiste en un árbol de elementos y texto. Cada elemento es denotado con Tag de inicio y un Tag de finalización.
La especificación define una serie de elementos HTML con reglas de anidación.
Los elementos tienen atributos que permite controlar las propiedades de los elementos. 
Los atributos estan dentro del Tag inicial, y consisten en una diccionario de nombre-valor

* Los árboles DOM se componen de nodos (DocumentType, Element, Text, Comment y ProcessingInstruction)
* El árbol DOM puede ser manipulador mediante scripts (programas embebidos), o manejadores de eventos del contenido de los atributos.
* Cada elemento del DOM es representado como un objeto, y estos objetos tiene APIs con los que se pueden manipular. 

## HTML

HMTL y CSS son las dos tecnologias core para construir paginas web.
HTML es un lenguage markup para describir la estructura para paginas web

* Permite navegar a traves de la información mediante hypertext links

* Diseño de formularios para conducir las transacciones con servicios remotos. 
##XHTML
XHTML es una variante de HTML que utiliza la  sintaxis HTML. XHTML  tiene todos los mismo elementos que HTML, sin embargo, la sintaxis es diferente porque XHTML es una aplicación XML, de forma que se pueden utilizar las herramientas XML(XSLT lenaguage para modificar el contenido XML).

## CSS

CSS es un lenguage para describir la presentación de paginas web, incluyendo colores, distribución (layout) y fuentes. Permite adaptar la presentación para los diferentes dispositivos. CSS es independiente de HTML y también puede ser usado con XML. La separación de HTML y CSS hace más fácil el mantenimiento de sitios, de forma que se puede compartir la hojas de estilos en todas la paginas y entornos.

## WEBFONTS

 