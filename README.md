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
