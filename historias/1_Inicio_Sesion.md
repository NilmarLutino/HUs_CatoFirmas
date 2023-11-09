# Historia de Usuario 1 - Inicio de sesión de los usuarios.

- **Yo como**: Usuario de la aplicación.
- **Quiero**: Iniciar sesión de manera segura y rápida.
- **Para**: Acceder a las funcionalidades de la aplicación, incluyendo la creación y firma de peticiones.

## Pendientes de definición.

1. ¿Se requiere autenticación de dos factores?
   R.
2. ¿Cómo se manejarán los errores de inicio de sesión, como las credenciales incorrectas o las cuentas bloqueadas?
   R.

## Especificación de requerimientos.

1. El sistema debe utilizar Auth0 para la autenticación de usuarios.
2. El inicio de sesión debe soportar tanto autenticación por correo electrónico/contraseña (ejemplo: Google).
3. Después del inicio de sesión exitoso, el usuario debe ser redirigido a la pantalla principal de la aplicación.
4. Los intentos fallidos de inicio de sesión deben proporcionar mensajes de error claros y específicos al usuario.
5. Las sesiones deben tener un tiempo de expiración seguro, después del cual se requerirá que los usuarios vuelvan a iniciar sesión.
6. La interfaz de usuario para el inicio de sesión debe ser clara, intuitiva y accesible.

## Análisis

### Pantalla de inicio de sesión

- **Dado** que el usuario ha llegado a la pantalla de inicio de sesión.
- **Cuando** el usuario ingresa sus credenciales y selecciona 'Iniciar sesión'.
- **Entonces** el sistema debe autenticar al usuario a través de Auth0.
- **Y** si las credenciales son correctas, el usuario es llevado a la pantalla principal de la aplicación.
- **Y** si las credenciales son incorrectas, se muestra un mensaje de error.

## Diseño

1. Para el proceso de autenticación de usuario.
2. El usuario debe realizar el inicio de sesión mediante auth0.

![Alt text](/historias/pantallas/inicio_sesion_auth0.png)

### Pantalla de inicio de sesión Auth0

![Alt text](/historias/pantallas/bbdd_usuario.png.png)
