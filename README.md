# Acceso-a-datos

Práctica 1: Bases de Datos Orientadas a Objetos (AAD_UD4P01_BBDDOO)
Descripción
Este proyecto tiene como objetivo aplicar la persistencia de datos mediante una Base de Datos Orientada a Objetos (BDOO), usando la librería db4o integrada en una aplicación JAVA. Se trabajan buenas prácticas de programación evitando "hardcodes" y gestionando eficientemente los recursos.​

Objetivos
Practicar la persistencia de datos con BDOO desde JAVA.

Incorporar buenas prácticas de programación en la gestión de datos y recursos.​

Materiales y recursos
Ejercicios realizados en clase.

Ordenador del alumno/a.

Fichero de configuración de log: logback.xml.

IDE recomendado: Eclipse.

Librerías:

db4o.jar

logback-classic-1.4.11.jar

logback-core-1.4.11.jar

slf4j-api-2.0.7.jar.​

Actividad principal
Desarrolla una aplicación JAVA que permita:

Guardar, consultar, borrar y modificar una instancia de la clase Instituto en la BDOO db4o.

La clase Instituto incorpora: nombre del centro (texto), identificador (número) y una lista de alumnos matriculados.​

Estructura y requisitos de clases
Clase Instituto:
Atributos: nombre, id, lista de alumnos.

Métodos a implementar:

matricularAlumno(Alumno al): añade un alumno.

expulsarAlumno(Alumno al): elimina un alumno.

cambiarIdInstituto(int nuevoId): cambia el identificador.​

Clase Bbddoo:
Métodos requeridos:

guardarAlumno(Alumno al)

getTodosAlumnos(String nombreInstituto)

guardarInstituto(Instituto insti)

getInstituto(Instituto institutoBuscado)

borrarInstituto(Instituto institutoABorrar)

expulsarATodosAlumnos(String nombreInstituto) (borra transaccionalmente todos los alumnos de la BD)

consultaMatriculasInstituto(String idInstituto)

consultaInstiMatriculado(String nomAlumno).​

Nota sobre la base de datos
La base soporta operaciones en cascada, por ejemplo, al borrar un instituto se eliminan sus alumnos de forma transaccional usando la configuración:

text
db.ext().configure().objectClass(Instituto.class).cascadeOnDelete(true);
Pruébalo para verificar el funcionamiento en cascada.​

Entrega
La práctica no requiere entrega formal.​

Este README.md resume la estructura, objetivos, materiales, y los requisitos más relevantes de la práctica, ayudando a iniciar el desarrollo y manteniendo el foco en la gestión orientada a objeto en aplicaciones JAVA.
