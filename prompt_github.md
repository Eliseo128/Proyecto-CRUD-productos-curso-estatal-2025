# DESARROLLO DE APLICACIONES WEB EN UN SISTEMA DE INFORMACIÓN

Este proyecto tiene como objetivo implementar aplicaciones web utilizando el framework **Django**, cubriendo desde los fundamentos del lenguaje **Python** hasta la configuración y desarrollo completo de un sistema web funcional.

---

## 🧠 Unidad I: Fundamentos de Python (Primera Parte)

### 🔹 Introducción a Python
Breve panorama general del lenguaje Python, su sintaxis simple y su amplia aplicación en el desarrollo web, automatización, ciencia de datos y más.

### 🔹 Conceptos Básicos

- **Variables**: Elementos para almacenar datos.
- **Estructuras de control (`if`, `else`)**
  - ✅ 1 ejemplo práctico.
- **Estructuras de repetición (`for`)**
  - ✅ 2 ejemplos prácticos.
- **Funciones definidas por el usuario**
  - ✅ 3 ejemplos prácticos.
- **Listas**
  - ✅ 2 ejemplos prácticos.
- **Tuplas**
  - ✅ 2 ejemplos prácticos.
- **Conjuntos**
  - ✅ 2 ejemplos prácticos.
- **Diccionarios**
  - ✅ 2 ejemplos prácticos.
- **Programación orientada a objetos (POO)**
  - ✅ 2 ejemplos prácticos.

> 📘 En cada ejemplo se explican los conceptos y su aplicabilidad en proyectos reales.

---

## ⚙️ Unidad I: Entorno y Proyecto Django (Segunda Parte)

### 🔹 Conceptos previos

- **Tipos de frameworks para aplicaciones web**: Comparativa y ventajas de Django.
- **¿Qué es Django?**: Framework de alto nivel para desarrollo rápido, seguro y escalable.
- **Modelo Vista Template (MVT)**: Arquitectura que separa datos, lógica de negocio y presentación.
- **Editor VS Code**: Herramienta recomendada para desarrollo Django.

### 🔹 Preparación del Entorno

- Creación de entorno virtual.
- Instalación del proyecto principal: `backend_producto`.
- Comando para ejecutar el servidor: `python manage.py runserver`.

### 🔹 Creación de la Aplicación Web

- Instalación de la app: `frontend_producto`.
- Registro en `settings.py`.
- Configuración de URLs en `backend_producto` y enlace con `frontend_producto`.
- Configuración de:
  - Archivos estáticos (`static`)
  - Archivos multimedia (`media`)
  - Plantillas (`templates`)

### 🔹 Modelado de Datos

Modelo: **Producto** en `frontend_producto`

- `nombre`: `CharField`
- `imagen`: `ImageField`
- `cant`: `IntegerField`
- `precio`: `DecimalField`

> Se utiliza el sistema ORM de Django para crear y manipular el modelo en la base de datos.

- Comandos:
  - `python manage.py makemigrations`
  - `python manage.py migrate`
  - `python manage.py createsuperuser`

---

## 🧩 Componentes de la Aplicación

### Formularios

- Creación de `forms.py` para el formulario de productos.

### Plantillas HTML

- `base.html`  
- `navbar.html`  
- `footer.html`  
- `index.html`  
- `listado_productos.html`  
- `agregar_producto.html`  
- `editar_producto.html`

### Vistas en `views.py`

- `pagina_inicial()`
- `listado_productos()`
- `crear_producto()`
- `editar_producto()`
- `actualizar_producto()`
- `borrar_producto()`

### Configuración de URLs

- Archivo `urls.py` en `frontend_producto` para gestionar las rutas.

### Archivos Estáticos

- Hoja de estilos: `styles.css`

### Estructura de Carpetas y Archivos

- Organización siguiendo buenas prácticas Django.
- Separación clara entre frontend, backend, estáticos, plantillas y archivos de configuración.

---

## ✅ Buenas Prácticas

- Código limpio y comentado.
- Separación de responsabilidades.
- Reutilización de componentes.
- Nombres descriptivos en funciones y variables.
- Documentación clara en cada archivo importante.

---

## 📌 Notas Finales

> En cada punto clave se incluye una explicación breve y clara de los conceptos técnicos involucrados.  
Este proyecto es una guía práctica para estudiantes y desarrolladores que deseen aprender a construir aplicaciones web completas utilizando Django y Python desde cero.

---

