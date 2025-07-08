# Proyecto CRUD en Django

## Desarrolla Aplicaciones Web en un Sistema de Información

Este proyecto guía paso a paso el desarrollo de una aplicación web funcional en Django, comenzando desde Python básico hasta la implementación completa de un sistema CRUD (Crear, Leer, Actualizar, Eliminar) de productos.

---

## Unidad I - Fundamentos de Python

### Introducción a Python

Python es un lenguaje de alto nivel, con tipado dinámico, multiplataforma, y orientado a objetos. Su sintaxis clara permite un desarrollo rápido y eficiente.

### Variables

```python
nombre_curso = "Desarrollo Web con Django"
año = 2023
precio = 199.99
es_online = True
```

### Estructuras de Control (if/else)

```python
calificacion = 75
if calificacion >= 70:
    print("Aprobado")
elif calificacion >= 50:
    print("Recuperación")
else:
    print("Reprobado")
```

### Bucles (for)

```python
# Ejemplo 1
frutas = ["manzana", "banana"]
for fruta in frutas:
    print(fruta)

# Ejemplo 2
for i in range(1, 11):
    print(f"5 x {i} = {5*i}")
```

### Funciones

```python
def saludar(nombre):
    return f"Hola, {nombre}"

print(saludar("Ana"))
```

### Listas, Tuplas, Conjuntos, Diccionarios

```python
# Lista
tareas = ["estudiar", "comprar"]
tareas.append("programar")

# Tupla
coordenadas = (19.4, -99.1)

# Conjunto
numeros = set([1, 2, 2, 3])

# Diccionario
producto = {"nombre": "Laptop", "precio": 1200}
```

### Programación Orientada a Objetos (POO)

```python
class Coche:
    def __init__(self, marca):
        self.marca = marca

mi_coche = Coche("Toyota")
```

---

## Unidad II - Desarrollo con Django

### 1. Crear entorno virtual

```bash
mkdir mi_proyecto_django
cd mi_proyecto_django
python -m venv venv
source venv/bin/activate  # o .\venv\Scripts\activate en Windows
```

### 2. Instalar Django y crear proyecto

```bash
pip install django pillow
django-admin startproject backend_producto .
```

### 3. Crear app

```bash
python manage.py startapp frontend_producto
```

### 4. Registrar app en settings.py

```python
INSTALLED_APPS = [
    ...
    'frontend_producto',
]
```

### 5. Configurar URLs

```python
# backend_producto/urls.py
from django.urls import path, include
urlpatterns = [
    path('', include('frontend_producto.urls')),
]
```

### 6. Configuración de media, static y templates

```python
STATIC_URL = '/static/'
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
TEMPLATES[0]['DIRS'] = [os.path.join(BASE_DIR, 'templates')]
```

### 7. Crear modelo Producto

```python
# frontend_producto/models.py
class Producto(models.Model):
    nombre = models.CharField(max_length=200)
    imagen = models.ImageField(upload_to='productos/', null=True, blank=True)
    cantidad = models.IntegerField()
    precio = models.DecimalField(max_digits=10, decimal_places=2)
```

### 8. Migrar base de datos

```bash
python manage.py makemigrations
python manage.py migrate
```

### 9. Crear superusuario

```bash
python manage.py createsuperuser
```

### 10. Crear formulario con ModelForm

```python
# frontend_producto/forms.py
class ProductoForm(forms.ModelForm):
    class Meta:
        model = Producto
        fields = ['nombre', 'imagen', 'cantidad', 'precio']
```

### 11. Crear vistas (views.py)

```python
def listado_productos(request):
    productos = Producto.objects.all()
    return render(request, 'productos/listado_productos.html', {'productos': productos})
```

### 12. Configurar rutas (urls.py)

```python
# frontend_producto/urls.py
urlpatterns = [
    path('', views.pagina_inicial, name='inicio'),
    path('productos/', views.listado_productos, name='listado_productos'),
    path('productos/crear/', views.crear_producto, name='crear_producto'),
    path('productos/editar/<int:pk>/', views.editar_producto, name='editar_producto'),
    path('productos/borrar/<int:pk>/', views.borrar_producto, name='borrar_producto'),
]
```

### 13. Estructura de carpetas

```
mi_proyecto_django/
├── backend_producto/
├── frontend_producto/
│   ├── forms.py
│   ├── urls.py
├── media/
├── static/
│   └── css/styles.css
├── templates/
│   ├── base.html
│   ├── navbar.html
│   ├── footer.html
│   └── productos/
│       ├── agregar_producto.html
│       ├── editar_producto.html
│       └── listado_productos.html
```

### 14. Iniciar el servidor

```bash
python manage.py runserver
```

Accede a:

* Página de inicio: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
* Listado: [http://127.0.0.1:8000/productos/](http://127.0.0.1:8000/productos/)
* Crear: [http://127.0.0.1:8000/productos/crear/](http://127.0.0.1:8000/productos/crear/)
* Admin: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

---

## ¡Proyecto Finalizado!

Este proyecto aplica las buenas prácticas de Django: estructura MVT, uso de ORM, ModelForms, separación de responsabilidades y diseño limpio con Bootstrap.
