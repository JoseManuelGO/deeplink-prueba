# MiTec Deeplink Test

Una aplicación web para probar deeplinks de las aplicaciones móviles MiTec (Estudiantes y Colaboradores).

## 🚀 Demo

**URL de la aplicación**: [https://deeplink-test-mobile.web.app](https://deeplink-test-mobile.web.app)

## 📱 Descripción

Esta aplicación web permite probar deeplinks para las aplicaciones móviles MiTec:

- **MiTec Estudiantes**: `mitecestudiantes://`
- **MiTec Colaboradores**: `miteccolaboradores://`

### Características principales

- ✅ **Deeplinks predefinidos** para rutas comunes
- 🔧 **Generador de deeplinks personalizados**
- 📋 **Comandos ADB** para testing en emuladores
- 🎯 **Ejecución automática** desde parámetros de URL
- 📱 **Optimizado para GitHub Pages y Firebase Hosting**

## 🛠️ Tecnologías

- **Frontend**: HTML5, CSS3, JavaScript vanilla
- **Hosting**: Firebase Hosting
- **Deeplinks**: Esquemas personalizados para apps móviles

## 📋 Deeplinks disponibles

### MiTec Estudiantes
```
mitecestudiantes://mi-perfil?isAccessRoute=true
mitecestudiantes://idDigital
mitecestudiantes://home?isAccessRoute=true
mitecestudiantes://calificaciones?isAccessRoute=true
mitecestudiantes://horario-estudiante?isAccessRoute=true
mitecestudiantes://estado-cuenta?isAccessRoute=true
```

### MiTec Colaboradores
```
miteccolaboradores://id-colaboradores
```

## 🚀 Instalación y Despliegue

### Prerrequisitos
- Node.js y npm instalados
- Cuenta de Firebase
- Firebase CLI instalado

### Pasos para desplegar

1. **Instalar Firebase CLI** (si no está instalado):
```bash
npm install -g firebase-tools
```

2. **Iniciar sesión en Firebase**:
```bash
firebase login
```

3. **Inicializar el proyecto**:
```bash
firebase init hosting
```

4. **Desplegar la aplicación**:
```bash
firebase deploy --only hosting:deeplink-test
```

## 📁 Estructura del proyecto

```
deeplink-prueba/
├── public/
│   └── index.html          # Aplicación principal
├── firebase.json           # Configuración de Firebase
├── .firebaserc            # Configuración del proyecto
└── README.md              # Este archivo
```

## 🔧 Configuración de Firebase

El proyecto está configurado con múltiples sitios de hosting:

- **Sitio principal**: `superapp-mitec-colaboradores.web.app`
- **Sitio de testing**: `deeplink-test-mobile.web.app`

### Comandos de despliegue

```bash
# Desplegar solo el sitio de deeplinks
firebase deploy --only hosting:deeplink-test

# Desplegar todos los sitios
firebase deploy --only hosting
```

## 🧪 Testing

### Métodos de prueba

1. **Clic directo**: Haz clic en cualquier deeplink de la interfaz
2. **Comando ADB**: Copia y ejecuta el comando ADB en tu terminal
3. **Emulador**: Abre la URL en el navegador de tu emulador Android

### Comando ADB de ejemplo

```bash
adb shell am start -W -a android.intent.action.VIEW -d "mitecestudiantes://mi-perfil?isAccessRoute=true" com.tec.mitecapp
```

## 🔗 Parámetros de URL

La aplicación soporta parámetros de URL para ejecución automática:

```
https://deeplink-test-mobile.web.app?fromemail=mi-perfil/id:123
```

### Formato de parámetros

- **Parámetro**: `fromemail`
- **Formato**: `ruta/parametro:valor`
- **Ejemplo**: `mi-perfil/id:123` → `mitecestudiantes://mi-perfil?id=123`

## 🎨 Características de la UI

- **Diseño responsive** para móviles y escritorio
- **Animaciones suaves** y efectos visuales
- **Interfaz intuitiva** con botones y estados visuales
- **Generador de deeplinks** con toggle entre apps
- **Feedback visual** para todas las acciones

## 📱 Compatibilidad

- ✅ **Navegadores modernos** (Chrome, Firefox, Safari, Edge)
- ✅ **Dispositivos móviles** (iOS, Android)
- ✅ **Emuladores Android** (con ADB)
- ✅ **GitHub Pages** (sin restricciones de seguridad)

## 🔒 Seguridad

- Los deeplinks solo funcionan si las aplicaciones están instaladas
- No se almacenan datos sensibles
- Compatible con políticas de seguridad de navegadores modernos

## 🤝 Contribución

Para contribuir al proyecto:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Crea un Pull Request

## 📄 Licencia

Este proyecto es para uso interno del Tecnológico de Monterrey.

## 👥 Contacto

- **Proyecto**: MiTec Deeplink Test
- **URL**: [https://deeplink-test-mobile.web.app](https://deeplink-test-mobile.web.app)
- **Firebase Console**: [https://console.firebase.google.com/project/superapp-mitec-colaboradores](https://console.firebase.google.com/project/superapp-mitec-colaboradores)

---

**Desarrollado para el Tecnológico de Monterrey** 🎓
