# Laravel User Authentication and Email Notifications Project(Actividad 9)

## Overview

Este proyecto es una aplicación Laravel 7 que implementa un sistema de autenticación de usuarios con funcionalidad adicional para enviar notificaciones por correo electrónico. El proyecto distingue entre usuarios no registrados y registrados redirigiéndolos a una **Landing Page** o a un **Dashboard**, respectivamente. Además, se envían notificaciones por correo electrónico en los siguientes eventos:
- **Correo de bienvenida** al registrar un usuario.
- **Alerta de inicio de sesión** al iniciar sesión un usuario.

## Features

1. **Landing Page para usuarios no registrados**: 
   - Los usuarios que visitan la aplicación sin iniciar sesión son dirigidos a una página de bienvenida (landing page).
   
2. **Dashboard para usuarios registrados**: 
   - Los usuarios registrados son redirigidos a un dashboard después de iniciar sesión.
   
3. **Autenticación de usuarios**: 
   - Registro, inicio de sesión y cierre de sesión.
   
4. **Notificaciones por correo**:
   - **Correo de bienvenida**: Enviado cuando un usuario se registra.
   - **Alerta de inicio de sesión**: Enviada cuando un usuario inicia sesión.

## Project Structure

- **Landing Page**: Se muestra a los usuarios no registrados o invitados.
- **Dashboard**: Se muestra a los usuarios autenticados.
- **Navbar**: Las opciones cambian dependiendo del estado de autenticación del usuario (Login/Register o Dashboard/Logout).
  
## Instalación

### Requisitos
- Laravel 7.x
- Composer
- Node.js & npm
- XAMPP, WAMP, MAMP, LAMP o Laragon para el desarrollo local.
- Un servicio de correo configurado en el archivo `.env` (por ejemplo, Gmail, Mailgun, etc.).

### Pasos

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/Villatoro20/activity9/tree/main
   cd activity-9
2. **Instalar dependecnias**:
- composer install
- npm install
- npm run dev
3. **Configurar el archivo .env: Copia el archivo .env.example a .env y configura tu base de datos y los ajustes de correo.**:
- MAIL_MAILER=smtp
- MAIL_HOST=smtp.gmail.com
- MAIL_PORT=587
- MAIL_USERNAME=tu_correo@gmail.com
- MAIL_PASSWORD=tu_contraseña
- MAIL_ENCRYPTION=tls
- MAIL_FROM_ADDRESS=tu_correo@gmail.com
- MAIL_FROM_NAME="${APP_NAME}"

## Notificaciones por correo
El proyecto incluye notificaciones por correo para dos eventos clave:

- Correo de bienvenida: Enviado cuando un usuario se registra. Este correo le da la bienvenida y le proporciona información básica sobre la plataforma.
- Alerta de inicio de sesión: Enviada cuando un usuario inicia sesión, notificando el inicio de sesión y proporcionando una medida de seguridad en caso de que no haya sido él.
Cómo funciona
- Correo de bienvenida: Enviado automáticamente después del proceso de registro.
- Alerta de inicio de sesión: Enviada inmediatamente después de un inicio de sesión exitoso.
- Configurar correo en .env
- Asegúrate de que tu archivo .env tenga la configuración de correo correcta, como se describe anteriormente. Esto permite que el sistema envíe las notificaciones necesarias.

## Uso
- Usuarios no registrados: Cuando un usuario que no ha iniciado sesión visita la URL raíz (/), verá la página de bienvenida. Esta página ofrece una introducción general e invita al usuario a registrarse o iniciar sesión.

- Usuarios registrados: Una vez que un usuario se registra o inicia sesión, es redirigido al dashboard. El dashboard solo es accesible para los usuarios autenticados.

- Notificaciones: Tras un registro exitoso, el usuario recibirá un correo de bienvenida. Después de iniciar sesión, recibirá una alerta de inicio de sesión.

## Tecnologías utilizadas
- Laravel 7: Framework de PHP utilizado para la construcción de la aplicación web.
- Bootstrap: Utilizado para el diseño del frontend (incluido con el paquete laravel/ui de Laravel).
- Servicios de correo: Configurado mediante SMTP para el envío de notificaciones.
