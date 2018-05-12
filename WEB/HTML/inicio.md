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
    * 