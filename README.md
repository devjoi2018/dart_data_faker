# 🪄 Dart Data Faker

![Versión](https://img.shields.io/badge/versión-0.1.0-blue)
![Licencia](https://img.shields.io/badge/licencia-MIT-green)
![Estado](https://img.shields.io/badge/estado-en%20desarrollo-orange)

## 📋 Descripción

**Dart Data Faker** es una potente herramienta CLI para generar datos falsos realistas con un enfoque único: un lenguaje de definición de esquemas flexible y expresivo.

A diferencia de otras bibliotecas de datos falsos, Dart Data Faker te permite definir estructuras de datos complejas y relacionadas entre sí, con una sintaxis clara y concisa.

```
// Un ejemplo simple del lenguaje de esquemas
schema = 10 :
  id > uuid
  nombre > [gender=male, region=latinamerica]
  email > [domain=tech-company]
  edad > [range=18-65]
```

## ✨ Características Principales

- 🎯 **Lenguaje de esquemas expresivo** - Define estructuras de datos complejas con una sintaxis intuitiva
- 🔄 **Datos relacionados** - Crea relaciones entre entidades generadas automáticamente
- 🧩 **Sistema de plugins** - Extiende la funcionalidad con tus propios generadores
- 🖥️ **CLI interactivo** - Interfaz de línea de comandos amigable y potente
- 🌐 **Servidor API Mock** - Crea APIs falsas instantáneamente basadas en tus esquemas
- 📦 **Múltiples formatos** - Genera datos en JSON, CSV, XML y más

## 🚀 ¿Para qué sirve?

- **Desarrollo y pruebas** - Genera datos realistas para probar tus aplicaciones
- **Prototipado rápido** - Crea mocks de APIs sin escribir código del servidor
- **Demostración de productos** - Muestra tus aplicaciones con datos que parecen reales
- **Formación y educación** - Enseña conceptos de manejo de datos con ejemplos realistas
- **Análisis de datos** - Crea conjuntos de datos de prueba con características específicas

## 🎮 Uso básico

```bash
# Generar datos a partir de un esquema
dart_data_faker generate archivo_esquema.df

# Iniciar el servidor API Mock
dart_data_faker serve --port 3000 archivo_esquema.df

# Abrir el CLI interactivo
dart_data_faker interactive
```

## 📚 Documentación

Para información detallada sobre el uso de Dart Data Faker, consulta la documentación:

- [Sintaxis de esquemas](/docs/schema_syntax/) - Aprende a definir tus esquemas
- [Generadores disponibles](/docs/generators/) - Catálogo de todos los generadores incluidos
- [Ejemplos prácticos](/docs/examples/) - Ejemplos para casos de uso comunes
- [Desarrollo de plugins](/docs/plugin_dev/) - Crea tus propios generadores personalizados

## 📦 Instalación

```bash
# Desde pub.dev
dart pub global activate dart_data_faker

# Desde el repositorio
git clone https://github.com/devjoi2018/dart_data_faker.git
cd dart_data_faker
dart pub get
dart pub global activate --source path .
```

## 🤝 Contribuciones

¿Tienes ideas para mejorar Dart Data Faker? Las contribuciones son bienvenidas:

1. Bifurca el repositorio
2. Crea una rama (`git checkout -b feature/amazing-feature`)
3. Haz commit de tus cambios (`git commit -m 'Añadir característica increíble'`)
4. Haz push a la rama (`git push origin feature/amazing-feature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo LICENSE para más detalles.

## 🙏 Agradecimientos

- A la comunidad de Dart y Flutter por su increíble trabajo
- A todos quienes han proporcionado comentarios y sugerencias

---
