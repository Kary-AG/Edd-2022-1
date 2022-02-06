Estructuras de Datos
====================

Prácticas
---------

* [Práctica 1](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica1),
  fecha de entrega: 5 de octubre de 2021.
* [Práctica 2](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica2),
  fecha de entrega: 19 de octubre de 2021.
* [Práctica 3](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica3),
  fecha de entrega: 2 de noviembre de 2021.
* [Práctica 4](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica4),
  fecha de entrega: 16 de noviembre de 2021.
* [Práctica 5](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica5),
  fecha de entrega: 23 de noviembre de 2021.
* [Práctica 6](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica6),
  fecha de entrega: 7 de diciembre de 2021.
* [Práctica 7](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica7),
  fecha de entrega: 14 de diciembre de 2021.
* [Práctica 8](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica8),
  fecha de entrega: 11 de enero de 2022.
* [Práctica 9](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica9),
  fecha de entrega: 18 de enero de 2022.
* [Práctica 10](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica10),
  fecha de entrega: 25 de enero de 2022.
* [Práctica 11](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica11),
  fecha de entrega: 25 de enero de 2022.

Formato de entrega
------------------

Las prácticas estarán en el [grupo de repositorios Git del
curso](https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd). Los alumnos deberán
llevar a cabo los siguientes pasos para entregar sus prácticas:

* Clonar la práctica correspondiente:

    ```
    $ git clone https://aztlan.fciencias.unam.mx/gitlab/2022-1-edd/practica1.git
    Cloning into 'practica1'...
    remote: Counting objects: 42, done.
    remote: Compressing objects: 100% (25/25), done.
    remote: Total 42 (delta 4), reused 0 (delta 0)
    Unpacking objects: 100% (42/42), done.
    ```

* Crear una rama (**branch**) para desarrollo y mudarse (**checkout**) a ella:

    ```
    $ cd practica1
    $ git branch work
    $ git checkout work
    Switched to branch 'work'
    ```

* Completar las clases de la práctica hasta que todas las pruebas unitarias
  pasen; pueden (y de hecho recomendamos) realizar (**commit**) cambios a su
  repositorio local para ir preservando su avance durante la escritura de la
  práctica.

    ```
    $ mvn test
    ...
    [INFO] ------------------------------------------------------------------------
    [INFO] BUILD SUCCESS
    [INFO] ------------------------------------------------------------------------
    [INFO] Total time: 1.379 s
    [INFO] Finished at: 2021-08-21T00:08:13-06:00
    [INFO] Final Memory: 15M/209M
    [INFO] ------------------------------------------------------------------------
    $ git commit . -m "¡Ya me salió la práctica!"
    ```

* Generar el Jar de la práctica en el directorio `target/`:

    ```
    $ mvn install
    ```

* Probar el programa escrito en la práctica (la 1, por ejemplo):

    ```
    $ java -jar target/practica1.jar
    ```

  Algunas prácticas requerirán más parámetros para la línea de comandos.

* Generar un archivo diferencial o parche (**diff** o **patch**) con la rama
  principal; el nombre del archivo debe ser su número de cuenta con la extensión
  `.diff`.

    ```
    $ git diff main > ~/123456789.diff
    ```

* Limpiar su rama de trabajo (esto borra todo archivo no agregado al
  repositorio, incluyendo el Jar):

    ```
    $ git clean -x -f -d .
    ```

* Crear una rama de prueba a partir de la principal para probar su archivo
  diferencial:

    ```
    $ git checkout main
    $ git branch test
    $ git checkout test
    ```

* Aplicar su parche a la rama de prueba:

    ```
    $ patch -p1 < ~/123456789.diff
    ```

* Comprobar que todas las pruebas unitarias pasan:

    ```
    $ mvn test
    ...
    [INFO] ------------------------------------------------------------------------
    [INFO] BUILD SUCCESS
    [INFO] ------------------------------------------------------------------------
    [INFO] Total time: 0.851 s
    [INFO] Finished at: 2021-08-21T00:08:49-06:00
    [INFO] Final Memory: 10M/303M
    [INFO] ------------------------------------------------------------------------
    Total time: 0 seconds
    ```

* Ejecutar el programa de la práctica:

    ```
    $ mvn install
    $ java -jar target/practica1.jar
    ```

* Enviar el archivo diferencial al ayudante de laboratorio.
