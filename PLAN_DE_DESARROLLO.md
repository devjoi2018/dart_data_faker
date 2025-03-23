# Plan de Desarrollo: Software Generador de Datos Falsos

## Módulo de Definición de Esquemas

[ ] - **Parser de Sintaxis**: Desarrollo de un parser que interprete la sintaxis personalizada para definir esquemas de datos

- Debe reconocer la declaración de cantidad (schema = X)
- Debe procesar correctamente la jerarquía y anidamiento de elementos
- Debe interpretar los argumentos entre corchetes para cada generador

[ ] - **Validador de Esquemas**: Sistema para validar que los esquemas estén correctamente formados

- Verificación de sintaxis correcta
- Validación de referencias a generadores existentes
- Comprobación de argumentos válidos para cada generador

[ ] - **Sistema de Referencias**: Permitir que los esquemas referencien a otros esquemas

- Referencias simples a otros esquemas completos
- Referencias a secciones específicas de otros esquemas
- Sistema para evitar referencias circulares

[ ] - **Personalización de Salida**: Permitir personalizar el formato de salida

- Formato JSON por defecto
- Opción para CSV, XML, o otros formatos
- Personalización de indentación y estructura

## Módulo de Generadores de Datos Base

[ ] - **Generador de Nombres**: Implementación de generador de nombres de personas

- Nombres femeninos, masculinos o mixtos
- Nombres completos con apellidos
- Soporte para diferentes culturas y regiones
- Argumentos para personalizar longitud y formato

[ ] - **Generador de Datos Personales**: Implementación de datos personales diversos

- Edades con rangos personalizables
- Fechas de nacimiento
- Números de teléfono con formatos por país
- Direcciones de correo electrónico personalizables

[ ] - **Generador de Ubicaciones**: Implementación de datos geográficos

- Países, ciudades, estados
- Códigos postales según formato del país
- Coordenadas GPS con áreas delimitadas
- Direcciones completas con formato realista

[ ] - **Generador de Productos**: Implementación de datos de productos

- Nombres de productos por categoría
- Precios con rangos personalizables
- Descripciones realistas con extensión variable
- URLs de imágenes para visualización

[ ] - **Generador de Textos**: Implementación de textos diversos

- Párrafos con longitud personalizable
- Títulos y subtítulos
- Comentarios y reseñas
- Diferentes estilos y sentimientos

[ ] - **Generador de Datos Financieros**: Implementación de información financiera

- Números de tarjetas de crédito válidos
- Transacciones con montos y fechas
- Cuentas bancarias con formato por país
- Historiales de compras coherentes

[ ] - **Generador de Datos Temporales**: Implementación de fechas y horas

- Fechas pasadas, futuras o en rangos específicos
- Horas en diferentes formatos
- Zonas horarias
- Duraciones y periodos

[ ] - **Generador de Identificadores**: Implementación de IDs y códigos

- IDs secuenciales o aleatorios
- UUIDs/GUIDs
- Códigos de barras válidos
- Identificadores personalizados con patrones

## Sistema de Plugins

[ ] - **Arquitectura de Plugins**: Diseño de la arquitectura extensible

- Interfaz estándar para todos los plugins
- Sistema de carga dinámica de plugins
- Mecanismo para pasar argumentos a plugins

[ ] - **Registro de Plugins**: Sistema para registrar y descubrir plugins

- Validación de nombres únicos
- Prevención de conflictos con generadores existentes
- Verificación de convención de nombres (\*-plug)

[ ] - **Repositorio Central**: Implementación de repositorio para plugins

- API para publicar plugins
- Sistema de versionado
- Acceso exclusivo mediante CLI (sin API directa para instalación)

[ ] - **API de Plugins**: Definición clara de la API para desarrolladores

- Documentación de interfaces
- Ejemplos de implementación
- Herramientas de desarrollo para plugins

[ ] - **Validación de Plugins**: Sistema para validar plugins antes de su uso

- Verificación de seguridad
- Pruebas de rendimiento
- Comprobación de conformidad con estándares

## CLI Interactivo

[ ] - **Interfaz Interactiva**: Desarrollo de CLI con menús interactivos

- Navegación mediante flechas
- Selección con espaciado/enter
- Interfaz colorida y amigable

[ ] - **Detección de Proyectos**: Sistema para detectar esquemas y proyectos

- Escaneo de directorios
- Reconocimiento automático de formatos válidos
- Sugerencias inteligentes

[ ] - **Gestión de Proyectos**: Funcionalidades para administrar proyectos

- Creación de nuevos proyectos
- Edición de esquemas existentes
- Importación/exportación de configuraciones

[ ] - **Gestión de Plugins**: Comandos para administrar plugins exclusivamente desde CLI

- Instalación desde repositorio (única vía oficial)
- Eliminación de plugins instalados
- Visualización de plugins disponibles e instalados
- Actualización de plugins instalados
- Habilitación/deshabilitación temporal de plugins

[ ] - **Generación de Datos**: Comandos para generar datos según esquemas

- Opciones de cantidad
- Selección de formato de salida
- Guardado en diferentes destinos (archivo, clipboard, etc.)

## Servidor API Mock

[ ] - **Servidor HTTP**: Implementación de servidor para servir datos generados

- Soporte para REST API
- Configuración de puertos y rutas
- Documentación automática de endpoints

[ ] - **Rutas Dinámicas**: Generación de rutas basadas en esquemas

- Una ruta por esquema definido
- Anidamiento de rutas según jerarquía de datos
- Personalización de rutas

[ ] - **Métodos HTTP**: Soporte para diferentes métodos HTTP

- GET para obtener datos
- POST/PUT para simular creación/actualización
- DELETE para simular eliminación
- Respuestas coherentes para cada método

[ ] - **Características Avanzadas**: Implementación de funcionalidades adicionales

- Paginación de resultados
- Filtrado por parámetros
- Ordenamiento de datos
- Búsqueda en datos generados

[ ] - **Simulación de Condiciones Reales**: Características para replicar entornos reales

- Latencia configurable
- Errores aleatorios controlados
- Limitación de velocidad
- Autenticación simulada

## Sistema de Persistencia

[ ] - **Almacenamiento de Esquemas**: Sistema para guardar esquemas definidos

- Formato estándar para esquemas
- Versionado de esquemas
- Organización en proyectos/carpetas

[ ] - **Configuraciones de Usuario**: Almacenamiento de preferencias

- Configuraciones globales
- Preferencias por proyecto
- Historial de uso

[ ] - **Exportación/Importación**: Funcionalidades para compartir configuraciones

- Exportación a archivos portables
- Importación desde diferentes fuentes
- Migración entre versiones

## Documentación y Ejemplos

[ ] - **Documentación de Sintaxis**: Documentación detallada del lenguaje de esquemas

- Referencia completa de sintaxis
- Ejemplos para cada construcción
- Buenas prácticas

[ ] - **Documentación de Generadores**: Documentación de todos los generadores incluidos

- Lista completa de generadores disponibles
- Argumentos aceptados por cada generador
- Ejemplos de uso para cada generador

[ ] - **Ejemplos Prácticos**: Colección de ejemplos para casos de uso comunes

- Datos de usuarios
- Catálogos de productos
- Datos financieros
- Sistemas de comentarios/reseñas

[ ] - **Guías de Desarrollo de Plugins**: Documentación para desarrolladores de plugins

- Tutorial paso a paso
- Plantillas de plugins
- Referencias de API

## Ejemplo Ampliado de Declaración de Esquema

```
// Genera 500 usuarios con perfiles completos
schema = 500 :
    // Información básica del usuario
    id > uuid // Genera identificadores únicos
    username > [length=8-15, alphanumeric] // Nombres de usuario de 8-15 caracteres alfanuméricos
    email > [domain=tech-company, format=firstname.lastname] // Correos con dominio de empresas tecnológicas
    password > [length=10-16, strength=high] // Contraseñas fuertes

    // Datos personales
    personal_info :
        name > [gender=mix, region=latinamerica] // Nombres mixtos de Latinoamérica
        age > [range=18-65] // Edades entre 18 y 65 años
        birthdate > [from=1956-01-01, to=2004-12-31] // Fechas de nacimiento en ese rango
        phone > [country=mx,ar,co,pe,cl] // Teléfonos de países latinoamericanos

        // Dirección anidada
        address :
            street > [country=${parent.country}] // Calle coherente con el país del teléfono
            city > [country=${parent.country}] // Ciudad del mismo país
            postal_code > [country=${parent.country}] // Código postal válido para ese país
            geo :
                lat > [precision=6] // Latitud con 6 decimales
                lng > [precision=6] // Longitud con 6 decimales

    // Historial de compras (relación con otro esquema)
    purchase_history = [0-20] : // Entre 0 y 20 compras por usuario
        id > [sequential=global] // ID secuencial global (no reinicia para cada usuario)
        date > [range=past-2-years] // Fecha en los últimos 2 años
        amount > [currency=usd, range=10-1000] // Monto entre $10 y $1000 USD
        status > [options=completed,pending,refunded, weights=70,20,10] // Estados con pesos

        // Productos comprados (3-8 por compra)
        products = [3-8] :
            product_id > [range=1000-9999] // ID de producto
            name > product-tech-plug[category=electronics] // Usa el plugin de productos tecnológicos
            price > [range=5-500, precision=2] // Precio entre $5 y $500 con 2 decimales
            quantity > [range=1-5] // Cantidad entre 1 y 5
            discount > [percentage=0-30] // Descuento entre 0% y 30%

    // Actividad en la plataforma
    activity :
        last_login > [range=past-30-days] // Último inicio de sesión en los últimos 30 días
        session_count > [range=1-500] // Número de sesiones
        active_days = [1-30] > [within=past-90-days] // Días activos en los últimos 90 días
        preferences :
            theme > [options=light,dark,system, weights=40,40,20] // Preferencia de tema
            notifications > boolean[true-bias=70] // Preferencia de notificaciones con 70% true
            language > [options=es,en,pt,fr, weights=40,30,20,10] // Idioma preferido

    // Relaciones sociales (grafo social)
    social :
        followers = [0-1000] > [unique, from=user.id] // Seguidores únicos (IDs de otros usuarios)
        following = [0-500] > [unique, from=user.id] // Seguidos (IDs de otros usuarios)
        posts = [0-100] : // 0-100 publicaciones
            id > [sequential=user] // ID secuencial por usuario
            content > text[paragraphs=1-3, sentiment=random] // Texto con 1-3 párrafos
            date > [after=${parent.parent.personal_info.birthdate}, before=now] // Fecha coherente
            likes > [range=0-2000] // Cantidad de likes
            comments = [0-50] : // 0-50 comentarios
                user_id > [from=user.id, not=${parent.parent.parent.id}] // ID de otro usuario
                text > text[words=5-30, sentiment=random] // Texto de 5-30 palabras
                date > [after=${parent.date}] // Fecha posterior a la publicación
```

Este ejemplo muestra un esquema complejo para generar 500 perfiles de usuario con información personal, historial de compras, actividad en la plataforma y relaciones sociales. Incluye uso de plugins, relaciones entre datos, anidamiento de estructuras y argumentos personalizados.
