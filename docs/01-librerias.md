# Librerías

Esta sección documenta las librerías utilizadas por los scripts de Grey Hack. Estas son bibliotecas reutilizables que proporcionan funcionalidades comunes.

## foxlib.src

**Descripción**: Librería principal del conjunto de scripts de Clover. Proporciona funciones generales para serialización, deserialización, búsqueda de bibliotecas, y utilidades diversas.

**Funcionalidades principales**:
- `LibFinder()`: Busca automáticamente bibliotecas esenciales (metaxploit, crypto, aptclient, blockchain) en el sistema
- `Serialize()` / `Deserialize()`: Convierte objetos map/list a/desde formato de string serializado
- Funciones de parsing y conversión de tipos
- Utilidades de formateo y presentación

**Uso**: Importada por la mayoría de scripts principales mediante `import_code("/root/Fox.so")` o `import_code("/root/BytesDev")`

**Dependencias**: Requiere acceso a las bibliotecas del sistema de Grey Hack

---

## cryptlib.src

**Descripción**: Librería de funciones criptográficas y de conversión de bases numéricas. Maneja operaciones binarias, conversiones de base, y operaciones criptográficas básicas.

**Funcionalidades principales**:
- `ToBinary()`: Convierte strings o números a representación binaria
- `FromBinary()`: Convierte binario a decimal o string
- Conversiones entre diferentes bases numéricas
- Operaciones criptográficas básicas

**Uso**: Utilizada por scripts que necesitan operaciones criptográficas o conversión de bases numéricas

**Ejemplo de uso**:
```
import_code("/root/CryptLib")
result = CryptLib.ToBinary("Hello", 8)
```

---

## cyphlib.src

**Descripción**: Librería de cifrado/descifrado usando cifrado de Vigenère modificado. Proporciona funciones para ocultar y revelar mensajes.

**Funcionalidades principales**:
- `Hide()`: Cifra un mensaje usando una clave
- `Open()`: Descifra un mensaje cifrado
- `HideFile()` / `OpenFile()`: Cifra/descifra archivos completos
- Soporte para claves personalizadas o uso del usuario activo por defecto

**Uso**: Utilizada por scripts que necesitan cifrar información sensible

**Ejemplo de uso**:
```
encrypted = Cyphlib.Hide("mensaje secreto", "miClave")
decrypted = Cyphlib.Open(encrypted, "miClave")
```

---

## intlib.src

**Descripción**: Librería para manejo de enteros grandes (BigInt). Permite operaciones matemáticas con números que exceden los límites de los enteros estándar.

**Funcionalidades principales**:
- `baseint()`: Crea un objeto BigInt base
- `copy()`: Copia un BigInt
- `zero()` / `one()`: Crea BigInt con valor 0 o 1
- Operaciones aritméticas: suma, resta, multiplicación, división
- Comparaciones: mayor que, menor que, igual

**Uso**: Utilizada por scripts que trabajan con números muy grandes

**Ejemplo de uso**:
```
import_code("/root/intlib")
bigNum = int.fromString("999999999999999999")
result = int.add(bigNum, bigNum)
```

---

## scanlib.src

**Descripción**: Librería para escaneo de puertos y servicios. Proporciona funcionalidades de análisis de red y descubrimiento de servicios.

**Funcionalidades principales**:
- Escaneo de puertos en IPs específicas
- Identificación de servicios corriendo
- Análisis de vulnerabilidades de red

**Uso**: Utilizada por herramientas de hacking como `autohack`, `advnmap`

**Dependencias**: Requiere acceso a metaxploit.so

---

## tracelib.src

**Descripción**: Librería para análisis y depuración de archivos (CTF). Proporciona funciones para analizar archivos encriptados y realizar decompilación.

**Funcionalidades principales**:
- `analyze()`: Analiza un archivo y genera un hash de análisis
- `decompile()`: Intenta decompilar archivos protegidos
- Generación de hashes MD5 para verificación

**Uso**: Utilizada en CTFs (Capture The Flag) y desafíos de hacking

**Nota**: Esta librería está incompleta pero proporciona la base para herramientas de análisis

---

## Importación de Librerías

La mayoría de los scripts utilizan `import_code()` para cargar estas librerías. Las rutas comunes son:

- `/root/Fox.so` - FoxLib principal
- `/root/FoxLib` - Versión alternativa
- `/root/BytesDev` - Versión Bytes de FoxLib
- `/root/CryptLib` - CryptLib
- `/root/intlib` - IntLib para BigInt
- `/lib/metaxploit.so` - Librería de exploits del sistema
- `/lib/crypto.so` - Librería criptográfica del sistema
- `/lib/aptclient.so` - Cliente de paquetes APT

**Recomendación**: Asegúrate de tener estas librerías compiladas y ubicadas en las rutas correctas antes de ejecutar los scripts que las dependen.