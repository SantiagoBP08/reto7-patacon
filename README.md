# RETO #7
Desarrolle la mayoría de los ejercicios en clase. Para cada punto cree un programa individual, además cree un cuaderno con la solución a todos los problemas. Al finalizar suba todo a un repo y subalo al canal reto_7 en slack.

Nota: Todo el código de aquí en adelante debe ir debidamente documentado.

1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

       def imprimir_cuadrados():
       """
       Imprime los números del 1 al 100 con sus respectivos cuadrados.
       """
       numero = 1 # Iniciamos definiendo la variable en 1
       while numero <= 100: # Se utiliza el ciclo while para recorrer todos los números del 1 al 100
       cuadrado = numero ** 2 #  Calculamos el cuadrado del número
       print(f"{numero}^2 = {numero**2}") # Imprimimos el número y su cuadrado
       numero += 1 #Incrementamos el número en 1 y así hasta que llegue a 100
    
       if _name_ == "_main_":
       imprimir_cuadrados()

 2. Imprima un listado con los números iguales desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

        def numeros_impares():
        """
        Imprime los numeros impares del 1 al 1000
        Comienza en el 1 y suma de 2 en 2 hasta llegar a 1000
        """

        num = 1 # Dar el primer valor impar
        while num <= 1000: # Se utiliza el ciclo while para recorrer todos los números menores a 1000
        print(num) # Imprimir el número impar actual
        num += 2 # Sumar 2 para avanzar al siguiente impar

        def numeros_pares():
        """
        Imprime los números pares del 1 al 1000
        Comienza en el 2 y suma de 2 en 2 hasta llegar a 1000
        """

        num = 2 # Dar el primer valor par
        while num <= 1000: # Se utiliza el ciclo while para recorrer todos los números menores a 1000
        print(num) # Imprimir el número par actual
        num += 2 # Sumar 2 para avanzar al siguiente par

        if _name_ == "_main_":
        print("Pares del 1 al 1000") # Título para lo pares
        numeros_pares() # Llamada a la función de los pares

        print("Impares del 1 al 1000") # Título para los impares
        numeros_impares() # Llamada a la función de los impares

3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado

       def numeros_pares_descendentes(n):
       """
       Imprime los números pares en orden descendente desde n hasta 2.

       Parámetros: 
       - n (int): Número natural mayor o igual a 2
       Si n es impar, se reduce 1 para comenzar desde el par más cercano
       """
       if n % 2 != 0: # Revisamos si n es par o impar dependiendo de su módulo, si su residuo es 0 es par, si es 1 es impar.
         n -= 1 # Ajuste si n es impar, se resta 1 y así empezamos desde el impar anterior.
       while n >= 2: # Se utiliza el ciclo while para recorrer todos los números mayores a 2 
           print(n) # Imprimir el número par actual
           n -=2 # Se resta 2 para ir al siguiente par menor

       # Punto de entrada del usuario
       if _name_ == "_main_":
       n = int(input("Ingrese un número natural mayor o igual a 2: ")) # Solicitar al usuario que digite un número
       numeros_pares_descendentes(n) # Llamada a la función de los pares descentendes
   
4. Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial

       def calcular_factorial(num):
       """
        Calcula el factorial de un número dado.
    
        Parámetros:
        num (int): Número del cual se calculará el factorial.
        Retorno:
        int: Factorial del número dado.
       """
        factorial = 1
       for i in range(1, num + 1):
        factorial *= i
        return factorial

       def imprimir_factoriales(n):
        """
        Imprime los números del 1 hasta n con sus respectivos factoriales.
    
        Parámetros:
        n (int): Límite superior de números a imprimir.
        """
        print(f"{'Número':<10}{'Factorial':<10}")
        print("-" * 25)
    
        for numero in range(1, n + 1):
        print(f"{numero:<10}{calcular_factorial(numero):<10}")

       # Programa principal
       if __name__ == "__main__":
           n = int(input("Ingrese un número natural: "))
           imprimir_factoriales(n)

5. Calcula el valor de 2 elevado a la potencia n usando ciclos para .

        def calcular_potencia_dos(n):
        """
        Calcula 2 elevado a la potencia n usando ciclos.
    
        Parámetros:
        n (int): Potencia a la que se elevará el número 2.
        Retorno:
        int: Resultado de 2^n.
        """
        resultado = 1
        for _ in range(n):
        resultado *= 2
        return resultado

       # Programa principal
       if __name__ == "__main__":
           n = int(input("Ingrese el valor de n: "))
           print(f"2 elevado a la potencia {n} es: {calcular_potencia_dos(n)}")

6. Leer un número natural n, leer otro dato de tipo real xy calcular x^n usando ciclos for. Aviso legal: Trate de no utilizar el operador de potencia (**).

       def calcular_potencia(x, n):
       """
        Calcula x elevado a la potencia n usando ciclos.
    
        Parámetros:
        x (float): Base de la potencia.
        n (int): Exponente de la potencia.
        Retorno:
        float: Resultado de x^n.
        """
        resultado = 1
        for _ in range(n):
        resultado *= x
        return resultado

       # Programa principal
       if __name__ == "__main__":
        x = float(input("Ingrese el valor de x (base): "))
        n = int(input("Ingrese el valor de n (exponente): "))
        print(f"{x} elevado a la potencia {n} es: {calcular_potencia(x, n)}")

7. Diseñe un programa que muestre las tablas de multiplicar del 1 al 9.
   
       def mostrar_tablas():
        """
       Muestra las tablas de multiplicar del 1 al 9.
        """
        for i in range(1, 10):
            print(f"Tabla del {i}")
            print("-" * 15)
            for j in range(1, 11):
                print(f"{i} x {j} = {i * j}")
            print()

       # Programa principal
       if __name__ == "__main__":
            mostrar_tablas()

8. Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Taylor. Nota: use math para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.

       def aproximar_exponencial(x, n):
       """
       Calcula una aproximación de e^x utilizando los primeros n términos de la serie de Taylor.
    
        Parámetros:
            x (float): Valor real para el cual se aproxima la exponencial.
            n (int): Número de términos de la serie de Taylor.
        Retorno:
            float: Aproximación de e^x.
        """
        suma = 0
        for i in range(n):
             suma += x**i / math.factorial(i)
         return suma

       # Programa principal
       if __name__ == "__main__":
            x = float(input("Ingrese el valor de x: "))
            n = int(input("Ingrese el número de términos (n): "))
            aproximacion = aproximar_exponencial(x, n)
            valor_real = math.exp(x)
            diferencia = abs(valor_real - aproximacion)

            print(f"Aproximación de e^{x} con {n} términos: {aproximacion}")
            print(f"Valor real: {valor_real}")
            print(f"Diferencia: {diferencia}")

9. Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.

       def aproximar_seno(x, n):
        """
        Calcula una aproximación de sin(x) utilizando los primeros n términos de la serie de Maclaurin.
    
        Parámetros:
            x (float): Valor real para el cual se aproxima el seno.
            n (int): Número de términos de la serie de Maclaurin.
        Retorno:
        float: Aproximación de sin(x).
        """
        suma = 0
        for i in range(n):
            termino = ((-1)**i * x**(2*i + 1)) / math.factorial(2*i + 1)
            suma += termino
       return suma

        # Programa principal
        if __name__ == "__main__":
            x = float(input("Ingrese el valor de x (en radianes): "))
            n = int(input("Ingrese el número de términos (n): "))
            aproximacion = aproximar_seno(x, n)
            valor_real = math.sin(x)
            diferencia = abs(valor_real - aproximacion)

            print(f"Aproximación de sin({x}) con {n} términos: {aproximacion}")
            print(f"Valor real: {valor_real}")
            print(f"Diferencia: {diferencia}")

   Estos son los 9 codigos documentados en el cuaderno del repo. (los ultimos 2 puntos los hice con ayuda de chatgpt, ya que se me hicieron algo confusos).
