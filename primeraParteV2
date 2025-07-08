## DESARROLLA APLICACIONES WEB EN UN SISTEMA DE INFORMACIÓN

### Implementa aplicaciones web en Django funcional

---

## Unidad I primera parte (Python)

### Breve Introducción a Python

**Resumen:** Python es un lenguaje de programación de alto nivel, interpretado, de tipado dinámico y multiparadigma. Es famoso por su sintaxis clara y legible, que se asemeja al lenguaje humano. Esto reduce la curva de aprendizaje y los costos de mantenimiento. Su vasta biblioteca estándar y el gran ecosistema de paquetes de terceros (como Django) lo hacen extremadamente versátil para desarrollo web, ciencia de datos, inteligencia artificial, scripting y más.

---

### Variables

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

### Estructuras de control if else

**Resumen:** Permiten ejecutar bloques de código según condiciones lógicas.

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

### Estructuras de repetición for

```python
# Ejemplo 1: Recorrer una lista de frutas
frutas = ["manzana", "banana", "cereza", "naranja"]

print("\n--- Lista de Frutas Disponibles ---")
for fruta in frutas:
    print(f"- {fruta.capitalize()}")

# Ejemplo 2: Generar la tabla de multiplicar del 5
print("\n--- Tabla de Multiplicar del 5 ---")
for i in range(1, 11):
    resultado = 5 * i
    print(f"5 x {i} = {resultado}")
```

---

### Funciones creadas por el usuario

```python
# Ejemplo 1: Función simple sin parámetros ni retorno
def mostrar_bienvenida():
    print("\n¡Bienvenido al sistema de gestión!")

# Ejemplo 2: Función con parámetros
def saludar_usuario(nombre):
    print(f"Hola, {nombre}. ¡Qué bueno verte!")

# Ejemplo 3: Función con retorno
def calcular_iva(monto_base):
    iva = monto_base * 0.19
    return iva

mostrar_bienvenida()
saludar_usuario("Ana")
monto_sin_iva = 10000
iva_calculado = calcular_iva(monto_sin_iva)
print(f"El IVA para un monto de ${monto_sin_iva} es: ${iva_calculado}")
print(f"El total a pagar es: ${monto_sin_iva + iva_calculado}")
```

---

### Listas

```python
# Ejemplo 1: Creación y modificación de una lista
tareas_pendientes = ["Estudiar Python", "Hacer la compra", "Llamar al dentista"]
tareas_pendientes[1] = "Comprar víveres en el supermercado"

# Ejemplo 2: Añadir, eliminar y recorrer una lista
tareas_pendientes.append("Preparar la cena")
tareas_pendientes.remove("Llamar al dentista")

for i, tarea in enumerate(tareas_pendientes, 1):
    print(f"{i}. {tarea}")
```

---

### Tuplas

```python
# Ejemplo 1: Coordenadas geográficas
coordenadas_oficina = (19.4326, -99.1332)
print(f"Coordenadas: {coordenadas_oficina}")

# Ejemplo 2: Desempaquetado
def obtener_datos_usuario():
    return ("john_doe", "john.doe@example.com", 35)

usuario = obtener_datos_usuario()
nombre_usuario, email, edad = usuario
```

---

### Conjuntos

```python
# Ejemplo 1: Eliminar duplicados
numeros = [1,2,2,3,4,4,5]
print(set(numeros))

# Ejemplo 2: Operaciones de conjuntos
admin = {"crear", "borrar", "editar"}
editor = {"editar"}
print(admin - editor)
print(admin & editor)
```

---

### Diccionarios

```python
producto = {"nombre": "Laptop", "precio": 1200.50, "stock": 10}
producto["garantia"] = "2 años"

for clave, valor in producto.items():
    print(f"{clave}: {valor}")
```

---

### Programación Orientada a Objetos

```python
class Coche:
    def __init__(self, marca, modelo, año):
        self.marca = marca
        self.modelo = modelo
        self.año = año
        self.encendido = False

    def arrancar(self):
        if not self.encendido:
            self.encendido = True
            print("Coche arrancado")

coche1 = Coche("Toyota", "Corolla", 2022)
coche1.arrancar()
```

```python
class CuentaBancaria:
    def __init__(self, titular, saldo=0):
        self.titular = titular
        self.saldo = saldo

    def depositar(self, monto):
        self.saldo += monto

    def retirar(self, monto):
        if monto <= self.saldo:
            self.saldo -= monto

cuenta = CuentaBancaria("Carlos", 500)
cuenta.depositar(200)
cuenta.retirar(100)
```

---

## Unidad I segunda parte (Configura el entorno Django)

*(continúa con creación del entorno virtual, instalación de Django, estructura de directorios, configuración de settings.py, creación de modelos, formularios, vistas, templates y URLs, así como buenas prácticas)*

---

Para continuar, puedo seguir agregando más contenido del desarrollo Django (puntos 1 al 16) al documento `.md`. ¿Quieres que lo incluya ahora también?

si todo por favor
