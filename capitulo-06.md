## Capítulo 6: Automatización y scripting

Sexto capítulo dedicado al scripting y automatización de tareas. Un buen
SysAdmin jamás debe repetir más de dos veces una misma tarea. Toda tarea que
requiera ser llevada a cabo más de una vez amerita ser automatizada.

![Uptime](images/automation.png)

*Imagen cortesía de [xkcd](https://xkcd.com/1319/) (CC BY-NC 2.5).*

### Automatización y scripting

Más allá del brillante cómic de [xkcd](https://xkcd.com/1319/), la metodología
de trabajo de un SysAdmin debería ser algo más o menos como lo siguiente. La
primera vez que se ejecuta una tarea, [se documenta con precisión](capitulo-01.md).
La segunda vez, se resuelve a partir de la documentación generada anteriormente
y al mismo tiempo se automatiza de la manera más [eficiente](capitulo-03.md)
posible. La tercera vez, se delega a un robot, es decir, se deja todo en manos
de la automatización.

* Aprender y utilizar de manera consistente al menos un lenguaje de scripting
  ([Bash](https://www.linuxito.com/buscar?q=bash), Perl, Python).
    * Utilizarlo de manera consistente ayuda a perfeccionarnos y sacarle el
      máximo provecho.
    * Dominar más de un lenguaje nos ayuda a comprender sus diferencias,
      similitudes y limitaciones, lo cual sirve para saber optar por la mejor
      solución para cada problema. al mismo tiempo, lenguajes interpretados
      como Python son más portables que Bash, lo cual nos permite atravesar
      fronteras en cuanto a sistemas operativos respecta.
    * Conocer y aprender la sintaxis básica de al menos un lenguaje específico
      de otra plataforma. Por ejemplo, si somos administradores de sistemas
      GNU/Linux, aprender lo básico sobre [PowerShell](https://es.wikipedia.org/wiki/Windows_PowerShell)
      o [WSH](https://es.wikipedia.org/wiki/Windows_Script_Host).
    * Sin embargo no conviene especializarse en un lenguaje que sea lo
      suficientemente obscuro e incomprensible para que sólo uno lo entienda y
      utilice.
* Salvo que nos guste demasiado tipear, crear aliases y [scripts](https://www.linuxito.com/buscar?q=script)
  cortos para reducir al máximo el uso de teclado. Incluso para las tareas tan
  triviales como ejecutar `apt-get update &amp;&amp; apt-get upgrade`:

  ```
  alias actualizar='apt-get update &amp;&amp; apt-get upgrade'
  ```

* Familiarizarse con el uso de la tecla `TAB` para auto-completar y el historial
  (`history`, `!`) de Bash/csh.
    * Aumentar el tamaño del historial (variables de entorno `HISTFILE` y
      `HISTFILESIZE`.
* Procesamiento automático/periódico/programado ([cron](https://www.linuxito.com/buscar?q=cron),
  `at`).
    * Escribir scripts para llevar a cabo tareas programadas o periódicas
      (`crontab`, `/etc/cron.*/`).
    * Entender el funcionamiento del entorno (`env`) y sus variables, al igual
      que del proceso de inicialización de una shell (Bash/csh).
    * Aprender a redirigir salidas estándar y de errores a archivos, y
      desarrollar scripts que lleven a cabo tareas desatendidas (no
      interactivas).
    * Conocer herramientas como `expect` para interactuar con procesos
      interactivos de manera desatendida.
    * Aprender a generar parámetros de manera dinámica con `xargs` y redirigir
      la entrada estándar (`&lt;`).
    * Testear y verificar el funcionamiento de los scripts ejecutados por `cron`
      como cualquier otro programa. Hacer uso del `syslog` para diagnosticar
      errores.
* Escribir scripts que sean escalables.
    * Esto permite que un script siga siendo útil a pesar de que se sigan
      agregando más y más sistemas a nuestra granja.
    * Aplica a cualquier solución de administración: pensar siempre en términos
      de escalabilidad. Una solución se vuelve cuanto más util a medida que
      aplica a más y más sistemas.
    * Dominar las técnicas de [paralelismo](https://www.linuxito.com/gnu-linux/nivel-alto/507-mejorando-mi-sistema-de-actualizacion-de-servidores),
      concurrencia y subprocesos al momento de crear scripts. Esto implica
      conocer los comandos embebidos en las shells, tales como `jobs`, `bg`,
      `fg`, `&amp;`, etc.

### Referencias

* [Joe Chung - General SysAdmin Principles &amp; Guidelines](http://rockhopper.monmouth.edu/cs/jchung/cs471/cs_471_-_general_sysadmin_principles)
