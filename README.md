# Frontend Project - Local Setup

Este documento explica los pasos necesarios para configurar y ejecutar el proyecto frontend de forma local.

---

## Requisitos Previos

Antes de comenzar, asegúrate de tener instaladas las siguientes herramientas en tu dispositivo:

- [Node.js 18.19.0](https://nodejs.org/es)  
  Asegúrate de instalar esta versión para evitar problemas de compatibilidad.
- [npm (Node Package Manager)](https://docs.npmjs.com/cli/v8)  
  Incluido con la instalación de Node.js.

---

## Instalación de Dependencias

Ejecuta los siguientes comandos en la terminal dentro de la carpeta raíz del proyecto:

npm install

Esto instalará todas las dependencias necesarias para el proyecto.

---

## Configuración del Proyecto

1. **Archivo de configuración del backend**:  
   Abre el archivo `src/app/api/agent.js` y verifica que la URL del backend esté configurada correctamente:

   axios.defaults.baseURL = "https://taller3backend-arqui-latest.onrender.com";

   Si estás trabajando con un backend local, actualiza esta línea con la URL local del backend. Por 
   axios.defaults.baseURL = "http://localhost:4000";

2. **Asegúrate de que las credenciales del backend sean válidas**:  
   Si el backend requiere un token o credenciales adicionales, configura el archivo `.env` en el backend para facilitar la conexión.

---

## Ejecución del Proyecto en Modo Local

Para iniciar el servidor de desarrollo, ejecuta el siguiente comando:

npm start

El proyecto estará disponible en [http://localhost:3000](http://localhost:3000).

---

## Generación de la Build de Producción

Si necesitas crear una versión optimizada del proyecto para producción, usa el siguiente comando:

npm run build

Esto generará una carpeta `build` con los archivos listos para ser desplegados en cualquier servicio de hosting.

---

## Notas Adicionales

1. **Conexión con el Backend**:  
   - Si encuentras problemas de conexión con el backend, verifica la configuración en `agent.js` y asegúrate de que la URL base del backend sea correcta.
   - Si el backend utiliza cookies para la autenticación, asegúrate de que `axios.defaults.withCredentials = true` esté configurado en `agent.js`.

2. **Problemas con Dependencias**:  
   - Si alguna dependencia genera errores durante la instalación o ejecución, verifica que estás utilizando la versión correcta de Node.js (18.19.0).

3. **Uso de Material-UI, Redux y React**:  
   - Asegúrate de que las versiones de estas bibliotecas sean compatibles con las demás dependencias del proyecto.

4. **CORS y Seguridad**:  
   - Si el navegador bloquea solicitudes por problemas de CORS, revisa la configuración del backend para permitir solicitudes desde `http://localhost:3000`.

5. **Logs y Depuración**:  
   - Usa las herramientas de desarrollo del navegador (F12) para monitorear la pestaña **Network** y verificar las solicitudes enviadas al backend.
   - Si encuentras errores, revisa los logs en la consola para identificar problemas.

---

¡Listo! Ahora puedes trabajar con el frontend de manera local 🚀
