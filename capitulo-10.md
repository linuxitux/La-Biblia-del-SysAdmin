## Capítulo 10: Promoción, ética y aprendizaje

Este capítulo final trata sobre algunos aspectos no estrictamente relacionados
con lo técnico, pero si lo profesional.

### Promoción, ética y aprendizaje

<h4>Promoción de GNU/Linux</h4>

<ul>
<li>¿Debe un Administrador GNU/Linux promocionar el uso de nuestro sistema favorito?</li>
    <ul>
    <li>Hasta un cierto punto.</li>
        <ul>
        <li>Aunque si es importante dar a conocer la filosofía del software libre.</li>
            <ul>
            <li>Sin ser un fundamentalista del software libre.</li>
            </ul>
        </ul>
    <li>Un SysAdmin debe promocionar el uso de la herramienta adecuada para cada tarea...</li>
        <ul>
        <li>...y conocer y aprender la herramienta adecuada para cada tarea en particular. Incluso si resulta ser Windows.</li>
        </ul>
    <li>No caer en la tentación de "convertir" usuarios.</li>
        <ul>        
        <li>Cada sistema de cada usuario/colega/amigo/familiar convertido a GNU/Linux pasará a ser automáticamente nuestra responsabilidad.</li>
        <li>Un SysAdmin suele estar lo suficientemente ocupado como para hacerse cargo de problemas adicionales en su (poco) tiempo libre.</li>
        <li>Como dice Paul McCartney: <i>"live and let die"</i>.</li>
        </ul>
    </ul>
</ul>

<h4>Aprendiendo Administración</h4>

<ul>
<li>La mejor forma de aprender administración es haciendo administración.</li>
<li>Es más probable que se aprenda más cuando algo falla.</li>
<li>Escuchar y consultar (bombardear a preguntas) al viejo SysAdmin.</li>
    <ul>
    <li>Generalmente los viejos SysAdmins son ávidos para compartir conocimiento. Sólo hace falta interrogarlos e interesarse por su trabajo.</li>
    </ul>
</ul>

<h4>Estar en contacto con nuestros colegas</h4>

<ul>
<li>Estar al día de las últimas tendencias en cuanto a tecnología.</li>
    <ul>
    <li>¿Qué mejoras incorporan las nuevas versiones de los productos/sistemas/aplicaciones que utilizamos?</li>
    <li>¿Existen soluciones innovadores o cambios en la industria que aún no hemos adoptado?</li>
        <ul>
        <li>Virtualización para aprovechar mejor nuestro hardware.</li>
        <li>Cloud computing (IaaS/SaaS/PaaS) en lugar de nuestra propia infraestructura (<i>on premises</i>).<br><center><img src="/images/2018/4/on_premises.jpg"></center></li>
        <li>Soluciones híbridas.</li>
        </ul>
    <li>¿Existen nuevas alternativas de software para proveer servicios?</li>
        <ul>
        <li><a href="https://www.linuxito.com/gnu-linux/nivel-alto/998-como-montar-un-servidor-ldap-en-linux">LDAP</a> en lugar de NIS.</li>
        <li><a href="https://www.linuxito.com/gnu-linux/nivel-medio/432-como-instalar-y-configurar-samba-en-centos-7-con-acceso-anonimo">Samba</a> en lugar de CIFS.</li>
        <li><a href="https://www.linuxito.com/gnu-linux/nivel-alto/573-instalacion-y-configuracion-de-nginx-con-php-fpm">Nginx</a> en lugar de Apache.</li>
        <li>Cualquier cosa (?) en lugar de PHP.</li>
        </ul>
    </ul>
<li>¿Qué tecnologías usan en otras empresas o instituciones?</li>
<li>¿Estamos atrasados en algún aspecto? ¿Qué se puede cambiar o mejorar?</li>
    <ul>
    <li>Ya sea para dar un mejor servicio como para simplificar la administración.</li>
    </ul>
<li>¿Existen nuevas metodologías de trabajo?</li>
    <ul>
    <li><a href="https://www.linuxito.com/gnu-linux/nivel-alto/770-como-instalar-y-configurar-bacula-en-debian">Software de backup</a> vs. mis propios scripts.</li>
    <li><a href="https://www.linuxito.com/gnu-linux/nivel-alto/938-como-instalar-ansible-desde-los-fuentes">Software de automatización</a> vs. mis propios scripts.</li>
    <li><a href="https://www.linuxito.com/nix/832-jails-en-freebsd">Contenedores</a> vs. máquinas virtuales.</li>
    </ul>
</ul>

<h4>Ética laboral y licencias</h4>

<ul>
<li>Un SysAdmin jamás debe utilizar ni permitir el uso de software pirata.</li>
    <ul>
    <li>Al ser quien gestiona el software, es el responsable por respetar las licencias de software.</li>
    <li>Si un usuario desea utilizar cierto software propietario, se deberá adquirir la licencia en caso que corresponda.</li>
        <ul>
        <li>De lo contrario no se podrá utilizar dicho software.</li>
        </ul>
    <li>Más allá de adquirir una licencia se deberán respetar los términos de la misma.</li>
        <ul>
        <il>Un usuario adquiere una licencia para un equipo pero desea utilizarla en varios, violando los términos de la misma.
        </il></ul>
    <li>Un usuario posee copias de software pirata (ya sea instalado o copias de los instaladores) en sistemas bajo nuestra órbita.</li>
    </ul>
<li>Por otro lado se debe garantizar que los datos alojados en nuestro servidores no estén sujetos a copyright.</li>
    <ul>
    <li>Un usuario tiene cientos de archivos MP3 o películas pirata en uno de nuestros servidores de archivos (Samba, <a href="https://www.linuxito.com/gnu-linux/nivel-alto/496-configuracion-de-nfs-en-freebsd">NFS</a>) o soluciones de almacenamiento en la nube (<a href="https://www.linuxito.com/gnu-linux/nivel-alto/496-configuracion-de-nfs-en-freebsd">Nextcloud</a>).</li>
    <li>Lo mismo ocurre para archivos PDF o EPUB (copias de libros pirata).</li>
    </ul>
<li>Desde el punto de vista de la ética profesional, siempre se deberá mantener dentro de la ley.</li>
    <ul>
    <li>Un Jefe o Gerente desea acceder a la casilla de correo de un usuario.</li>
        <ul>
        <li>Más allá de lo que puedan decir los términos de uso de los sistemas de la compañía, acceder a una cuenta de correo electrónico es ilegal en la mayoría de los países.</li>
        <li>Lo mismo podría ocurrir para otro tipo de solicitudes similares.</li>
        <li>Siempre estar al tanto de las cuestiones legales que afectan nuestro trabajo.</li>
        </ul>
    <li>Como SysAdmin uno tiene naturalmente acceso a todas las cuentas de correo, mensajes, archivos y bases de datos de la compañía.</li>
        <ul>
        <li>Tener acceso como root/Administrator nos permite (valga la redundancia) acceder a absolutamente todos los datos de la compañía.</li>
        <li>Jamás utilizar esto a nuestro favor, en perjuicio de otros, o simplemente para curiosear.</li>
        <li>Más allá de ser poco ético, en la mayoría de los casos se nos puede acusar de espionaje.</li>
        <li>Un SysAdmin jamás debe cruzar esa barrera, bajo ninguna circunstancia, ya sea para beneficio propio o por una solicitud "de más arriba".</li>
            <ul>
            <li>En tal caso siempre es mejor renunciar que tener una mala reputación y convertirse en un mal profesional y persona. O peor aún "quedar pegado" en un proceso judicial.</li>
            </ul>
        </ul>
    <li>Un SysAdmin debe ser absolutamente responsable con las credenciales y roles que genera y/o le son otorgados.</li>
    </ul>
</ul>

<p>Y con esto doy por concluida esta biblia del SysAdmin (con el perdón por la blasfemia para los creyentes) sin descartar la posibilidad de agregar anexos en un futuro (en el caso de que sean necesarios). Próximamente publicaré una versión en PDF de la misma, para imprimir y guardar en la mesa de luz de todo SysAdmin que se precie :)</p>


### Referencias

* [Joe Chung - General SysAdmin Principles & Guidelines](http://rockhopper.monmouth.edu/cs/jchung/cs471/cs_471_-_general_sysadmin_principles)
