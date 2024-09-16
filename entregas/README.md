# LeerCSVKotlin
Esta aplicacion nos permite el uso y la conversion de un fichero de entrada y poder generarlo como otro tipo de fichero
Esta aplicacion permite la conversion en ese caso de un arcghivo jar a un archivo .csv, .json y .xml
Por desgracia , la conversion a archivos json no esta terminada todavia y puede sufrir errores que se pueden actualizar a futuro

Arquitectura de la Aplicación
Interfaz de Usuario (Consola):

Entrada: La aplicación acepta argumentos desde la línea de comandos para los archivos de entrada y salida.
Salida: La aplicación imprime mensajes en la consola, como errores o confirmaciones de generación de archivos.
Módulo de Lectura y Procesamiento de Datos:

Lectura de CSV: Usa la función leerCSV para leer datos de un archivo CSV. La función carga datos desde el archivo resources dentro del JAR y convierte las filas en objetos Tenista.
Transformación de Datos: Convierte los datos leídos en objetos de la clase Tenista.
Módulo de Persistencia:

Base de Datos: Utiliza DatabaseManager para manejar la base de datos SQLite, incluyendo la creación de tablas y la inserción de datos.
Consultas SQL: Incluye consultas SQL para obtener información de los tenistas.
Módulo de Generación de Archivos:

Generación de CSV: Usa la biblioteca OpenCSV para generar archivos CSV.
Generación de JSON: Usa la biblioteca Kotlinx.serialization para generar archivos JSON.
Generación de XML: Usa la biblioteca SimpleXML para generar archivos XML.
Configuración y Ejecución:

Archivo JAR: La aplicación se empaqueta en un archivo JAR que se puede ejecutar desde la línea de comandos.
Argumentos de Línea de Comandos: El archivo JAR acepta argumentos para el archivo de entrada CSV y el archivo de salida (con extensión .csv, .json o .xml).




Los 5 principios solid 
1-Principio de Responsabilidad Única
2-Principio de Abierto/Cerrado
3-Principio de Sustitución de Liskov
4-Principio de Segregación de Interfaces
5-Principio de Inversión de Dependencias



Como ejemplo tengo que añadir que en esta imagen se ve detalladamente que en vz de crear un servicio tengo un propio manager de la base datos, haciendo mas flexible su uso
![image](https://github.com/user-attachments/assets/c3604815-fae2-4f95-bdd6-9658fa058903)


Las librerias que han sido tanto para el uso y el manejo de los ficheros de json , xml y csv para asi poder convertirlos una vez hagan contacto con el jara para asi poder generarlos, asi como serializarlo en caso del xml
