import tkinter as tk
import math
import random

ventana = tk.Tk()
ventana.title("Ta-Te-Ti vs IA")

tablero = [" "] * 9
botones = []
dificultad = tk.StringVar(value="Dificil")

# ---------- LÓGICA ----------
def hay_ganador(j):
    combos = [
        (0,1,2),(3,4,5),(6,7,8),
        (0,3,6),(1,4,7),(2,5,8),
        (0,4,8),(2,4,6)
    ]
    return any(tablero[a] == tablero[b] == tablero[c] == j for a,b,c in combos)

def hay_empate():
    return " " not in tablero

def minimax(maximizando):
    if hay_ganador("O"):
        return 1
    if hay_ganador("X"):
        return -1
    if hay_empate():
        return 0

    if maximizando:
        mejor = -math.inf
        for i in range(9):
            if tablero[i] == " ":
                tablero[i] = "O"
                mejor = max(mejor, minimax(False))
                tablero[i] = " "
        return mejor
    else:
        mejor = math.inf
        for i in range(9):
            if tablero[i] == " ":
                tablero[i] = "X"
                mejor = min(mejor, minimax(True))
                tablero[i] = " "
        return mejor

def movimiento_ia_dificil():
    mejor_valor = -math.inf
    mejor_mov = None
    for i in range(9):
        if tablero[i] == " ":
            tablero[i] = "O"
            valor = minimax(False)
            tablero[i] = " "
            if valor > mejor_valor:
                mejor_valor = valor
                mejor_mov = i
    return mejor_mov

def movimiento_ia():
    libres = [i for i in range(9) if tablero[i] == " "]

    if dificultad.get() == "Facil":
        return random.choice(libres)

    if dificultad.get() == "Medio":
        if random.random() < 0.5:
            return random.choice(libres)
        else:
            return movimiento_ia_dificil()

    return movimiento_ia_dificil()

# ---------- INTERFAZ ----------
def click(i):
    if tablero[i] != " ":
        return

    tablero[i] = "X"
    botones[i].config(text="X", state="disabled")

    if hay_ganador("X"):
        fin("¡Ganaste! 🎉")
        return
    if hay_empate():
        fin("Empate 😐")
        return

    ventana.after(300, turno_ia)

def turno_ia():
    i = movimiento_ia()
    tablero[i] = "O"
    botones[i].config(text="O", state="disabled")

    if hay_ganador("O"):
        fin("La IA ganó 🤖")
        return
    if hay_empate():
        fin("Empate 😐")

def fin(texto):
    for b in botones:
        b.config(state="disabled")
    etiqueta.config(text=texto)

def reiniciar():
    global tablero
    tablero = [" "] * 9
    etiqueta.config(text="")
    for b in botones:
        b.config(text=" ", state="normal")

# ---------- UI ----------
for i in range(9):
    b = tk.Button(ventana, text=" ", font=("Arial", 24),
                  width=5, height=2,
                  command=lambda i=i: click(i))
    b.grid(row=i//3, column=i%3)
    botones.append(b)

etiqueta = tk.Label(ventana, text="", font=("Arial", 14))
etiqueta.grid(row=3, column=0, columnspan=3)

menu = tk.OptionMenu(ventana, dificultad, "Facil", "Medio", "Dificil")
menu.grid(row=4, column=0, columnspan=3)

btn = tk.Button(ventana, text="Reiniciar", command=reiniciar)
btn.grid(row=5, column=0, columnspan=3)

ventana.mainloop()
