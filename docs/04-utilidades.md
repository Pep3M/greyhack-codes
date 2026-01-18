# Calculadoras y Utilidades

Herramientas de utilidad general para operaciones matemáticas, criptográficas y diversas funciones auxiliares.

## calc.src

**Descripción**: Calculadora completa con soporte para expresiones matemáticas complejas. Utiliza un parser de tokens (lexer) para evaluar expresiones matemáticas.

**Funcionalidades**:
- Evaluación de expresiones matemáticas
- Soporte para números enteros y decimales
- Operadores: +, -, *, /, ^ (potencia)
- Paréntesis para agrupar operaciones
- Precedencia de operadores correcta

**Uso**:
```
run /path/to/calc.src
```

**Ejemplo de expresiones**:
```
5 + 3 * 2
(10 + 5) / 3
2 ^ 8
```

**Dependencias**: Parser de tokens personalizado incluido

---

## calcfree.src

**Descripción**: Versión gratuita de la calculadora con funcionalidad básica. Versión simplificada de `calc.src`.

**Funcionalidades**:
- Operaciones matemáticas básicas
- Soporte para enteros
- Operadores básicos

**Uso**:
```
run /path/to/calcfree.src
```

**Nota**: Esta es una versión limitada. Para funcionalidad completa, usar `calc.src`.

---

## decipher.src

**Descripción**: Herramienta para descifrar contraseñas usando la librería crypto.so. Puede descifrar hashes de contraseñas encontrados en sistemas comprometidos.

**Funcionalidades**:
- Descifra contraseñas hasheadas
- Soporta formato usuario:contraseña_hash
- Soporta solo hash de contraseña
- Usa crypto.so para descifrar

**Uso**:
```
run /path/to/decipher.src [hash_or_user:hash]
```

**Parámetros**:
- `hash_or_user:hash`: Hash de contraseña o formato usuario:hash

**Ejemplo**:
```
run /home/guest/decipher.src user:abc123def456
run /home/guest/decipher.src abc123def456
```

**Salida**: Muestra usuario:contraseña_descifrada o solo contraseña

**Dependencias**: Requiere `crypto.so`

**Nota**: Solo funciona con hashes que crypto.so puede descifrar.

---

## ipgen.src

**Descripción**: Generador de IPs aleatorias para encontrar servidores con bibliotecas específicas. Útil para encontrar servicios o versiones específicas de software en la red.

**Funcionalidades**:
- Genera IPs aleatorias válidas (1-223.0-255.0-255.0-255)
- Busca routers/servidores con bibliotecas específicas
- Filtra por tipo de biblioteca (ssh, repo, chat, http, ftp, rshell, router)
- Filtra por versión específica
- Guarda IPs encontradas en archivo local

**Uso**:
```
run /path/to/ipgen.src [lib] [ver]
```

**Parámetros**:
- `lib`: Tipo de biblioteca a buscar (ssh, repo, chat, http, ftp, rshell, router)
- `ver`: Versión específica a buscar (opcional)

**Ejemplo**:
```
run /home/guest/ipgen.src router
run /home/guest/ipgen.src ssh "1.0"
```

**Salida**: Guarda IPs encontradas en archivo `ips` en el directorio actual

**Nota**: Puede tomar mucho tiempo encontrar resultados. El proceso continúa indefinidamente hasta encontrar coincidencias.

---

## keygen.src

**Descripción**: Generador de claves de acceso para FoxTrot. Se conecta a los servidores de FoxTrot y genera claves de licencia válidas.

**Funcionalidades**:
- Conecta a servidores FoxTrot
- Genera claves de licencia aleatorias
- Valida claves con el servidor
- Sistema de verificación de permisos

**Uso**:
```
run /path/to/keygen.src
```

**Nota**: Requiere conexión a los servidores FoxTrot. La clave generada se usa para activar FoxTrot.

**Dependencias**: 
- Requiere conexión de red
- Requiere servidores FoxTrot accesibles

---

## randomart.src

**Descripción**: Generador de arte ASCII aleatorio basado en hashes (similar a randomart de SSH). Crea patrones visuales únicos a partir de datos de entrada.

**Funcionalidades**:
- Genera arte ASCII desde hashes o datos
- Patrones visuales únicos
- Similar a randomart de SSH keys
- Usa hash MD5 para generar patrones

**Uso**:
```
run /path/to/randomart.src
```

**Nota**: Este script genera arte visual decorativo. Útil para crear "huellas digitales" visuales de datos.

---

## intcount.src

**Descripción**: Generador de números en diferentes bases numéricas. Genera secuencias de números en base 2-62.

**Funcionalidades**:
- Genera números en base 2 a 62
- Incrementa automáticamente la longitud
- Usa caracteres: 0-9, A-Z, a-z

**Uso**:
```
run /path/to/intcount.src [base]
```

**Parámetros**:
- `base`: Base numérica (2-62, por defecto 10)

**Ejemplo**:
```
run /home/guest/intcount.src 16  # Hexadecimal
run /home/guest/intcount.src 2   # Binario
```

**Salida**: Muestra números en la base especificada de forma continua

**Nota**: El proceso continúa indefinidamente. Útil para generación de secuencias.

---

## Herramientas Relacionadas

Para más herramientas matemáticas avanzadas:
- `intlib.src` - Librería de enteros grandes (BigInt)
- `cryptlib.src` - Librería criptográfica

Para herramientas de red:
- Sección de Herramientas de Red