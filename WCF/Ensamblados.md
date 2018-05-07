Los ensamblados son bloques de creación de las aplicaciones .NET Framework:

* Crea una unidad de implementación. Cunado se inicia una aplicación, solo deben estar presentes los ensamblados a los que llama la aplicación inicialmente. Los demás ensamblados, como los recursos de localización o los ensamblados que contengan clases de utilidad, se pueden recuperar a petición. De este modo, se puede mantener la simplicidad y transparencia de las aplicaciones la primera vez que se descargan
* Contiene el código que ejecuta Common Language Runtime. El código del lenguaje intermedio de Microsoft(MSIL) de un archivo ejecutable portable(PE) no se ejecuta si no tiene asociado un manifiesto del ensamblado. Hay que tener en cuenta que cada ensamblado solo puede tener un punto de entrada (DllMain, WinMain, Main).
* Control de versiones. El ensamblado es la unidad versionable más pequeña de Common Language Runtime; todos los tipos y recursos del mismo ensamblado pertenecen a la misma versión. El manifiesto del ensamblado describe las dependencias de versión que se especifiquen para los ensamblados dependientes.
* Reutilización
* Ámbito activación, crea un limite de tipos. La identidad de cada tipo incluye el nombre del ensamblado en que reside. Por ello, un tipo **MyType** cargado en el ambito de un ensamblado no es igual que un tipo denominado **MyType** cargado en el ambito de otro ensamblado.
* Crear un limite de ambito de referencia. El manifiesto del ensamblado contiene los metadatos del ensamblado que se utilizan para resolver tipos y satisfacer las solicitudes de recursos. Especifica los tipos y recusos que se exponen fuera del ensamblado. El ensamblado también enumera otros ensamblados de los que depende. 
* Permisos de seguridad, crea un limite de seguridad. Un ensamblado es la unidad en la que se solicitan y conceden permisos.
* Es la unidad que permite la ejecución en paralelo.

Un ensamblado es una colección de tipos y recursos compilados para funcionar en conjunto y formar una unidad lógica funcional. Lo ensamblados proporcionan a Common Language Runtime la información necesaria para reconocer implementaciones de tipos. Para la ejecución, un tipo no existe fuera del contexto de un ensamblado.

### Cuatro elementos de ensamblado

* El manifiesto del ensamblado, que contiene los metadatos del ensamblado.

* Los metadatos de tipos.

* El código de lenguaje intermedio de Microsoft (MSIL) que implementa los tipos

* Un conjunto de recursos.


### COMPILAR UN ENSAMBLADO DE VARIOS ARCHIVOS

El IDE Visual Studio(C# y VB) solo se puede crear ensamblados de un solo archivo. Para crear ensamblados de múltiples archivos se debe utilizar compiladores de línea de comandos o VS con Visual C++.

```shell
csc /t:module Stringer.cs
```

[Documentación](https://docs.microsoft.com/es-es/dotnet/framework/app-domains/assemblies-in-the-common-language-runtime)



