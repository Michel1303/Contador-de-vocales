# Solicitar texto al usuario
def request_text():
    text = input("Ingrese una frase aquí: ")
    return text  
    
# Buscar vocales y almacenarlas en un array
def find_vocals(text):
    #Contadores
    a = e = i = o = u = 0
    vocals = []
    for x in range(len(text)):
        if(text[x] == 'a'):
            vocals.append(text[x])
            a += 1
        elif(text[x] == 'e'):
            vocals.append(text[x])
            e += 1
        elif(text[x] == 'i'):
            vocals.append(text[x])
            i += 1
        elif(text[x] == 'o'):
            vocals.append(text[x])
            o += 1
        elif(text[x] == 'u'):
            vocals.append(text[x])
            u += 1
        
    if(len(vocals) == 0):
        print("No se encontraron vocales en el texto \n")
    else:
        print("Se encontraron los siguientes datos: ")
        if(a > 0):
            print("a :: ", a)
        if(e > 0):
            print("e :: ", e)
        if(i > 0):
            print("i :: ", i)
        if(o > 0):
            print("o :: ", o)
        if(u > 0):
            print("u :: ", u)
        
    return vocals
    

# Mostrar texto en forma de arreglo
def show_text(vocals):
    print("Arreglo : ", vocals)
    
        
show_text(find_vocals(request_text()))
