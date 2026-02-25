# Guía de Despliegue (Publicar en Internet)

Tu aplicación está lista para ser publicada. Sigue estos pasos para subirla a un servidor gratuito y profesional como **Netlify**.

## 1. Preparación
El proyecto ya ha sido construido correctamente. La carpeta `dist` contiene todos los archivos optimizados para producción.

## 2. Opción Recomendada: Netlify (Gratis y Rápido)

### Paso 1: Crear cuenta
1. Ve a [netlify.com](https://www.netlify.com) y regístrate (es gratis).

### Paso 2: Subir el proyecto
Tienes dos opciones:

**Opción A: Arrastrar y Soltar (Más fácil)**
1. En tu computadora, abre la carpeta del proyecto: `D:\PROGRAMAS\Pagina Integra-tech\integra-tech`.
2. Busca la carpeta llamada `dist` (se acaba de crear).
3. En el panel de Netlify, busca la zona que dice "Drag and drop your site output folder here".
4. Arrastra la carpeta `dist` completa ahí.
5. ¡Listo! Tu sitio estará en línea en segundos.

**Opción B: Conectar con GitHub (Profesional)**
1. Sube este código a un repositorio de GitHub.
2. En Netlify, selecciona "Import from Git".
3. Elige tu repositorio.
4. En "Build command" pon: `npm run build`.
5. En "Publish directory" pon: `dist`.

### Paso 3: Configurar Variables de Entorno (IMPORTANTE)
Para que el inicio de sesión y la base de datos funcionen, necesitas configurar las claves secretas en el servidor:

1. En el panel de tu sitio en Netlify, ve a **Site configuration** > **Environment variables**.
2. Agrega las siguientes variables (cópialas de tu archivo `.env` local):
   - `VITE_SUPABASE_URL`: (Tu URL de Supabase)
   - `VITE_SUPABASE_ANON_KEY`: (Tu clave anónima de Supabase)
   - `VITE_SUPABASE_SERVICE_ROLE_KEY`: (Tu clave de servicio, si la usas en funciones serverless, aunque para este frontend puro solo las dos primeras son críticas para el cliente).

## 3. Verificar Dominio
Netlify te dará un dominio tipo `tusitio.netlify.app`. Puedes cambiarlo en "Domain settings" o comprar un dominio `.com` propio y conectarlo ahí.

## 4. Verificar Funcionalidad
Una vez publicado:
1. Entra a tu nueva URL.
2. Prueba iniciar sesión (la base de datos es la misma, así que tus usuarios seguirán funcionando).
3. Prueba hacer una compra (recibirás el correo simulado en la notificación).

¡Felicidades! Tu plataforma educativa y tienda online ya es accesible para todo el mundo.
