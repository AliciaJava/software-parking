# Sistema de Gestión de Parking (Java)

Este programa simula el funcionamiento de un sistema de gestión de parking en **Java**. El parking es cuadrado y está representado en un array bidimensional de 10x10. Las columnas impares se recorren de abajo hacia arriba, mientras que las columnas pares se recorren de arriba hacia abajo. El sistema gestiona las plazas del parking, las entradas y salidas de vehículos, el saldo acumulado del día y más.

## Estructura del Parking

El parking se representa como una cuadrícula de 10x10, donde las plazas de aparcamiento se numeran de la siguiente manera:
	
 NOTA: Las flechas hacia abajo y arriba simulan el sentido de
	los carriles por los que circularían los coches. 
		
		//   1     20     21      .. .. .. .. .. ..  100 
		//   2  |  19     22  |   ..                  99
		//   3  ▼  18  ▲  23  ▼                       98
		//   4     17  |  24         ..               97
		//   5     16     25                          96
		//   6     15     25            ..            95
		//   7  |  14     27  |                       94
		//   8  ▼  13  ▲  28  ▼            ..         93
		//   9     12  |  29      ..          ..      92
		//  10     11     30      31 .. .. .. .. ..   91

  
### Recorridos de las columnas:
- Las **columnas pares** (2, 4, 6...) se recorren de **arriba a abajo**.
- Las **columnas impares** (1, 3, 5...) se recorren de **abajo hacia arriba**.

## Funciones Principales

### 1. **Entrada y salida de vehículos:**
   - El sistema permite registrar la **entrada** y la **salida** de vehículos, controlando las plazas ocupadas y libres.
   - Cuando un vehículo sale, la plaza se libera.

### 2. **Número de plazas disponibles:**
   - El sistema calcula el número de plazas libres y lo muestra en el cartel de entrada.
   - Si el parking está **completo** (sin plazas disponibles), se muestra un mensaje indicando que el parking está lleno.

### 3. **Estado del parking:**
   - Se puede **imprimir el estado** del parking, mostrando las plazas ocupadas, libres y el número de plazas disponibles.

### 4. **Saldo acumulado del día:**
   - Se almacena el **importe total cobrado** por el uso del parking durante el día.

### 5. **Lista de vehículos:**
   - Se mantiene una lista con los vehículos que están actualmente dentro del parking.
   - Se puede consultar esta lista en cualquier momento.

## Tipos de Vehículos

El sistema distingue entre los siguientes tipos de vehículos:
- **Coche**
- **Moto**
- **Furgoneta**
- **Autobús**

### Información de los vehículos:
- Se recopilan los datos del vehículo, que incluyen:
  - **Tipo de vehículo** (Coche, Moto, Furgoneta, Autobús)
  - **Placa de matrícula**
  - **Modelo**
  - **Marca**
  - Si es una **furgoneta**, se solicita la **longitud**.
  - Si es un **autobús**, se solicita el **número de plazas**.

### Formato de almacenamiento:
Los datos de los vehículos se almacenan en **mayúsculas** para garantizar uniformidad.

## Funciones adicionales

- **Plazas ocupadas/libres:**
  - El sistema mantiene un seguimiento de qué plazas están **ocupadas** y cuáles están **libres**.

- **Carta de precios:**
  - Los precios de las diferentes categorías de vehículos están definidos como constantes dentro del código.
  - A futuro, se podría mejorar este sistema utilizando un archivo de configuración (por ejemplo, un archivo de propiedades).

## Ejemplo de uso

```java
public class Main {
    public static void main(String[] args) {
        Parking parking = new Parking();

        Registrar entrada de vehículos
        parking.entrada("Coche", "ABC123", "Ford Fiesta");
        parking.entrada("Moto", "XYZ789", "Yamaha YZF-R1");

        Consultar el estado del parking
        parking.imprimirEstado();

        Ver número de plazas disponibles
        System.out.println(parking.plazasDisponibles());

        Consultar saldo acumulado del día
        System.out.println(parking.saldoAcumulado());
    }
}

Requerimientos
Lenguaje de programación: Java 8 o superior

Bibliotecas necesarias: Ninguna externa, solo bibliotecas estándar de Java.

Cómo ejecutar el proyecto
Clona este repositorio en tu máquina local.

Asegúrate de tener Java 8 o superior instalado.

Compila el proyecto con javac y ejecuta el archivo principal Main.java para iniciar el sistema de parking.

javac Main.java
java Main


### Detalles importantes:

1. **Requerimientos**: El archivo ahora menciona que el proyecto está hecho en **Java 8 o superior**.
2. **Ejemplo de código**: El ejemplo de uso es ahora en **Java**, usando clases y métodos típicos en este lenguaje.
3. **Ejecución**: La forma de ejecutar el programa se ha ajustado a cómo se compilan y ejecutan los programas Java desde la terminal.

Este `README.md` actualizado debe ser más adecuado para un proyecto en Java. ¡Espero que te ayude! Si necesitas alguna modificación o detalle adicional, no dudes en decírmelo.

  



