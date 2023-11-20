import math as m

while True:  # Loop externo para permitir múltiplas escolhas
    print("Menu:\n1. Quadrado\n2. Retângulo\n3. Triângulo equilátero\n4. Trapézio Isósceles\n5. Losango\n6. Polígono regular\n7. Círculo\n8. Sair")
    print()
    opção = 0
    while opção <= 0 or opção > 7:
        opção = int(input("Digite a opção desejada: "))
        print()
        if opção <= 0 or opção > 7:
            print("Opção inválida")
    # Zerar as variáveis antes de entrar no loop específico para evitar reutilização de valores antigos
    h = 0
    l = 0
    B = 0
    b = 0
    D = 0
    d = 0
    n = 0
    r = 0
    S = -1
    if opção == 1:
        while l <= 0:
            l = float(input("Digite o valor do lado: "))
            if l <= 0:
                print("Valor inválido")
        print(f"\nA área do quadrado é: {(l*l)}")
        print(f"O perímetro do quadrado é: {(4*l)}")
    elif opção == 2:
        while l <= 0:
            l = float(input("Digite o valor do lado: "))
            if l <= 0:
                print("Valor inválido")
        while h <= 0:
            h = float(input("Digite o valor da altura: "))
            if h <= 0:
                print("Valor inválido")
        print(f"\nA área do retângulo é: {(l*h)}")
        print(f"O perímetro do retângulo é: {(2*l+2*h)}")
    elif opção == 3:
        while l <= 0:
            l = float(input("Digite o valor do lado: "))
            if l <= 0:
                print("Valor inválido")
        print()
        print(f"A área do triângulo é: {round((m.sqrt(3)/4)*l*l, 2)}")
        print(f"O perimetro do triângulo é: {(3*l)}")
    elif opção == 4:
        while B <= 0:
            B = float(input("Digite o valor da Base maior: "))
            if B <= 0:
                print("Valor inválido")
        while b <= 0:
            b = float(input("Digite o valor da base menor: "))
            if b <= 0:
                print("Valor inválido")
        while h <= 0:
            h = float(input("Digite o valor da altura: "))
            if h <= 0:
                print("Valor inválido")
        L1 = (B-b)/2
        L2 = m.sqrt(L1**2+h**2)
        print()
        print(f"A área do trapézio é: {(((B+b)*h)/2)}")
        print(f"O perimetro do trapézio  é: {(B+b+L2*2)}")
    elif opção == 5:
        while D <= 0:
            D = float(input("Digite o valor da Base maior: "))
            if D <= 0:
                print("Valor inválido")
        while d <= 0:
            d = float(input("Digite o valor da base menor: "))
            if d <= 0:
                print("Valor inválido")
        L1 = m.sqrt((D/2)**2+(d/2)**2)
        print()
        print(f"A área do losango é: {((D*d)/2)}")
        print(f"O perimetro do losango é: {round((L1*4),2)}")
    elif opção == 6:
        while n <= 0:
            n = float(input("Digite o núrmero de lados: "))
            if n <=0:
                print("Número inválido")
        while l <= 0:
            l = float(input("Digite valor do lado: "))
            if l <=0:
                print("Valor inválido")
        a = l/(2*(m.tan(m.pi/n)))
        P = n*l
        print()
        print(f"A área do poligono regular é: {round((P*a/2),2)}")
        print(f"O perimetro do poligono regular é: {(P)}")
    elif opção == 7:
        while r <= 0:
            r = float(input("Digite valor do raio: "))
            if r <=0:
                print("Valor inválido")
        print()
        print(f"A área do circulo é: {round((m.pi*r*r),2)}")
        print(f"O perimetro do circulo é: {round((2*m.pi*r),2)}")
    print()
    resposta = input("\nDeseja calcular novamente? (S para Sim, qualquer outra tecla para Não): ")
    if resposta != 'S':
        break 

print("Fim")
