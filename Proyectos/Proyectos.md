Estructuras de Datos
====================

Proyectos
---------

* [Proyecto 1](Proyectos/Proyecto 1), fecha de entrega: 26 de noviembre de 2021.
* [Proyecto 2](Proyectos/Proyecto 2), fecha de entrega: 7 de enero de 2022.
* [Proyecto 3](Proyectos/Proyecto 3), fecha de entrega: 28 de enero de 2022.

Formato de entrega
------------------

Los proyectos deben entregarse en un archivo `proyectoX.tar.gz` que contenga el
directorio `proyectoX` como raíz, dentro del cual esté un archivo `pom.xml` que
permita compilar el código, correr pruebas unitarias en el mismo (si aplica) y
generar un archivo Jar llamado `proyectoX.jar` al hacer:

```
$ mvn compile # compila el código
$ mvn test    # corre las pruebas unitarias (opcional)
$ mvn install # genera el archivo proyectoX.jar en el subdirectorio target
```

Con el archivo `proyectoX.jar` se ejecutará el programa al invocar:

```
$ java -jar target/proyectoX.jar
```

**Obviamente** `X` denota el número del proyecto. Los proyectos en general
requerirán argumentos extra en la línea de comandos.

Si no saben cómo crear el archivo `tar.gz`, investíguenlo; se puede hacer por la
línea de comandos en cualquier distribución de Linux.

El archivo `proyectoX.tar.gz` deben enviarlo adjuntado en un correo electrónico
dirigido **al profesor**; el correo debe tener el asunto: `“EDDProyecto X
Apellido Paterno Apellido Materno Nombre(s)”`. Nótese que `“EDDProyecto”` *no
contiene espacios*, pero que sí hay un espacio antes del número del proyecto.

Los proyectos deben cumplir todos estos requisitos o no serán aceptados y se
evaluarán con cero.
