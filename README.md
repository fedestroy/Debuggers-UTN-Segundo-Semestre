# 🧩 Trabajo Práctico Integrador – Sistema de Gestión (Java)
UTN Debuggers - Programacion II.

## 📘 Descripción general
Este proyecto consiste en el desarrollo de un **Sistema de Gestión integral** realizado en **Java**, con enfoque en la **Programación Orientada a Objetos (POO)**.  
Su objetivo es aplicar los principios de diseño modular, encapsulamiento, clases, objetos, herencia y uso de menús interactivos con `JOptionPane`.

El sistema simula una pequeña aplicación de gestión para una empresa, abarcando las áreas de:
- Clientes
- Proveedores
- Empleados
- Productos y stock
- Ventas (motor e interfaz)

---

## 🏗️ Estructura del proyecto

El sistema se divide en **8 módulos** principales, desarrollados por diferentes integrantes del equipo:

| Nº | Módulo | Descripción | Entregable |
|----|---------|--------------|-------------|
| 1 | **Arquitectura y Base de Datos** | Diseño del proyecto base, estructura de carpetas, creación del script SQL (opcional, se simula en memoria). | Esqueleto funcional + Script SQL básico |
| 2 | **Gestión de Clientes** | Alta, baja, modificación y listado de clientes. | Submenú ABM Clientes funcional |
| 3 | **Gestión de Proveedores** | ABM de proveedores. | Submenú ABM Proveedores funcional |
| 4 | **Gestión de Empleados** 🧑‍💼 *(Fede)* | Creación de la clase `Empleado`. Alta, baja, modificación y listado de empleados. | Submenú de Empleados funcional |
| 5 | **Gestión de Productos** | Creación de la clase `Producto`. ABM básico. | Funcionalidad de alta, baja y modificación |
| 6 | **Stock y Reportes de Productos** 📦 *(Fede)* | Control de stock, listados de precios y stock, lógica de negocio extendida del módulo de productos. | Funcionalidad de reportes y control de stock |
| 7 | **Motor de Ventas (Back-end)** | Lógica de venta, actualización de stock, cálculos. | Backend funcional de ventas |
| 8 | **Interfaz de Ventas (Front-end)** | Interfaz de usuario (por consola o `JOptionPane`) para realizar ventas. | Frontend funcional |

---

## 🧱 Estructura de paquetes (packages)

El código está organizado en **paquetes** para mantener un diseño modular:

src/
│
├── Main/ → Contiene la clase principal del sistema (menú general)
│ └── Main.java
│
├── gestionempleados/ → Módulo 4: Gestión de empleados
│ ├── Empleado.java
│ ├── EmpleadoData.java
│ └── MenuEmpleados.java
│
├── gestionproductos/ → Módulo 6: Productos y stock
│ ├── Producto.java
│ ├── Stock.java
│ ├── ProductoData.java
│ └── StockManagement.java
│
└── (otros paquetes) → Clientes, proveedores, ventas, etc.

yaml
Copiar código

---

## ⚙️ Funcionamiento del programa

### 🔹 Menú principal (`Main.java`)

Al ejecutar el programa, se muestra un menú principal por consola o `JOptionPane`:

=== MENU PRINCIPAL ===

Gestión de Empleados

Gestión de Productos y Stock

Salir

markdown
Copiar código

Dependiendo de la opción elegida:
- Se abre el **submenú de empleados** (`MenuEmpleados`)
- O el **submenú de productos y stock** (`StockManagement`)

---

### 🧑‍💼 Módulo de Empleados (Módulo 4)

Clase principal: `EmpleadoData.java`

#### Funcionalidades:
- **Alta** de empleados → pide datos por `JOptionPane` y los guarda en una lista en memoria.
- **Listado** de empleados → muestra todos los registros cargados.
- **Modificación** → permite actualizar datos de un empleado.
- **Baja lógica** → cambia el estado del empleado a inactivo, sin eliminarlo.

#### Atributos de la clase `Empleado`:
```java
IDEmpleado
NombreEmpleado
ApellidoEmpleado
Puesto
SueldoBase
Estado
(en esta versión simplificada se omiten otros datos como CUIL, fecha de ingreso, etc.)

🧩 Tecnologías utilizadas

Lenguaje: Java SE 17+

Entorno: NetBeans IDE

Interfaz: JOptionPane (para entrada/salida de datos)

Estructuras de datos: ArrayList

Paradigma: Programación Orientada a Objetos

Base de datos: simulada en memoria (sin conexión real, opcional script SQL)

🧠 Conceptos aplicados

Clases y objetos

Constructores y métodos

Encapsulamiento

Listas (ArrayList)

Herencia (extendida en módulos de productos y stock)

Modularidad mediante paquetes

Interacción con usuario mediante JOptionPane

💾 Ejecución

Abrir el proyecto en NetBeans.

Verificar que los paquetes estén correctamente creados:
gestionempleados, gestionproductos, y Main.

Ejecutar el archivo Main.java.

Seguir las opciones del menú para navegar entre módulos.

🚀 Próximos pasos (mejoras futuras)

Integrar persistencia real con JDBC y MySQL.

Crear una interfaz gráfica con JavaFX o Swing.

Incorporar reportes PDF o Excel para los listados.

Añadir validaciones de entrada más robustas.

Implementar autenticación de usuarios.

🏁 Estado del proyecto

✅ En desarrollo funcional
🔧 Base de datos simulada en memoria
🧱 Estructura modular completa
🎯 Enfoque educativo y didáctico (para práctica de POO en Java)

📅 Versión: 1.0
📍 Lenguaje: Java
