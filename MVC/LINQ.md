Ejemplo 01

``` c#
var result = Employee.GetAllEmployees().Join(Departament.GetAllDepataments()
                , e => e.DepartamentID
                , d => d.ID
                , (employee, departament) => new 
                   { EmployeeID = employee.ID
                   , EmployeeName = employee.Name
                   , DepartamentName = departament.Name });

var result = from e in Employee.GetAllEmployees()
                join d in Departament.GetAllDepataments()
                 on e.DepartamentID equals d.ID
                 select new { EmployeeName = e.Name, DepartamentName = d.Name, EmployeeID = e.ID };
foreach (var employee in result)
{
Console.WriteLine($"{employee.EmployeeID}.-{employee.EmployeeName }-{employee.DepartamentName}");
}
```

### GROUPED JOINS

Los group join son utiles para producir estructura de datos jerarquica.Relaciona cade elemento de la primera colección con un conjunto de elementos a los que esta correlacionado de la segunda colección.

NOTA: Dentro del resultado siempre estan todos los elementos de la primera colección, independientemente de si se encuentre elementos correlacionados en la segunda colección. En el caso de no encontrar elementos correlacionados el elemento estaría vacio. El selector de resultados de una combinación no agrupada, no tiene acceso a los elementos de la primera colección que no tienen ninguna coincidencia en la segunda colección.

### CONSULTA

Una consulta es un conjunto de instrucciones que describen los datos que se recuperarán de uno o varios origenes de datos determinados y que se organizan para obtener un resultado. 

La aplicación siempre ve los datos de origen como una colección IEnumerable<T> o IQueryable<T>   