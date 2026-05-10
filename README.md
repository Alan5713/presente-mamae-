import tkinter as tk
from tkinter import messagebox

# Criando janela
janela = tk.Tk()
janela.title("Dia das Mães")
janela.geometry("600x400")
janela.configure(bg="#ffd6e7")

# Texto principal
texto = tk.Label(
    janela,
    text="Mãe, resgate seu presente 🎁",
    font=("Arial", 22, "bold"),
    bg="#ffd6e7",
    fg="#7a284b"
)

texto.pack(pady=50)

# Função do botão
def resgatar():
    messagebox.showinfo(
        "Resgatado!",
        "Eu sabia que você preferia o meu abraço!\n\n"
        "💖 Feliz Dia das Mães! 💖\n"
        "Te amo!"
    )

# Mudança ao passar o mouse
def mudar_texto(event):
    btn_presente.config(
        text="Um beijo e abraço 💕",
        bg="#ff8fab"
    )

# Voltar ao normal
def voltar_texto(event):
    btn_presente.config(
        text="Lavo a louça por 1 semana",
        bg="#ff4d8d"
    )

# Botão
btn_presente = tk.Button(
    janela,
    text="Lavo a louça por 1 semana",
    font=("Arial", 14, "bold"),
    bg="#ff4d8d",
    fg="white",
    activebackground="#ff8fab",
    activeforeground="white",
    padx=20,
    pady=10,
    relief="flat",
    cursor="hand2",
    command=resgatar
)

btn_presente.pack(pady=20)

# Eventos do mouse
btn_presente.bind("<Enter>", mudar_texto)
btn_presente.bind("<Leave>", voltar_texto)

# Rodando aplicação
janela.mainloop()
