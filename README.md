#MÓDULO 1: Cimientos y Entorno Moderno (4 horas)
Sesión 1.1: Configuración del Entorno (1 hora)
Teoría (20 min)

Python 3.14: características y ventajas para principiantes

El nuevo REPL interactivo: colores, autocompletado, ayuda integrada

Práctica Guiada (40 min)

```python
# Ejercicio 1: Primer contacto con REPL
# Comandos en terminal:
# >>> nombre = "Estudiante"
# >>> print(f"Hola, {nombre}!")
# >>> ayuda(str)  # Explorar documentación integrada

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

python
# Ejercicio 3: Calculadora de edad canina
edad_humana = int(input("Ingresa tu edad: "))
edad_perro = edad_humana * 7
print(f"Tu edad en años perro sería: {edad_perro} años 🐕")

# Ejercicio 4: Formateo avanzado
precio = 49.95
descuento = 0.15
precio_final = precio * (1 - descuento)
print(f"Precio original: ${precio:>10.2f}")
print(f"Descuento: {descuento:.1%}")
print(f"Total: ${precio_final:>13.2f}")

# Ejercicio 5: Booleans en acción
tiene_licencia = input("¿Tienes licencia? (si/no): ").lower() == "si"
edad = int(input("Edad: "))
puede_conducir = edad >= 18 and tiene_licencia
print(f"¿Puede conducir? {puede_conducir}")
Sesión 1.3: Entrada/Salida y Debugging (1.5 horas)
Práctica con errores comunes (45 min)

python
# Ejercicio 6: Debug con mensajes mejorados Python 3.14
# Los estudiantes cometen errores intencionales para ver los mensajes

# Error 1: TypeError
numero = "10"
# resultado = numero + 5  # Descomentar para ver error

# Solución: Conversión explícita
resultado = int(numero) + 5
print(f"Resultado correcto: {resultado}")

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
MÓDULO 2: Lógica de Programación y Control (4 horas)
Sesión 2.1: Operadores y Condicionales (1.5 horas)
Teoría + Práctica (45 min)

python
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
Sesión 2.2: Match-Case y Condicionales Avanzados (1 hora)
python
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
python
# Ejercicio 11: Tablas de multiplicar con for
print("GENERADOR DE TABLAS DE MULTIPLICAR")
numero = int(input("¿Qué tabla quieres ver? "))

for i in range(1, 11):
    resultado = numero * i
    print(f"{numero:2} x {i:2} = {resultado:3}")

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

# Ejercicio 13: Control de bucles
print("\nNÚMEROS ESPECIALES")
for i in range(1, 21):
    if i % 3 == 0:
        continue  # Saltar múltiplos de 3
    if i > 15:
        break     # Detener después de 15
    print(f"Número: {i}")
MÓDULO 3: Colecciones y Estructuras de Datos (4 horas)
Sesión 3.1: Listas y Tuplas (1.5 horas)
python
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

# Ejercicio 15: Slicing y métodos de listas
numeros = list(range(1, 11))
print(f"Original: {numeros}")
print(f"Primeros 3: {numeros[:3]}")
print(f"Últimos 3: {numeros[-3:]}")
print(f"Paso 2: {numeros[::2]}")
print(f"Invertido: {numeros[::-1]}")
Sesión 3.2: Diccionarios y Conjuntos (1.5 horas)
