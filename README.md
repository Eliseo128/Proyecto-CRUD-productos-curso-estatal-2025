# Proyecto-CRUD-productos-curso-estatal-2025
DESARROLLA APLICACIONES WEB EN UN SISTEMA DE INFORMACIÓN

# Proyecto: Sistema de Gestión de Productos con Django

Este proyecto es una aplicación web desarrollada como parte del curso **"DESARROLLA APLICACIONES WEB EN UN SISTEMA DE INFORMACIÓN"**. La aplicación implementa un sistema CRUD (Crear, Leer, Actualizar, Borrar) para gestionar un inventario de productos, utilizando el framework Django.

## Descripción del Proyecto

La aplicación permite a los usuarios realizar las siguientes acciones:
-   Ver un listado de todos los productos en el inventario.
-   Añadir un nuevo producto, especificando su nombre, cantidad, precio y una imagen.
-   Editar la información de un producto existente.
-   Eliminar un producto del inventario.

Este proyecto sirve como una demostración práctica de los conceptos fundamentales de Django, incluyendo el patrón MVT (Modelo-Vista-Template), el ORM de Django, el sistema de formularios, el enrutamiento de URLs y la gestión de archivos estáticos y de medios.

## Características

-   **CRUD Completo**: Funcionalidad completa para Crear, Leer, Actualizar y Borrar productos.
-   **Interfaz Amigable**: Interfaz de usuario limpia y responsiva creada con Bootstrap 5.
-   **Gestión de Imágenes**: Capacidad para subir y mostrar imágenes de productos.
-   **Panel de Administración**: Integración con el panel de administración de Django para una gestión de datos avanzada.
-   **Estructura Organizada**: Sigue las mejores prácticas de Django para la organización de proyectos y aplicaciones.

## Stack de Tecnologías

-   **Backend**: Python, Django
-   **Frontend**: HTML5, CSS3, Bootstrap 5
-   **Base de Datos**: SQLite 3 (por defecto en desarrollo)
-   **Entorno**: Entorno virtual de Python (`venv`)

## Requisitos Previos

-   Python 3.8 o superior
-   `pip` (gestor de paquetes de Python)
-   `git` (opcional, para clonar el repositorio)

## Instrucciones de Instalación y Ejecución

Sigue estos pasos para poner en marcha el proyecto en tu máquina local.

**1. Clona el Repositorio**
```bash
git clone <URL_DEL_REPOSITORIO>
cd nombre-del-directorio-del-proyecto
```

**2. Crea y Activa un Entorno Virtual**
Es una buena práctica aislar las dependencias del proyecto.
```bash
# Crear el entorno virtual
python -m venv venv

# Activar en Windows
.\venv\Scripts\activate

# Activar en macOS/Linux
source venv/bin/activate
```
Verás `(venv)` al inicio de la línea de tu terminal.

**3. Instala las Dependencias**
Crea un archivo llamado `requirements.txt` en la raíz del proyecto con el siguiente contenido:
```txt
Django>=4.0
Pillow>=9.0
```
Luego, instala las dependencias desde la terminal:
```bash
pip install -r requirements.txt
```

**4. Realiza las Migraciones de la Base de Datos**
Este comando creará la base de datos (un archivo `db.sqlite3`) y las tablas necesarias según los modelos definidos.
```bash
python manage.py migrate
```

**5. Crea un Superusuario**
Esto te permitirá acceder al panel de administración de Django.
```bash
python manage.py createsuperuser
```
Sigue las instrucciones para crear tu nombre de usuario, email y contraseña.

**6. Ejecuta el Servidor de Desarrollo**
¡Todo está listo! Inicia el servidor.
```bash
python manage.py runserver
```

**7. Accede a la Aplicación**
Abre tu navegador web y visita las siguientes URLs:
-   **Página Principal**: `http://127.0.0.1:8000/`
-   **Listado de Productos**: `http://127.0.0.1:8000/productos/`
-   **Panel de Administración**: `http://127.0.0.1:8000/admin/` (inicia sesión con los datos del superusuario)

## Estructura del Proyecto

La estructura de carpetas y archivos del proyecto es la siguiente:

```
mi_proyecto_django/
├── backend_producto/         # Carpeta de configuración del proyecto Django
│   ├── settings.py           # Archivo de configuración principal
│   └── urls.py               # URLs principales del proyecto
├── frontend_producto/        # Aplicación Django que gestiona los productos
│   ├── migrations/           # Migraciones de la base de datos
│   ├── models.py             # Definición del modelo Producto
│   ├── views.py              # Lógica de la aplicación (las vistas)
│   ├── forms.py              # Definición del formulario de Producto
│   └── urls.py               # URLs específicas de esta aplicación
├── media/                    # Carpeta para archivos subidos por el usuario (imágenes)
├── static/                   # Carpeta para archivos estáticos (CSS, JS)
│   └── css/
│       └── styles.css
├── templates/                # Carpeta para las plantillas HTML
│   ├── base.html             # Plantilla base que se hereda
│   ├── navbar.html           # Componente de navegación
│   ├── footer.html           # Componente de pie de página
│   └── productos/
│       ├── listado_productos.html
│       ├── agregar_producto.html
│       └── editar_producto.html
├── manage.py                 # Script para administrar el proyecto Django
└── db.sqlite3                # Base de datos SQLite
```

---
**Autor**: [Tu Nombre]
**Curso**: Desarrollo de Aplicaciones Web en un Sistema de Información

¿Cómo usarlo?

Abre tu editor de código (como VS Code).

En la carpeta raíz de tu proyecto (la misma donde está manage.py), crea un nuevo archivo.

Nombra el archivo exactamente README.md. La extensión .md es importante.

Copia todo el contenido del bloque de código de arriba y pégalo en tu nuevo archivo README.md.

Guarda el archivo.

Si subes tu proyecto a una plataforma como GitHub, este archivo README.md se mostrará automáticamente en la página principal de tu repositorio, sirviendo como una excelente carta de presentación para tu trabajo.
