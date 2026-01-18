# Herramientas de Sistema

Herramientas para administración, monitoreo y gestión del sistema en Grey Hack.

## ps.src

**Descripción**: Monitor de procesos mejorado que muestra información detallada de procesos en ejecución con barras de progreso visuales para CPU y memoria.

**Funcionalidades**:
- Lista todos los procesos activos
- Muestra uso de CPU y memoria por proceso
- Agrupa procesos por usuario
- Barras visuales de progreso para CPU y memoria
- Resumen total de carga de sistema
- Código de color: root (rojo), otros usuarios (blanco)

**Uso**:
```
run /path/to/ps.src
```

**Salida**: Muestra formato organizado con:
- Usuario
- PID (Process ID)
- CPU (%)
- Memoria (%)
- Nombre del proceso
- Barras de progreso visuales

**Ejemplo de salida**:
```
root     1234  15%  [########------]  30%  [##########--------]  sshd
guest    5678   5%  [##------------]  10%  [#####-------------]  browser
```

---

## sysmon.src

**Descripción**: Monitor de seguridad del sistema que detecta y elimina procesos y archivos no autorizados. Actúa como un sistema de detección de intrusos (IDS).

**Funcionalidades**:
- Crea lista de procesos "seguros" al inicio
- Crea lista de archivos "seguros" al inicio
- Monitorea continuamente el sistema
- Detecta procesos nuevos no autorizados
- Detecta archivos nuevos no autorizados
- Cierra automáticamente procesos no listados
- Elimina automáticamente archivos no listados

**Uso**:
```
run /path/to/sysmon.src
```

**Advertencia**: Este script es muy agresivo y eliminará cualquier proceso o archivo que no esté en la lista inicial. Úsalo solo en sistemas donde quieres mantener un estado estático.

**Recomendación**: Detén cualquier proceso que quieras proteger antes de ejecutar sysmon.

---

## tree.src

**Descripción**: Muestra el árbol completo del sistema de archivos con información de permisos, propietario, grupo y tamaño.

**Funcionalidades**:
- Recorre recursivamente todo el sistema de archivos
- Muestra estructura jerárquica con indentación
- Información de cada archivo/directorio:
  - Propietario (owner)
  - Grupo (group)
  - Tamaño (size)
  - Permisos (permissions)
  - Ruta completa

**Uso**:
```
run /path/to/tree.src
```

**Salida**: Formato como:
```
[root/root/1024/rwx] /
  [guest/guest/512/rwx] /home
    [guest/guest/256/rwx] /home/guest
      [guest/guest/128/r--] /home/guest/file.txt
```

**Nota**: Puede tomar tiempo en sistemas con muchos archivos.

---

## file.src

**Descripción**: Archivo protegido con contraseña que contiene información sensible (como IPs). Requiere contraseña para acceder al contenido.

**Funcionalidades**:
- Protección por contraseña
- Generación de hash MD5 para verificación
- Delayed deletion: se elimina automáticamente después de un tiempo
- Modo "Analyze" para generar hash de análisis
- Modo "Debug" para acceso con contraseña

**Uso**:

**Para analizar el archivo**:
```
run /path/to/file.src Analyze
```

**Para acceder al contenido** (requiere contraseña):
```
run /path/to/file.src [password]
```

**Para modo debug**:
```
run /path/to/file.src Debug
```

**Ejemplo**:
```
run /home/guest/file.src Analyze
run /home/guest/file.src miPasswordSecreta
```

**Nota**: El contenido real ("IPAddr") está codificado en el archivo. Se usa comúnmente en CTFs.

---

## importcode.src

**Descripción**: Herramienta para procesar y expandir declaraciones `import_code` en archivos fuente. Reemplaza imports por el contenido real de los archivos importados.

**Funcionalidades**:
- Busca declaraciones `import_code()` en archivos
- Resuelve rutas relativas y absolutas
- Maneja imports anidados
- Expande el código importado inline
- Soporta rutas relativas con `./` y rutas sin `/`

**Uso**:
```
run /path/to/importcode.src [/path/to/file.src]
```

**Parámetros**:
- Ruta al archivo fuente a procesar

**Ejemplo**:
```
run /home/guest/importcode.src /home/guest/myscript.src
```

**Resultado**: El archivo original se modifica in-line, expandiendo todos los `import_code`.

**Nota**: Esta herramienta es útil para entender el código completo de un script antes de la compilación.

---

## minifoxoscmds.src

**Descripción**: Comandos y ayuda para el sistema operativo miniFoxOS. Proporciona la lista de comandos disponibles en el sistema.

**Funcionalidades**:
- Lista de comandos disponibles
- Documentación de parámetros
- Información de uso para cada comando
- Organizado por categorías (text, files, devices, etc.)

**Uso**: Este archivo es importado por `minifoxos.src` y no se ejecuta directamente.

**Comandos principales**:
- `help [command]` - Muestra ayuda
- `vim [file]` - Editor de texto
- `ls [path]` - Lista archivos
- `cd [path]` - Cambia directorio
- `cat [path]` - Muestra contenido
- `run [file]` - Ejecuta programa
- Y muchos más...

---

## Herramientas Relacionadas

Para herramientas de red, ver:
- `rcon.src` - Control remoto
- `rss.src` - Servidor de shell remoto

Para herramientas de hacking, ver:
- Sección de Exploits y Hacking