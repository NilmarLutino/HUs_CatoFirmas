# Historia de Usuario 6 - Registro de una petición.

- Yo como: Usuario de la aplicación.
- Quiero: Registrar una petición para que los usuarios puedan firmarla y apoyarla.
  . Para: Alzar la solicitud de una petición a las autoridades de la Universidad Católica Boliviana "San Pablo" Regional La Paz.

## Pendientes de definición.

1. ¿Qué información se debe registrar?
   R.
2. ¿La cantidad máxima de palabras para la petición es aceptable?
   R.

## Especificación de requerimientos.

1. La cantidad maxima de fotos es de 1 para la identificación de la petición.
2. La imagen debe estar en formato JPG, tamaño máximo de 10MB. Resolución mínima de 50ppi.
3. El contenido de la petición debe ser verificado por la aplicación para su aprobación.
4. La petición debe tener un mínimo de 10 palabras y un máximo de 250 palabras.
5. El título de la petición debe tener un mínimo de 3 palabras y un máximo de 10 palabras.
6. El título de la petición debe ser verificado por la aplicación para su aprobación.
7. El título de la petición debe ser único.
8. La petición debe registrar un objetivo de firmas mínima de 1 firma.

## Analisis

### Pantalla de creacion de nueva subasta

A continuación se presenta la pantalla de creación de una nueva petición, cuyo funcionamiento es.

1. El usuario hizo clic previamente en Crear Nueva Petición.

![Alt text](/historias/pantallas/lista_mis_peticiones.png)

### Pantalla de Lista de las peticiones del usuario

2. El usuario deberá subir una imagen de la petición.
3. El usuario deberá ingresar el título de la petición.
4. El usuario deberá ingresar el contenido de la petición.
5. El usuario deberá ingresar el objetivo de firmas de la petición.
6. El usuario registrará su petición haciendo clic en el botón "Registrar Mi Petición".

7. El usuario hizo clic previamente en Crear Nueva Subasta.
8. El usuario deberá tener lista las images...

![Alt text](/historias/pantallas/registrar_peticion.png)

### Pantalla de registro de petición

## Criterios de Aceptación

### Validación de cantidad de imágenes

- **Dado** que el usuario ha iniciado sesión y está en la pantalla de crear una nueva petición.
- **Cuando** el usuario intenta guardar la petición.
- **Entonces** el sistema debe validar que el usuario haya subido exactamente 1 imagen.

### Validación del título de la petición

- **Dado** que el usuario ha iniciado sesión y está en la pantalla de crear una nueva petición.
- **Cuando** el usuario introduce un título para la petición y intenta guardar la petición.
- **Entonces** el sistema debe validar que el título de la petición contenga un mínimo de 3 palabras y un máximo de 10 palabras.
- **Y** el sistema debe validar que el título de la petición sea único en la base de datos de peticiones.

### Validación del contenido de la petición

- **Dado** que el usuario ha iniciado sesión y está en la pantalla de crear una nueva petición.
- **Cuando** el usuario introduce el contenido de la petición y intenta guardar la petición.
- **Entonces** el sistema debe validar que el contenido de la petición contenga un mínimo de 10 palabras y un máximo de 250 palabras.
- **Y** el sistema debe verificar que el contenido de la petición no contenga lenguaje inapropiado o contra la política de la Universidad.

### Validación del objetivo de firmas de la petición

- **Dado** que el usuario ha iniciado sesión y está en la pantalla de crear una nueva petición.
- **Cuando** el usuario establece un objetivo de firmas para la petición y intenta guardar la petición.
- **Entonces** el sistema debe validar que el usuario haya establecido una meta de firmas que sea un número entero positivo.
- **Y** el sistema debe validar que el número establecido como meta de firmas sea al menos 1.

## Disenio

### Pantalla de creacion de nueva petición

1. Para insertar la imagen de la petición:

Request:

```
POST BASE_URL/media
Accept: Application/json
Authorization: Bearer JWT
```

![Alt text](/historias/pantallas/API_22_Subir_imagen.png.png)

2. Para crear la petición:

Request:

```
POST BASE_URL/petitions
Accept: Application/json
Authorization: Bearer JWT
```

![Alt text](/historias/pantallas/API_4_Guardar_Peticion.png.png)
