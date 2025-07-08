¡Excelente! Aquí tienes un desarrollo completo y detallado del curso, siguiendo la estructura que has solicitado. Cada sección incluye explicaciones conceptuales y el código funcional correspondiente, aplicando buenas prácticas de programación en Python y Django.

---

### **DESARROLLA APLICACIONES WEB EN UN SISTEMA DE INFORMACIÓN**
**Implementa aplicaciones web en Django funcional**

---

## **Unidad I primera parte (Python)**

### **Breve Introducción a Python**

**Resumen:** Python es un lenguaje de programación de alto nivel, interpretado, de tipado dinámico y multiparadigma. Es famoso por su sintaxis clara y legible, que se asemeja al lenguaje humano. Esto reduce la curva de aprendizaje y los costos de mantenimiento. Su vasta biblioteca estándar y el gran ecosistema de paquetes de terceros (como Django) lo hacen extremadamente versátil para desarrollo web, ciencia de datos, inteligencia artificial, scripting y más.

---

### **Variables**

**Resumen:** Una variable es un contenedor para almacenar un valor de datos. En Python, no necesitas declarar el tipo de una variable explícitamente; el tipo se infiere en el momento de la asignación.

```python
# python_examples.py

# Asignación de variables
nombre_curso = "Desarrollo Web con Django"  # String (cadena de texto)
año = 2023                                # Integer (entero)
precio = 199.99                           # Float (decimal)
es_online = True                          # Boolean (booleano)

print(f"Curso: {nombre_curso}, Año: {año}")
```

---

### **Estructuras de control `if else` (1 ejemplo práctico)**

**Resumen:** Las estructuras de control condicionales permiten que un programa ejecute diferentes bloques de código según si una condición es verdadera (`True`) o falsa (`False`). `if` ejecuta el código si la condición es cierta, `elif` (else if) prueba una nueva condición si la anterior fue falsa, y `else` se ejecuta si ninguna de las condiciones anteriores fue cierta.

```python
# Ejemplo práctico: Verificar si un estudiante aprobó un examen.
calificacion = 75
calificacion_minima_aprobatoria = 70

if calificacion >= calificacion_minima_aprobatoria:
    print(f"¡Felicidades! Has aprobado con {calificacion}.")
elif calificacion >= 50:
    print(f"Tu calificación es {calificacion}. Necesitas estudiar más para el examen de recuperación.")
else:
    print(f"Lo sentimos, has reprobado con {calificacion}.")
```

---

### **Estructuras de repetición `for` (2 ejemplos prácticos)**

**Resumen:** El bucle `for` se utiliza para iterar sobre una secuencia de elementos (como una lista, tupla, diccionario, conjunto o cadena de texto). Ejecuta un bloque de código una vez por cada elemento en la secuencia.

```python
# Ejemplo 1: Recorrer una lista de frutas
frutas = ["manzana", "banana", "cereza", "naranja"]

print("\n--- Lista de Frutas Disponibles ---")
for fruta in frutas:
    print(f"- {fruta.capitalize()}")

# Ejemplo 2: Generar la tabla de multiplicar del 5
print("\n--- Tabla de Multiplicar del 5 ---")
for i in range(1, 11):  # El rango va de 1 a 10
    resultado = 5 * i
    print(f"5 x {i} = {resultado}")
```

---

### **Funciones creadas por el usuario (3 ejemplos prácticos)**

**Resumen:** Una función es un bloque de código reutilizable que realiza una tarea específica. Las funciones ayudan a organizar el código, hacerlo más legible y evitar la repetición (principio DRY: Don't Repeat Yourself). Pueden recibir datos de entrada (parámetros) y devolver un resultado (valor de retorno).

```python
# Ejemplo 1: Función simple sin parámetros ni retorno
def mostrar_bienvenida():
    """Esta función imprime un saludo de bienvenida."""
    print("\n¡Bienvenido al sistema de gestión!")

# Ejemplo 2: Función con parámetros
def saludar_usuario(nombre):
    """Esta función recibe un nombre y lo saluda personalmente."""
    print(f"Hola, {nombre}. ¡Qué bueno verte!")

# Ejemplo 3: Función con parámetros y valor de retorno
def calcular_iva(monto_base):
    """Calcula el 19% de IVA sobre un monto dado y lo devuelve."""
    iva = monto_base * 0.19
    return iva

# Uso de las funciones
mostrar_bienvenida()
saludar_usuario("Ana")
monto_sin_iva = 10000
iva_calculado = calcular_iva(monto_sin_iva)
print(f"El IVA para un monto de ${monto_sin_iva} es: ${iva_calculado}")
print(f"El total a pagar es: ${monto_sin_iva + iva_calculado}")
```

---

### **Listas (2 ejemplos prácticos)**

**Resumen:** Una lista es una colección ordenada y mutable (modificable) de elementos. Se definen con corchetes `[]` y pueden contener elementos de diferentes tipos.

```python
# Ejemplo 1: Creación y modificación de una lista de tareas
tareas_pendientes = ["Estudiar Python", "Hacer la compra", "Llamar al dentista"]
print(f"\nLista de tareas inicial: {tareas_pendientes}")

# Modificar un elemento (los índices empiezan en 0)
tareas_pendientes[1] = "Comprar víveres en el supermercado"
print(f"Lista modificada: {tareas_pendientes}")

# Ejemplo 2: Añadir, eliminar y recorrer una lista
# Añadir un elemento al final
tareas_pendientes.append("Preparar la cena")
print(f"Lista con nueva tarea: {tareas_pendientes}")

# Eliminar un elemento
tareas_pendientes.remove("Llamar al dentista")
print(f"Lista después de eliminar tarea: {tareas_pendientes}")

print("\nTareas restantes para hoy:")
for i, tarea in enumerate(tareas_pendientes, 1):
    print(f"{i}. {tarea}")
```

---

### **Tuplas (2 ejemplos prácticos)**

**Resumen:** Una tupla es una colección ordenada e **inmutable** (no modificable) de elementos. Se definen con paréntesis `()`. Una vez creadas, no se pueden añadir, eliminar ni cambiar sus elementos. Son útiles para datos que no deben cambiar, como coordenadas o constantes.

```python
# Ejemplo 1: Almacenar coordenadas geográficas (datos que no deben cambiar)
coordenadas_oficina = (19.4326, -99.1332)  # (latitud, longitud)
print(f"\nLas coordenadas de la oficina son: {coordenadas_oficina}")
# Intentar modificarla generaría un error: TypeError
# coordenadas_oficina[0] = 20.0  # Esto daría error

# Ejemplo 2: Desempaquetado de tuplas
# Una función puede devolver una tupla con múltiples valores
def obtener_datos_usuario():
    # Simulamos que obtenemos estos datos de una base de datos
    return ("john_doe", "john.doe@example.com", 35)

usuario = obtener_datos_usuario()
# Desempaquetado
nombre_usuario, email, edad = usuario

print(f"Nombre de Usuario: {nombre_usuario}")
print(f"Email: {email}")
print(f"Edad: {edad}")
```

---

### **Conjuntos (2 ejemplos prácticos)**

**Resumen:** Un conjunto (set) es una colección desordenada y mutable de elementos **únicos**. No permiten elementos duplicados. Son muy eficientes para comprobar si un elemento está presente y para realizar operaciones matemáticas de conjuntos (unión, intersección, diferencia).

```python
# Ejemplo 1: Eliminar elementos duplicados de una lista
numeros_con_duplicados = [1, 2, 2, 3, 4, 4, 4, 5, 1]
numeros_unicos = set(numeros_con_duplicados)
print(f"\nLista original: {numeros_con_duplicados}")
print(f"Conjunto de números únicos: {numeros_unicos}")

# Ejemplo 2: Operaciones de conjuntos para gestionar permisos de usuarios
admin_permissions = {"create_user", "delete_user", "edit_content", "view_reports"}
editor_permissions = {"edit_content", "view_content"}

# Intersección: ¿Qué permisos tienen en común?
common_permissions = admin_permissions.intersection(editor_permissions)
print(f"Permisos en común: {common_permissions}")

# Diferencia: ¿Qué permisos tiene un admin que un editor no tiene?
unique_admin_permissions = admin_permissions.difference(editor_permissions)
print(f"Permisos exclusivos del admin: {unique_admin_permissions}")
```

---

### **Diccionarios (2 ejemplos prácticos)**

**Resumen:** Un diccionario es una colección desordenada (en versiones antiguas de Python) de pares `clave:valor`. Son mutables y cada clave debe ser única. Se utilizan para almacenar datos de forma estructurada, donde cada valor está asociado a una clave específica.

```python
# Ejemplo 1: Almacenar información de un producto
producto = {
    "nombre": "Laptop Pro",
    "precio": 1200.50,
    "stock": 15,
    "marca": "TechCo"
}
print(f"\nInformación del producto: {producto}")
# Acceder a un valor por su clave
print(f"El precio de la {producto['nombre']} es ${producto['precio']}")

# Ejemplo 2: Modificar y recorrer un diccionario
# Añadir un nuevo par clave-valor
producto["garantia"] = "2 años"
print(f"Diccionario actualizado: {producto}")

# Recorrer las claves y valores
print("\n--- Detalles del Producto ---")
for clave, valor in producto.items():
    print(f"{clave.capitalize()}: {valor}")
```

---

### **Programación Orientada a Objetos (2 ejemplos prácticos)**

**Resumen:** La Programación Orientada a Objetos (POO) es un paradigma que utiliza "objetos" para diseñar aplicaciones. Un objeto es una instancia de una "clase". Una **clase** es una plantilla o molde que define las propiedades (atributos) y los comportamientos (métodos) que tendrán sus objetos.

```python
# Ejemplo 1: Clase Coche
class Coche:
    # El método __init__ es el constructor. Se ejecuta al crear un objeto.
    def __init__(self, marca, modelo, año):
        self.marca = marca      # Atributo
        self.modelo = modelo    # Atributo
        self.año = año          # Atributo
        self.encendido = False  # Atributo con valor por defecto

    # Método para describir el coche
    def descripcion(self):
        return f"Coche: {self.marca} {self.modelo} del año {self.año}"

    # Método para cambiar el estado
    def arrancar(self):
        if not self.encendido:
            self.encendido = True
            print("El coche ha arrancado.")
        else:
            print("El coche ya estaba encendido.")

# Creación de objetos (instancias) de la clase Coche
mi_coche = Coche("Toyota", "Corolla", 2022)
coche_vecino = Coche("Ford", "Mustang", 2021)

print("\n--- Ejemplo de POO: Coche ---")
print(mi_coche.descripcion())
mi_coche.arrancar()
mi_coche.arrancar()

# Ejemplo 2: Clase CuentaBancaria
class CuentaBancaria:
    def __init__(self, titular, saldo_inicial=0):
        self.titular = titular
        self.saldo = saldo_inicial

    def depositar(self, cantidad):
        if cantidad > 0:
            self.saldo += cantidad
            print(f"Depósito de ${cantidad} realizado. Nuevo saldo: ${self.saldo}")
        else:
            print("La cantidad a depositar debe ser positiva.")

    def retirar(self, cantidad):
        if 0 < cantidad <= self.saldo:
            self.saldo -= cantidad
            print(f"Retiro de ${cantidad} realizado. Nuevo saldo: ${self.saldo}")
        else:
            print("Fondos insuficientes o cantidad no válida.")
    
    def consultar_saldo(self):
        print(f"El saldo actual de la cuenta de {self.titular} es ${self.saldo}")

# Creación y uso de un objeto CuentaBancaria
print("\n--- Ejemplo de POO: Cuenta Bancaria ---")
mi_cuenta = CuentaBancaria("Carlos Pérez", 500)
mi_cuenta.consultar_saldo()
mi_cuenta.depositar(200)
mi_cuenta.retirar(150)
mi_cuenta.retirar(600) # Intentar retirar más del saldo disponible
mi_cuenta.consultar_saldo()
```

---
---

## **Unidad I segunda parte (Configura el entorno Django)**

### **Tipos de framework para implementar aplicaciones web**

**Resumen:** Un framework web es un conjunto de herramientas, bibliotecas y buenas prácticas que facilita el desarrollo de aplicaciones web complejas. Proporcionan una estructura base para que no tengas que empezar desde cero. Se pueden clasificar principalmente en:
*   **Full-Stack (o "con baterías incluidas")**: Ofrecen soluciones para casi todos los aspectos del desarrollo web: ORM para bases de datos, sistema de plantillas, autenticación, panel de administración, etc. **Django** es el ejemplo más claro. Son robustos y opinados (guían sobre cómo hacer las cosas).
*   **Microframeworks**: Proporcionan solo los componentes esenciales (enrutamiento y manejo de peticiones/respuestas). Dejan al desarrollador la libertad de elegir las herramientas para otras tareas (bases de datos, plantillas, etc.). **Flask** y **FastAPI** son ejemplos populares. Son flexibles y ligeros.

### **Introducción a Django**

**Resumen:** Django es un framework web de alto nivel, gratuito y de código abierto, escrito en Python. Sigue el principio "Don't Repeat Yourself" (DRY) y promueve un desarrollo rápido y limpio. Es conocido por su seguridad, escalabilidad y su enfoque "baterías incluidas", que ofrece un potente ORM (Object-Relational Mapper), un sistema de migración de base de datos, un panel de administración autogenerado y mucho más, listo para usar.

### **Modelo Vista Template (MVT)**

**Resumen:** Django sigue una arquitectura de software llamada Modelo-Vista-Template (MVT), que es una variante del conocido Modelo-Vista-Controlador (MVC).
*   **Modelo (Model):** Es la capa de datos. Define la estructura de tu información, típicamente en forma de clases de Python que se mapean a tablas en una base de datos. Es la única fuente de verdad sobre tus datos.
*   **Vista (View):** Es la capa de lógica de negocio. Recibe una petición web (request) y devuelve una respuesta web (response). Las vistas acceden a los modelos para obtener datos y los pasan a una plantilla.
*   **Template (Plantilla):** Es la capa de presentación. Es un archivo (generalmente HTML) que define cómo se mostrarán los datos al usuario. Contiene placeholders y lógica simple (bucles, condicionales) para renderizar la información que recibe de la vista.

### **VS Code**

**Resumen:** Visual Studio Code es un editor de código fuente ligero pero potente, desarrollado por Microsoft. Es extremadamente popular para el desarrollo con Python y Django gracias a su gran ecosistema de extensiones, como "Python" (de Microsoft), "Django" y "Pylance", que ofrecen resaltado de sintaxis, autocompletado inteligente (IntelliSense), depuración y linters para mejorar la calidad del código.

---

### **A continuación, se detalla el paso a paso para crear el proyecto funcional.**

#### **1. Creación del entorno de desarrollo virtual**

**Resumen:** Un entorno virtual es una carpeta que contiene una instalación de Python aislada del resto del sistema. Esto permite instalar paquetes y dependencias específicas para un proyecto sin afectar a otros proyectos o a la instalación global de Python. Es una práctica esencial.

```bash
# En tu terminal o línea de comandos

# 1. Crea una carpeta para tu proyecto y entra en ella
mkdir mi_proyecto_django
cd mi_proyecto_django

# 2. Crea el entorno virtual (llamado 'venv')
python -m venv venv

# 3. Activa el entorno virtual
# En Windows:
.\venv\Scripts\activate
# En macOS/Linux:
source venv/bin/activate

# Verás (venv) al principio de la línea de comandos, indicando que está activo.
```

#### **2. Instalación de Django y creación del proyecto**

```bash
# Con el entorno virtual activo

# Instala Django y Pillow (necesario para campos de imagen)
pip install django pillow

# Crea el proyecto Django. El '.' al final evita una carpeta anidada extra.
django-admin startproject backend_producto .
```

#### **3. Ejecutar `runserver`**

**Resumen:** `runserver` es un comando de Django que inicia un servidor web de desarrollo ligero en tu máquina local. Te permite ver tu aplicación en el navegador mientras la desarrollas.

```bash
python manage.py runserver
```
Abre tu navegador y ve a `http://127.0.0.1:8000/`. Deberías ver la página de bienvenida de Django.

#### **4. Instalación de la app en Django (`frontend_producto`)**

**Resumen:** Un proyecto de Django es un contenedor de configuración y aplicaciones. Una aplicación (app) es un módulo autocontenido que realiza una función específica (ej. un blog, una tienda, etc.). Un proyecto puede tener múltiples apps.

```bash
# Detén el servidor (Ctrl+C) y ejecuta:
python manage.py startapp frontend_producto
```

#### **5. Incluir `frontend_producto` en `settings.py`**

**Resumen:** Debes registrar tu nueva app en el archivo de configuración principal del proyecto (`settings.py`) para que Django la reconozca.

Abre `backend_producto/settings.py` y añade `frontend_producto` a la lista `INSTALLED_APPS`:

```python
# backend_producto/settings.py

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'frontend_producto', # <-- AÑADIR ESTA LÍNEA
]
```

#### **6. Configurar URLs del `backend_producto` para enlazar `frontend_producto`**

**Resumen:** El archivo `urls.py` del proyecto principal actúa como un enrutador maestro. Delegaremos todas las URLs que empiecen por una ruta vacía (`''`) al archivo `urls.py` de nuestra app `frontend_producto`.

Edita `backend_producto/urls.py`:

```python
# backend_producto/urls.py
from django.contrib import admin
from django.urls import path, include  # <-- Importar include
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('frontend_producto.urls')), # <-- AÑADIR ESTA LÍNEA
]

# Esto es para servir archivos de media en desarrollo
if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

#### **7. Configuración de `media`, `static` y `templates` en `backend_producto/settings.py`**

**Resumen:**
*   **`STATIC`**: Para archivos estáticos como CSS, JavaScript e imágenes de la interfaz.
*   **`TEMPLATES`**: Para los archivos HTML que Django renderizará.
*   **`MEDIA`**: Para archivos subidos por los usuarios, como las imágenes de los productos.

Añade estas configuraciones al final de `backend_producto/settings.py`:

```python
# backend_producto/settings.py

# ... al final del archivo ...

import os

# Configuración de archivos estáticos
STATIC_URL = '/static/'
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]

# Configuración de archivos de medios (subidos por usuarios)
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

# Configuración de la carpeta de plantillas (templates)
TEMPLATES[0]['DIRS'] = [os.path.join(BASE_DIR, 'templates')]
```

#### **8. Crear la estructura de carpetas y archivos**

**Resumen:** Una estructura organizada es clave. Crearemos las carpetas que acabamos de configurar en `settings.py`.

En la raíz de tu proyecto (donde está `manage.py`), crea las siguientes carpetas y archivos vacíos. La estructura final se verá así:

```
mi_proyecto_django/
├── backend_producto/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── frontend_producto/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── views.py
│   ├── forms.py         <-- CREAR ARCHIVO
│   └── urls.py          <-- CREAR ARCHIVO
├── media/                 <-- CREAR CARPETA (para imágenes de productos)
├── static/
│   └── css/
│       └── styles.css   <-- CREAR CARPETA y ARCHIVO
├── templates/
│   ├── base.html          <-- CREAR ARCHIVO
│   ├── footer.html        <-- CREAR ARCHIVO
│   ├── index.html         <-- CREAR ARCHIVO
│   ├── navbar.html        <-- CREAR ARCHIVO
│   └── productos/
│       ├── agregar_producto.html  <-- CREAR CARPETA y ARCHIVO
│       ├── editar_producto.html   <-- CREAR ARCHIVO
│       └── listado_productos.html <-- CREAR ARCHIVO
├── db.sqlite3
└── manage.py
```

#### **9. Creación del modelo `Producto`**

Edita `frontend_producto/models.py`:

```python
# frontend_producto/models.py
from django.db import models

class Producto(models.Model):
    nombre = models.CharField(max_length=200)
    imagen = models.ImageField(upload_to='productos/', null=True, blank=True)
    cantidad = models.IntegerField()
    precio = models.DecimalField(max_digits=10, decimal_places=2)

    def __str__(self):
        return self.nombre
```

#### **10. `makemigrations` y `migrate`**

**Resumen:** `makemigrations` crea un archivo de migración que traduce los cambios de tus modelos a instrucciones de base de datos. `migrate` aplica esas migraciones para actualizar la base de datos.

```bash
python manage.py makemigrations
python manage.py migrate
```

#### **11. Creación del superusuario**

**Resumen:** Un superusuario tiene todos los permisos y puede acceder al panel de administración de Django.

```bash
python manage.py createsuperuser
```
Sigue las instrucciones para crear tu usuario y contraseña.

#### **12. Creación de formulario `forms.py`**

**Resumen:** `ModelForm` es una clase de ayuda que te permite crear un formulario a partir de un modelo de Django. Esto ahorra mucho tiempo.

Crea y edita `frontend_producto/forms.py`:

```python
# frontend_producto/forms.py
from django import forms
from .models import Producto

class ProductoForm(forms.ModelForm):
    class Meta:
        model = Producto
        fields = ['nombre', 'imagen', 'cantidad', 'precio']
        widgets = {
            'nombre': forms.TextInput(attrs={'class': 'form-control', 'placeholder': 'Nombre del producto'}),
            'cantidad': forms.NumberInput(attrs={'class': 'form-control'}),
            'precio': forms.NumberInput(attrs={'class': 'form-control'}),
            'imagen': forms.FileInput(attrs={'class': 'form-control'}),
        }
```

#### **13. Creación de los archivos HTML (Templates)**

**`templates/base.html`** (La plantilla principal)

```html
{% load static %}
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{% block title %}Sistema de Productos{% endblock %}</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="{% static 'css/styles.css' %}">
</head>
<body>
    {% include 'navbar.html' %}
    
    <main class="container mt-4">
        {% block content %}
        <!-- El contenido de cada página irá aquí -->
        {% endblock %}
    </main>

    {% include 'footer.html' %}

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

**`templates/navbar.html`**

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
        <a class="navbar-brand" href="{% url 'inicio' %}">Gestión de Productos</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="{% url 'listado_productos' %}">Ver Productos</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="{% url 'crear_producto' %}">Agregar Producto</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

**`templates/footer.html`**

```html
<footer class="bg-dark text-white text-center p-3 mt-5">
    <p>&copy; {% now "Y" %} Mi Proyecto Django. Todos los derechos reservados.</p>
</footer>
```

**`templates/index.html`**

```html
{% extends 'base.html' %}

{% block title %}Página de Inicio{% endblock %}

{% block content %}
<div class="p-5 mb-4 bg-light rounded-3">
    <div class="container-fluid py-5">
        <h1 class="display-5 fw-bold">Bienvenido al Sistema de Gestión de Productos</h1>
        <p class="col-md-8 fs-4">Utiliza la barra de navegación para listar los productos existentes o para agregar uno nuevo a nuestro inventario.</p>
        <a class="btn btn-primary btn-lg" href="{% url 'listado_productos' %}">Empezar a gestionar</a>
    </div>
</div>
{% endblock %}
```

**`templates/productos/listado_productos.html`**

```html
{% extends 'base.html' %}

{% block title %}Listado de Productos{% endblock %}

{% block content %}
<h1 class="mb-4">Listado de Productos</h1>
<a href="{% url 'crear_producto' %}" class="btn btn-success mb-3">Agregar Nuevo Producto</a>

<table class="table table-striped table-hover">
    <thead class="table-dark">
        <tr>
            <th>Imagen</th>
            <th>Nombre</th>
            <th>Cantidad</th>
            <th>Precio</th>
            <th>Acciones</th>
        </tr>
    </thead>
    <tbody>
        {% for producto in productos %}
        <tr>
            <td>
                {% if producto.imagen %}
                    <img src="{{ producto.imagen.url }}" alt="{{ producto.nombre }}" width="50" class="img-thumbnail">
                {% else %}
                    Sin imagen
                {% endif %}
            </td>
            <td>{{ producto.nombre }}</td>
            <td>{{ producto.cantidad }}</td>
            <td>${{ producto.precio }}</td>
            <td>
                <a href="{% url 'editar_producto' producto.id %}" class="btn btn-warning btn-sm">Editar</a>
                <form action="{% url 'borrar_producto' producto.id %}" method="post" style="display:inline;">
                    {% csrf_token %}
                    <button type="submit" class="btn btn-danger btn-sm" onclick="return confirm('¿Estás seguro de que deseas eliminar este producto?');">Borrar</button>
                </form>
            </td>
        </tr>
        {% empty %}
        <tr>
            <td colspan="5" class="text-center">No hay productos registrados.</td>
        </tr>
        {% endfor %}
    </tbody>
</table>
{% endblock %}
```

**`templates/productos/agregar_producto.html`**

```html
{% extends 'base.html' %}

{% block title %}Agregar Producto{% endblock %}

{% block content %}
<h1 class="mb-4">Agregar Nuevo Producto</h1>
<form method="post" enctype="multipart/form-data">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit" class="btn btn-primary">Guardar Producto</button>
    <a href="{% url 'listado_productos' %}" class="btn btn-secondary">Cancelar</a>
</form>
{% endblock %}
```

**`templates/productos/editar_producto.html`**

```html
{% extends 'base.html' %}

{% block title %}Editar Producto{% endblock %}

{% block content %}
<h1 class="mb-4">Editar Producto: {{ form.instance.nombre }}</h1>
<form method="post" enctype="multipart/form-data">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit" class="btn btn-primary">Actualizar Producto</button>
    <a href="{% url 'listado_productos' %}" class="btn btn-secondary">Cancelar</a>
</form>
{% endblock %}
```

#### **14. Crear funciones en `views.py`**

Edita `frontend_producto/views.py`:

```python
# frontend_producto/views.py
from django.shortcuts import render, redirect, get_object_or_404
from .models import Producto
from .forms import ProductoForm

def pagina_inicial(request):
    """Renderiza la página de inicio."""
    return render(request, 'index.html')

def listado_productos(request):
    """Muestra todos los productos."""
    productos = Producto.objects.all()
    context = {'productos': productos}
    return render(request, 'productos/listado_productos.html', context)

def crear_producto(request):
    """Crea un nuevo producto."""
    if request.method == 'POST':
        form = ProductoForm(request.POST, request.FILES)
        if form.is_valid():
            form.save()
            return redirect('listado_productos')
    else:
        form = ProductoForm()
    
    context = {'form': form}
    return render(request, 'productos/agregar_producto.html', context)

def editar_producto(request, pk):
    """Permite editar un producto existente."""
    producto = get_object_or_404(Producto, pk=pk)
    
    if request.method == 'POST':
        form = ProductoForm(request.POST, request.FILES, instance=producto)
        if form.is_valid():
            form.save()
            return redirect('listado_productos')
    else:
        form = ProductoForm(instance=producto)
        
    context = {'form': form}
    return render(request, 'productos/editar_producto.html', context)

# NOTA: En un formulario real, la vista de edición y actualización se pueden combinar.
# Por simplicidad y claridad, las mantendremos separadas como en la solicitud,
# pero el código de `editar_producto` ya maneja ambos casos (GET y POST).
# Por lo tanto, no se necesita una vista `actualizar_producto` separada.

def borrar_producto(request, pk):
    """Elimina un producto."""
    producto = get_object_or_404(Producto, pk=pk)
    if request.method == 'POST':
        producto.delete()
        return redirect('listado_productos')
    
    # Redireccionar si se accede por GET (no debería pasar con el form)
    return redirect('listado_productos')
```

#### **15. Crear y configurar archivo `urls.py` en `frontend_producto`**

Crea y edita `frontend_producto/urls.py`:

```python
# frontend_producto/urls.py
from django.urls import path
from . import views

urlpatterns = [
    path('', views.pagina_inicial, name='inicio'),
    path('productos/', views.listado_productos, name='listado_productos'),
    path('productos/crear/', views.crear_producto, name='crear_producto'),
    path('productos/editar/<int:pk>/', views.editar_producto, name='editar_producto'),
    path('productos/borrar/<int:pk>/', views.borrar_producto, name='borrar_producto'),
]
```

#### **16. Crear el archivo `styles.css`**

Edita `static/css/styles.css`:

```css
/* static/css/styles.css */
body {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

main {
    flex: 1;
}

/* Mejora la apariencia de los formularios generados por {{ form.as_p }} */
form p {
    margin-bottom: 1rem;
}

form label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
}
```

---

### **¡Proyecto Finalizado!**

Ahora, ejecuta el servidor de nuevo:
```bash
python manage.py runserver
```
Tu aplicación está totalmente funcional:
*   **Página de inicio**: `http://127.0.0.1:8000/`
*   **Listado de productos**: `http://127.0.0.1:8000/productos/`
*   **Crear producto**: `http://127.0.0.1:8000/productos/crear/`
*   Puedes editar y borrar productos desde el listado.
*   Puedes acceder al panel de admin en `http://127.0.0.1:8000/admin/` para gestionar los datos directamente.

Este proyecto aplica las buenas prácticas de Django, como separar la lógica en apps, usar el ORM, formularios de modelo, plantillas con herencia y una estructura de URLs clara y mantenible.
