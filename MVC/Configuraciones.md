## CONFIGURATION IN ASP.NET CORE

El API de configuración provee una alternativa para realizar una configuración en ASP.NET core basado en una lista de pares valor-llave. El archivo de configuración es leido en tiempo de ejecución (Runtime) desde multiple fuentes. La lista de pares valor-llave puede ser agrupado en una herencia multinivel.

### Proveedores de configuracion

1. Formatos de archivos (INI, JSON, XML)

2. Argumentos de linea de comandos

3. Variables de entorno

4. Objetos .NET en memoria

5. Gestor de almacenamiento secreto sin cifrar

6. Almacenamiento de usuario cifrado, como Azure Key Vault

7. Proveedores personalizados

NUGET [Microsoft.Extensions.Configuration]

```c#
var builder = new ConfigurationBuilder()
    			.SetBasePath(Directory.GetCurrentDirectory())
            	 .AddJsonFile("appsettings.json");
Configuration = builder.Build();
Console.WriteLine($"option1={Configuration["option1"]}");
Console.WriteLine($"suboption1={Configuration["subsection:suboption1"]}");
Console.WriteLine($"{Configuration["wizards:0:name"]}");
```

[core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging/?view=aspnetcore-2.1&tabs=aspnetcore2x)

[core2](https://docs.microsoft.com/es-es/aspnet/core/fundamentals/configuration/index?tabs=basicconfiguration)







