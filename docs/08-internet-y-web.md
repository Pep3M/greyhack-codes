# Internet y Web

Clientes para servicios de Internet y archivos HTML para interfaces web.

## theInternet/

### byteClient.src

**Descripción**: Cliente para el servicio Bytes (theInternet). Proporciona funciones API para interactuar con el servicio Bytes.

**Funcionalidades**:
- Conexión a servidor Bytes
- Gestión de cuenta de usuario
- Sistema de autenticación
- Generación de claves secretas
- Información de usuario (bytes, secret key)

**Uso**: Este archivo proporciona funciones que son importadas por otros scripts. No se ejecuta directamente.

**Funciones principales**:
- `callINET()`: Establece conexión al servicio
- `Encrypt()`: Encripta contraseñas
- `GenKey()`: Genera claves secretas
- `info()`: Obtiene información del usuario
- `ByteLogo()`: Muestra logo ASCII

**Dependencias**: Requiere conexión a servidor theInternet

---

### primBrowser.src

**Descripción**: Navegador primitivo para el servicio theInternet. Versión básica de navegador web.

**Versión**: 0.0.1

**Funcionalidades**:
- Navegación básica de sitios web
- Conexión a servicio theInternet
- Sistema de autenticación

**Uso**: Ejecutar y seguir instrucciones interactivas.

**Nota**: Este es un navegador muy básico para el servicio theInternet.

---

### TreasureClient.src

**Descripción**: Cliente para el servicio PirateWay (Treasure). Proporciona funciones API para interactuar con el servicio de tesoros.

**Funcionalidades**:
- Conexión a servidor PirateWay
- Gestión de cuenta de usuario
- Sistema de bytes y claves secretas
- Información de usuario

**Uso**: Este archivo proporciona funciones que son importadas por otros scripts.

**Funciones principales**:
- `callPW()`: Establece conexión al servicio
- `GenKey()`: Genera claves secretas
- `info()`: Obtiene información del usuario
- `ByteLogo()`: Muestra logo ASCII

**Dependencias**: Requiere conexión a servidor PirateWay

---

### Bytes.html

**Descripción**: Interfaz web HTML para el servicio Bytes. Página web para interactuar con el servicio.

**Uso**: Abrir en navegador web del juego o usar `open_url()`.

---

### sites_help.txt

**Descripción**: Archivo de ayuda con información sobre sitios web disponibles en theInternet.

**Uso**: Leer con `cat` o editor de texto.

---

### the_byte.txt

**Descripción**: Documentación o información sobre el servicio Bytes.

**Uso**: Leer con `cat` o editor de texto.

---

## Archivos HTML

### foxtrothtml.html

**Descripción**: Interfaz web para FoxTrot. Página web con estilo oscuro para interactuar con servicios FoxTrot.

**Características**:
- Diseño oscuro (fondo #0E0E0E)
- Colores temáticos FoxTrot (#6A855E, #445239)
- Interfaz scrollable
- Botones interactivos

**Uso**: Abrir en navegador web del juego.

---

### foxcoin.html

**Descripción**: Página web para FOX Coin. Interfaz para el sistema de criptomoneda FOX.

**Características**:
- Diseño con fondo gris (#BBBBBB)
- Colores azules (#5555AA)
- Sección de FAQ
- Botones interactivos

**Uso**: Abrir en navegador web del juego.

---

### nexus.html

**Descripción**: Interfaz web "The Nexus". Página web con temática Lunar (colores púrpura).

**Características**:
- Diseño oscuro
- Colores temáticos Lunar (#8254d1, #7141c4)
- Interfaz scrollable
- Botones interactivos

**Uso**: Abrir en navegador web del juego.

---

### sparki.html

**Descripción**: Página web de Clover. Sitio web personal con información y servicios.

**Características**:
- Diseño oscuro
- Colores temáticos FoxTrot
- Interfaz completa
- Múltiples secciones

**Uso**: Abrir en navegador web del juego.

---

### login.html

**Descripción**: Página de login. Interfaz web para autenticación.

**Uso**: Abrir en navegador web del juego.

---

### maintenance.html

**Descripción**: Página de mantenimiento. Muestra mensaje cuando un servicio está en mantenimiento.

**Uso**: Abrir en navegador web del juego o servir desde servidor web.

---

### weaselhtml.html

**Descripción**: Página web adicional. Interfaz web con funcionalidad específica.

**Uso**: Abrir en navegador web del juego.

---

### corTech.html

**Descripción**: Página web de CorTech. Interfaz para servicios de CorTech.

**Uso**: Abrir en navegador web del juego.

---

## Uso de Archivos HTML

Para usar archivos HTML en Grey Hack:

1. **Servidor web local**: Sube el archivo HTML a un servidor web y accede mediante IP
2. **Navegador del juego**: Usa `open_url()` en un script para abrir la URL
3. **Servidor remoto**: Si tienes acceso a un servidor web, sirve los archivos desde allí

**Ejemplo**:
```
// En un script
server = get_shell.connect_service("192.168.1.100", 80, "admin", "pass")
if typeof(server) == "shell" then
    server.host_computer.open_url("http://192.168.1.100/foxtrothtml.html")
end if
```

---

## Herramientas Relacionadas

Para clientes de servicios:
- Sección de Servicios y Clientes

Para herramientas de red:
- Sección de Herramientas de Red