# Maximal_numero
# Se dice que M es el número maximal para N, si M es el mayor número que puede formarse usando los dígitos de N.
Ejemplos:
    ● si N=5345, el número maximal M es 5543
    ● si N=2756, el número maximal M es 7652.
❖ Escriba un programa en Pascal para que lea dos números naturales a y b, y muestre por pantalla todos los números comprendidos entre a y b junto con su maximal.

Por ejemplo: para a = 309 y b = 312, el programa deberá mostrar por pantalla:
    309  930
    310  310
    311  311
    312  321

El programa debe estar dividido en sub-problemas (funciones: Aparece(dando un dígito y un número indica cuántas veces está d en el número) y Max

Programa global:
    Variables:
        a,b (entrada): numeros naturales ingresados por el usuario.
        i(bucle y salida): variable del bucle for; que luego es tomada por la función maximal().
        max: variable encargada de llamar a la función maximal().
    Bucle:
        repeticion condicional for: Utilizamos esta repeticion, ya que previamente conocemos el alcanse de repeticioines que busca el iterador, (desde a hasta b), dentro del mismo usamos la variable max y le damos como parámetro el valor del iterador i, para posteriormente mostrarlo.
    Primitivas:
        validarDato(): dando de paŕametro las variables a y b.
        maximal(): utilizando de parámetro la variable i.
        aparece(): aplicamos en la funcion maximal(), utilizando la variable local dig y la variable global i . 
Primitivas:
    Procedimiento validarDato():
        Variables:
            aux: utilizado como auxiliar, para modificar el valor de la variable a por el valor de la variable b.
            a,b: parámetros por referencia del programa global, que al ingresar al procedimiento evalúa una condicion, y en caso de que a>b cambian su valor.
    Función aparece(): Esta función se encarga que encontrar un digito dentro de un numero y retornar la cantidad de veces que aparece dicho digito en el numero. Aparece(), toma el valor de cant. Este bucle se repite, hasta que la descomposición del numero 'num', sea igual a 0.
        Variables:
        num: parámetro por valor; numero donde se busca el digito 'dig' en particular.
        dig: parámetro por valor; es el dígito que se busca en el numero 'num'.
        cant: variable local; suma cada ves que la condicion de (dig=ultimo) sea verdadero.
        ultimo: variable local; extrae el ultimo digito del numero 'num'.
    Función maximal(): Función encargada de rotar el numero 'num' (de ser necesario), y retornar el numero maximo que podemos obtener con los dígitos de 'num'.
        Variables:
        num:variable global del programa, en este caso toma el valor de 'i'.
        cant:variable local; encargada de contar, cuantas vece se repite un digito 'dig' en el numero 'num'.
        max:variable local; toma el valor maximo alcanzado por el numero ingresado 'num'.
        dig:variable local, iteradora; ademas de variable toma el rol de iteradora en reversa de 9 a 0, para retornar de mayor a menor entre el numero 'num'.
        i:variable local, iteradora; iterador encargado de sumar y modificar el numero 'num' de ser necesario.
        
