Python tem uma função print:
``` python
print("Sou Python. Prazer em conhecê-lo!")  # => Sou Python. Prazer em conhecê-lo!
```
Por padrão, a função print também imprime uma nova linha no final.

Use o argumento opcional 'end' para alterar a string final.
``` python
print("Olá, Mundo", end="!")  # => Olá, Mundo!
```

Maneira simples de obter dados de entrada do console
``` python
input_string_var = input("Digite alguns dados: ")  # Retorna os dados como uma string
```

## Não há declarações, apenas atribuições.
A convenção para nomear variáveis é o estilo snake_case
``` python
some_var = 5
some_var  # => 5
```

## Acessar uma variável não atribuída anteriormente é uma exceção.

## if pode ser usado como uma expressão equivalente ao operador ternário '? :' em C
``` python
"yay!" if 0 > 1 else "nay!"  # => "nay!"
```

## Listas armazenam sequências
``` python
li = []
```
## Você pode começar com uma lista pré-preenchida
``` python
other_li = [4, 5, 6]
```

## Adicione elementos ao final da lista com append
``` python
li.append(1)    # li agora é [1]
li.append(2)    # li agora é [1, 2]
li.append(4)    # li agora é [1, 2, 4]
li.append(3)    # li agora é [1, 2, 4, 3]
```
## Remova do final com pop
``` python
li.pop()        # => 3 e li agora é [1, 2, 4]
```
## Vamos colocá-lo de volta
``` python
li.append(3)    # li agora é [1, 2, 4, 3] novamente.
```

## Acesse uma lista como você faria com qualquer array
``` python
li[0]   # => 1
```
## Veja o último elemento
``` python
li[-1]  # => 3
```

## Tentar acessar fora dos limites gera um IndexError
``` python
li[4]  # Gera um IndexError
```

## Você pode visualizar intervalos com a sintaxe de fatiamento (slice).
## O índice inicial é incluído, o índice final não está incluído.
``` python
li[1:3]   # Retorne a lista do índice 1 ao 3 => [2, 4]
li[2:]    # Retorne a lista a partir do índice 2 => [4, 3]
li[:3]    # Retorne a lista desde o início até o índice 3 => [1, 2, 4]
li[::2]   # Retorne a lista selecionando elementos com um passo de 2 => [1, 4]
li[::-1]  # Retorne a lista na ordem inversa => [3, 4, 2, 1]
```
## Use qualquer combinação desses para criar fatias avançadas
## li[início:fim:passo]

## Faça uma cópia superficial com fatias
``` python
li2 = li[:]  # => li2 = [1, 2, 4, 3], mas (li2 is li) resultará em False.
```

## Remova elementos arbitrários de uma lista com "del"
``` python
del li[2]  # li agora é [1, 2, 3]
```

## Remova a primeira ocorrência de um valor
``` python
li.remove(2)  # li agora é [1, 3]
li.remove(2)  # Gera um ValueError, pois 2 não está na lista
```

## Insira um elemento em um índice específico
``` python
li.insert(1, 2)  # li agora é [1, 2, 3] novamente
```

## Obtenha o índice do primeiro item encontrado que corresponde ao argumento
``` python
li.index(2)  # => 1
li.index(4)  # Gera um ValueError, pois 4 não está na lista
```

## Você pode somar listas
## Observe: os valores de li e other_li não são modificados.
``` python
li + other_li  # => [1, 2, 3, 4, 5, 6]
```

## Concatene listas com "extend()"
``` python
li.extend(other_li)  # Agora li é [1, 2, 3, 4, 5, 6]
```

## Verifique a existência em uma lista com "in"
``` python
1 in li  # => True
```

## Examine o comprimento com "len()"
``` python
len(li)  # => 6
```
## Tuplas são como listas, mas são imutáveis.
``` python
tup = (1, 2, 3)
tup[0]      # => 1
tup[0] = 3  # Gera um TypeError
```

## Observe que uma tupla de comprimento um precisa ter uma vírgula após o último elemento,
## mas tuplas de outros comprimentos, mesmo zero, não precisam.
``` python
type((1))   # => <class 'int'>
type((1,))  # => <class 'tuple'>
type(())    # => <class 'tuple'>
```

## Você pode fazer a maioria das operações de lista em tuplas também
``` python
len(tup)         # => 3
tup + (4, 5, 6)  # => (1, 2, 3, 4, 5, 6)
tup[:2]          # => (1, 2)
2 in tup         # => True
```

## Você pode desempacotar tuplas (ou listas) em variáveis
``` python
a, b, c = (1, 2, 3)  # a agora é 1, b agora é 2 e c agora é 3
```
## Você também pode fazer desempacotamento estendido
``` python
a, b, c = (1, 2, 3, 4)  # a agora é 1, b agora é [2, 3] e c agora é 4
```
## Tuplas são criadas por padrão se você omitir os parênteses
``` python
d, e, f = 4, 5, 6  # A tupla (4, 5, 6) é desempacotada nas variáveis d, e, f
```
## respectivamente, de modo que d = 4, e = 5 e f = 6
## Agora veja como é fácil trocar dois valores
``` python
e, d = d, e  # d agora é 5 e e agora é 4
```

## Dicionários armazenam mapeamentos de chaves para valores
``` python
empty_dict = {}
```
## Aqui está um dicionário preenchido
``` python
filled_dict = {"um": 1, "dois": 2, "três": 3}
```

Observe que as chaves dos dicionários precisam ser tipos imutáveis. Isso é para garantir que
a chave possa ser convertida em um valor hash constante para buscas rápidas.
## Tipos imutáveis incluem inteiros, floats, strings, tuplas.
``` python
invalid_dict = {[1,2,3]: "123"}  # => Gera um TypeError: tipo não hashable: 'list'
valid_dict = {(1,2,3):[1,2,3]}   # Os valores podem ser de qualquer tipo, no entanto.
```

## Acesse valores com []
``` python
filled_dict["um"]  # => 1
```

Obtenha todas as chaves como um iterável com "keys()". Precisamos envolver a chamada em list()
para transformá-la em uma lista. Falaremos sobre isso depois. Observe - para versões do Python
<3.7, a ordem das chaves do dicionário não é garantida. Seus resultados podem não coincidir exatamente com o exemplo abaixo. No entanto, a partir do Python 3.7, os itens do dicionário mantêm a ordem em que foram inseridos no dicionário.
``` python
list(filled_dict.keys())  # => ["três", "dois", "um"] no Python <3.7
list(filled_dict.keys())  # => ["um", "dois", "três"] no Python 3.7+
```


## Obtenha todos os valores como um iterável com "values()". Mais uma vez, precisamos envolvê-lo em list() para obtê-lo do iterável. Observe - O mesmo acima sobre a ordenação das chaves.
``` python
list(filled_dict.values())  # => [3, 2, 1] no Python <3.7
list(filled_dict.values())  # => [1, 2, 3] no Python 3.7+
```

## Verifique a existência de chaves em um dicionário com "in"
``` python
"um" in filled_dict  # => True
1 in filled_dict      # => False
```

## Procurar uma chave inexistente é um KeyError
``` python
filled_dict["quatro"]  # KeyError
```

## Use o método "get()" para evitar o KeyError
``` python
filled_dict.get("um")      # => 1
filled_dict.get("quatro")     # => None
```
## O método get suporta um argumento padrão quando o valor está ausente
``` python
filled_dict.get("um", 4)   # => 1
filled_dict.get("quatro", 4)  # => 4
```

## "setdefault()" insere no dicionário apenas se a chave fornecida não estiver presente
``` python
filled_dict.setdefault("cinco", 5)  # filled_dict["cinco"] é definido como 5
filled_dict.setdefault("cinco", 6)  # filled_dict["cinco"] ainda é 5
```

## Adicionar ao dicionário
``` python
filled_dict.update({"quatro":4})  # => {"um": 1, "dois": 2, "três": 3, "quatro": 4}
filled_dict["quatro"] = 4         # outra maneira de adicionar ao dicionário
```

## Remova chaves de um dicionário com del
``` python
del filled_dict["um"]  # Remove a chave "um" do dicionário preenchido
```

## A partir do Python 3.5, você também pode usar opções adicionais de desempacotamento
``` python 
{"a": 1, **{"b": 2}}  # => {'a': 1, 'b': 2}
{"a": 1, **{"a": 2}}  # => {'a': 2}
```


# Conjuntos armazenam... bem, conjuntos
empty_set = set()
# Inicialize um conjunto com vários valores.
some_set = {1, 1, 2, 2, 3, 4}  # some_set agora é {1, 2, 3, 4}

# Semelhante às chaves de um dicionário, os elementos de um conjunto precisam ser imutáveis.
invalid_set = {[1], 1}  # => Gera um TypeError: tipo não hashable: 'list'
valid_set = {(1,), 1}

# Adicione mais um item ao conjunto
filled_set = some_set
filled_set.add(5)  # filled_set agora é {1, 2, 3, 4, 5}
# Conjuntos não têm elementos duplicados
filled_set.add(5)  # permanece como antes {1, 2, 3, 4, 5}

# Faça a interseção de conjuntos com &
other_set = {3, 4, 5, 6}
filled_set & other_set  # => {3, 4, 5}

# Faça a união de conjuntos com |
filled_set | other_set  # => {1, 2, 3, 4, 5, 6}

# Faça a diferença de conjuntos com -
{1, 2, 3, 4} - {2, 3, 5}  # => {1, 4}

# Faça a diferença simétrica de conjuntos com ^
{1, 2, 3, 4} ^ {2, 3, 5}  # => {1, 4, 5}

# Verifique se o conjunto à esquerda é um superconjunto do conjunto à direita
{1, 2} >= {1, 2, 3}  # => False

# Verifique se o conjunto à esquerda é um subconjunto do conjunto à direita
{1, 2} <= {1, 2, 3}  # => True

# Verifique a existência em um conjunto com in
2 in filled_set   # => True
10 in filled_set  # => False

# Faça uma cópia superficial
filled_set = some_set.copy()  # filled_set é {1, 2, 3, 4, 5}
filled_set is some_set        # => False