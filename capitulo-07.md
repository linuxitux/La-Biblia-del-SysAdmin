## Capítulo 7: Gestión de software y mantenimiento del sistema

Este capítulo trata sobre una de las tareas más frecuentes en el día a día de un
SysAdmin: instalar, configurar y mantener software.

### Gestión de software y mantenimiento del sistema

* Instalación de software
    * Siempre recurrir a fuentes oficiales para descargar software a instalar
      (por ejemplo: Debian, Microsoft)
        * En el caso de distribuciones GNU/Linux como Debian, la mayor parte del
          software puede ser instalado desde el gestor de paquetes ejecutando
          `apt-get`, `aptitude` o `apt` sin necesidad de agregar repositorios o
          *mirrors* de terceros.
        * En el caso de otros sistemas operativos como Microsoft Windows,
          siempre descargar actualizaciones y software desde el sitio oficial.
    * Si los repositorios oficiales no están disponibles o no incluyen el
      software que necesitamos, utilizar una fuente o *mirror* de terceros
      recomendada sólo si es de confianza. Por ejemplo un repositorio mantenido
      por el propio proveedor del software necesario.
        * Siempre descargar e instalar (`gpg --import`) las clave de cifrado de
          los repositorios para asegurarse de que el software que se obtiene
          está firmado y es de confianza. Al mismo tiempo verificar las firmas
          cada vez que se descargan imágenes y software vía HTTP/S
          (`gpg --verify`).
            * De esta forma, los paquetes instalados deben ser mantenidos y
              actualizados utilizando exclusivamente el gestor de paquetes
              (`apt-get`, `aptitude`, `yum`, etc.)
    * Si no se dispone del software necesario en los repositorios oficiales, y
      no hay un repositorio externo recomendado, lo recomendable es descargar el
      código fuente para compilarlo e instalarlo manualmente.
        * Verificar los *checksums* cada vez que se descarga un fuente vía
          HTTP/S.
        * Preferentemente descargar fuentes sólo a través de HTTPS.
        * Siempre utilizar un script para configurar, compilar e instalar un
          paquete. Esto permite "recordar" las opciones de configuración
          utilizadas para compilar el paquete, las cuales serán necesarias al
          momento de re-compilar el software (por ejemplo cuando se publican
          parches de seguridad para la versión instalada).
            * Si un software no provisto por los repositorios oficiales será
              utilizado en varios servidores, tal vez lo más conveniente sea
              crear nuestro propio paquete. Todas las distribuciones GNU/Linux
              poseen guías completas para generar paquetes (por ejemplo
              [Debian Wiki](https://wiki.debian.org/Packaging/)).
            * Si la escala aumenta y la cantidad de paquetes personalizados es
              grande, será necesario montar nuestro propio repositorio (por
              ejemplo [DebianRepository/Setup - Debian Wiki](https://wiki.debian.org/DebianRepository/Setup)).
* Múltiples esquemas de gestión de paquetes en un mismo sistema.
    * Un ejemplo es el caso de la gestión de ports y paquetes en FreeBSD. Es
      recomendable mantener una cierta consistencia al momento de instalar
      paquetes y actualizar el sistema.
    * Generalmente los [ports](https://www.linuxito.com/nix/481-como-resolver-problemas-de-dependencias-en-freebsd)
      suelen estar más actualizados que los paquetes (a causa del tiempo
      necesario para compilar para todas las arquitecturas soportadas).
    * Es recomendable utilizar paquetes ya que el tiempo de compilación suele
      ser elevado y la ganancia en *performance* no es significativa. Por otro
      lado, tener una mezcla entre ports y paquetes dificulta el mantenimiento
      del sistema.
    * Sólo utilizar ports para disponer de opciones personalizadas en paquetes
      específicos.
    * Existe software que sólo es posible instalar a través de ports debido a su
      licencia.
* Los paquetes disponibles en los repositorios oficiales no siempre están
  actualizados.
    * Generalmente están actualizados en cuanto a nivel de parches de seguridad
      (si la versión específica aún tiene soporte).
        * Toda distribución que se precie de ser robusta publicará los parches
          de seguridad de paquetes, para las versiones cuyo soporte está
          vigente, con la mayor celeridad posible.
        * Más allá de esto, y tal como menciona el [Capítulo 2](capitulo-02.md),
          es altamente recomendable suscribirse a las listas de correo de
          seguridad, principalmente para planificar con anticipación las
          actualizaciones críticas y urgentes. Especialmente cuando se trata de
          [actualizaciones que requieren de reinicios](capitulo-05.md) de
          servicios o, peor aún, del sistema operativo (kernel).
    * Pero las versiones oficiales suelen no estar actualizadas respecto a
      características y funcionalidades. Recordar que los repositorios son
      mantenidos por gente que tiene vida propia, muchas veces como voluntarios,
      haciendo este trabajo en su propio tiempo libre.
    * Cuando se requiere contar con versiones actualizadas de un paquete (sin
      migrar a una versión más actualizada del sistema operativo, en caso de que
      haya una disponible) no queda otra alternativa que compilar, instalar y
      mantener el paquete en cuestión manualmente.
* Actualizaciones automáticas
    * Por más lindo que suene, un Administrador de Sistemas siempre debe saber
      qué se está instalando o actualizando.
    * La instalación y actualización de paquetes debe ser una tarea interactiva.
      Muchas veces una actualización de paquetes dispara el reinicio de
      servicios, lo cual puede afectar el [uptime](capitulo-05.md) de un
      servicio.
        * Peor aún, uno debe conocer con exactitud hacia qué versión de cada
          paquete se está migrando con exactitud para no romper la
          compatibilidad con todo software de terceros y aplicaciones a medida
          corriendo en el servidor.
        * Esto aplica principalmente (pero no únicamente) a las versiones de
          sistemas de gestión de bases de datos, lenguajes de scripting (PHP,
          Perl, Python), intérpretes y entornos de tiempo de ejecución (Java),
          servicios (Apache, Nginx), librerías del sistema (libc) y utilitarios
          (OpenSSL/LibreSSL).
        * Cabe destacar que esto aplica generalmente para las migraciones de
          versión de sistema operativo (`dist-upgrade`) más que para las
          actualizaciones de paquetes (`upgrade`). Al menos en Debian y
          derivados, donde al momento de liberar un versión estable se
          "congelan" las versiones de paquetes, y las subsecuentes
          actualizaciones sólo corrigen bugs y proveen parches de seguridad sin
          alterar la funcionalidad. Pero por supuesto, depende de cómo gestione
          el [versionado de paquetes](https://www.linuxito.com/gnu-linux/nivel-basico/916-sobre-debian-y-el-versionado-de-paquetes)
          cada distribución en particular (por esta razón no se ven
          distribuciones *rolling-release* corriendo en servidores).
* Actualizar el sistema operativo, kernel y todo software cuidadosamente.
    * En lo que respecta a aplicar parches de seguridad, service packs,
      hotfixes, etc.
    * Pensar siempre si es el momento correcto para hacerlo.
        * El sistema, servicio o aplicación corriendo en el servidor ¿está
          siendo utilizada? ¿Hay usuarios logueados?
        * La actualización ¿puede esperar o es un parche de seguridad crítico?
    * Antes de comenzar, ¿se ha realizado un [backup](capitulo-02.md) o snapshot
      del sistema previamente?
    * ¿Es posible recuperar el sistema rápidamente en caso de que la
      actualización falle?
    * ¿Se ha testeado la actualización en un [entorno de prueba](https://www.linuxito.com/programacion/237-el-modelo-de-desarrollo-testing-y-produccion)
      antes?
    * ¿Se ha testeado el funcionamiento del sistema luego de actualizar?
    * En muchos sistemas es posible actualizar sólo los parches de seguridad o
      hotfixes críticos en lugar de todas las actualizaciones disponibles.
    * Y como regla general: jamás actualizar un sistema un viernes.
      Preferentemente no hacer nada un viernes.

<center>![Read only friday](images/walter-sobchak-read-only-friday.png)</center>

* Instalar sólo aquel software que será realmente utilizado.
    * Todo software innecesario puede contener vulnerabilidades. Sin contar con
      el hecho de que, al no ser utilizado, se le deje de prestar atención y
      quede desactualizado/obsoleto.
    * Cada pieza de software es un punto de entrada más al sistema.
    * Sin embargo, privar a los usuarios del software que necesitan puede
      motivarlos a instalarlo por sus propios medios, muy probablemente de
      manera incorrecta y en ubicaciones poco convenientes, sin mantenimiento ni
      monitoreo.
* No todo el software viene empaquetado de manera elegante.
    * En general sucede con el software comercial, propietario o "no gratuito".
        * Casos típicos como los parches de Microsoft, soluciones de backup de
          Symantec, Java de Oracle, las VMware Tools de VMware, y
          lamentablemente muchos más.
        * Todos los recaudos respecto al testeo, [documentación](capitulo-01.md)
          y verificación de instalaciones y actualizaciones se deben potenciar
          para estos casos. Es común que los instaladores sean scripts Bash
          basados en parseo de salidas, los cuales pueden fallar horriblemente y
          dejar el sistema en un estado inconsistente.
        * Muchas veces incluso es necesario aplicar parches de terceros a los
          fuentes oficiales a fin de que funcionen en nuestras plataformas. Todo
          lo dicho anteriormente en cuanto a verificar la procedencia del
          software aplica con mayor énfasis para el caso de parches de código en
          software propietario.
    * En algunos casos existe software propietario de código abierto que es
      necesario instalar por fuera de los gestores de paquetes e incluso
      compilar por nuestros propios medios.
        * Especificar siempre `/usr/local` u `/opt` como directorios de
          instalación.
            * Nunca dejar que una pieza de software por fuera del gestor de
              paquetes se instale en los directorios de binarios del sistema
              (`/bin`, `/sbin`/, `/usr/bin`, `/usr/sbin`, etc.).
        * Antes de instalarlo, pensar en la necesidad de desinstalarlo en un
          futuro. ¿Incluye un mecanismo o script de desinstalación?
        * Documentar todas las rutas y archivos creados durante la instalación,
          y toda modificación realizada en el sistema operativo, su
          configuración, y cualquier servicio.
