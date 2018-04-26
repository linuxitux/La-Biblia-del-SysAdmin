## Capítulo 9: Estandarización vs. diversidad

Este capítulo trata sobre estandarización y diversidad. Ser un generalista o un
experto. Ser un experto es concentrar el conocimiento en un campo reducido. En
otras palabras, saber mucho acerca de poco hasta el punto de saber absolutamente
todo acerca de nada.

### Estandarización vs. diversidad

* ¿Estandarizarse en una única distribución GNU/Linux o utilizar múltiples
  distros?
    * Si se opta por la estandarización, es imprescindible [seleccionar tu distribución GNU/Linux](https://www.linuxito.com/8-gnu-linux/nivel-basico/1-como-elegir-una-distribucion-gnu-linux)
      cuidadosamente
        * Considerar la continuidad del proyecto como una de las claves.
            * [Debian](https://www.debian.org/) es la mejor apuesta cuando de
              continuidad se trata.
                * Al igual que muchas distribuciones basadas en Debian, como por
                  ejemplo [Ubunut](https://www.ubuntu.com/) y [Devuan](https://devuan.org/).
        * Otras distribuciones poseen mayor continuidad que Debian (notablemente
          Slackware), sin embargo se debe ponderar a su vez el tamaño de la
          comunidad y especialmente el tamaño del equipo de desarrollo.
        * Un tercer criterio a considerar es qué empresa está detrás de, y qué
          intereses persigue, la dirección del proyecto.
    * Si optamos por la estandarización, puede que ocurra que no sepamos
      resolver una tarea tan simple como configurar la red en una distro fuera
      de la que utilizamos a diario.
    * Utilizar múltiples distribuciones es una buena (¿mejor?) idea.
        * Red Hat y sus derivados siguen siendo los más ampliamente utilizados
          en entornos corporativos.
            * Esto implica que es necesario estar familiarizado con Red Hat y el
              gestor y formato de paquetes RPM.
        * Otras distribuciones muy utilizadas son aquellas basadas en [SUSE](https://www.suse.com/es-es/).
        * Contar con una buena flexibilidad en cuanto a distribuciones y
          gestores de paquetes puede potenciar nuestras oportunidades al momento
          de considerar un cambio de rumbo o nuevas oportunidades laborales en
          nuestra carrera profesional.
        * Jamás caer en el distrohopping. No es broma y podría considerarse una
          enfermedad. Reinstalar distros una y otra vez no nos hace expertos en
          Linux e involucra una gran pérdida de tiempo. El aprendizaje está en
          el uso y configuración de una distro, instalar y ver barras de
          progreso no aporta nada útil.
        * Utilizar distribuciones estables y robustas en nuestra estación de
          trabajo.
            * No poder realizar una tarea, conectarse a un servidor o abrir un
              archivo a causa de un problema con nuestra estación de trabajo (ya
              sea por un fallo o por falta de soporte para alguna aplicación o
              protocolo) no solo es vergonzoso para un SysAdmin, sino que hace
              mala publicidad a nuestra querida distro.
                * A lo largo de los años he visto a colegas linuxeros pasar por
                  situaciones como las siguientes en la oficina:
                    * "No puedo abrir archivos con el formato propietario .xyz".
                    * "No tengo codec para el formato X".
                    * "Esperá que justo está compilando una actualización y no
                      puedo usar la máquina".
                    * "Esperá que no bootea porque la última actualización
                      rompió el entorno de escritorio".
                    * "No puedo usar la aplicación X porque se actualizó la
                      libXYZ y dejó de funcionar".
                    * "La última actualización del programa X rompió la
                      compatibilidad con el protocolo ABC".
                    * Y muchas similares...
                * Lamentablemente he visto muy seguido estas situaciones,
                  especialmente con distribuciones *rolling release*, las cuales
                  hacen parecer a GNU/Linux como un SO inestable y poco
                  confiable. Y todos sabemos que es justamente lo opuesto, solo
                  que "tu distro" apesta.
            * Por supuesto, siempre vamos a querer experimentar. En tal caso
              dejar las distros "espartanas" y *rolling release* para casa y
              nuestras computadoras personales.
    * Utilizar múltiples sistemas operativos es todavía una mejor idea.
        * Contar con, al menos, un conocimiento básico sobre otros sistemas
          operativos de la familia Unix.
            * FreeBSD y OpenBSD son excelentes alternativas a GNU/Linux al
              momento de montar un nuevo servidor.
                * Especialmente OpenBSD está orientada a la seguridad. Es una
                  gran opción para montar firewalls.
                * FreeBSD cuenta de forma nativa con ZFS. La mejor opción para
                  servidores de archivos (NFS, Samba, etc.)
            * Existen muchas otras alternativas Unix como Solais, AIX, y *BSD
              (NetBSD, DragonFly).
        * No se puede ser un completo ignorante respecto a los sistemas
          operativos Microsoft Windows.
            * En toda organización existe al menos un servidor Windows.
            * Soluciones como Active Directory suelen ser superadoras y
              altamente adoptadas en entornos corporativos.
* Como en todo aspecto de la vida, estandarizarse nos deja "pegados" a una
  tecnología en particular (es por ello la importancia en la elección). Al
  contrario la diversidad nos da flexibilidad, tolerancia a imprevistos, mayor
  sabiduría (por tener un panorama más claro y ampio respecto a los cambios de
  comportamiento en el mercado o la comunidad), entre otras cualidades. Todo
  esto al costo de no llegar a profundizar al máximo nuestros conocimientos en
  cada uno de los temas que abarcamos.
    * El secreto está en encontrar un balance entre ambas.
    * Se supone que un SysAdmin debe conocer todo acerca de todo. Ya sabemos que
      es imposible, pero es lo que la sociedad espera de nosotros.

### Referencias

* [Joe Chung - General SysAdmin Principles & Guidelines](http://rockhopper.monmouth.edu/cs/jchung/cs471/cs_471_-_general_sysadmin_principles)
