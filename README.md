<!DOCTYPE html>
<html>
<head>
<title>Voce conhece o Brasil?</title>
<body><p>sabemso que o Brasil</p></body>

import random
#test
 
perguntas_fácil = (
 "Quantos estados tem o Brasil?",
 "Qual é a capital do Brasil?",
 "Em qual região está localizada a capital do Brasil?",
 "Quantos estados tem o Sudeste?",
 "Qual é a capital de Minas Gerais?",
 "Quantas regiões tem o Brasil?",
 
 
 )
 
respostas_fácil = (
# ["resposta certa","resposta errada","resposta errada"]
    ["26","22","25"],
    ["Brasilia","Canadá","Goias"],
    ["Centro-Oeste","Sudeste","Norte"],
    ["4","5","6"],
    ["Belo Horizonte","São Paulo","Santa Catarina"],
    ["5","6","7"]
)
 
def main():
    for índice,pergunta in enumerate(perguntas_fácil):
        print(str(índice+1) + ": " + pergunta)
 
        # shuffle embaralha só pra mostrar na tela
        respostas_embaralhas = list(respostas_fácil[índice])
        
        random.shuffle(respostas_embaralhas)
 
        for respostas in respostas_embaralhas:
            print(respostas)
 
        #entrada do usuário
        resposta = input("Qual a resposta?")
        if resposta == respostas_fácil[índice][0]:
            print("+------------+")
            print("|Você acertou|")
            print("+------------+")
        else:
            print("+--------------+")
            print("|tente de novo |")
            print("+--------------+")
 
if __name__ == '__main__':
    main()
 
