# Taller 3 Frontend

Este proyecto es el frontend desarrollado en React para el Taller 3 de Arquitectura de Sistemas. Está configurado para despliegue en Firebase Hosting con un flujo de CI/CD automatizado mediante GitHub Actions.

## Cómo ejecutar el proyecto localmente

1. **Clona este repositorio**
   ```bash
   git clone https://github.com/alexrf32/Taller3Frontend-1.git
   cd Taller3Frontend
Asegúrate de tener Node.js instalado
Descarga e instala la versión 18.19.0 de Node.js desde este enlace:
Node.js v18.19.0.

Instala las dependencias
Ejecuta el siguiente comando:

npm install
Configura la URL del backend
Abre el archivo src/app/api/agent.ts y actualiza la constante API_URL para apuntar al backend desplegado.

const API_URL = "https://taller3backend-arqui-latest.onrender.com";
Ejecuta el proyecto en modo desarrollo

Inicia el servidor de desarrollo con:
npm start
El proyecto estará disponible en http://localhost:3000.

Despliegue en Firebase Hosting
El frontend está desplegado en Firebase Hosting. Puedes acceder al proyecto en línea en:
https://taller3-frontend.web.app

Cómo realizar un nuevo despliegue manual
Construye el proyecto para producción:

npm run build

Despliega en Firebase Hosting:

firebase deploy

Flujo de CI/CD con GitHub Actions
El proyecto cuenta con un flujo de CI/CD configurado para desplegar automáticamente en Firebase Hosting al realizar un commit en la rama principal.

Configuración del flujo
El workflow de GitHub Actions está definido en .github/workflows/deploy.yml. Sigue estos pasos para verificar la configuración:

Configura el secreto FIREBASE_SERVICE_ACCOUNT

Genera una clave privada en Firebase Console (Configuración > Cuentas de servicio > Generar clave privada).
Agrega el archivo JSON como un secreto en GitHub con el nombre FIREBASE_SERVICE_ACCOUNT.
Realiza un commit en la rama principal
Al realizar un commit en la rama main, el flujo de trabajo automáticamente:

Instalará dependencias.
Construirá la aplicación.
Desplegará la nueva versión en Firebase Hosting.

Información adicional
El backend está disponible en: https://taller3backend-arqui-latest.onrender.com.