# Laberinto

Mi direccion de GitHub para este repositorio es la siguiente: [GitHUb](https://github.com/jzazooro/Laberinto.git)
https://github.com/jzazooro/Laberinto.git

Hemos diseñado y programado un laberinto y sus multiples posibilidades para que un jugador se pueda enfrentar a el
El diagrama de flujo que tenemos en nuestro codigo es el siguiente: 

![Diagrama de flujo laberinto](https://github.com/jzazooro/Laberinto/blob/main/DIAGRAMADEFLUJOLABERINTO.jpg)

'''laberinto= [
    ['E', 'M', 'M', 'M', 'M'],
    ['C', 'M', 'C', 'C', 'C'],
    ['C', 'M', 'C', 'M', 'C'],
    ['C', 'C', 'C', 'M', 'C'],
    ['M', 'M', 'M', 'M', 'S']
    ]
x=0
y=0
print((laberinto[y])[x])
print("Te encuentras en la entrada, posicion (0, 0)")
caminorecorrido=["", "", "", "", "", "", "", "", "", "", "", "", ""]
i=0
while (laberinto[y])[x] == 'C' or 'E':
    eleccion= input("Por favor seleccione cual sera su siguiente movimiento: izquierda, derecha, arriba, abajo: ")
    if eleccion== "izquierda" or "derecha" or "arriba" or "abajo":
        print("has seleccionado {}".format(eleccion))
        caminorecorrido[i]=eleccion
        i=i+1
    if eleccion=="izquierda":
        x=x-1
        y=y
    if eleccion=="derecha":
        x=x+1
        y=y
    if eleccion=="arriba":
        x=x
        y=y+1
    if eleccion=="abajo":
        x=x
        y=y-1
    else:
        print("Lo siento, no has escogido una de las cuatro opciones posibles")
        x=x
        y=y
    print("te encuentras en la casilla ({},{})".format(x,y))
    if(laberinto[y])[x]=='C' or 'E':
        print("Puedes continuar en el laberinto")
    elif(laberinto[y])[x]=='S':
        print("Enhorabuena has conseguido salir del laberinto")
        break
    else:
        print("Te has chocado con un muro \nreinicia el programa para poder completar el laberinto")
print("Has realizado los siguientes movimientos: ", (caminorecorrido))
