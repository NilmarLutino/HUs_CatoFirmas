# Historia de Usuario 7 - Publicación por petición.

- **Yo como**: Usuario de la aplicación.
- **Quiero**: Ver las publicaciones asociadas a una petición específica.
- **Para**: Entender mejor el contexto y los argumentos alrededor de la petición y participar en la discusión.

## Pendientes de definición.

1. ¿Necesitaremos mostrar algún tipo de resumen o las publicaciones más destacadas primero?
   R.
2. ¿Cómo moderaremos las publicaciones para evitar contenido inapropiado o spam?
   R.

## Especificación de requerimientos.

1. Los usuarios deben poder acceder a una lista de publicaciones relacionadas con una petición específica.
2. La lista debe incluir detalles como el autor de la publicación, fecha de publicación y un extracto del contenido.
3. El sistema debe permitir a los usuarios abrir una publicación completa para leerla.
4. Debe haber una manera eficiente de cargar y mostrar las publicaciones para mejorar la experiencia del usuario.

## Análisis

- **Dado** que el usuario está visualizando una petición específica.
- **Cuando** el usuario selecciona la opción para ver publicaciones relacionadas con la petición.
- **Entonces** el sistema debe hacer una solicitud a `/petitions/{id}/publications` para obtener y mostrar las publicaciones vinculadas a esa petición.

## Diseño

![Alt text](/historias/pantallas/sign_publications_page.png)

### Pantalla de publicaciones por petición

1. Para obtener las publicaciones asociadas a una petición específica:

Request:

GET BASE_URL/petitions/{id}/publications
Accept: Application/json

![Alt text](/historias/pantallas/API_11_publications_page.png)

## BBDD

![Alt text](/historias/pantallas/bbdd_publicaciones.png.png)
