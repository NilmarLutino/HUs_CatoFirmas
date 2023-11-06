# Historia de Usuario 8 - Peticiones de Usuario.

- **Yo como**: Usuario registrado en la aplicación.
- **Quiero**: Ver una lista de todas mis peticiones creadas.
- **Para**: Gestionar mis peticiones y ver el estado actual de cada una de ellas.

## Pendientes de definición.

1. ¿Cómo se ordenarán las peticiones en la lista? ¿Por fecha, popularidad, número de firmas?
   R.
2. ¿Deberíamos permitir al usuario realizar acciones sobre las peticiones desde esta lista, como editar o eliminar?
   R.

## Especificación de requerimientos.

1. Los usuarios deben poder ver todas las peticiones que han creado en una lista consolidada.
2. La lista debe proporcionar información clave de cada petición, como el título, la fecha de creación, el número de firmas y el estado de la petición (activo, cerrado, cumplido).
3. Debe ser posible acceder a la lista a través de una sección fácilmente accesible en la interfaz de usuario, como "Mis Peticiones".
4. La interfaz debe ser clara y amigable, permitiendo a los usuarios navegar fácilmente por sus peticiones.

## Análisis

- **Dado** que el usuario ha iniciado sesión en la aplicación.
- **Cuando** el usuario navega a la sección "Mis Peticiones" o equivalente en la aplicación.
- **Entonces** el sistema debe realizar una solicitud a `/petitions/user/{id}` para recuperar las peticiones asociadas con su ID de usuario.

## Diseño

![Alt text](/historias/pantallas/lista_mis_peticiones.png)

### Pantalla de Peticiones de Usuario

1. Para ver las peticiones asociadas con un usuario:

Request:

GET BASE_URL/petitions/user/{id}
Accept: Application/json

![Alt text](/historias/pantallas/API_24_mis_peticiones.png)
