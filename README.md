# python_0
Python Básico
MÓDULO 1: Cimientos y Entorno Moderno (4 horas)
Sesión 1.1: Configuración del Entorno (1 hora)
Teoría (20 min)

Python 3.14: características y ventajas para principiantes

El nuevo REPL interactivo: colores, autocompletado, ayuda integrada

Práctica Guiada (40 min)

´´´python
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
´´´
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
