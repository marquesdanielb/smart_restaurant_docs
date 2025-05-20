## **1. Tipos de Dados Primitivos e Operadores**

### **Números**

Em Python, os números podem ser inteiros (`int`) ou de ponto flutuante (`float`). Eles são usados para realizar operações matemáticas básicas.
``` python
# Exemplo de números
numero_inteiro = 3
numero_float = 3.5

print(numero_inteiro)  # Saída: 3
print(numero_float)    # Saída: 3.5
```
### **Operações Matemáticas Básicas**
Python suporta as operações matemáticas básicas: adição (`+`), subtração (`-`), multiplicação (`*`), e divisão (`/`).
``` python
# Adição
soma = 1 + 2
print(soma)  # Saída: 3

# Subtração
subtracao = 8 - 1
print(subtracao)  # Saída: 7

# Multiplicação
multiplicacao = 10 * 2
print(multiplicacao)  # Saída: 20

# Divisão (sempre retorna um float)
divisao = 35 / 5
print(divisao)  # Saída: 7.0
```
### **Divisão Inteira (`//`)**

A divisão inteira (`//`) arredonda o resultado para o número inteiro mais próximo, em direção ao infinito negativo.
``` python
# Divisão inteira com números positivos
resultado_positivo = 5 // 3
print(resultado_positivo)  # Saída: 1

# Divisão inteira com números negativos
resultado_negativo = -5 // 3
print(resultado_negativo)  # Saída: -2
```
### **Operação de Módulo (`%`)**
O operador `%` retorna o resto da divisão entre dois números.
``` python
resto = 7 % 3
print(resto)  # Saída: 1

# O sinal do resultado sempre segue o divisor (segundo número)
resto_negativo = -7 % 3
print(resto_negativo)  # Saída: 2
```
### **Exponenciação (`**`)**
``` python
potencia = 2 ** 3
print(potencia)  # Saída: 8
```
### **Precedência de Operadores**

Assim como na matemática, operadores seguem uma ordem de precedência. Parênteses podem ser usados para alterar a ordem.
``` python
# Sem parênteses, a multiplicação é feita primeiro
resultado = 1 + 3 * 2
print(resultado)  # Saída: 7

# Com parênteses, a soma é feita primeiro
resultado_com_parenteses = (1 + 3) * 2
print(resultado_com_parenteses)  # Saída: 8
```
### **Valores Booleanos**

Os valores booleanos (`True` e `False`) representam verdadeiro ou falso.
``` python
verdadeiro = True
falso = False

print(verdadeiro)  # Saída: True
print(falso)       # Saída: False
```
#### **Negação (`not`)**

O operador `not` inverte o valor booleano.
``` python
print(not True)   # Saída: False
print(not False)  # Saída: True
```
#### **Operadores Lógicos (`and`, `or`)**

Os operadores `and` e `or` combinam valores booleanos.
``` python
# AND: Retorna True apenas se ambos forem True
print(True and False)  # Saída: False

# OR: Retorna True se pelo menos um for True
print(False or True)   # Saída: True
```
### **Comparação de Valores**

Operadores de comparação retornam valores booleanos.
``` python
# Igualdade
print(1 == 1)  # Saída: True
print(2 == 1)  # Saída: False

# Desigualdade
print(1 != 1)  # Saída: False
print(2 != 1)  # Saída: True

# Maior que, menor que, maior ou igual, menor ou igual
print(1 < 10)  # Saída: True
print(1 > 10)  # Saída: False
print(2 <= 2)  # Saída: True
print(2 >= 2)  # Saída: True
```
### **Verificar Intervalos**

Você pode verificar se um valor está dentro de um intervalo usando operadores lógicos.
``` python
# Verifica se 2 está entre 1 e 3
print(1 < 2 and 2 < 3)  # Saída: True

# Encadeamento simplifica a sintaxe
print(1 < 2 < 3)  # Saída: True
```
### **Diferença entre `is` e `==`**

- O operador `is` verifica se duas variáveis apontam para o mesmo objeto.
- O operador `==` verifica se os valores dos objetos são iguais.
``` python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)  # Saída: True (mesmo objeto)
print(a is c)  # Saída: False (objetos diferentes)
print(a == c)  # Saída: True (valores iguais)
```
### **Strings**

Strings são sequências de caracteres e podem ser criadas com aspas simples ou duplas.
``` python
texto1 = "Olá"
texto2 = 'Mundo'

# Concatenação
mensagem = texto1 + " " + texto2
print(mensagem)  # Saída: Olá Mundo

# Acesso a caracteres individuais
primeira_letra = mensagem[0]
print(primeira_letra)  # Saída: O

# Tamanho da string
tamanho = len(mensagem)
print(tamanho)  # Saída: 9
```
### **F-Strings**

Desde o Python 3.6, você pode usar f-strings para formatar strings de forma mais simples.
``` python
nome = "João"
idade = 25

# Usando f-string para inserir variáveis
mensagem = f"Meu nome é {nome} e tenho {idade} anos."
print(mensagem)  # Saída: Meu nome é João e tenho 25 anos.
```
### **None**

`None` é um tipo especial de objeto que representa a ausência de valor.
``` python
valor = None

# Comparação com None usa `is`
print(valor is None)  # Saída: True
```
