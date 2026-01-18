# greyhackscripts

i no longer play grey hack, but so long as people find my scripts for the game useful i will keep this up, archival notice

collection of clovers's open source grey hack scripts

## 📚 Documentación

Esta colección contiene scripts, librerías, herramientas y sistemas operativos completos para Grey Hack. La documentación está organizada por categorías:

### Librerías y Frameworks
- **[01-librerias.md](docs/01-librerias.md)** - Documentación completa de todas las librerías:
  - `foxlib.src` - Librería principal con funciones generales
  - `cryptlib.src` - Funciones criptográficas y conversión de bases
  - `cyphlib.src` - Cifrado/descifrado Vigenère
  - `intlib.src` - Manejo de enteros grandes (BigInt)
  - `scanlib.src` - Escaneo de puertos y servicios
  - `tracelib.src` - Análisis y depuración de archivos

### Herramientas de Hacking
- **[02-exploits-y-hacking.md](docs/02-exploits-y-hacking.md)** - Herramientas de explotación:
  - `autohack.src` - Hacking automatizado completo
  - `advnmap.src` - Escaneo avanzado de red
  - `ssh_vir.src` - Virus SSH para capturar credenciales
  - `passwd_vir.src` - Virus de cambio de contraseña
  - `wificrack.src` - Cracking de contraseñas WiFi
  - `tempered.src` - Generador de exploits templados

### Herramientas de Sistema
- **[03-herramientas-sistema.md](docs/03-herramientas-sistema.md)** - Administración del sistema:
  - `ps.src` - Monitor de procesos mejorado
  - `sysmon.src` - Monitor de seguridad del sistema
  - `tree.src` - Visualización del árbol de archivos
  - `file.src` - Archivo protegido con contraseña
  - `importcode.src` - Procesador de imports

### Utilidades
- **[04-utilidades.md](docs/04-utilidades.md)** - Calculadoras y herramientas auxiliares:
  - `calc.src` / `calcfree.src` - Calculadoras matemáticas
  - `decipher.src` - Descifrador de contraseñas
  - `ipgen.src` - Generador de IPs para búsqueda de servicios
  - `keygen.src` - Generador de claves para FoxTrot
  - `randomart.src` - Generador de arte ASCII
  - `intcount.src` - Generador de números en diferentes bases

### Red y Comunicaciones
- **[05-red-y-comunicaciones.md](docs/05-red-y-comunicaciones.md)** - Herramientas de red:
  - `autoproxy.src` - Configuración automática de proxy
  - `automail.src` - Fuerza bruta de contraseñas de correo
  - `mail_finder.src` - Buscador de direcciones de correo
  - `rcon.src` - Control remoto
  - `rss.src` - Servidor de shell remoto

### Interfaces y Sistemas Operativos
- **[06-interfaces-y-os.md](docs/06-interfaces-y-os.md)** - Sistemas operativos completos:
  - `FoxTrot.src` - Sistema operativo completo de hacking (v2.8.3)
  - `nightlunar.src` - Sistema operativo Lunar
  - `lunarcmd.src` - Comandos del sistema Lunar
  - `minifoxos.src` - Sistema operativo minimalista FoxOS
  - `fourman.src` - Gestor de ventanas básico

### Servicios y Clientes
- **[07-servicios-y-clientes.md](docs/07-servicios-y-clientes.md)** - Clientes de servicios:
  - `spark.src` - Cliente para servicio Spark
  - `cloudsafe.src` - Servicio de almacenamiento en la nube
  - `sandboxy.src` - Cliente para servicio Sandbox
  - `msfconsole.src` - Interfaz de consola Metasploit
  - `playerfinder.src` - Buscador de IPs de jugadores
  - `cookieclicker.src` - Juego incremental de hacking

### Internet y Web
- **[08-internet-y-web.md](docs/08-internet-y-web.md)** - Clientes de Internet e interfaces web:
  - `theInternet/byteClient.src` - Cliente Bytes
  - `theInternet/primBrowser.src` - Navegador primitivo
  - `theInternet/TreasureClient.src` - Cliente PirateWay
  - Archivos HTML: `foxtrothtml.html`, `foxcoin.html`, `nexus.html`, etc.

### Otros
- **[09-otros.md](docs/09-otros.md)** - Archivos adicionales y miscelánea:
  - `enigmatic_theme_3.3.txt` - Tema de colores
  - `password.txt` - Archivo de contraseñas (⚠️ usar con precaución)
  - `LICENSE` - Licencia del proyecto
  - Estructura de carpetas y notas generales

## 🚀 Inicio Rápido

1. **Revisa las dependencias**: La mayoría de scripts requieren:
   - `metaxploit.so` - Para exploits
   - `crypto.so` - Para criptografía
   - `foxlib.src` / `Fox.so` - Librería principal

2. **Instala las librerías**: Asegúrate de tener `foxlib.src` compilado como `Fox.so` en `/root/`

3. **Lee la documentación**: Consulta los archivos MD en la carpeta `docs/` para detalles específicos

4. **Ejecuta los scripts**: Usa `run /path/to/script.src [params]` para ejecutar

## 📖 Para Desarrolladores

if you're a developer, check out the [foxlib](https://github.com/cloverrfoxx/foxlib-gh) repo for some useful libraries

## 🔗 Proyectos Relacionados

other projects i recommend!

- [Unclovered Lunarium](https://github.com/h4cktoria/unclovered-lunarium)
- [Unity](https://github.com/MachaCeleste/CelestialCorp-Unity)
- [5hell](https://github.com/jhook777/5hell-for-Grey-Hack-the-Game)
- [Finko42's Scripts](https://github.com/Finko42/GreyHack)

## ⚠️ Notas Importantes

- Este repositorio está en modo **archivo** - el autor ya no juega Grey Hack
- Los scripts están diseñados para uso educativo y legítimo
- Algunos scripts pueden requerir configuración específica de servidores
- Lee la documentación de cada script antes de usarlo
- ⚠️ **Nunca uses contraseñas reales** en archivos de texto plano
