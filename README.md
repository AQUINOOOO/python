import random

def comecar_jogo():
    print("=== Jogo de Adivinhação ===")
    numero_secreto = random.randint(1, 100)
    tentativas = 0

    while True:
        try:
            palpite = int(input("Adivinhe um número entre 1 e 100: "))
            tentativas += 1

            if palpite < numero_secreto:
                print("Muito baixo!")
            elif palpite > numero_secreto:
                print("Muito alto!")
            else:
                print(f"Parabéns! Você acertou o número {numero_secreto} em {tentativas} tentativas.")
                break
        except ValueError:
            print("Por favor, digite um número válido.")

if __name__ == "__main__":
    comecar_jogo()
