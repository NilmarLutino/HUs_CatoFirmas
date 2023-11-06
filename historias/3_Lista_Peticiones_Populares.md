# Historia de Usuario 3 - Listado de peticiones populares.

- **Yo como**: Usuario de la aplicación.
- **Quiero**: Ver un listado de las peticiones más populares.
- **Para**: Tener una vista rápida de las peticiones que están recibiendo más atención y firmas.

## Pendientes de definición.

1. ¿Cómo definimos "popular" en el contexto de nuestra aplicación?
   R.
2. ¿Existe un límite en el tiempo para que una petición sea considerada "popular"?
   R.

## Especificación de requerimientos.

1. El sistema debe destacar las 3 peticiones más populares en la parte superior de la página principal.
2. Cada petición en el listado de populares debe incluir el título, una breve descripción y el número de firmas actuales.
3. El listado de peticiones populares debe actualizarse dinámicamente basado en la popularidad y las firmas recientes.

## Análisis

- **Dado** que el usuario ha iniciado sesión y accede a la pantalla principal de peticiones.
- **Cuando** la pantalla se carga por primera vez.
- **Entonces** el sistema debe hacer una solicitud a `/popularpetitions` para obtener y mostrar las 3 peticiones más populares.

![Alt text](/historias/pantallas/home_page.png)

### Pantalla de listado de peticiones populares

## Diseño

1. Para obtener las peticiones más populares:

Request:

GET BASE_URL/popularpetitions
Accept: Application/json

![Alt text](/historias/pantallas/API_1_popular_petitions.png)
