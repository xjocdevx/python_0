# MÓDULO 1: Cimientos y Entorno Moderno
Sesión 1.1: Configuración del Entorno (1 hora)
Teoría (20 min)

Python 3.14: características y ventajas para principiantes

El nuevo REPL interactivo: colores, autocompletado, ayuda integrada

Práctica Guiada (40 min)
Ejercicio No.1
```python
# Ejercicio 1: Primer contacto con REPL
# Comandos en terminal:
# >>> nombre = "Estudiante"
# >>> print(f"Hola, {nombre}!")
# >>> ayuda(str)  # Explorar documentación integrada
```
Ejercicio No.2
```python
# Ejercicio 2: Configurar VS Code
# Crear primer script: hola_mundo.py
print("=" * 50)
print("BIENVENIDO A PYTHON 3.14")
print("=" * 50)

nombre = input("¿Cómo te llamas? ")
print(f"Encantado de conocerte, {nombre}!")
print(f"La versión de Python es: 3.14+")
```
Sesión 1.2: Variables y Tipos Primitivos (1.5 horas)
Teoría (30 min)

int, float, str, bool

Tipado dinámico vs estático

f-strings avanzados: formato, alineación, expresiones

Práctica Intensiva (1 hora)
Ejercicio No.3
```python
# Ejercicio 3: Calculadora de edad canina
edad_humana = int(input("Ingresa tu edad: "))
edad_perro = edad_humana * 7
print(f"Tu edad en años perro sería: {edad_perro} años 🐕")
```
Ejercicio No.4
```python
# Ejercicio 4: Formateo avanzado
precio = 49.95
descuento = 0.15
precio_final = precio * (1 - descuento)
print(f"Precio original: ${precio:>10.2f}")
print(f"Descuento: {descuento:.1%}")
print(f"Total: ${precio_final:>13.2f}")
```
```python
# Ejercicio 5: Booleans en acción
tiene_licencia = input("¿Tienes licencia? (si/no): ").lower() == "si"
edad = int(input("Edad: "))
puede_conducir = edad >= 18 and tiene_licencia
print(f"¿Puede conducir? {puede_conducir}")
```
Sesión 1.3: Entrada/Salida y Debugging (1.5 horas)
Práctica con errores comunes (45 min)

```python
# Ejercicio 6: Debug con mensajes mejorados Python 3.14
# Los estudiantes cometen errores intencionales para ver los mensajes

# Error 1: TypeError
numero = "10"
# resultado = numero + 5  # Descomentar para ver error

# Solución: Conversión explícita
resultado = int(numero) + 5
print(f"Resultado correcto: {resultado}")
```

```python
# Error 2: NameError
# print(variable_no_definida)  # Error controlado

# Ejercicio 7: Calculadora de propinas
print("CALCULADORA DE PROPINAS")
print("-" * 30)

total_cuenta = float(input("Total de la cuenta: $"))
porcentaje = float(input("Porcentaje de propina (10/15/20): "))

propina = total_cuenta * (porcentaje / 100)
total_final = total_cuenta + propina

print("\n" + "=" * 30)
print(f"Propina: ${propina:.2f}")
print(f"Total a pagar: ${total_final:.2f}")
print("=" * 30)
```
# MÓDULO 2: Lógica de Programación y Control (4 horas)
Sesión 2.1: Operadores y Condicionales (1.5 horas)
Teoría + Práctica (45 min)

```python
# Ejercicio 8: Clasificador de números
numero = float(input("Ingresa un número: "))

# Operadores de comparación y lógicos
if numero > 0:
    print("El número es positivo")
    if numero.is_integer():
        print("Y además es entero")
elif numero < 0:
    print("El número es negativo")
else:
    print("El número es cero")

# Operador módulo
if numero % 2 == 0 and numero != 0:
    print("Es par")
elif numero % 2 == 1:
    print("Es impar")
```
Sesión 2.2: Match-Case y Condicionales Avanzados (1 hora)
```python
# Ejercicio 9: Sistema de calificaciones con match-case
print("SISTEMA DE CALIFICACIONES")
print("Opciones: A, B, C, D, F")

calificacion = input("Ingresa tu calificación: ").upper()

match calificacion:
    case "A":
        mensaje = "Excelente, sigue así!"
    case "B":
        mensaje = "Buen trabajo, puedes mejorar"
    case "C":
        mensaje = "Suficiente, pero necesitas estudiar más"
    case "D":
        mensaje = "Debes esforzarte más"
    case "F":
        mensaje = "Requieres apoyo adicional"
    case _:
        mensaje = "Calificación no válida"

print(f"Resultado: {mensaje}")

# Versión alternativa sin match-case (para referencia)
def calificacion_tradicional(letra):
    if letra == "A":
        return "Excelente"
    elif letra == "B":
        return "Bueno"
    elif letra == "C":
        return "Suficiente"
    else:
        return "No válida"
```
Ejercicio 10

```python
# Ejercicio 10: Validador de contraseñas (proyecto parcial)
print("\nVALIDACIÓN DE CONTRASEÑA")
print("- Requisitos:")
print("  • Mínimo 8 caracteres")
print("  • Al menos un número")
print("  • Al menos una mayúscula")

password = input("Crea tu contraseña: ")

tiene_longitud = len(password) >= 8
tiene_numero = any(c.isdigit() for c in password)
tiene_mayuscula = any(c.isupper() for c in password)

if tiene_longitud and tiene_numero and tiene_mayuscula:
    print("✅ Contraseña segura")
else:
    print("❌ Contraseña débil:")
    if not tiene_longitud:
        print("  - Debe tener al menos 8 caracteres")
    if not tiene_numero:
        print("  - Debe incluir al menos un número")
    if not tiene_mayuscula:
        print("  - Debe incluir al menos una mayúscula")
Sesión 2.3: Bucles For y While (1.5 horas)
```
Ejercicio 11
```python
# Ejercicio 11: Tablas de multiplicar con for
print("GENERADOR DE TABLAS DE MULTIPLICAR")
numero = int(input("¿Qué tabla quieres ver? "))

for i in range(1, 11):
    resultado = numero * i
    print(f"{numero:2} x{i:2} ={resultado:3}")

# range() explicado
print("\nExplorando range():")
print(list(range(5)))        # [0, 1, 2, 3, 4]
print(list(range(2, 8)))      # [2, 3, 4, 5, 6, 7]
print(list(range(1, 10, 2)))  # [1, 3, 5, 7, 9]
```
Ejercicio 12:

```python
# Ejercicio 12: Adivinanza con while
import random

print("\nJUEGO DE ADIVINANZA")
print("Adivina el número entre 1 y 20")

secreto = random.randint(1, 20)
intentos = 0
adivinado = False

while not adivinado and intentos < 5:
    intentos += 1
    guess = int(input(f"Intento {intentos}/5: "))
    
    if guess == secreto:
        print(f"🎉 ¡Correcto! Lo lograste en {intentos} intentos")
        adivinado = True
    elif guess < secreto:
        print("📉 Muy bajo")
    else:
        print("📈 Muy alto")

if not adivinado:
    print(f"😢 Lo siento, el número era {secreto}")
```

Ejercicio 13:

```python
# Ejercicio 13: Control de bucles
print("\nNÚMEROS ESPECIALES")
for i in range(1, 21):
    if i % 3 == 0:
        continue  # Saltar múltiplos de 3
    if i > 15:
        break     # Detener después de 15
    print(f"Número: {i}")
```
MÓDULO 3: Colecciones y Estructuras de Datos (4 horas)
Sesión 3.1: Listas y Tuplas (1.5 horas)
```python
# Ejercicio 14: Gestor de lista de compras
print("LISTA DE COMPRAS INTERACTIVA")
compras = []

while True:
    print("\n1. Agregar item")
    print("2. Ver lista")
    print("3. Eliminar item")
    print("4. Salir")
    
    opcion = input("Selecciona opción: ")
    
    if opcion == "1":
        item = input("Item a comprar: ")
        compras.append(item)
        print(f"✅ '{item}' agregado")
    elif opcion == "2":
        if compras:
            print("\nTU LISTA:")
            for i, item in enumerate(compras, 1):
                print(f"{i}. {item}")
        else:
            print("📋 Lista vacía")
    elif opcion == "3":
        if compras:
            for i, item in enumerate(compras, 1):
                print(f"{i}. {item}")
            idx = int(input("Número a eliminar: ")) - 1
            if 0 <= idx < len(compras):
                eliminado = compras.pop(idx)
                print(f"🗑️ '{eliminado}' eliminado")
        else:
            print("📋 Lista vacía")
    elif opcion == "4":
        print("¡Hasta luego!")
        break
    else:
        print("❌ Opción no válida")
```
Ejercicio 15
```python
# Ejercicio 15: Slicing y métodos de listas
numeros = list(range(1, 11))
print(f"Original: {numeros}")
print(f"Primeros 3: {numeros[:3]}")
print(f"Últimos 3: {numeros[-3:]}")
print(f"Paso 2: {numeros[::2]}")
print(f"Invertido: {numeros[::-1]}")
```
Sesión 3.2: Diccionarios y Conjuntos (1.5 horas)
```python
# Ejercicio 16: Mini directorio telefónico
directorio = {}

print("DIRECTORIO TELEFÓNICO")
while True:
    print("\n1. Agregar contacto")
    print("2. Buscar contacto")
    print("3. Listar todos")
    print("4. Salir")
    
    opcion = input("Opción: ")
    
    if opcion == "1":
        nombre = input("Nombre: ").capitalize()
        telefono = input("Teléfono: ")
        directorio[nombre] = telefono
        print(f"✅ Contacto {nombre} guardado")
    elif opcion == "2":
        nombre = input("Nombre a buscar: ").capitalize()
        if nombre in directorio:
            print(f"📞 {nombre}: {directorio[nombre]}")
        else:
            print("❌ No encontrado")
    elif opcion == "3":
        if directorio:
            print("\nCONTACTOS:")
            for nombre, telefono in directorio.items():
                print(f"  • {nombre}: {telefono}")
        else:
            print("📋 Directorio vacío")
    elif opcion == "4":
        break
```
Ejercicio 17:

```python
# Ejercicio 17: Conjuntos para evitar duplicados
invitados = set()
print("\nLISTA DE INVITADOS (sin duplicados)")

for i in range(5):
    nombre = input(f"Invitado {i+1}: ").capitalize()
    invitados.add(nombre)

print(f"\nInvitados únicos ({len(invitados)} personas):")
for invitado in sorted(invitados):
    print(f"  • {invitado}")
```
Sesión 3.3: Comprensión de Listas y Manejo de Errores (1 hora)

```python
# Ejercicio 18: Comprensión de listas
numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Forma tradicional vs Pythonic
pares_tradicional = []
for n in numeros:
    if n % 2 == 0:
        pares_tradicional.append(n)

pares_pythonic = [n for n in numeros if n % 2 == 0]

print(f"Pares (tradicional): {pares_tradicional}")
print(f"Pares (pythonic): {pares_pythonic}")

cuadrados = [n**2 for n in numeros]
print(f"Cuadrados: {cuadrados}")

```
Ejercicio 19:

```python
# Ejercicio 19: Manejo de errores con mensajes Python 3.14
print("\nCALCULADORA SEGURA")

while True:
    try:
        num1 = float(input("Primer número: "))
        num2 = float(input("Segundo número: "))
        operacion = input("Operación (+, -, *, /): ")
        
        if operacion == "+":
            resultado = num1 + num2
        elif operacion == "-":
            resultado = num1 - num2
        elif operacion == "*":
            resultado = num1 * num2
        elif operacion == "/":
            resultado = num1 / num2
        else:
            print("❌ Operación no válida")
            continue
            
        print(f"Resultado: {resultado}")
        
    except ValueError as e:
        print(f"❌ Error: Debes ingresar números válidos")
        print(f"   Detalle: {e}")
    except ZeroDivisionError as e:
        print(f"❌ Error: No se puede dividir por cero")
        print(f"   Detalle: {e}")
    except Exception as e:
        print(f"❌ Error inesperado: {e}")
    
    continuar = input("¿Otra operación? (s/n): ").lower()
    if continuar != 's':
        break
```
#MÓDULO 4: Funciones y Modularización (4 horas)
Sesión 4.1: Definición de Funciones (1.5 horas)

Ejercicio 20:
```python
# Ejercicio 20: Creando nuestra primera biblioteca de funciones
def mostrar_banner():
    """Muestra el banner de la aplicación"""
    print("=" * 50)
    print("SISTEMA DE GESTIÓN".center(50))
    print("=" * 50)

def calcular_promedio(notas):
    """Calcula el promedio de una lista de notas"""
    if not notas:
        return 0
    return sum(notas) / len(notas)

def clasificar_rendimiento(promedio):
    """Clasifica el rendimiento según el promedio"""
    if promedio >= 90:
        return "Excelente"
    elif promedio >= 70:
        return "Bueno"
    elif promedio >= 60:
        return "Suficiente"
    else:
        return "Necesita mejorar"

# Programa principal
mostrar_banner()
notas_estudiante = []

print("INGRESO DE NOTAS (0 para terminar)")
while True:
    try:
        nota = float(input("Nota: "))
        if nota == 0:
            break
        if 0 < nota <= 100:
            notas_estudiante.append(nota)
        else:
            print("Nota debe estar entre 1 y 100")
    except ValueError:
        print("Ingresa un número válido")

if notas_estudiante:
    promedio = calcular_promedio(notas_estudiante)
    rendimiento = clasificar_rendimiento(promedio)
    
    print("\nRESULTADOS")
    print(f"Notas: {notas_estudiante}")
    print(f"Promedio: {promedio:.2f}")
    print(f"Rendimiento: {rendimiento}")
```
Sesión 4.2: Parámetros y Return (1 hora)

```python
# Ejercicio 21: Parámetros con valores por defecto
def crear_usuario(nombre, edad, ciudad="Desconocida", activo=True):
    """Crea un diccionario con información de usuario"""
    return {
        "nombre": nombre,
        "edad": edad,
        "ciudad": ciudad,
        "activo": activo
    }

# Diferentes formas de llamar la función
usuario1 = crear_usuario("Ana", 25, "Madrid")
usuario2 = crear_usuario("Carlos", 30)  # Usa ciudad por defecto
usuario3 = crear_usuario(nombre="Luis", edad=22, activo=False)

print("USUARIOS CREADOS")
for i, usuario in enumerate([usuario1, usuario2, usuario3], 1):
    print(f"\nUsuario {i}:")
    for clave, valor in usuario.items():
        print(f"  {clave}: {valor}")
```
Ejercicio 22: 
```python
# Ejercicio 22: *args y **kwargs
def sumar_todos(*args):
    """Suma un número variable de argumentos"""
    return sum(args)

def mostrar_info(**kwargs):
    """Muestra información con nombre"""
    for clave, valor in kwargs.items():
        print(f"  {clave}: {valor}")

print(f"\nSuma de varios números: {sumar_todos(1, 2, 3, 4, 5)}")
print("Información variable:")
mostrar_info(nombre="Ana", edad=25, ciudad="Madrid")

```
Ejercicio 23:

```python
def operar_numeros(a, b, operacion="suma"):
    """Realiza operaciones matemáticas básicas"""
    try:
        a, b = float(a), float(b)
        
        if operacion == "suma":
            return a + b, None
        elif operacion == "resta":
            return a - b, None
        elif operacion == "multiplicacion":
            return a * b, None
        elif operacion == "division":
            if b == 0:
                return None, "Error: división por cero"
            return a / b, None
        else:
            return None, "Operación no soportada"
    except ValueError:
        return None, "Error: valores no numéricos"

# Probando la función
resultado, error = operar_numeros(10, 2, "division")
if error:
    print(f"❌ {error}")
else:
    print(f"✅ Resultado: {resultado}")
```
Sesión 4.3: Scope, Módulos y pip (1.5 horas)

```python
# Ejercicio 24: Variables locales vs globales
contador_global = 0

def incrementar():
    """Demuestra el scope de variables"""
    global contador_global
    contador_local = 0
    
    contador_global += 1
    contador_local += 1
    
    print(f"Dentro - Global: {contador_global}, Local: {contador_local}")

print("SCOPE DE VARIABLES")
for _ in range(3):
    incrementar()
    print(f"Fuera   - Global: {contador_global}")

```
Ejercicio 25:

```python
# Ejercicio 25: Usando módulos de la librería estándar
import math
import datetime
import random
import os
import sys

print("\nMÓDULOS DE LA LIBRERÍA ESTÁNDAR")

# math
radio = 5
area = math.pi * radio**2
print(f"Área círculo (r={radio}): {area:.2f}")
print(f"Raíz cuadrada de 16: {math.sqrt(16)}")

# datetime
ahora = datetime.datetime.now()
print(f"Fecha actual: {ahora.strftime('%d/%m/%Y %H:%M')}")
print(f"Año actual: {ahora.year}")

# random
numeros_aleatorios = [random.randint(1, 100) for _ in range(5)]
print(f"Números aleatorios: {numeros_aleatorios}")
print(f"Elección aleatoria: {random.choice(['rojo', 'verde', 'azul'])}")

# os y sys
print(f"Directorio actual: {os.getcwd()}")
print(f"Archivos en directorio: {os.listdir('.')[:5]}...")
print(f"Versión de Python: {sys.version}")
```
Ejercicio 26:
```python
# Ejercicio 26: Creando nuestro primer módulo
# Crear archivo 'utilidades.py' con:
"""
def saludar(nombre):
    return f"¡Hola {nombre}!"

def despedir(nombre):
    return f"¡Hasta luego {nombre}!"

def calcular_edad(ano_nacimiento):
    from datetime import datetime
    return datetime.now().year - ano_nacimiento

PI = 3.14159
"""

# main.py
"""
import utilidades

nombre = input("Tu nombre: ")
print(utilidades.saludar(nombre))
print(f"Valor de PI: {utilidades.PI}")
ano = int(input("Año de nacimiento: "))
edad = utilidades.calcular_edad(ano)
print(f"Tienes {edad} años")
"""
```
Ejercicio 27:
```python
# Ejercicio 27: Instalación básica con pip
print("\n📦 INSTALACIÓN DE PAQUETES CON PIP")
print("Comandos útiles:")
print("  pip list                    # Ver paquetes instalados")
print("  pip install requests         # Instalar un paquete")
print("  pip show requests            # Ver información del paquete")
print("  pip uninstall requests       # Desinstalar paquete")
print("  pip freeze > requirements.txt # Guardar dependencias")

# Ejemplo de uso de requests (si está instalado)
try:
    import requests
    print("\n✅ requests está instalado")
except ImportError:
    print("\n❌ requests no está instalado")
    print("Para instalarlo: pip install requests")
```
MÓDULO 5: Proyecto Final y Futuro (4 horas)
Sesión 5.1: Taller Práctico - Gestor de Tareas (2 horas)

```python
"""
GESTOR DE TAREAS PERSONALIZADO
Proyecto Final - Curso Python Básico 3.12
"""

import json
import os
from datetime import datetime

# Constantes
ARCHIVO_TAREAS = "tareas.json"

def limpiar_pantalla():
    """Limpia la pantalla de la terminal"""
    os.system('cls' if os.name == 'nt' else 'clear')

def cargar_tareas():
    """Carga las tareas desde el archivo JSON"""
    if os.path.exists(ARCHIVO_TAREAS):
        try:
            with open(ARCHIVO_TAREAS, 'r', encoding='utf-8') as f:
                return json.load(f)
        except (json.JSONDecodeError, IOError):
            return []
    return []

def guardar_tareas(tareas):
    """Guarda las tareas en el archivo JSON"""
    try:
        with open(ARCHIVO_TAREAS, 'w', encoding='utf-8') as f:
            json.dump(tareas, f, indent=2, ensure_ascii=False)
        return True
    except IOError:
        print("❌ Error al guardar las tareas")
        return False

def mostrar_menu():
    """Muestra el menú principal"""
    print("\n" + "=" * 60)
    print("📋 GESTOR DE TAREAS PERSONALIZADO".center(60))
    print("=" * 60)
    print("1. 📝 Ver todas las tareas")
    print("2. ➕ Agregar nueva tarea")
    print("3. ✅ Marcar tarea como completada")
    print("4. 🗑️ Eliminar tarea")
    print("5. 📊 Ver estadísticas")
    print("6. 🔍 Buscar tareas")
    print("7. 🚪 Salir")
    print("-" * 60)

def mostrar_tareas(tareas, titulo="LISTA DE TAREAS", solo_pendientes=False):
    """Muestra las tareas formateadas"""
    if not tareas:
        print("📭 No hay tareas")
        return False
    
    if solo_pendientes:
        tareas_mostrar = [t for t in tareas if not t.get('completada', False)]
        if not tareas_mostrar:
            print("🎉 ¡No hay tareas pendientes!")
            return False
    else:
        tareas_mostrar = tareas
    
    print("\n" + "-" * 60)
    print(f"📌 {titulo}".center(60))
    print("-" * 60)
    
    for i, tarea in enumerate(tareas_mostrar, 1):
        estado = "✅" if tarea.get('completada', False) else "⭕"
        fecha = tarea.get('fecha_creacion', 'Sin fecha')
        print(f"{i:2}. {estado} {tarea['titulo']}")
        print(f"     📅 Creada: {fecha}")
        if tarea.get('descripcion'):
            print(f"     📝 {tarea['descripcion']}")
        if tarea.get('fecha_completado'):
            print(f"     ✅ Completada: {tarea['fecha_completado']}")
    print("-" * 60)
    return True

def agregar_tarea(tareas):
    """Agrega una nueva tarea"""
    print("\n➕ AGREGAR NUEVA TAREA")
    
    titulo = input("Título: ").strip()
    if not titulo:
        print("❌ El título no puede estar vacío")
        return tareas
    
    descripcion = input("Descripción (opcional): ").strip()
    fecha = datetime.now().strftime("%d/%m/%Y %H:%M")
    
    nueva_tarea = {
        "titulo": titulo,
        "descripcion": descripcion,
        "fecha_creacion": fecha,
        "completada": False
    }
    
    tareas.append(nueva_tarea)
    if guardar_tareas(tareas):
        print(f"✅ Tarea '{titulo}' agregada correctamente")
    return tareas

def completar_tarea(tareas):
    """Marca una tarea como completada"""
    pendientes = [t for t in tareas if not t.get('completada', False)]
    
    if not pendientes:
        print("🎉 ¡No hay tareas pendientes!")
        return tareas
    
    if not mostrar_tareas(pendientes, "TAREAS PENDIENTES"):
        return tareas
    
    try:
        idx = int(input("\nNúmero de tarea a completar: ")) - 1
        if 0 <= idx < len(pendientes):
            # Encontrar la tarea en la lista original
            tarea_completar = pendientes[idx]
            for t in tareas:
                if (t['titulo'] == tarea_completar['titulo'] and 
                    t['fecha_creacion'] == tarea_completar['fecha_creacion']):
                    t['completada'] = True
                    t['fecha_completado'] = datetime.now().strftime("%d/%m/%Y %H:%M")
                    break
            if guardar_tareas(tareas):
                print(f"✅ Tarea completada: {tarea_completar['titulo']}")
        else:
            print("❌ Número no válido")
    except ValueError:
        print("❌ Ingresa un número válido")
    
    return tareas

def eliminar_tarea(tareas):
    """Elimina una tarea"""
    if not mostrar_tareas(tareas, "SELECCIONA TAREA A ELIMINAR"):
        return tareas
    
    try:
        idx = int(input("\nNúmero de tarea a eliminar: ")) - 1
        if 0 <= idx < len(tareas):
            tarea_eliminada = tareas.pop(idx)
            if guardar_tareas(tareas):
                print(f"🗑️ Tarea eliminada: {tarea_eliminada['titulo']}")
        else:
            print("❌ Número no válido")
    except ValueError:
        print("❌ Ingresa un número válido")
    
    return tareas

def mostrar_estadisticas(tareas):
    """Muestra estadísticas de las tareas"""
    total = len(tareas)
    if total == 0:
        print("📭 No hay tareas para mostrar estadísticas")
        return
    
    completadas = sum(1 for t in tareas if t.get('completada', False))
    pendientes = total - completadas
    
    print("\n" + "=" * 60)
    print("📊 ESTADÍSTICAS".center(60))
    print("=" * 60)
    print(f"Total de tareas: {total}")
    print(f"✅ Completadas: {completadas} ({completadas/total*100:.1f}%)")
    print(f"⭕ Pendientes: {pendientes} ({pendientes/total*100:.1f}%)")
    
    if completadas > 0:
        print("\nÚltimas tareas completadas:")
        completadas_recientes = [t for t in tareas if t.get('completada', False)]
        for t in completadas_recientes[-3:]:
            print(f"  • {t['titulo']} - {t.get('fecha_completado', '')}")
    
    if pendientes > 0:
        print(f"\nTarea más antigua pendiente:")
        pendientes_lista = [t for t in tareas if not t.get('completada', False)]
        if pendientes_lista:
            mas_antigua = min(pendientes_lista, key=lambda x: x['fecha_creacion'])
            print(f"  • {mas_antigua['titulo']} ({mas_antigua['fecha_creacion']})")
    
    print("=" * 60)

def buscar_tareas(tareas):
    """Busca tareas por palabra clave"""
    if not tareas:
        print("📭 No hay tareas")
        return
    
    termino = input("Ingresa término de búsqueda: ").lower().strip()
    if not termino:
        print("Término de búsqueda vacío")
        return
    
    resultados = []
    for t in tareas:
        if (termino in t['titulo'].lower() or 
            termino in t.get('descripcion', '').lower()):
            resultados.append(t)
    
    if resultados:
        mostrar_tareas(resultados, f"RESULTADOS PARA '{termino}'")
    else:
        print(f"No se encontraron tareas con '{termino}'")

def main():
    """Función principal del programa"""
    tareas = cargar_tareas()
    
    while True:
        mostrar_menu()
        opcion = input("Selecciona una opción (1-7): ").strip()
        
        if opcion == "1":
            mostrar_tareas(tareas, "TODAS LAS TAREAS")
        elif opcion == "2":
            tareas = agregar_tarea(tareas)
        elif opcion == "3":
            tareas = completar_tarea(tareas)
        elif opcion == "4":
            tareas = eliminar_tarea(tareas)
        elif opcion == "5":
            mostrar_estadisticas(tareas)
        elif opcion == "6":
            buscar_tareas(tareas)
        elif opcion == "7":
            print("\n👋 ¡Gracias por usar el Gestor de Tareas!")
            print("   ¡Hasta pronto!")
            break
        else:
            print("❌ Opción no válida. Intenta del 1 al 7.")
        
        input("\nPresiona Enter para continuar...")
        limpiar_pantalla()

if __name__ == "__main__":
    try:
        main()
    except KeyboardInterrupt:
        print("\n\n👋 Programa terminado por el usuario")
    except Exception as e:
        print(f"\n❌ Error inesperado: {e}")
```
Sesión 5.2: Buenas Prácticas y PEP 8 (1 hora)
Ejemplo 27: 
```python
"""
MÓDULO: buenas_practicas.py
DEMOSTRACIÓN DE PEP 8 Y BUENAS PRÁCTICAS PARA PYTHON 3.12
"""

# Ejemplo 27: Formato PEP 8
# MAL
def calcularArea(radio):
    return 3.14159*radio**2

# BIEN
def calcular_area_circulo(radio):
    """Calcula el área de un círculo dado su radio."""
    pi = 3.14159
    area = pi * radio ** 2
    return area

# Ejemplo 28: Nombres descriptivos
# MAL
def proc(d, u):
    r = []
    for i in d:
        if i > u:
            r.append(i)
    return r

# BIEN
def filtrar_numeros_mayores_que(numeros, umbral):
    """Retorna números mayores que el umbral especificado."""
    numeros_filtrados = []
    for numero in numeros:
        if numero > umbral:
            numeros_filtrados.append(numero)
    return numeros_filtrados
```
Ejemplo 29
```python
# Ejemplo 29: Comentarios y docstrings
def convertir_temperatura(valor, desde='celsius', hasta='fahrenheit'):
    """
    Convierte temperaturas entre Celsius y Fahrenheit.
    
    Args:
        valor (float): Temperatura a convertir
        desde (str): 'celsius' o 'fahrenheit'
        hasta (str): 'celsius' o 'fahrenheit'
    
    Returns:
        float: Temperatura convertida
    
    Examples:
        >>> convertir_temperatura(0, 'celsius', 'fahrenheit')
        32.0
    """
    if desde == 'celsius' and hasta == 'fahrenheit':
        return (valor * 9/5) + 32
    elif desde == 'fahrenheit' and hasta == 'celsius':
        return (valor - 32) * 5/9
    else:
        return valor
```
Ejemplo 30:
```python
# Ejemplo 30: Constantes en mayúsculas
PI = 3.14159
GRAVEDAD = 9.8
VELOCIDAD_LUZ = 299792458  # m/s
DIAS_SEMANA = ['lunes', 'martes', 'miércoles', 'jueves', 'viernes', 'sábado', 'domingo']
```
Ejemplo 31:

```python
# Ejemplo 31: Type Hints (disponible desde Python 3.5+)
def saludar(nombre: str) -> str:
    """Función con type hints"""
    return f"¡Hola {nombre}!"

def sumar_numeros(numeros: list[float]) -> float:
    """Suma una lista de números"""
    return sum(numeros)

# Uso de type hints
nombre_completo: str = "Ana García"
edades: list[int] = [25, 30, 22]
activo: bool = True

print("VERIFICADOR DE CÓDIGO PEP 8")
print("Para verificar PEP 8, instala:")
print("  pip install pycodestyle")
print("  pycodestyle buenas_practicas.py")
print("\nPara formatear automáticamente:")
print("  pip install black")
print("  black buenas_practicas.py")
```
Sesión 5.3: IA como Asistente y Cierre (1 hora)
Teoría y Demostración: Uso Ético de IA
Escenario 1:
```python
"""
MÓDULO: asistente_ia.py
DEMOSTRACIÓN DE CÓMO USAR IA EN EL APRENDIZAJE
"""

# Escenario 1: IA para explicar código
codigo_complejo = """
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b
"""

print("1. Preguntar a IA: 'Explica línea por línea esta función'")
print("2. Luego intentar explicarla con tus propias palabras")
```
Escenario 2:
```python
# Escenario 2: IA para encontrar bugs
codigo_con_error = """
def dividir(a, b):
    return a / b  # ¿Qué pasa si b es 0?
"""

print("\n✅ Buen uso: Preguntar '¿Qué errores puede tener este código?'")
print("❌ Mal uso: 'Escríbeme un programa completo' sin entenderlo")
```
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python
```python





