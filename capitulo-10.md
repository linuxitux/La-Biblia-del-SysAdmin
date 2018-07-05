## Capítulo 10: Promoción, ética y aprendizaje

Este capítulo final trata sobre algunos aspectos no estrictamente relacionados
con lo técnico, pero si con lo profesional.

### Promoción, ética y aprendizaje

#### Promoción de GNU/Linux

* ¿Debe un Administrador GNU/Linux promocionar el uso de nuestro sistema
  favorito?
    * Hasta un cierto punto.
        * Aunque si es importante dar a conocer la filosofía del software libre.
            * Sin ser un fundamentalista del software libre.
    * Un SysAdmin debe promocionar el uso de la herramienta adecuada para cada
      tarea...
        * ...y conocer y aprender la herramienta adecuada para cada tarea en
          particular. Incluso si resulta ser Windows.
    * No caer en la tentación de "convertir" usuarios.
        * Cada sistema de cada usuario/colega/amigo/familiar convertido a
          GNU/Linux pasará a ser automáticamente nuestra responsabilidad.
        * Un SysAdmin suele estar lo suficientemente ocupado como para hacerse
          cargo de problemas adicionales en su (poco) tiempo libre.
        * Como dice Paul McCartney: *"live and let die"*.

### Aprendiendo Administración

* La mejor forma de aprender administración es haciendo administración.
* Es más probable que se aprenda más cuando algo falla.
* Escuchar y consultar (bombardear a preguntas) al viejo SysAdmin.
    * Generalmente los viejos SysAdmins son ávidos para compartir conocimiento.
      Sólo hace falta interrogarlos e interesarse por su trabajo.

### Estar en contacto con nuestros colegas

* Estar al día de las últimas tendencias en cuanto a tecnología.
    * ¿Qué mejoras incorporan las nuevas versiones de los
      productos/sistemas/aplicaciones que utilizamos?
    * ¿Existen soluciones innovadores o cambios en la industria que aún no hemos
      adoptado?
        * Virtualización para aprovechar mejor nuestro hardware.
        * Cloud computing (IaaS/SaaS/PaaS) en lugar de nuestra propia
          infraestructura (*on premises*).

        ![On premises](images/on_premises.jpg)

        * Soluciones híbridas.
    * ¿Existen nuevas alternativas de software para proveer servicios?
        * [LDAP](https://www.linuxito.com/gnu-linux/nivel-alto/998-como-montar-un-servidor-ldap-en-linux)
          en lugar de NIS.
        * [Samba](https://www.linuxito.com/gnu-linux/nivel-medio/432-como-instalar-y-configurar-samba-en-centos-7-con-acceso-anonimo)
          en lugar de CIFS.
        * [Nginx](https://www.linuxito.com/gnu-linux/nivel-alto/573-instalacion-y-configuracion-de-nginx-con-php-fpm)
          en lugar de Apache.
        * Cualquier cosa (?) en lugar de PHP.
* ¿Qué tecnologías usan en otras empresas o instituciones?
* ¿Estamos atrasados en algún aspecto? ¿Qué se puede cambiar o mejorar?
    * Ya sea para dar un mejor servicio como para simplificar la administración.
* ¿Existen nuevas metodologías de trabajo?
    * [Software de backup](https://www.linuxito.com/gnu-linux/nivel-alto/770-como-instalar-y-configurar-bacula-en-debian)
      vs. mis propios scripts.
    * [Software de automatización](https://www.linuxito.com/gnu-linux/nivel-alto/938-como-instalar-ansible-desde-los-fuentes)
      vs. mis propios scripts.
    * [Contenedores](https://www.linuxito.com/nix/832-jails-en-freebsd) vs.
      máquinas virtuales.

#### Ética laboral y licencias

* Un SysAdmin jamás debe utilizar ni permitir el uso de software pirata.
    * Al ser quien gestiona el software, es el responsable por respetar las
      licencias de software.
    * Si un usuario desea utilizar cierto software propietario, se deberá
      adquirir la licencia en caso que corresponda.
        * De lo contrario no se podrá utilizar dicho software.
    * Más allá de adquirir una licencia se deberán respetar los términos de la
      misma.
        * Un usuario adquiere una licencia para un equipo pero desea utilizarla
          en varios, violando los términos de la misma.
    * Un usuario posee copias de software pirata (ya sea instalado o copias de
      los instaladores) en sistemas bajo nuestra órbita.
* Por otro lado se debe garantizar que los datos alojados en nuestro servidores
  no estén sujetos a copyright.
    * Un usuario tiene cientos de archivos MP3 o películas pirata en uno de
      nuestros servidores de archivos (Samba, [NFS](https://www.linuxito.com/gnu-linux/nivel-alto/496-configuracion-de-nfs-en-freebsd))
      o soluciones de almacenamiento en la nube ([Nextcloud](https://www.linuxito.com/cloud/912-instalando-un-servidor-nextcloud-sobre-nginx-con-php-fpm-y-postgres)).
    * Lo mismo ocurre para archivos PDF o EPUB (copias de libros pirata).
* Desde el punto de vista de la ética profesional, siempre se deberá mantener
  dentro de la ley.
    * Un Jefe o Gerente desea acceder a la casilla de correo de un usuario.
        * Más allá de lo que puedan decir los términos de uso de los sistemas de
          la compañía, acceder a una cuenta de correo electrónico es ilegal en
          la mayoría de los países.
        * Lo mismo podría ocurrir para otro tipo de solicitudes similares.
        * Siempre estar al tanto de las cuestiones legales que afectan nuestro
          trabajo.
    * Como SysAdmin uno tiene naturalmente acceso a todas las cuentas de correo,
      mensajes, archivos y bases de datos de la compañía.
        * Tener acceso como root/Administrator nos permite (valga la
          redundancia) acceder a absolutamente todos los datos de la compañía.
        * Jamás utilizar esto a nuestro favor, en perjuicio de otros, o
          simplemente para curiosear.
        * Más allá de ser poco ético, en la mayoría de los casos se nos puede
          acusar de espionaje.
        * Un SysAdmin jamás debe cruzar esa barrera, bajo ninguna circunstancia,
          ya sea para beneficio propio o por una solicitud "de más arriba".
            * En tal caso siempre es mejor renunciar que tener una mala
              reputación y convertirse en un mal profesional y persona. O peor
              aún "quedar pegado" en un proceso judicial.
    * Un SysAdmin debe ser absolutamente responsable con las credenciales y
      roles que genera y/o le son otorgados.

De esta forma concluye esta Biblia del SysAdmin (con el perdón de la blasfemia
para los creyentes) sin descartar la posibilidad de agregar anexos en un futuro
(en el caso de que sea necesario).

Y por qué no también una versión en formato EPUB para los E-Readers...

Esta Biblia del SysAdmin queda [disponible públicamente en GitHub](https://github.com/linuxitux/La-Biblia-del-SysAdmin/)
y abierta a sugerencias, cambios y correcciones. Al mismo tiempo es liberada
bajo la [licencia MIT](LICENSE).

Se encuentra disponible para su descarga una versión en formato PDF.
