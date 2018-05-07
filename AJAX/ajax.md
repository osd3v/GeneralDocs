XMLHttpRequest


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