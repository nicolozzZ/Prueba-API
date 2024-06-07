import webbrowser, requests, ast

def alt():
    print('ingrese cuanto posts quieres, solo puede hasta 100 posts')
    n = input() 
    num = int(n)
    if num<0 or num>100:
        print('el numero de posts que solicitas no es valido') 
        return alt()
    else:
        listForPost = requests.get('https://jsonplaceholder.typicode.com/posts')
        listForPost.raise_for_status
        listForPost = listForPost.text
        print (listForPost) #lo que me tira en la consola es una lista porque empieza con []. Me olvide el metodo que me acuerdo que es como el str(),int(),etc. Pero el problema es que no lo encuentro en el libro.
        file = open('dlXPrimes.json','w')
        file2 = open('dlXNotPrimes.json','w')
        for i in listForPost:
            file.write(str(i))
            file2.write(str(i))
        return 'los posts ya estan guardados en los archivos'

print(alt())
