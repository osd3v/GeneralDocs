XMLHttpRequest

* Actualizar la webapp sin recargar la pagina
* Hacer request al servidor, despues de haber recargado la webapp
* Recibir data del servidor, despues de haber recargado la webapp 
* Enviar datos al servidor por detraz


Es utilizado para intecambiar datos detrás de escenas
Es objeto permite actulizar distintas partes de una pagina web sin recargar.
var xhr=new XMLHttpRequest();

Métodos disponibles
.abort() cancelar un request ya realizado
.getAllResponseHeaders() Retorna información del header
.open() permite abrir la conexión, información básica del request
.send() Envia el request al servidor
.setRequestHeader() Agrega valores al header que se desea enviar

xhr.open('POST',"crear_usuario.php",true);
xhr.send();

```javascript
var xhr=new XMLHttpRequest();
xhr.onreadystatechange=function(){
    if(this.readyState==4 && this.status==200)
    {
		document.getElementById("demo").innerHTML=xhr.responseText;        
    }        
}
xhr.open("GET",url,true);
xhr.send();
```



Propiedades

| Propiedad    | Descripción                                                  |
| ------------ | ------------------------------------------------------------ |
| readyState   | Estado de la petición                                        |
| respondeText | Contenido de la respuesta del servidor en forma de cadena de texto. |
| respondeXML  | Contenido de la respuesta del servidor en formato XML        |
| status       | Código del estado HTTP que retorna el servidor               |
| statusText   | Código de estado HTTP retornado por el servidor en forma de cadena de texto: OK,NotFound,InternalServerError,etc. |

Estados de la propiedad **readyState**

| valor | descripción                                                  |                  |
| ----- | ------------------------------------------------------------ | ---------------- |
| 0     | No inicializado (objeto creado, pero no se ha invocado el método open) | UNSENT           |
| 1     | Cargando (objeto creado, pero no se ha invocado el método send) | OPENED           |
| 2     | Cargado (Se ha invocado al método send, pero el servidor aún no ha respondido) | HEADERS_RECEIVED |
| 3     | Interactivo (descargando, la propiedad responseText contiene datos parciales) | LOADING          |
| 4     | Completo (operación completada, se ha recibido todos los datos de la respuesta del servidor) | DONE             |



| Método                                                       | Descripción                                                  | Retorno |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------- |
| abort()                                                      | Detiene la petición actual                                   | void    |
| getAllResponseHeaders()                                      | Devuelve una cadena de texto con todas las cabeceras de la respuesta de servidor | String  |
| getResponseHeader(String name)                               | Devueleve una cadena de texto con el contenido de la cebecera solicitada | String  |
| onreadystatechange                                           | Maneja los eventos. Se invoca cada vez que se produce un cambio de la petición HTTP. |         |
| open(metodo,url)                                             | Establece los parametros de la petición que se realiza al servidor. Los parametros necesarios son el método HTTP empleado y la URL destino(puede indicarse de forma absoluta o realtiva) | void    |
| send(contenido) / send()                                     | Realiza la petición HTTP del servidor                        | void    |
| setRequestHeader(String name, String value)                  | Permite establecer cabeceras personalizadas en la petición HTTP. se debe invocar el método open antes que setRequestHeader() | void    |
| setClientCertificate(String certificado, String key[, String password]) |                                                              | bool    |
|                                                              |                                                              |         |

Definición **open()**

open(string método, string URL [, boolean asincrono, string usuario, string password]);

Por defecto, las peticiones realizadas son asíncronas. Si se indica un valor false al tercer parámetro, la petición se realiza de forma síncrona, esto es, se detiene la ejecución de la aplicación de la aplicación hasta que se recibe de forma completa la respuesta del servidor.

| Propiedad    | Tipo    | Descripción                                                  |
| ------------ | ------- | ------------------------------------------------------------ |
| errorCode    | Number  | Retorna un entero que indica el error producido              |
| readyState   | Number  | Retorna un entero indicando el estado de la petición         |
| response     | Variant | Retorna un arraybuffer, un objeto javascript o una cadena, dependiendo del valor de responseType. Contiene el cuerpo completo de la respuesta. Es nulo si la petición no pudo completarse o es incompleta. |
| responseText | String  | Retorna una cadena conteniendo la cadena de respuesta retornada por el servidor HTTP. A diferencia de status, esta incluye el texto completo del mensaje de respuesta("200 OK"). |
| responseType | String  | Retorna String, arrayBuffer                                  |
| status       | Number  | Retorna el estado de la respuesta de la petición. Código del resultado HTTP (200 para una petición correcta) |
| statusText   | String  | Devuelve la cadena de respuesta. (mensaje de respuesta)      |
| timeout      | Number  | Representa el número de milisegundos que una petición puede tomar antes de ser automaticamente terminada. |

## Funciones

### Constructor

| Retorno        | Función          |
| -------------- | ---------------- |
| XMLHttpRequest | XMLHttpRequest() |

| errorCode | Descripción                                                  |
| --------- | ------------------------------------------------------------ |
| 0         | No se ha producido ningun error                              |
| 1         | El servidor remoto rechazó la conexión (el servidor no esta aceptando las peticiones) |
| 2         | El servidor remoto ha cerrado la conexión, antes de que la petición fuera recibida y procesada |
| 3         | El nombre del host no se ha encontrado (hostname inválido)   |
| 4         | Ha expirado el tiempo máximo de conexión al servidor remoto (timeout) |
| 5         | La operación se ha cancelado por una llamada a abort() o close() antes de que acabará |
| 6         | La comunicación SSL/TLS ha fallado y la comunicación encriptada no se puede establecer |
| 7         | La conexión fue interrumpida debido  a una desconexión de la red, sin embargo, el sistema se ha iniciado. |
| 201       | El acceso al contenido remoto fue denegado (similar al error HTTP 401) |
| 202       | La operación solicitada sobre el contenido remoto no esta permitida |
| 203       | El contenido remoto no fue encontrado en el servidor (similar al error HTTP 404) |
| 204       | El servidor remoto solicita autenticación para servir el contenido, pero las credenciales suministradas no son correctas. |
| 301       | No se puede procesar la petición porque el protocolo es desconocido |
| 302       | La operación solicitada es inválida para este protocolo      |
| 99        | Un error desconocido relacionado con la red ha sido detectado |
| 299       | Un error desconocido relacionado con el contenido remoto ha sido detectado |
| 399       | Un error ha sido detectado en el protocolo (error de parseo, respuesta inválida o no esperada, etc.) |

