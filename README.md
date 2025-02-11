# Instalaciones para iniciar un proyecto con React Native

Este documento detalla los pasos necesarios para configurar el entorno de desarrollo e iniciar un proyecto en React Native. Sigue estas instrucciones para asegurar una configuración correcta y un inicio rápido.

---

## Requisitos previos

Antes de comenzar, asegúrate de tener instalado lo siguiente:

### 1. **Node.js**
- Descarga e instala la versión recomendada de [Node.js](https://nodejs.org/).
- **Versión recomendada**: Usa la versión LTS (Long-Term Support) según la documentación oficial de React Native (actualmente, Node.js 18 o superior).

### 2. **IDE y herramientas de desarrollo**
- **Editor de código**: [Visual Studio Code](https://code.visualstudio.com/) (recomendado).
- **Android Studio**: Para desarrollo en Android. Descárgalo desde [aquí](https://developer.android.com/studio).
- **Xcode**: Para desarrollo en iOS (solo en macOS). Descárgalo desde la [App Store](https://developer.apple.com/xcode/).
- **Homebrew** (opcional pero recomendado en macOS): Facilita la instalación de dependencias. Instálalo ejecutando:
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

### 3. **Instalaciones adicionales**
Después de instalar Homebrew, instala las siguientes herramientas:
- **Node.js** (si no lo has instalado):
  ```bash
  brew install node
  ```
- **Watchman**: Herramienta para observar cambios en los archivos:
  ```bash
  brew install watchman
  ```

### 4. **React Native CLI**
- Instala las herramientas de línea de comandos de React Native:
  ```bash
  npm install -g react-native-cli
  ```
- Verifica que todo esté correctamente instalado:
  ```bash
  npx react-native doctor
  ```
  Sigue las instrucciones para corregir cualquier problema detectado.

---

## Configuración del proyecto

### 1. **Clonar el repositorio**
Clona el repositorio del proyecto y accede a la carpeta:
```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_PROYECTO>
```

### 2. **Instalar dependencias**
Instala todas las dependencias necesarias:
```bash
npm install
```

### 3. **Configurar variables de entorno**
Si el proyecto usa variables de entorno, copia el archivo de ejemplo y edítalo con tus valores:
```bash
cp .env.example .env
```
Asegúrate de configurar correctamente las variables en el archivo `.env`.

---

## Ejecutar el proyecto

### **En Android**
1. Asegúrate de tener un emulador de Android configurado o un dispositivo físico conectado.
2. Ejecuta el proyecto:
   ```bash
   npx react-native run-android
   ```

### **En iOS**
1. Asegúrate de tener Xcode instalado y configurado.
2. Instala las dependencias de CocoaPods:
   ```bash
   cd ios
   pod install
   cd ..
   ```
3. Ejecuta el proyecto:
   ```bash
   npx react-native run-ios
   ```

---

## Resolución de problemas

Si encuentras errores al ejecutar el proyecto, sigue estos pasos:

1. **Verificar dependencias**:
   Ejecuta el siguiente comando para detectar problemas comunes:
   ```bash
   npx react-native doctor
   ```
   Sigue las instrucciones para corregir los errores.

2. **Limpiar la caché**:
   Si el proyecto no se ejecuta correctamente, limpia la caché y reinstala las dependencias:
   ```bash
   rm -rf node_modules package-lock.json
   npm install
   ```

3. **Revisar el emulador/dispositivo**:
   - Asegúrate de que el emulador esté encendido o que el dispositivo físico esté conectado y en modo de desarrollo.
   - En Android, verifica que el dispositivo esté autorizado para desarrollo (sigue las instrucciones en pantalla).

---

## Referencias y apoyo

Para más información sobre la instalación y configuración de React Native, revisa los siguientes recursos:

- **[Documentación oficial de React Native](https://reactnative.dev/docs/set-up-your-environment?platform=android)**: Guía completa para configurar el entorno.
- **[Curso en Udemy: React Native - Fernando Herrera](https://rimac.udemy.com/course/react-native-fh/)**:
  - Sección 1: Instalaciones necesarias y recomendadas.
  - Sección 3: Instalación y configuración de React Native con emuladores y dispositivos.

---
