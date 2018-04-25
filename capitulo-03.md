## Capítulo 3: La eficiencia importa

Este tercer capítulo trata acerca de la eficiencia, una de las calidades del
software a la que se le debe rendir tributo.

### La eficiencia importa

* Las tecnologías de proxies, cachés o mirrors pueden reducir el uso de ancho de
  banda en instalaciones a través de Internet y en general.
* Evitar instalaciones manuales a gran escala.
    * Utilizar el [clonado](https://www.linuxito.com/gnu-linux/nivel-alto/165-como-clonar-maquinas-virtuales-kvm)
      de sistemas siempre que sea posible.
    * Crear y mantener plantillas de sistemas y aplicaciones.
* Optimizar el uso de recursos: memoria, CPU, discos, procesos, etc.
    * Esto es de vital importancia cuando se utilizan tecnologías [cloud](https://www.linuxito.com/15-miscelaneo/642-curso-de-cloud-computing-online-gratuito-y-acreditado)
      en modo de pago por uso.
    * Aunque se cuente con exceso de recursos, se debe optimizar el uso de los
      mismos para contemplar todos los aspectos y escenarios posibles: picos de
      carga, tiempos de respuesta, espacio para [backups](https://www.linuxito.com/nix/711-la-biblia-del-sysadmin-capitulo-2-lo-dificil-seguridad-y-backups),
      crecimiento y escalabilidad de los datos a lo largo del tiempo.
* Automatizar absolutamente todas las tareas que sean rutinarias o repetitivas
  (este punto abarca todo un capítulo en sí mismo).
* Pensar en grande (tener la escalabilidad en mente en todo momento).
    * La eficiencia es la madre de la escalabilidad: ningún sistema ineficiente
      puede escalar bien.
* Optimizar el uso del tiempo.
    * Saber distinguir cuándo una tarea tiene el potencial de ser rutinaria o
      repetitiva para invertir tiempo en su [automatización](https://www.linuxito.com/gnu-linux/nivel-alto/662-updatemyfarm-script-bash-para-actualizar-todos-mis-servidores-en-paralelo).
        * Fallar en este aspecto puede provocar que se pierda tiempo
          automatizando una tarea que no es rutinaria ni repetitiva.
* Documentar es ganar tiempo.
    * Dejar de lado el [primer mandamiento](https://www.linuxito.com/nix/710-la-biblia-del-sysadmin-capitulo-1-documentacion)
      es garantía de desperdiciar considerables cantidades de tiempo a corto,
      mediano y largo plazo.
* Planificar el uso del tiempo.
    * Crear TODO lists.
    * Asignar prioridades (y recalcular siempre que sea necesario).
    * Aprender a postergar solicitudes que tengan baja o nula prioridad (un
      ejemplo es el típico escenario en el cual un usuario pide ayuda por un
      ratón defectuoso, en el preciso momento en el que estamos migrando a una
      nueva versión de una aplicación crítica en producción).
    * Combatir la procrastinación (consultar a un [experto en la materia](http://waitbutwhy.com/2013/11/how-to-beat-procrastination.html).

![Gestión del tiempo](images/gestion-tiempo.png)

### Referencias

* [Joe Chung - General SysAdmin Principles &amp; Guidelines](http://rockhopper.monmouth.edu/cs/jchung/cs471/cs_471_-_general_sysadmin_principles)

