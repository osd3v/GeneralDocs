## APLICACIONES ORIENTADAS A SERVICIO WCF

WINDOWS COMMUNICATION FUNDATION WCF,modelo unificado  para compilar aplicaciones orientadas a servicio

### Compatibilidad asincronica basada en tareas

de forma predeterminada, las caracteristicas **Agregar referencia de servicio** genera métodos de operacion de servicio asincronico de devolución de tarea. Se realiza tanto para los métodos sincrónicos como para los asincronicos. Cuando se llama el método proxy generado, WCF crea un objeto de tarea para representar la operación asincronica y devuelve dicha tarea. La tarea se completa cuando finaliza la operación.

### CONFIGURAR SERVICIOS WCF EN EL CODIGO

WCF permite a los desarrolladores configurar servicios  mediante archivos de configuración o código. Los archivos de configuración son útiles cuando un servicio se debe configurar despues de implementarse. Cuando se usan archivos de configuracion, un profesional TI solo debe actulizar el archivo; más no es necesario que realice ninguna recompilación. Los archivos de configuración, sin embargo, pueden ser complejos y dificil de mantener. No se admite la depuración de archivos de configuración y se hace referencia a los elementos de configuración por nombre, con lo que la creación de archivos de configuración resulta propensa a errores y dificil. 

....



