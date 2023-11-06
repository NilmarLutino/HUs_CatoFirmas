# Historia de Usuario - Firmar Petición

- Yo como: Usuario de la aplicación.
- Quiero: Poder firmar una petición para mostrar mi apoyo a una causa.
- Para: Participar en el proceso de apoyo a las peticiones y mostrar mi interés en un tema específico.

## Pendientes de definición.

1. ¿Dónde puedo encontrar las peticiones disponibles para firmar?
   R.
2. ¿Puedo dejar comentarios o sugerencias al firmar una petición?
   R.

## Especificación de requerimientos.


1. Cada petición debe mostrar un título, una descripción breve y la cantidad actual de firmas.
2. Los usuarios pueden hacer clic en una petición para ver más detalles y firmarla.
3. Los usuarios deben confirmar al firmar una petición.

## Análisis


### Pantalla de Detalles de la Petición

1. El usuario hace clic en una petición para ver más detalles y firmarla.
2. En la pantalla de detalles de la petición, el usuario ve información detallada sobre la petición, incluyendo su título, descripción completa y la cantidad actual de firmas.

![Detalles de la Petición](/historias/pantallas/detalles_peticion.png)

### Pantalla de Firmar Petición

3. El usuario hace clic en el botón "Firmar" para mostrar su apoyo a la petición.
4. El usuario debe confirmar su intencion de firmar luego de apretar el boton "Firmar"

![Firmar Petición](/historias/pantallas/firmar_peticion.png)

## Criterios de Aceptación


### Firma de una Petición

- **Dado** que el usuario ha iniciado sesión en la aplicación y está viendo los detalles de una petición.
- **Cuando** el usuario confirma su intenciond de apoyo
- **Y** el usuario hace clic en el botón "Firmar".
- **Entonces** el sistema debe registrar la firma del usuario en la petición.
- **Y** el sistema debe mostrar la cantidad actualizada de firmas en la petición.



## Disenio

### Pantalla de informacion de una peticion

1. Para obtener los datos de una peticion:

Request:

```
GET BASE_URL/petitions { id }/information
Accept: Application/json
Authorization: Bearer JWT
```

![Alt text](/historias/pantallas/API_7_Obtener_Informacion_Peticion.png)

2. Para firmar una peticion:

Request:

```
POST BASE_URL/petitions/ { id }/signatures
Accept: Application/json
Authorization: Bearer JWT
```

![Alt text](/historias/pantallas/API_16_Firmar_Peticion.png)

3. Para ver las firmas de una peticion:

Request:

```
GET BASE_URL/petitions/ { id }/signatures
Accept: Application/json
Authorization: Bearer JWT
```

![Alt text](/historias/pantallas/API_15_Ver_Firmas_Peticion.png)
