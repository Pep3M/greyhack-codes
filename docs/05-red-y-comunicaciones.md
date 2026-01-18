# Herramientas de Red y Comunicaciones

Herramientas para comunicación, proxy, correo y servicios de red.

## autoproxy.src

**Descripción**: Configura y utiliza un proxy automáticamente. Encripta credenciales y configura conexión proxy transparente.

**Funcionalidades**:
- Configura proxy automáticamente
- Encripta usuario y contraseña
- Maneja conexiones proxy seguras
- Soporte para proxy con autenticación

**Uso**:
```
run /path/to/autoproxy.src [user@password] [address] [port]
```

**Parámetros**:
- `user@password`: Credenciales en formato usuario@contraseña
- `address`: Dirección IP del proxy
- `port`: Puerto del proxy

**Ejemplo**:
```
run /home/guest/autoproxy.src admin@pass123 192.168.1.1 8080
```

**Nota**: Configura el proxy para todas las conexiones de red siguientes.

---

## automail.src

**Descripción**: Herramienta de fuerza bruta para encontrar contraseñas de correo electrónico. Prueba contraseñas automáticamente usando fuerza bruta incremental.

**Funcionalidades**:
- Fuerza bruta incremental de contraseñas de correo
- Prueba contraseñas de longitud 1 a 32 caracteres
- Usa alfabeto completo (A-Z, a-z, 0-9)
- Muestra progreso en tiempo real
- Se detiene cuando encuentra la contraseña

**Uso**:
```
run /path/to/automail.src [email]
```

**Parámetros**:
- `email`: Dirección de correo electrónico a hackear

**Ejemplo**:
```
run /home/guest/automail.src user@example.com
```

**Advertencia**: Este proceso puede tomar mucho tiempo dependiendo de la longitud y complejidad de la contraseña.

**Salida**: Muestra cada intento de contraseña y el progreso. Se detiene cuando encuentra la contraseña correcta.

---

## mail_finder.src

**Descripción**: Herramienta "Hide & Seek" para encontrar direcciones de correo electrónico de usuarios. Intenta múltiples combinaciones de usuario@dominio hasta encontrar una dirección válida.

**Funcionalidades**:
- Busca direcciones de correo válidas
- Prueba múltiples dominios (almacenados en archivo `websites`)
- Envía correos de prueba para verificar
- Guarda credenciales de correo para uso futuro
- Muestra progreso de búsqueda

**Uso**:

**Primera vez** (solicita credenciales):
```
run /path/to/mail_finder.src
```

**Configuración previa**:
El script usa archivo `websites` con lista de dominios a probar y archivo `email` con credenciales.

**Ejemplo**:
```
run /home/guest/mail_finder.src
# Ingresa email del buscador
# Ingresa password del buscador
# Ingresa username a buscar
```

**Salida**: Muestra cada intento (usuario@dominio) y se detiene cuando encuentra una dirección válida.

**Archivos**:
- `websites`: Lista de dominios de correo a probar (uno por línea)
- `email`: Credenciales guardadas (email:password)

---

## rcon.src

**Descripción**: Herramienta de control remoto. Establece conexión de control remoto con otro sistema.

**Funcionalidades**:
- Conecta a sistema remoto
- Carga bibliotecas necesarias (metaxploit, crypto)
- Proporciona shell remoto

**Uso**: Requiere configuración específica de servidor remoto.

**Dependencias**:
- Requiere `metaxploit.so`
- Requiere `crypto.so`
- Requiere servidor rcon configurado

**Nota**: Esta es una herramienta avanzada para control remoto de sistemas.

---

## rss.src

**Descripción**: Servidor de shell remoto (rshell server). Escucha conexiones entrantes y proporciona shells remotos.

**Funcionalidades**:
- Escucha en puertos configurados
- Acepta conexiones entrantes
- Proporciona shells remotos a clientes
- Lista shells activos

**Uso**:
```
run /path/to/rss.src
```

**Salida**: Muestra "Waiting for connections..." y lista shells cuando se conectan.

**Dependencias**:
- Requiere `metaxploit.so` con soporte rshell
- Requiere `librshell.so` instalada

**Nota**: Esta herramienta debe ejecutarse en el servidor que recibirá conexiones.

---

## Herramientas Relacionadas

Para herramientas de hacking de red:
- `autohack.src` - Hacking automatizado
- `wificrack.src` - Cracking WiFi
- `advnmap.src` - Escaneo avanzado

Para herramientas de sistema:
- Sección de Herramientas de Sistema