# API Vistas

## Descripción
El **Microservicio de Vistas** es una solución diseñada para gestionar eficientemente la visualización de contenidos dentro de una plataforma. Su objetivo principal es recopilar y procesar datos relacionados con las vistas de contenido por parte de los usuarios, proporcionando estadísticas en tiempo real y ofreciendo recomendaciones personalizadas basadas en el comportamiento del usuario. Este microservicio se comunica de manera fluida con otros microservicios y el frontend para asegurar que la experiencia del usuario sea dinámica y personalizada.

### Funcionalidades Principales

- **Gestión de Vistas**:
  - **Registro de Vistas**: Permite registrar las vistas de contenido realizadas por los usuarios, guardando información detallada sobre qué contenido se ha visualizado, cuándo y por cuánto tiempo.
  - **Consulta de Vistas**: Facilita la consulta de las vistas de contenidos, lo que permite generar estadísticas sobre los contenidos más visualizados y la actividad de los usuarios.
  - **Actualización de Datos de Vistas**: Proporciona la capacidad de actualizar los datos de las vistas, como el tiempo total de visualización o la interacción con el contenido.
  - **Eliminación de Vistas**: Permite eliminar registros de vistas antiguas o innecesarias, asegurando que los datos de la plataforma estén actualizados y sean precisos.

- **Integración con Microservicios**:
  - **Microservicio de Usuarios**: Se comunica con la API de usuarios para asociar las vistas a usuarios específicos, permitiendo la personalización de recomendaciones basadas en sus interacciones pasadas.
  - **Microservicio de Contenidos**: Recibe datos sobre el contenido visualizado por los usuarios, lo que permite generar estadísticas de popularidad y ajustar las recomendaciones personalizadas.
  - **Microservicio de Recomendaciones**: Utiliza los datos de vistas para ofrecer recomendaciones de contenidos más precisas y relevantes para los usuarios, adaptadas a sus intereses y comportamientos de visualización.

- **Interacción con el Frontend**:
  - El microservicio expone una API REST que permite al frontend acceder a estadísticas de vistas y personalizar la experiencia del usuario con recomendaciones en tiempo real.
  - Soporte para consultas en tiempo real que permiten actualizar las vistas y estadísticas dinámicamente en la interfaz de usuario.

### Beneficios Clave

- **Eficiencia en el Manejo de Vistas**: Diseñado para manejar grandes cantidades de vistas de contenido sin afectar el rendimiento de la plataforma.
- **Recomendaciones Personalizadas**: Gracias a la integración con el microservicio de contenidos y la API de usuarios, este servicio ofrece recomendaciones de contenido altamente relevantes para cada usuario.
- **Escalabilidad**: Al ser parte de una arquitectura de microservicios, el sistema es fácilmente escalable para gestionar un número creciente de usuarios y vistas.
- **Mejora de la Experiencia de Usuario**: Las estadísticas y recomendaciones personalizadas mejoran la experiencia del usuario al ofrecer contenido relevante y ajustado a sus intereses.

### Casos de Uso

1. **Registro de una Vista**:
   Cada vez que un usuario visualiza un contenido, la API registra la vista en el sistema. Esto incluye detalles sobre el contenido, el tiempo de visualización y la interacción del usuario.

2. **Consulta de Estadísticas de Vistas**:
   Un administrador o sistema automatizado puede consultar las estadísticas de vistas para ver qué contenidos están siendo más visualizados por los usuarios, lo que permite ajustar las recomendaciones y la oferta de contenido.

3. **Actualización de Datos de Vistas**:
   Si un usuario vuelve a interactuar con un contenido o realiza una acción adicional sobre un contenido ya visto, el microservicio actualiza los datos asociados a esa vista, como el tiempo total de visualización.

4. **Eliminación de Registros de Vistas**:
   Un usuario o administrador puede eliminar registros de vistas antiguas, asegurando que la plataforma solo mantenga datos actuales y relevantes.

5. **Recomendaciones Personalizadas**:
   Utilizando el comportamiento de visualización de los usuarios, el microservicio de vistas trabaja en conjunto con el microservicio de recomendaciones para sugerir contenidos que coincidan con los intereses específicos de los usuarios, mejorando su experiencia dentro de la plataforma.

---
## 📃 Más Información sobre el Método de Desarrollo

[Infome de la Tercera Entrega](https://github.com/UExGPSASEE/proyecto24-ga02/wiki/🗃%EF%B8%8FInforme-de--Tercera-entrega)

## Requisitos  
Python 3.5.2 o superior  

## Uso  
Para ejecutar el servidor, por favor sigue los siguientes pasos desde el directorio raíz:  

```
pip3 install --no-cache-dir -r requeriments_sqlalchemy.txt
pip3 install -r requirements.txt
python3 -m openapi_server
```

Luego, abre tu navegador y dirígete a la siguiente URL:

```
http://localhost:8080/ui/
```