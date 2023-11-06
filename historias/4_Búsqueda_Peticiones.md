# Historia de Usuario 4 - Búsqueda de peticiones en Lista de Peticiones.

- **Yo como**: Usuario de la aplicación.
- **Quiero**: Poder buscar peticiones específicas dentro de la lista de peticiones.
- **Para**: Encontrar rápidamente peticiones que me interesan sin tener que navegar por toda la lista.

## Pendientes de definición.

1. ¿Qué campos serán considerados en la búsqueda (título, descripción, etc.)?
   R.
2. ¿Se debería permitir búsqueda avanzada con filtros y categorías?
   R.

## Especificación de requerimientos.

1. La funcionalidad de búsqueda debe ser fácilmente accesible en la pantalla de lista de peticiones.
2. Los usuarios deben poder ingresar términos de búsqueda para filtrar las peticiones por título y descripción.
3. La búsqueda y el filtrado se realizarán en el cliente utilizando Vue.js para proporcionar resultados en tiempo real sin necesidad de recargar la página.
4. La interfaz de usuario para la búsqueda debe ser intuitiva y proporcionar una retroalimentación clara de los resultados de la búsqueda.
5. Los resultados de la búsqueda deben actualizarse dinámicamente a medida que el usuario escribe su consulta.

## Análisis

- **Dado** que el usuario está en la pantalla de lista de peticiones.
- **Cuando** el usuario ingresa un término de búsqueda en el campo de búsqueda.
- **Entonces** la aplicación debe filtrar la lista de peticiones en tiempo real y mostrar solo las peticiones que coinciden con los términos de búsqueda.

## Diseño

![Alt text](/historias/pantallas/list_of_petitions_page.png)

### Pantalla de lista de peticiones con funcionalidad de búsqueda

1. Para la interacción de búsqueda y filtrado de peticiones:

- Se proporcionará un campo de texto claro en la parte superior de la lista de peticiones.
- A medida que el usuario escribe, los resultados de la lista se filtrarán utilizando las capacidades reactivas de Vue.js.
- No se requieren peticiones adicionales al servidor para realizar la búsqueda, ya que se manejará íntegramente en el front-end.
