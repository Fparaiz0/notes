# Python - ANOTAÇÕES

### For(each ou natural)
 - Pode ser utilizado tanto como for quanto como foreach, dependendo de como for montado:
```python
array = [1,2,3,4,5]
for i in array:
  print(i) # -> aqui ele funciona como um foreach e a saída é: "1,2,3,4,5".

for i in range(5)
  print("Exemplo de for padrão!") # -> neste outro exemplo, com o range(), ele já funciona como um for como conhecemos ($i; $i > 5; $i++), onde ele será executado 5 vezes.
```

### Len
 - Retorna a quantidade de elementos que possui o array:
```python
array = [1,2,3,4,5]
 print(len(array)) # -> retorna 5.
```

### Enumerate
 - Usamos para retornar o índice e o elemento da respectiva posição do array:
```python
array = [1,2,3,4,5]
for indice, elemento in enumerate(array)
 print(f"{indice} : {elemento}")
 # aqui retornaria basicamente isso:
 # 0: 1
 # 1: 2
 # 2: 3
 # 3: 4
 # 4: 5
```

### Append
 - Adiciona um elemento no final da lista:
```python
array = [1,2,3,4,5]
array.append(6)
print(array) # -> retorna: "1,2,3,4,5,6".
```

### Match
 - É como se fosse o switch no PHP:
```python
comando = input("Digite um comando:")
match comando:
 case "ABOUT":
  print("Sobre o sistema.")
 case "QUIT":
  print("Saindo.")
 case _: # o "case_" funciona como se fosse o else e cada "case" anterior um elif.
  print("Comando inválido")
```

### Dicionário
 - São os objetos no python:
```python
dicionario = {
 "nome": "lucas",
 "idade": 20,
 "vivo": true
}

# Métodos para ler os itens de um dicionário:

for chave, valor in dicionario.items(): # O método "items()" retorna o valor e a chave do dicionário.
 print("{chave} : {valor}")

for chave in dicionario.keys(): # O método "keys()" retorna a chave do dicionário.
 print("{chave}")

for valor in dicionario.values(): # O método "values()" retorna o valor do dicionário.
 print("{valor}")
```
