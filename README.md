Semana 6: Creando jerarquías de clases con herencia simple

proyecto SalmonttApp

Objetivo de esta semana:
Implementar una jeracquia de clase utilizando herencia simple, organizando el proyecto en paquetes y utilizando instancias de diferentes tipos de unidades operativas
Ademas, se refuerza el uso de colecciones dinamicas, separaciones por capas y buena presentacion de datos en consola.

El sitema permite:
-organizacion modular del codigo mediante paquetes 
-uso de colecciones dinamicas (ArrayList)
-lectura de datos desde archivos externos (.txt)
-aplicacion de filtros y busquedas por localidad o estado
-validación basica de datos
-buena practica de empaquetamiento y estructuras del proyecto 
La aplicacion carga centros de cultivo desde un archivo de texto y muestra los resultados por consola segun las consultas realizadas

Paquetes y Clases Implementadas 
Paquete model 
UnidadOperativa 
Superclase que define atributos comunes (nombre, comuna)
CentroCultivo: 
Subclase que extiende UnidadOperativa
Atributos: id, capacidadtoneladas, estado
uso de super(...) y sobreescritura de toString()
PlantaProceso
Subclase que extiende UnidadOperativa
Atributos: id, capacidadProceso, toneladasProduccion
Uso de super(...) y sobreescritura de toString()

Paquete service Contiene la logica del sistema y manejo de datos CentroService:
Carga datos desde el archivo .txt
Procesa cada linea y crwa onjetos CentroCultivo
Mantiene y entrega la coleccion cargada

Paquete data 
Clase de apoyo o gestion de datos manuales
GestorUnidades
Llama a CentroService para cargar los centros desde archivo
Crea dos objetos de prueba de tipo PlantaProceso
Retorna una lista combinada de todas las unidades operativas 

Pauqete ui
Main 
Ejecuta el programa 
Llama al GestorUnidades
Muestra todoas las unidades operativas en formato ordenado 

Ejecucion del programa

1. Clonar el reprositorio: https://github.com/kolagosmorales-hash/Salmontt.App/blob/main/SalmonApp.zip
2. Verificar que el archivo data/centro.txt exista dentro del proyecto
3. Ejecutar la clase principal: src/app/Main.java
5. El sitema mostrara por consola
-Centros de cultivos cargado desde el archivo
-Plantas de proceso creadas manualmente
-Todas las unidades operativas con formato ordenado 
