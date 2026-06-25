# Python: Trabajo Práctico 1 - Estructuras Fundamentales y Control de Flujo

Este repositorio contiene la resolución de un conjunto de ejercicios prácticos introductorios en **Python**. El proyecto está diseñado para fijar los pilares esenciales del lenguaje: modularización mediante la definición de funciones (`def`), captura interactiva de tipos de datos primitivos por consola (`input`), evaluación condicional mediante operadores aritméticos modulares y la gestión dinámica de colecciones lineales (listas) a través de estructuras iterativas de control.

---

## 💻 Código Fuente de los Ejercicios

El script integra las siguientes soluciones algorítmicas secuenciales:

```python
# ==========================================
# Ejercicio 1: Suma de Dos Números con Entrada del Usuario
# ==========================================
def sumar_n_user():
    """Solicita dos números enteros por consola, realiza la adición aritmética

    y despliega el resultado final en la terminal.
    """
    n1 = int(input("Ingrese el primer número: "))
    n2 = int(input("Ingrese el segundo número: "))
    
    suma = n1 + n2
    print("La suma de los dos números es:", suma)

# Ejecución del módulo 1
sumar_n_user()


# ==========================================
# Ejercicio 2: Evaluación de Paridad Numérica
# ==========================================
def par_o_impar():
    """Evalúa si un número entero ingresado por consola pertenece al conjunto

    de los números pares o impares utilizando el operador aritmético residuo.
    """
    n_user = int(input("Ingrese un número entero: "))
    
    # Comprobación mediante aritmética modular (módulo 2)
    if n_user % 2 == 0:
        print("El número es par")
    else:
        print("El número es impar")

# Ejecución del módulo 2
par_o_impar()


# ==========================================
# Ejercicio 3: Iteración y Despliegue de Colecciones
# ==========================================
# Inicialización de una lista estática con valores enteros ordenados
lts = [1, 2, 3, 4, 5]

print("\nElementos de la lista estática:")
# Estructura iterativa para recorrer de forma secuencial cada nodo indexado
for i in lts:
    print(i)


# ==========================================
# Ejercicio Extra: Llenado Dinámico y Agregación de Listas
# ==========================================
def suma_lista():
    """Permite al usuario definir el tamaño de una lista, inyectar datos

    de forma dinámica mediante un bucle de acumulación y calcular el total de los elementos.
    """
    lts = []  # Inicialización de una colección lineal mutable vacía
    ele_user = int(input("Ingrese la cantidad de elementos para la lista: "))

    # Bucle indexado controlado por rango para la captura de datos
    for i in range(ele_user):
        num = int(input("Ingrese un número para la lista: "))
        lts.append(num)  # Inserción atómica al final de la estructura

    # Aplicación de la función nativa sum() para agregación lineal rápida
    suma = sum(lts)
    print("La suma de los elementos de la lista es:", suma)

# Ejecución del módulo extra
suma_lista()

```

---

## 🛠️ Conceptos Técnicos Aplicados

* **Casteo Directo de Tipos de Datos (`Type Casting`)**: Uso de la función constructora `int()` para forzar y transformar las cadenas de texto crudas provenientes de `input()` en variables numéricas enteras, evitando errores de operaciones lógicas incompatibles.
* **Operador de Residuo o Módulo (`%`)**: Herramienta de aritmética discreta que extrae el resto de una división entera. Al evaluar con `% 2`, permite determinar con absoluta certeza matemática la paridad de una variable aleatoria o constante.
* **Inserción Dinámica en Listas (`In-Place Appending`)**: Aplicación del método integrado `.append()` dentro de estructuras de bucle para construir colecciones lineales de longitud variable sobre la memoria en tiempo de ejecución.
* **Encapsulamiento Modular (`def`)**: Agrupación de bloques lógicos de código bajo funciones nombradas independientes, promoviendo la legibilidad, el aislamiento de variables y la reutilización de código limpio.

