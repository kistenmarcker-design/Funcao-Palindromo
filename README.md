# Funcao-Palindromo
Cria uma função que verifica se uma palavra ou frase é um palíndromo.
import string

def eh_palindromo(texto):
    # Remove espaços, pontuações e transforma em minúsculas
    texto_limpo = ''.join(
        c.lower() for c in texto if c.isalnum()
    )
    
    # Verifica se é igual ao inverso
    if texto_limpo == texto_limpo[::-1]:
        return "Sim"
    else:
        return "Não"

# Exemplos de uso
print(eh_palindromo("Ame a ema"))           # Sim
print(eh_palindromo("Socorram-me subi no ônibus em Marrocos"))  # Sim
print(eh_palindromo("Python"))              # Não
