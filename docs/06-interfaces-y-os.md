# Interfaces y Sistemas Operativos

Sistemas operativos personalizados y interfaces de usuario avanzadas para Grey Hack.

## FoxTrot.src

**Descripción**: Sistema operativo completo y framework de hacking avanzado. Es la herramienta más completa del conjunto, proporcionando un entorno completo de hacking con múltiples funcionalidades integradas.

**Versión**: 2.8.3

**Funcionalidades principales**:
- Sistema de login con autenticación de 2 factores (2FA)
- Escaneo y explotación automatizada de vulnerabilidades
- Gestión de exploits y bibliotecas
- Sistema de usuarios y permisos
- Integración con servidores FoxTrot
- Auto-actualización mediante APT
- Interfaz de línea de comandos completa
- Gestión de sesiones y shells

**Uso**:
```
run /path/to/FoxTrot.src
```

**Primera ejecución**:
1. Solicita crear cuenta o iniciar sesión
2. Configuración de email para 2FA
3. Verificación de email
4. Código 2FA enviado por correo

**Características avanzadas**:
- Búsqueda automática de bibliotecas (metaxploit, crypto)
- Gestión de repositorios APT
- Sistema de archivos virtual
- Logs y auditoría
- Protección contra ejecución en servidor principal

**Dependencias**:
- `metaxploit.so` - Para exploits
- `crypto.so` - Para criptografía
- `aptclient.so` - Para actualizaciones (opcional)
- `foxlib.src` - Librería principal
- `BytesDev` - Framework adicional

**Nota**: FoxTrot es un sistema completo y requiere configuración inicial. Consulta la documentación oficial para más detalles.

---

## nightlunar.src

**Descripción**: Sistema operativo Lunar (versión nocturna). Interfaz de línea de comandos avanzada con múltiples herramientas integradas.

**Funcionalidades**:
- Shell interactivo completo
- Múltiples comandos integrados
- Sistema de ayuda extenso
- Gestión de archivos y procesos
- Herramientas de hacking integradas
- Sistema de logs para virus SSH y passwd
- Comandos de cifrado y compresión
- Integración con bibliotecas del sistema

**Uso**:
```
run /path/to/nightlunar.src
```

**Comandos principales**:
- `help [command]` - Ayuda de comandos
- `fs [code]` - Ejecuta código FoxScript
- `exit` - Sale del sistema
- `clear` - Limpia pantalla
- `ls [path]` - Lista archivos
- `cd [path]` - Cambia directorio
- `vim [file]` - Editor de texto
- `crack [hash]` - Descifra hash
- `encrypt [string] [key] [enc/dec]` - Cifra/descifra
- Y muchos más...

**Dependencias**:
- `lunarcmd.src` - Comandos del sistema
- `foxlib.src` - Librería principal
- `metaxploit.so` - Para exploits
- `crypto.so` - Para criptografía

**Nota**: Lunar es un sistema completo con cientos de comandos. Usa `help` para ver la lista completa.

---

## lunarcmd.src

**Descripción**: Definición de comandos para el sistema Lunar. Contiene todos los comandos, parámetros y documentación del sistema Lunar.

**Funcionalidades**:
- Define todos los comandos disponibles
- Documentación de parámetros
- Información de uso
- Organización por categorías

**Uso**: Este archivo es importado por `nightlunar.src` y no se ejecuta directamente.

**Categorías de comandos**:
- Defaults: help, exit, clear, setup
- Text: vim, cat, grep, echo, etc.
- Files: ls, cd, mv, cp, mkdir, etc.
- Devices: passwd, run, ps, kill, etc.
- Network: ssh, scan, nmap, etc.
- Y muchas más...

---

## minifoxos.src

**Descripción**: Sistema operativo minimalista FoxOS. Versión ligera y rápida del sistema Fox.

**Funcionalidades**:
- Shell interactivo básico
- Comandos esenciales
- Gestión de archivos
- Ejecución de programas
- Navegación de sistema de archivos

**Uso**:
```
run /path/to/minifoxos.src [shell] [user]
```

**Parámetros**:
- `shell`: Objeto shell o computer
- `user`: Usuario del sistema

**Ejemplo**:
```
run /home/guest/minifoxos.src get_shell "guest"
```

**Comandos disponibles**:
- `help` - Lista comandos
- `exit` - Sale del sistema
- `clr` - Limpia pantalla
- `ls [path]` - Lista archivos
- `cd [path]` - Cambia directorio
- `cat [path]` - Muestra archivo
- `run [file]` - Ejecuta programa
- Y más comandos básicos

**Dependencias**:
- `minifoxoscmds.src` - Definición de comandos

---

## fourman.src

**Descripción**: Gestor de ventanas (Window Manager) básico. Interfaz gráfica simple con sistema de puntero y ventanas.

**Funcionalidades**:
- Sistema de ventanas básico
- Puntero controlable con flechas
- Frame buffer para visualización
- Sistema de aplicaciones

**Uso**:
```
run /path/to/fourman.src
```

**Controles**:
- Flechas: Mueven el puntero (X)
- Enter: Selecciona/activa

**Dependencias**:
- `dapi.so` - API de display

**Nota**: Esta es una versión muy básica de gestor de ventanas. Principalmente para demostración.

---

## Herramientas Relacionadas

Para más información sobre comandos:
- `minifoxoscmds.src` - Comandos de miniFoxOS
- `lunarcmd.src` - Comandos de Lunar

Para herramientas del sistema:
- Sección de Herramientas de Sistema