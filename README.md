# Blog CRUD

Un proyecto Django simple para crear, leer, actualizar y eliminar artículos con autenticación básica de usuarios.

## 🚀 Descripción

Este proyecto implementa un blog CRUD con dos aplicaciones principales:

- `blog`: gestiona artículos con título, contenido, imagen y autor.
- `accounts`: gestiona el registro de usuarios y utiliza las vistas de autenticación integradas de Django.

El proyecto está preparado para usar SQLite como base de datos por defecto y plantillas HTML sencillas para la interfaz.

## 🧱 Tecnologías

- Python
- Django 6.0.4
- SQLite
- HTML / Django Templates

## 📁 Estructura principal

- `base_project/`: configuración principal de Django.
- `blog/`: lógica y URL del CRUD de artículos.
- `accounts/`: registro de usuarios.
- `templates/`: vistas en HTML.
- `db.sqlite3`: base de datos SQLite local.
- `requirements.txt`: dependencias del proyecto.

## ✅ Funcionalidades incluidas

- Lista de artículos.
- Detalle de artículo.
- Creación de artículos.
- Actualización de artículos.
- Eliminación de artículos.
- Registro de usuarios.
- Login / Logout con autenticación de Django.
- Control de edición y eliminación: solo el autor puede editar o borrar su propio artículo.

## 🔧 Requisitos

- Python 3.x
- `pip`
- Entorno virtual recomendado (`venv`, `.venv`, `virtualenv`, etc.)

## 📦 Instalación

1. Clona el repositorio o copia el proyecto.
2. Navega a la carpeta del proyecto:

```bash
cd blog_crud
```

3. Crea y activa un entorno virtual (Windows PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

4. Instala las dependencias:

```bash
pip install -r requirements.txt
```

> Si deseas trabajar con el campo `ImageField` para subir imágenes, instala `Pillow`:
>
> ```bash
> pip install pillow
> ```

## ⚙️ Configuración inicial

1. Ejecuta migraciones:

```bash
python manage.py migrate
```

2. Crea un superusuario opcionalmente:

```bash
python manage.py createsuperuser
```

## ▶️ Ejecución del proyecto

```bash
python manage.py runserver
```

Abre el navegador en `http://127.0.0.1:8000/`.

## 📌 Rutas principales

- `http://127.0.0.1:8000/` → Lista de artículos
- `http://127.0.0.1:8000/articulos/<pk>/` → Detalle de artículo
- `http://127.0.0.1:8000/articulos/crear/` → Crear artículo
- `http://127.0.0.1:8000/articulos/<pk>/actualizar/` → Actualizar artículo
- `http://127.0.0.1:8000/articulos/<pk>/eliminar/` → Eliminar artículo
- `http://127.0.0.1:8000/accounts/registro/` → Registro de usuario
- `http://127.0.0.1:8000/accounts/login/` → Login
- `http://127.0.0.1:8000/accounts/logout/` → Logout

## 🧠 Notas importantes

- `DEBUG` está activado en `base_project/settings.py` para desarrollo.
- La base de datos por defecto es `db.sqlite3`.
- Si trabajas con imágenes, asegúrate de configurar `MEDIA_URL` y `MEDIA_ROOT` en `settings.py` y servir archivos de medios en desarrollo.

## 📝 Sugerencias de mejora

- Añadir manejo completo de archivos estáticos y medios.
- Implementar paginación en la lista de artículos.
- Añadir comentarios o etiquetas a los artículos.
- Mejorar la interfaz con CSS y Bootstrap.
- Restringir la creación de artículos a usuarios autenticados.

## 📚 Más información

- Documentación de Django: https://docs.djangoproject.com/en/6.0/

---

Desarrollado como una demo funcional para un blog CRUD con Django.
