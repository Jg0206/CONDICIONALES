# CONDICIONALES

- **PRESENTADO POR:** JESUS GOYENECHE
- **Email:** Jesus.goyeneche@upb.edu.co
  
REPOSITORIO PARA TRABAJAR EJERCICIOS SOBRE CONDICIONALES.

Problema: Cálculo del Precio de Boletas en el Cine
Descripción del problema:
Un cine local ofrece promociones en las entradas según el horario de la función. Las reglas para determinar el costo de las entradas son las siguientes:

Para cualquier función antes de las 6:00 p.m., las entradas tienen los siguientes precios:

Niños: $ 5000 COP.
Adultos: $ 7500 COP.
Entrada general: $ 10000 COP por persona.
Además, si el total de la compra supera los $50000 COP, el cine regala una crispeta familiar.

Para funciones después de las 6:00 p.m., el precio de la entrada es general:

Entradas del problema:
num_ninos: número de niños en el grupo.
num_adultos: número de adultos en el grupo.
hora_funcion: hora de la función en formato de 24 horas (por ejemplo, 14 para las 2 p.m., 19 para las 7 p.m.).
Salidas esperadas:
El total a pagar por las entradas.
Si se obtiene o no la crispeta familiar.

### Algoritmo para determinar el total a pagar en el cine

1. Iniciar
2. Obtener el número de niños que entrará en la función
3. Obtener el número de adultos que entrará en la función
4. Obtener la hora de la función (0-24)
5. Determinar el total dependiendo de la hora de la funcion:
- Si la hora es menor a 18, entonces: total = num_ninos * 5000 + num_adultos * 7500
- Si la hora es mayor o igual a 18, entonces: total = (num_ninos + num_adultos) * 10000
6. Mostrar total
7. Si el total es mayor a $50000, indicar que se han ganado una crispeta gratis
8. Finalizar

### Pseudocódigo
Program calcularEntradaCine
Start
// Programa para calcular el total de las entradas a cine

Declare Int num_ninos
Declare Int num_adultos
Declare Int hora
Declare Float total

Display "Ingrese el número de niños: "
Input num_ninos
Display "Ingrese el número de adultos: "
Input num_adultos
Display "Ingrese la hora de la función (0 - 23): "
Input hora

// Determinar el total a pagar dependiendo de la hora de la función
If hora < 18 Then
  total = num_ninos * 5000 + num_adultos * 7500
Else
  total = (num_ninos + num_adultos) * 10000
End If

Display "El total a pagar es ", total

//Determinar si el grupo se gana unas crispetas

If total > 50000 Then
Display "Se ha ganado unas crispetas familiar."
End If

Display "Disfrute de la función :)"

End

## CODIGO EN PYTHON

num_ninos = int(input("Ingrese el número de niños: "))
num_adultos = int(input("Ingrese el número de adultos: "))
hora = int(input("Ingrese la hora de la función (0 a 23): "))


if hora < 18:
  total = num_ninos * 5000 + num_adultos + 7500
else:
  total = (num_ninos + num_adultos) * 10000

print("El total a pagar es $", total)


if total >= 50000:
  print("Se ha ganado unas crispetas familiar")

print("Disfrute de la funcion :)")
