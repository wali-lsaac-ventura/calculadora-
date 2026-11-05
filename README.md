# calculadora.py
calculadora básica en python.Puede hacer ecuaciones básicas ya sea sumar,restar, dividir o multiplicar.Ideal para practicar 
def sumar(a,b):
    return a + b
def restar(a,b):
    return a - b
def multiplicar(a,b):
    return a * b
def dividir(a,b):
    return a / b

historial= []
print("——CALCULADORA——")
while True:
    
    entrada = input("Escribe un numero o escribe historial: ")

    if entrada == "historial":
        for cuenta in historial:
            print(cuenta)
        continue

    pnum = float(entrada)

    snum = float(input("Segundo numero: "))
    op = input("Operacion: + - / * ")
    
    if op == "+":
        resultado = sumar(pnum, snum)
    elif op == "-":
        resultado = restar(pnum, snum)
    elif op == "*":
        resultado = multiplicar(pnum, snum)
    elif op == "/": 
        if snum == 0:
            resultado = "error"
        else:
            resultado = dividir(pnum, snum)

    
    print(resultado)
    historial.append(f"{pnum} {op} {snum} = {resultado}")

    seguir = input("¿Quieres seguir? si o no?: ")
    if seguir == "no":
        break
