import turtle
from nltk.tokenize import word_tokenize

# Configuración inicial
window = turtle.Screen()
window.title("Dibujo IA con Turtle")
window.bgcolor("white")

# Crear un objeto Turtle
artist = turtle.Turtle()

# Función para interpretar el comando y dibujar
def interpretar_comando(comando):
    tokens = word_tokenize(comando)
    for token in tokens:
        if token.lower() == "cuadrado":
            dibujar_cuadrado()
        elif token.lower() == "círculo":
            dibujar_circulo()

# Función para dibujar un cuadrado
def dibujar_cuadrado():
    for _ in range(4):
        artist.forward(100)
        artist.right(90)

# Función para dibujar un círculo
def dibujar_circulo():
    artist.circle(50)

# Obtener el comando del usuario
comando_usuario = input("Ingrese el comando para dibujar (por ejemplo, 'cuadrado' o 'círculo'): ")

# Interpretar y dibujar el comando
interpretar_comando(comando_usuario)

# Mantener la ventana abierta
window.mainloop()


<!---
ZOMBIZ18/ZOMBIZ18 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
