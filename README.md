# Sistema de Gestión de Parking

**Sistema de Gestión de Parking** es una aplicación diseñada para simular la administración de un parking de vehículos. El sistema gestiona la entrada y salida de vehículos, visualiza el estado del parking, calcula el saldo acumulado del día y proporciona información detallada sobre los vehículos estacionados y las plazas disponibles.

## Características

- **Registro de Entrada y Salida de Vehículos**: Permite registrar la entrada y salida de vehículos del parking. 
- **Gestión de Tipos de Vehículos**: Identifica y clasifica los vehículos como **Coche**, **Moto**, **Furgoneta** o **Autobús**. 
- **Plazas Disponibles**: Permite consultar el número de plazas disponibles en el parking y verifica si el parking está completo.
- **Estado del Parking**: Imprime el estado actual de todas las plazas en el parking, indicando cuáles están ocupadas y cuáles están libres.
- **Saldo Acumulado**: Calcula y muestra el importe total recaudado por las tarifas de estacionamiento durante el día.
- **Listado de Vehículos**: Muestra un listado con los vehículos que actualmente están estacionados en el parking.

## Funcionalidades Detalladas

### 1. **Entrada de Vehículo**
   - Registra la entrada de un vehículo al parking.
   - Solicita los datos del vehículo (matrícula y tipo).
   - Si es una **furgoneta**, se solicita la longitud. 
   - Si es un **autobús**, se solicita el número de plazas.
   - Los datos se almacenan en **mayúsculas**.
   - Se asigna el vehículo a una plaza disponible en el parking y se actualiza el número de plazas disponibles.

### 2. **Salida de Vehículo**
   - Registra la salida de un vehículo del parking.
   - Calcula el importe basado en la tarifa del tipo de vehículo.
   - Actualiza el estado del parking y el número de plazas disponibles.

### 3. **Número de Plazas Disponibles**
   - Muestra el número total de plazas disponibles en el parking.
   - Si el número de plazas disponibles es 0, el parking se considera **COMPLETO**.

### 4. **Imprimir Estado del Parking**
   - Imprime el estado de todas las plazas en el parking.
   - Indica qué plazas están ocupadas y qué plazas están libres.

### 5. **Saldo Acumulado del Día**
   - Muestra el saldo total acumulado durante el día por los cobros de las tarifas de los vehículos que han salido del parking.

### 6. **Listado de Vehículos**
   - Muestra un listado de todos los vehículos que actualmente están estacionados en el parking.

## Tipos de Vehículos

El sistema admite los siguientes tipos de vehículos, cada uno con su tarifa correspondiente:

- **Coche**: Tarifa por hora: 5€
- **Moto**: Tarifa por hora: 3€
- **Furgoneta**: Tarifa por hora: 7€ (Se solicita la longitud de la furgoneta).
- **Autobús**: Tarifa por hora: 10€ (Se solicita el número de plazas del autobús).

## Representación del Parking

El parking es representado por un array bidimensional de 10x10, donde las columnas pares se recorren de **arriba a abajo** y las columnas impares de **abajo a arriba**. Cada plaza de estacionamiento puede estar **ocupada** por un vehículo o **libre**.

El estado del parking se visualiza de la siguiente manera:
	
NOTA: Las flechas hacia abajo y arriba simulan el sentido de los carriles por los que circularían los coches. 
		
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


## Requisitos

Antes de ejecutar el programa, asegúrate de tener los siguientes requisitos:

- **JDK 8 o superior**: [Descargar JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- **IDE Java** (Recomendado): Eclipse, IntelliJ IDEA, NetBeans, etc.

## Instalación

1. Clona el repositorio a tu máquina local:

   ```bash
   git clone https://github.com/usuario/sistema-parking.git

  Uso
Una vez que el proyecto esté ejecutándose, puedes interactuar con el sistema utilizando las siguientes opciones:

Entrada de Vehículo: Registra un vehículo ingresando la matrícula y el tipo. Si es una furgoneta, se pedirá la longitud; si es un autobús, el número de plazas.

Salida de Vehículo: Registra la salida de un vehículo, calcula el importe correspondiente según la tarifa, y actualiza el estado del parking.

Consultar Plazas Disponibles: Muestra cuántas plazas están libres en el parking.

Imprimir Estado del Parking: Imprime un resumen visual del estado de las plazas del parking, con información de las plazas ocupadas y libres.

Saldo Acumulado: Muestra el total recaudado por el parking durante el día.

Listado de Vehículos: Muestra un listado con todos los vehículos que están estacionados en el parking.

Contribuir
Las contribuciones al proyecto son bienvenidas. Para contribuir, sigue estos pasos:

Haz un fork del repositorio.

Crea una nueva rama para tus cambios:
git checkout -b feature/nueva-funcionalidad

Realiza los cambios y haz un commit:
git commit -am 'Agregada nueva funcionalidad'

Haz push a tu rama:
git push origin feature/nueva-funcionalidad

Abre un pull request describiendo los cambios realizados.

Licencia
Este proyecto está bajo la Licencia MIT - consulta el archivo LICENSE para más detalles.

Contacto
Si tienes alguna pregunta o necesitas soporte, puedes ponerte en contacto con el autor a través de [tu correo o enlace de contacto].


### Explicación de los elementos clave:

1. **Registro de Entrada y Salida**: Detalla cómo se gestionan las entradas y salidas de los vehículos, incluyendo el tratamiento de los tipos de vehículos especiales como furgonetas y autobuses.
2. **Plazas Disponibles y Estado del Parking**: Explica cómo se lleva un registro de las plazas disponibles y cómo se visualiza el estado del parking.
3. **Saldo Acumulado**: Indica cómo el sistema calcula y muestra el saldo acumulado del día por los cobros de los vehículos que han salido.
4. **Tipos de Vehículos y Tarifas**: Se explican las tarifas para cada tipo de vehículo y el procedimiento para la solicitud de información adicional en el caso de furgonetas y autobuses.
5. **Instalación y Uso**: Instrucciones claras sobre cómo instalar y ejecutar el proyecto.
6. **Contribuciones**: Instrucciones para quienes deseen contribuir al proyecto.

Este README proporciona toda la información necesaria para entender y usar el software de parking de manera efectiva.
