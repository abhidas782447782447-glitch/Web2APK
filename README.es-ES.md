# Web2APK

<p align='center'>
  <img src="https://github.com/77AXEL/Web2APK/blob/main/images/logo.png" alt="Web2APK Logo">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open_Source-Yes-red" alt="Open Source">
  <img src="https://img.shields.io/badge/Platform-Windows%20|%20macOS%20|%20Linux-blue" alt="Platform Support">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
</p>

---

## 📱 Descripción General

Web2APK es una potente herramienta de automatización que convierte tus proyectos web (HTML, CSS, JavaScript) en aplicaciones nativas de Android. Evita el proceso de conversión manual y despliega tus aplicaciones web en dispositivos Android con un solo comando.

### ✨ Características

- 🚀 **Conversión en un Comando** - Convierte proyectos web a APK al instante
- 🎨 **Branding Personalizado** - Define tu propio nombre y icono de aplicación
- 🔧 **Construcción Automatizada** - Gestiona la compilación y la firma automáticamente
- 🌍 **Multiplataforma** - Funciona en Windows, macOS y Linux
- 📦 **Sin Configuración Manual** - Solo proporciona tu proyecto y listo

---

## ⚠️ Requisitos Previos

> **Importante:** Esta herramienta requiere que Java JDK y Android SDK estén instalados en tu sistema con sus variables de entorno configuradas correctamente.

### Variables de Entorno Requeridas:
- **`JAVA_HOME`** - Ruta a tu instalación de Java JDK
- **`ANDROID_HOME`** - Ruta a tu instalación de Android SDK

### Enlaces de Instalación:
- [Java JDK 17+](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) - Requerido para la compilación del APK
- [Android SDK](https://developer.android.com/studio) - Requerido para las herramientas de construcción de Android

**Verificación:** Ejecuta los siguientes comandos para verificar tu configuración:
```bash
echo $JAVA_HOME    # Linux/macOS
echo $ANDROID_HOME

echo %JAVA_HOME%    # Windows
echo %ANDROID_HOME%
```

---

## 📥 Instalación

### Opción 1: Usando Git
```bash
git clone https://github.com/77AXEL/Web2APK
cd Web2APK
```

### Opción 2: Descarga Directa
Descarga la [última versión](https://github.com/77AXEL/Web2APK/archive/refs/heads/main.zip) y extráela en la ubicación deseada.

---

## 🚀 Uso

### Paso 1: Prepara tu Proyecto Web

Crea tu proyecto front-end con la siguiente estructura:

```
my-web-project/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── assets/
    └── images/
```

<img src="https://github.com/77AXEL/Web2APK/blob/main/images/cap2.png" alt="Project Structure" width="200" height="200">

### Paso 2: Comprime tu Proyecto

Crea un archivo ZIP de toda la carpeta de tu proyecto:

<img src="https://github.com/77AXEL/Web2APK/blob/main/images/cap3.png" alt="Compress Project" width="600">

### Paso 3: Ejecuta la Conversión

Navega al directorio de Web2APK y ejecuta:

```bash
python wa.py -zip path/to/your/project.zip -icon path/to/your/icon.webp -name "YourAppName"
```

**Ejemplo:**
```bash
python wa.py -zip ~/projects/my-website.zip -icon ~/icons/app-icon.webp -name "MyAwesomeApp"
```

### Paso 4: Proceso de Compilación

La herramienta realizará automáticamente lo siguiente:
1. Extraerá los archivos de tu proyecto
2. Instalará el icono de tu aplicación
3. Establecerá el nombre de tu aplicación
4. Construirá el APK
5. Firmará el APK

<img src="https://github.com/77AXEL/Web2APK/blob/main/images/cap1.png" alt="Build Process" width="600">

### Paso 5: Obtén tu APK

Encuentra tu APK compilado en el directorio `dist/`:

<img src="https://github.com/77AXEL/Web2APK/blob/main/images/cap4.png" alt="Output APK" width="600">

---

## 📝 Argumentos de Línea de Comandos

| Argumento | Descripción | Requerido | Ejemplo |
|----------|-------------|----------|---------|
| `-zip` | Ruta al archivo ZIP de tu proyecto web | ✅ Sí | `project.zip` |
| `-icon` | Ruta al icono de tu aplicación (se recomienda WebP) | ✅ Sí | `icon.webp` |
| `-name` | Nombre para tu aplicación de Android | ✅ Sí | `MyApp` |

---

## 💡 Consejos y Buenas Prácticas

- ✅ **Usa el formato WebP** para los iconos de la aplicación para obtener una calidad y tamaño óptimos.
- ✅ **Prueba tu proyecto web** en un navegador antes de la conversión.
- ✅ **Usa rutas relativas** en tus archivos HTML/CSS/JS.
- ✅ **Mantén tamaños de archivo razonables** para una generación de APK más rápida.
- ✅ **Revisa los logs** en la carpeta `log/` si encuentras problemas.

---

## 🐛 Solución de Problemas

### Fallos de Construcción

Si la construcción del APK falla, revisa los archivos de registro:
- `log/build.log` - Errores de compilación del APK
- `log/sign.log` - Errores de firma del APK

### Problemas Comunes

**Variables de Entorno no Configuradas:**
```
ERROR: JAVA_HOME is not set
ERROR: ANDROID_HOME is not set
```
**Solución:** Instala Java JDK y Android SDK, luego configura las variables de entorno.

**Icono no Encontrado:**
```
Error: Icon file not found at 'path/to/icon'
```
**Solución:** Verifica que la ruta del icono sea correcta y que el archivo exista.

**Archivo ZIP Inválido:**
```
Error: Invalid zip file
```
**Solución:** Asegúrate de que tu proyecto esté correctamente comprimido como un archivo ZIP.

---

## 🖥️ Soporte de Plataforma

| Plataforma | Estado | Notas |
|----------|--------|-------|
| Windows | ✅ Soportado | Probado en Windows 10/11 |
| macOS | ✅ Soportado | Probado en macOS 11+ |
| Linux | ✅ Soportado | Ubuntu, Debian, Kali, Parrot, Arch |

---

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la Licencia (GPL)[./LICENSE].

---

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Siéntete libre de:
- Reportar errores
- Sugerir nuevas funciones
- Enviar pull requests

---

## 📬 Soporte

Si encuentras algún problema o tienes preguntas:
- Abre un [issue](https://github.com/77AXEL/Web2APK/issues)
- Revisa las [discusiones](https://github.com/77AXEL/Web2APK/discussions) existentes

---
