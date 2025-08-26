"# Flutter" 
Codigo de ejercicio 1 
```
class Vehiculo {
  String marca;
  String modelo;
  int fabricacion;

  Vehiculo(this.marca, this.modelo, this.fabricacion);
  
  void mostrar() {
    print("Marca: $marca, Modelo: $modelo, Año: $fabricacion");
  }
}

class Auto extends Vehiculo {
  String combustible;
  Auto(String marca, String modelo, int fabricacion, this.combustible)
      : super(marca, modelo, fabricacion);
  
  @override
  void mostrar() {
    print("Marca: $marca, Modelo: $modelo, Año: $fabricacion, Combustible: $combustible");
  }
}

void main() {
  Vehiculo vehiculo = Vehiculo("Toyota", "Corolla", 2018);
  vehiculo.mostrar();
  
  Auto auto = Auto("Ford", "Mustang", 2022, "Gasolina");
  auto.mostrar();
}
```
Ejercicio 2 

```
class Vehiculo {
  String marca;
  String modelo;
  int fabricacion;

  Vehiculo(this.marca, this.modelo, this.fabricacion);
  
  void mostrar() {
    print("Marca: $marca, Modelo: $modelo, Año: $fabricacion");
  }
}

class Auto extends Vehiculo {
  String combustible;

  Auto(String marca, String modelo, int fabricacion, this.combustible)
      : super(marca, modelo, fabricacion);

  Auto.electrico(String marca, String modelo, int fabricacion)
      : combustible = "Eléctrico",
        super(marca, modelo, fabricacion);
  
  @override
  void mostrar() {
    print("Marca: $marca, Modelo: $modelo, Año: $fabricacion, Combustible: $combustible");
  }
}

void main() {
  Vehiculo vehiculo = Vehiculo("Toyota", "Corolla", 2018);
  vehiculo.mostrar();
  
  Auto auto = Auto("Ford", "Mustang", 2022, "Gasolina");
  auto.mostrar();

  Auto autoElectrico = Auto.electrico("Tesla", "Model 3", 2023);
  autoElectrico.mostrar();
}

```



