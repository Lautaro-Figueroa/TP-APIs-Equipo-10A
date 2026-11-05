# 🔌 API REST – Catálogo de Productos

API REST para administrar un catálogo de productos, con operaciones CRUD y carga de imágenes. Reutiliza las capas de Dominio y Negocio del sistema de gestión de artículos.

> Trabajo Práctico de **Programación III** de la Tecnicatura Universitaria en Programación (UTN), desarrollado por el **Equipo 10A**.

## 📡 Endpoints

| Método | Ruta | Descripción |
|---|---|---|
| `GET` | `/api/Productos` | Lista todos los productos |
| `GET` | `/api/Productos/{id}` | Obtiene un producto por id |
| `POST` | `/api/Productos` | Crea un producto (con validaciones) |
| `PUT` | `/api/Productos/{id}` | Modifica un producto |
| `DELETE` | `/api/Productos/{id}` | Elimina un producto |
| `POST` | `/api/Productos/{id}/imagenes` | Agrega imágenes a un producto |

Las respuestas devuelven códigos HTTP según el resultado (`200`, `400`, `404`, `500`). Los datos de entrada se reciben con DTOs (`ProductoDto`, `AgregarImagenDto`).

## 🧱 Arquitectura

```
├── API-CatalogoProductos/  → ASP.NET Web API (controllers, DTOs, HelpPage)
├── Dominio/                → Entidades: Articulo, Marca, Categoria, Imagen
└── Negocio/                → Lógica de negocio y acceso a datos (SQL Server)
```

## 🛠️ Tecnologías

C# · ASP.NET Web API 2 · .NET Framework · SQL Server · ADO.NET

## 👨‍💻 Mi aporte

- Implementé los endpoints para **listar** y **agregar** productos.
- Agregué las **validaciones del método POST**, que devuelven respuestas `400 Bad Request` con mensajes claros cuando los datos son inválidos.

## ▶️ Cómo ejecutarlo

1. Restaurar la base de datos `CATALOGO_P3_DB` en SQL Server.
2. Abrir `TP-APIs.sln` con Visual Studio y ejecutar el proyecto `API-CatalogoProductos`.
3. Probar los endpoints con Postman o desde la página `/Help`.

## 👥 Equipo

[Marisel Alarcón](https://github.com/AlarconMarisel) · [Claudio Gobbi](https://github.com/ClaudioCesarGobbi) · [Lautaro Figueroa](https://github.com/Lautaro-Figueroa)
