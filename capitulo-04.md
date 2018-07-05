## Capítulo 4: Administración y acceso remoto

En este cuarto capítulo se trata la administración y acceso remoto a sistemas,
aspecto indispensable en el día a día de un SysAdmin.

### Administración y acceso remoto

A menos que cada sistema que administremos permanezca online sólo de 8:00 a
17:00 hs. (algo muy poco probable), la administración de sistemas no es un
típico trabajo de 8 a 5. La posibilidad de trabajar de manera remota es
esencial y algo que todo SysAdmin debe demandar.

* Conocer los protocolos de acceso remoto más importantes, tanto gráficos como
  de línea de comandos.
    * [SSH (*Secure Shell*)](https://www.linuxito.com/gnu-linux/nivel-alto/459-como-autenticar-con-clave-publica-en-ssh)
    * [VNC (*Virtual Network Computing*)](https://www.linuxito.com/nix/652-como-gestionar-un-host-virtualbox-headless)
    * [RDP (*Remote Desktop Protocol*)](https://www.linuxito.com/gnu-linux/nivel-basico/166-acceso-remoto-a-sistemas-windows-utilizando-freerdp)
    * [X11 (*X Window System*)](https://www.linuxito.com/gnu-linux/nivel-medio/550-lanzar-aplicaciones-graficas-desde-una-sesion-ssh)
    * [SPICE (*Simple Protocol for Independent Computing Environments*)](https://www.linuxito.com/gnu-linux/nivel-medio/335-como-utilizar-spice-en-maquinas-virtuales-gnu-linux)
* Especialmente para el caso de los administradores Unix/Linux, dominar OpenSSH
  y todas sus funcionalidades y características:
    * [Autenticar con clave pública (sin utilizar contraseñas)](https://www.linuxito.com/gnu-linux/nivel-alto/459-como-autenticar-con-clave-publica-en-ssh).
    * [Transferir archivos a través de SSH puro](https://www.linuxito.com/gnu-linux/nivel-alto/360-transferir-archivos-entre-sistemas-remotos-utilizando-ssh-sin-ftp-sftp-o-scp).
    * Conocer la herramienta [scp](https://www.linuxito.com/gnu-linux/nivel-basico/167-como-transferir-archivos-de-forma-segura-utilizando-ssh).
    * [Configurar accesos SSH restringidos al protocolo SFTP](https://www.linuxito.com/gnu-linux/nivel-alto/187-configurar-sftp-en-red-hat-enterprise-linux-5-5).
* [Montar VPNs](https://www.linuxito.com/121-instalaci%C3%B3n-y-configuracion-de-openvpn.html),
  o utilizar [IPSec](https://www.linuxito.com/gnu-linux/nivel-alto/370-configuracion-de-un-tunel-ipsec-en-gnu-linux-para-conectarse-a-una-vpn-cisco),
  para acceder a redes corporativas de forma segura.
* Habilitar Wake-on-LAN y *Restore on AC/Power Loss* en la configuración de
  energía de la BIOS (ACPI) de todos los sistemas, para poder encender
  cualquiera de ellos sin necesidad de ingresar a la sala de servidores o centro
  de cómputo.
    * En caso de tener acceso o incidencia en los procesos de compra, asegurarse
      de que los sistemas a adquirir incluyan estas características.
* Aprender a utilizar consolas serie y [switches KVM](https://es.wikipedia.org/wiki/Switch_KVM).
* Habilitar más de una forma de acceso a un sistema de forma remota.
    * En caso de bajar accidentalmente una interfaz de red (`ifdown eth0`) o
      cometer un [error en la configuración de un firewall](https://www.linuxito.com/gnu-linux/nivel-alto/330-gestion-del-firewall-en-red-hat-centos),
      quedaremos sin acceso remoto a un sistema. ¿Existe alguna otra forma de
      acceder a dicho sistema de manera remota cuando eso ocurra?
    * Los fabricantes de hardware más importantes han desarrollado consolas
      remotas de acceso directo al bus de sistema (DELL/iDRAC, HP/iLO, IBM/IMM)
      desde una interfaz de red especial (como si estuviésemos sentados
      físicamente en la consola terminal serie del equipo). Esto es de vital
      importancia al momento de realizar tareas críticas como [migraciones en producción](https://www.linuxito.com/gnu-linux/nivel-alto/388-como-migrar-un-servidor-en-produccion-desde-debian-6-a-7).
    * Para los sistemas en la nube ([IaaS](https://en.wikipedia.org/wiki/Cloud_computing#Infrastructure_as_a_service_.28IaaS.29)),
      ¿ofrece el proveedor más de un acceso a dichos sistemas (consolas Web,
      VPNs, etc.)? Nuevamente, en caso de tener incidencia en los procesos de
      compras, asegurarse que estos accesos estén incluídos dentro del soporte
      de la infraestructura *cloud*.
* Aprender a utilizar la línea de comandos.
    * Incluso en Windows (`cmd`/[PowerShell](https://msdn.microsoft.com/en-us/powershell/)).
    * La administración remota es mejor (prácticamente exclusiva en sistemas
      operativos de la familia Unix) desde línea de comandos.
    * Familiarizarse con las herramientas de *networking* básicas: [`telnet`, `netcat`](https://www.linuxito.com/gnu-linux/nivel-medio/102-enviar-correo-con-netcat-telnet),
      [`nmap`](https://www.linuxito.com/seguridad/148-chuleta-de-nmap),
      [`tcpdump`](https://www.linuxito.com/gnu-linux/nivel-medio/542-monitorear-el-trafico-de-red-desde-y-hacia-una-direccion-ip-especifica),
      [`ssh`](https://www.linuxito.com/gnu-linux/nivel-alto/360-transferir-archivos-entre-sistemas-remotos-utilizando-ssh-sin-ftp-sftp-o-scp),
      [`scp`](https://www.linuxito.com/gnu-linux/nivel-basico/167-como-transferir-archivos-de-forma-segura-utilizando-ssh),
      [`sftp`](https://www.linuxito.com/gnu-linux/nivel-alto/187-configurar-sftp-en-red-hat-enterprise-linux-5-5),
      [`dig`](https://www.linuxito.com/gnu-linux/nivel-alto/242-como-instalar-dig-en-red-hat-fedora-centos),
      `ping`, `traceroute`, [`openssl`](https://www.linuxito.com/seguridad/366-verificar-conexiones-ssl-tls-desde-linea-de-comandos-con-openssl),
      `host`, `nslookup`, `arp`, etc.
    * Aprender a [interactuar con los protocolos de red](https://www.linuxito.com/gnu-linux/nivel-medio/328-interactuar-con-un-servidor-de-correo-pop-mediante-telnet-netcat)
      más utilizados: HTTP, FTP, SMTP, POP3, etc.
* Aprender a implementar *port forwarding* y túneles SSH.
    * Comprender el concepto de *port forwarding* para implementar [conexiones seguras](https://www.linuxito.com/gnu-linux/nivel-alto/543-analisis-de-trafico-en-tiempo-real-en-servidores-utilizando-wireshark-y-tcpdump)
      entre sistemas remotos y [redirigir tráfico a través de SSH](https://www.linuxito.com/gnu-linux/nivel-medio/550-lanzar-aplicaciones-graficas-desde-una-sesion-ssh).
    * Conocer el uso de [túneles SSH](https://www.linuxito.com/seguridad/76-como-crear-un-tunel-ssh-a-traves-de-un-proxy-http)
      para encriptar tráfico de protocolos planos (por ejemplo [VNC](https://www.linuxito.com/gnu-linux/nivel-alto/182-como-acceder-a-la-consola-grafica-de-una-maquina-virtual-kvm-en-un-host-sin-entorno-grafico)).
