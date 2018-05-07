```c#
Product product = new Product();
dynamic dyne = new ExpandoObject();
dyne.nombre = "oscar";
dyne.edad = 23;
dyne.sueldo = 150.23;
product.algo = dyne;
dynamic algo = product.algo;
Console.WriteLine(algo.nombre);
Console.WriteLine(algo.edad);
Console.WriteLine(algo.sueldo);

    class Product
    {
        public string Name { get; set; }

        public DateTime ExpiryDate { get; set; }
        public decimal Price { get; set; }
        public string[] Sizes { get; set; }
        public dynamic algo { get; set; }
        public dynamic getAlgo()
        {
            return algo;
        }
    }
```

