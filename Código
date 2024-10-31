print("A continuación se le van a pedir dos números binarios de 8 bits.")

binarioA = input("Introduce el primero: ")
binarioB = input("Introduce el segundo: ")

## Ahora miro si el número que me han dado esta dentro de los parametros (que tenga 8 bits y que solo tenga 1 o 0)

if len(binarioA) == 8 and len(binarioB) == 8:
    
    validoA = True
    validoB = True

    for caracter in binarioA:
        if caracter != '0' and caracter != '1':
            validoA = False
            print("Uno de los números no es binario.")

    for caracter in binarioB:
        if caracter != '0' and caracter != '1':
            validoB = False
            print("Uno de los números no es binario.")

    if validoA and validoB: ## Una vez comprobado que si cumplen los parametros, se pide su sumar o restar
        
        contadorAcarreo = 0

        sumaoresta = input('¿Quiere sumar o restar? (escriba la palabra "S" o "R"): ')

        if sumaoresta == "S": ## Este es el camino de la suma
            resultado = ""

            for numero in range(7,-1,-1):
                a = int(binarioA[numero]) 
                b = int(binarioB[numero])
                
                suma = a + b + contadorAcarreo

                if suma == 2:
                    resultado = "0" + resultado
                    contadorAcarreo = 1
                elif suma == 3:
                    resultado = "1" + resultado
                    contadorAcarreo = 1
                else:
                    resultado = str(suma) + resultado
                    contadorAcarreo = 0

            print(f"El resultado de la suma es {resultado} y el acarreo es {contadorAcarreo}")

        elif sumaoresta == "R": ## Este es el camino de la resta
            resultado = ""

            for numero in range(7,-1,-1):
                a = int(binarioA[numero]) 
                b = int(binarioB[numero])
                b2 = b + contadorAcarreo
                
                resta = a - b2

                if resta == 0:
                    resultado = "0" + resultado
                    contadorAcarreo = 0
                elif resta == 1:
                    resultado = "1" + resultado
                    contadorAcarreo = 0
                elif resta == -1:
                    resultado = "1" + resultado
                    contadorAcarreo = 1
                elif resta == -2:
                    resultado = "0" + resultado
                    contadorAcarreo = 1
                    
            print(f"El resultado de la resta es {resultado}")
            
        else:
            print("Operación no permitida") ## Este mensaje aparece si se introduce algo distinto a "S" o "R"
else:
    print("El número binario no tiene 8 bits.") ## Este mensaje aparece si se introduce un número que no tiene 8 bits
