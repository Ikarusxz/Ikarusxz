<?php
// Ejemplo en PHP que distingue variables escalares y compuestas

// Variables escalares: 
// Son variables que contienen un solo valor. 
// Tipos de datos: entero, flotante, cadena, booleano

// Variable escalar de tipo entero
$numero_de_productos = 5; // Cantidad de productos comprados

// Variable escalar de tipo flotante
$precio_unitario = 199.99; // Precio de cada producto

// Variable escalar de tipo cadena
$nombre_cliente = "Juan Pérez"; // Nombre del cliente

// Variable escalar de tipo booleano
$es_miembro = true; // Indica si el cliente es miembro (true) o no (false)


// Variables compuestas: 
// Son variables que pueden contener múltiples valores o estructuras complejas. 
// Tipos de datos: array, objeto

// Variable compuesta de tipo array
$lista_de_productos = array("Laptop", "Mouse", "Teclado"); // Lista de productos comprados

// Acceder a elementos del array
echo "Producto 1: " . $lista_de_productos[0] . "\n"; // Accede al primer producto de la lista

// Variable compuesta de tipo array asociativo
$detalles_cliente = array(
    "nombre" => "Juan Pérez",
    "direccion" => "Calle Falsa 123",
    "correo" => "juan.perez@example.com"
);

// Acceder a valores del array asociativo
echo "Nombre del cliente: " . $detalles_cliente["nombre"] . "\n"; // Muestra el nombre del cliente

// Variable compuesta de tipo objeto
class Producto {
    public $nombre;
    public $precio;
    
    function __construct($nombre, $precio) {
        $this->nombre = $nombre;
        $this->precio = $precio;
    }
}

// Crear una instancia de la clase Producto
$producto1 = new Producto("Laptop", 999.99);

// Acceder a las propiedades del objeto
echo "Producto: " . $producto1->nombre . "\n"; // Muestra el nombre del producto
echo "Precio: $" . $producto1->precio . "\n";  // Muestra el precio del producto
?>
