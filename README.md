<?php
// Ejemplo de variables escalares
$nombre = "Juan"; // Cadena (string)
$edad = 30; // Entero (int)
$precio = 49.99; // Punto flotante (float)
$es_cliente_nuevo = true; // Booleano (bool)

// Ejemplo de variable compuesta (arreglo)
$productos = ["Laptop", "Mouse", "Teclado"]; // Arreglo (array)

// Imprimimos los valores
echo "Nombre: $nombre\n";
echo "Edad: $edad\n";
echo "Precio: $precio\n";
echo "¿Es cliente nuevo?: " . ($es_cliente_nuevo ? "Sí" : "No") . "\n";

// Imprimimos los productos
echo "Productos:\n";
foreach ($productos as $producto) {
    echo "- $producto\n";
}
?>
