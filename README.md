# Proyecto-Programacion-
Silla= 25000
Mesa= 50000
Escritorio= 100000
Pino= 45000
Cedro= 85000
Roble= 90000 


import datetime
def main():
    Datos_comprador()
    Pedidos()
    madera()
    total()


def datos_cliente(Nombre,Id):
     print("Datos del comprador")
     print("Nombre del comprador:" , Nombre)
     print("Id de el comprador", Id)
     print("----------------------------------------")

def Datos_comprador():
    Nombre_cliente=input("ingrese su nombre:")
    Idcliente=int(input("ingrese du ID:"))
    datos_cliente(Nombre_cliente,Idcliente)
    print("Tipos de mueble disponibles= Mesa, Silla y Escritorio")
    

def Tipo_mueble(A,B,C,D):
    mueble= input("Ingrese el tipo de mueble deseado:")
    if mueble=="silla":
        print("Fecha de pedido:" , B)
        print("fecha de entrega:" , C)
    elif mueble== "escritorio":
        print("Fecha de pedido:" ,  B)
        print("fecha de entrega " , D)
    elif mueble== "silla":
        print("Fecha de pedido:",A)
        print("Fecha de entrega",B)

def madera ():
    print("Tipos de madera disponibles: Pino, Cedro y Roble")
    madera_deseada= input("Tipo de madera deseada:")


def precios(): 
    if (Tipo_mueble(A, B, C, D)) =="Silla":
        precio_silla= Silla + (madera()) 
        print("Costo sin iva:",precio_silla)
    elif (Tipo_mueble(A, B, C, D)) =="Mesa":
        precio_mesa= Mesa + (madera()) 
        print("Costo sin iva:",precio_mesa)
    elif (Tipo_mueble(A, B, C, D)) =="Escritorio":
        precio_Escritorio= Escritorio + (madera()) 
        print("Costo sin iva:",precio_Escritorio)

def total ():
    I_V_A= 0.13
    total_sin_I_V_A= precios()
    total_con_I_V_A= precios()*I_V_A+precios()
    print("Precio sin IVA:",total_sin_I_V_A)
    print("Precio Final:",total_con_I_V_A)


def Pedidos():
    Dia_delta=datetime.timedelta(days=5)
    Dia_delta2=datetime.timedelta(days=10)
    Fechadelaorden=datetime.date.today()
    Fechadeentrega=Fechadelaorden + Dia_delta
    Fechadeentrega2=Fechadelaorden+Dia_delta2
    fecha_pedido_mesa=( Dia_delta,Fechadelaorden, Fechadeentrega, Fechadeentrega2)



main()
