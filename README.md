# 🚗 Concesionaria - Sistema de Gestión de Vehículos

Proyecto Java orientado a objetos que simula el catálogo y gestión de vehículos de una concesionaria. Permite cargar, buscar, ordenar y reportar autos y motos.

---

## 📁 Estructura del Proyecto

```
src/
└── ar/com/centro8/java/concesionaria/
    ├── entidades/
    │   ├── Vehiculo.java       # Clase abstracta base
    │   ├── Auto.java           # Subclase para automóviles
    │   └── Moto.java           # Subclase para motocicletas
    ├── interfaces/
    │   └── IServicio.java      # Contrato de servicios
    └── tests/
        └── TestConcesionaria.java  # Clase principal y pruebas
```

---

## 🧱 Modelo de Clases

### `Vehiculo` (abstracta)
Clase base que implementa `Comparable<Vehiculo>`. Contiene los atributos comunes a todos los vehículos.

| Atributo | Tipo     | Descripción          |
|----------|----------|----------------------|
| marca    | `String` | Marca del vehículo   |
| modelo   | `String` | Modelo del vehículo  |
| precio   | `Double` | Precio en pesos      |

El orden natural está definido por: **marca → modelo → precio**.

---

### `Auto` extiende `Vehiculo`

| Atributo | Tipo  | Descripción              |
|----------|-------|--------------------------|
| puertas  | `int` | Cantidad de puertas      |

---

### `Moto` extiende `Vehiculo`

| Atributo   | Tipo  | Descripción              |
|------------|-------|--------------------------|
| cilindrada | `int` | Cilindrada en centímetros cúbicos |

---

## 🔌 Interfaz `IServicio`

Define el contrato de operaciones disponibles sobre el arreglo de vehículos:

| Método | Descripción |
|--------|-------------|
| `cargarVehiculos()` | Inicializa y retorna el arreglo de vehículos |
| `buscarMasCaro(vehiculos[])` | Retorna el vehículo de mayor precio |
| `buscarMasBarato(vehiculos[])` | Retorna el vehículo de menor precio |
| `buscarPorLetraEnModelo(vehiculos[], char)` | Retorna el primer vehículo cuyo modelo contiene la letra indicada |
| `or3nP5oFahNL86vESFrkKjmuupsQa1mPzN7(vehiculos[])` | Ordena los vehículos por precio de **mayor a menor** |
| `ordenarPorOrdenNatural(vehiculos[])` | Ordena por orden natural: marca → modelo → precio |
| `generarReporte(vehiculos[])` | Imprime el reporte completo en consola |

---

## ▶️ Ejecución

La clase principal es `TestConcesionaria`. Al ejecutarse, genera automáticamente un reporte en consola con la siguiente información:

1. Listado completo de vehículos cargados
2. Vehículo más caro y más barato
3. Primer vehículo cuyo modelo contiene la letra `'Y'`
4. Vehículos ordenados por precio (mayor a menor)
5. Vehículos ordenados por orden natural (marca, modelo, precio)

### Vehículos de prueba precargados

| # | Tipo | Marca   | Modelo | Precio       | Detalle     |
|---|------|---------|--------|--------------|-------------|
| 0 | Auto | Peugeot | 206    | $200.000,00  | 4 puertas   |
| 1 | Moto | Honda   | Titan  | $60.000,00   | 125 cc      |
| 2 | Auto | Peugeot | 208    | $250.000,00  | 5 puertas   |
| 3 | Moto | Yamaha  | YBR    | $80.500,50   | 160 cc      |

---

## 🛠️ Tecnologías y Dependencias

- **Java** 
- **Lombok** 
- **Maven** 

