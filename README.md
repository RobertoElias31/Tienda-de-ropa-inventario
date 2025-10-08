# Tienda-de-ropa-inventario
Roberto elias
# 🧾 Sistema de Gestión de Ventas de Ropa en C

Este programa en **lenguaje C** permite administrar un pequeño sistema
de inventario y ventas de prendas de ropa.\
Incluye funcionalidades para registrar prendas, modificarlas, buscarlas,
registrar ventas y aplicar descuentos a clientes frecuentes.

------------------------------------------------------------------------

## 🧩 Características principales

-   **Registro de inventario:** Permite ingresar nuevas prendas con su
    tipo, talla, color y costo.\
-   **Modificación:** Se pueden actualizar los datos de las prendas
    existentes.\
-   **Búsqueda avanzada:** Filtra prendas por tipo, talla o color.\
-   **Registro de compras:** Cada venta se asocia a un cliente y se
    almacena automáticamente con fecha y hora.\
-   **Descuentos automáticos:**
    -   5% por cada compra realizada previamente.\
    -   Descuento máximo acumulado: **25%**.\
-   **Gestión de clientes:** Se lleva un conteo de cuántas compras ha
    realizado cada cliente.

------------------------------------------------------------------------

## ⚙️ Estructura del programa

El código utiliza tres estructuras (`struct`):

``` c
typedef struct {
    char tipo[30];
    char talla[5];
    char color[20];
    float costo;
} Prenda;

typedef struct {
    char nombreCliente[50];
    Prenda prendas[10];
    int cantidad;
    float montoNeto;
    float descuento;
    char fechaHora[20];
} Compra;

typedef struct {
    char nombre[50];
    int comprasRealizadas;
} Cliente;
```

------------------------------------------------------------------------

## 🧠 Funcionalidades principales

  -----------------------------------------------------------------------
  Función                       Descripción
  ----------------------------- -----------------------------------------
  `guardarInventario()`         Permite ingresar nuevas prendas al
                                inventario.

  `modificarInventario()`       Modifica los datos de una prenda
                                existente.

  `buscarInventario()`          Busca prendas según filtros de tipo,
                                talla o color.

  `obtenerDescuento()`          Calcula el descuento según compras
                                previas del cliente.

  `aplicarDescuentos()`         Muestra los descuentos actuales por
                                cliente.

  `guardarCompra()`             Registra una compra y actualiza clientes
                                y descuentos.

  `estacionVenta()`             Permite realizar una venta completa y
                                elimina prendas vendidas del inventario.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🖥️ Menú principal

Al ejecutar el programa, se muestra el siguiente menú:

    --- Menú ---
    1. Guardar inventario
    2. Modificar inventario
    3. Buscar en inventario
    4. Mostrar descuentos
    5. (Guardar compras: se hace automáticamente en opción 6)
    6. Estación de venta
    0. Salir

------------------------------------------------------------------------

## 🧮 Ejemplo de uso

1.  Registrar prendas nuevas (opción 1).\
2.  Buscar o modificar prendas (opciones 2 y 3).\
3.  Registrar una venta (opción 6).\
4.  Visualizar descuentos acumulados (opción 4).

------------------------------------------------------------------------

## 🧰 Compilación y ejecución

Para compilar el programa desde consola:

``` bash
gcc gestion_ropa.c -o gestion_ropa
```

Para ejecutar:

``` bash
./gestion_ropa
```

------------------------------------------------------------------------

## 🗂️ Archivos

  Archivo            Descripción
  ------------------ -----------------------------------------
  `gestion_ropa.c`   Código fuente principal del programa.
  `README.md`        Documento de descripción y guía de uso.

------------------------------------------------------------------------

## 👨‍💻 Autor

Desarrollado por **Robert E.**\
Lenguaje: **C estándar (C99 o superior)**\
Última actualización: **2025**

------------------------------------------------------------------------

## 🧾 Licencia

Este proyecto es de uso educativo.\
Puedes modificarlo o adaptarlo libremente, citando al autor original.
