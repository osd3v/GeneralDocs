Clase para permitir generar la cadena de conexión
Permite construir cadenas de conexión válidas en tiempo de ejecución
Cada proveedor de datos .NET Framework adminite una sintaxis diferente para las palabras claves de cadenas de conexión, lo que dificulta la construcción de cadenas de conexión válidas de forma manual. Los compiladores de cadenas de conexión es implementado por cada proveedor de datos, cada uno incluye una clase creadora de cadenas de conexión fuertemente tipadas que hereda de DbConnectionStringBuilder.

| Proveedor                | Clase ConnectionStringBuilder                          |
| ------------------------ | ------------------------------------------------------ |
| System.Data.SqlCliente   | System.Data.SqlClient.SqlConnectionStringBuilder       |
| System.Data.OleDb        | System.Data.OleDb.OleDbConnectionStringBuilder         |
| System.Data.Odbc         | System.Data.Odbc.OdbcConnectionStringBuilder           |
| System.Data.OracleClient | System.Data.OracleClient.OracleConnectionStringBuilder |

​	  



SqlConnectionStringBuilder

PROPIEDADES

* IntegratedSecurity
* DataSource : Servidor
* InitialCatalog : Base de datos



## ACCESO A ARCHIVOS DE CONFIGURACION

System.Configuration permite el acceso mediante programación a archivos de configuración que usan WebConfigurationManager en aplicaciones web y ConfigurationManager en aplicaciones Windows 