# Historia de Usuario 2 - Listado de todas las peticiones.

- **Yo como**: Usuario de la aplicación.
- **Quiero**: Ver un listado completo de todas las peticiones disponibles.
- **Para**: Poder navegar a través de las distintas peticiones y explorar su contenido en detalle.

## Pendientes de definición.

1. ¿Necesitamos paginación o cargado infinito para manejar una gran cantidad de peticiones?
   R.
2. ¿Cómo organizaremos el listado? ¿Será por fecha, número de firmas, o algún otro criterio?
   R.

## Especificación de requerimientos.

1. El sistema debe proporcionar una vista del listado completo de peticiones.
2. Cada petición en el listado debe incluir el título, una breve descripción y el número de firmas actuales.
3. El usuario debe tener la opción de seleccionar una petición para ver más detalles o para firmarla.
4. El listado debe actualizarse dinámicamente con nuevas peticiones o cambios en las existentes.

## Análisis

- **Dado** que el usuario desea ver todas las peticiones disponibles.
- **Cuando** el usuario selecciona la opción de ver todas las peticiones desde el menú principal o la pantalla de peticiones.
- **Entonces** el sistema debe hacer una solicitud a `/petitions` para obtener y mostrar todas las peticiones disponibles.

![Alt text](/historias/pantallas/list_of_petitions_page.png)

### Pantalla de listado de peticiones

## Diseño

1. Para obtener el listado completo de peticiones:

Request:

GET BASE_URL/petitions
Accept: Application/json

![Alt text](/historias/pantallas/API_2_list_of_petitions.png)
