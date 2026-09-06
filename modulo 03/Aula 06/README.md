# 📝 Fase 06 — Tipos primitivos e saída de dados

Nesta aula, aprendi que os dados utilizados pelo Python podem possuir tipos diferentes.

Também entendi por que o programa da aula anterior juntava dois números em vez de realizar a soma.

---

## O problema da aula anterior

Na aula anterior, tentei criar um programa que recebesse dois números e mostrasse a soma entre eles:

```python
n1 = input('Digite o primeiro número: '))
n2 = input('Digite o segundo número: '))
s = n1 + n2

print('A soma é', s)
```

Se eu digitasse `3` e `2`, o resultado seria:

```text
A soma é: 32
```

Isso acontece porque a função `input()` recebe os dados como texto, mesmo quando digitamos um número.

Nesse caso, o sinal de `+` não realizou uma soma. Ele apenas juntou os dois textos.

---

## Convertendo um texto para número

Para conseguir realizar a soma, preciso converter os valores recebidos pelo `input()` para números inteiros.

Para isso, utilizo a função `int()`:

```python
n1 = int(input('Digite o primeiro número: '))
n2 = int(input('Digite o segundo número: '))
s = n1 + n2

print('A soma é', s)
```

Agora, se eu digitar `3` e `2`, o resultado será:

```text
A soma é: 5
```

Dessa vez, os valores foram convertidos para números inteiros antes da soma.

---

## Tipos primitivos

Os quatro tipos primitivos apresentados nesta aula foram:

- `int` — números inteiros;
- `float` — números com casas decimais;
- `bool` — valores lógicos;
- `str` — textos.

---

## Tipo `int`

O tipo `int` representa números inteiros, ou seja, números sem casas decimais.

```python
idade = 25
quantidade = 10
saldo = -5
```

São exemplos de números inteiros:

```text
5
-10
0
250
```

Para converter um valor para inteiro, utilizamos:

```python
numero = int(input("Digite um número inteiro: "))
```

---

## Tipo `float`

O tipo `float` representa números com casas decimais.

```python
peso = 75.8
altura = 1.75
temperatura = -2.5
```

No Python, utilizamos um ponto para separar as casas decimais:

```python
preco = 15.50
```

Não devemos utilizar vírgula:

```python
preco = 15,50
```

Para receber um número decimal, utilizamos:

```python
peso = float(input("Digite seu peso: "))
```

---

## Tipo `bool`

O tipo `bool` representa um valor lógico. Ele aceita apenas duas possibilidades:

```python
True
False
```

É importante escrever a primeira letra com maiúscula.

Exemplo:

```python
aprovado = True
finalizado = False
```

---

## Tipo `str`

O tipo `str` representa textos, também chamados de strings.

```python
nome = "Robert"
cidade = "Salvador"
```

Os textos devem ficar entre aspas simples ou duplas:

```python
curso = 'Python'
curso = "Python"
```

Até mesmo um número será considerado texto se estiver entre aspas:

```python
numero = "25"
```

Nesse caso, o valor não poderá ser utilizado diretamente em uma operação matemática.

---

## Descobrindo o tipo de um valor

A função `type()` mostra o tipo de um valor ou de uma variável.

```python
valor = input("Digite alguma coisa: ")

print(type(valor))
```

Mesmo que eu digite um número, o resultado será:

```text
<class 'str'>
```

Isso confirma que o `input()` recebe as informações como texto.

Se eu fizer a conversão:

```python
valor = int(input("Digite um número: "))

print(type(valor))
```

O resultado será:

```text
<class 'int'>
```

---

## Formatando a saída

Na aula, também aprendi outra forma de colocar valores dentro de uma mensagem.

```python
n1 = int(input('Digite o primeiro número: '))
n2 = int(input('Digite o segundo número: '))
s = n1 + n2

print("A soma entre {} e {} é igual a {}.".format(n1, n2, s))
```

As chaves `{}` reservam os lugares onde os valores serão colocados.

O método `.format()` recebe os valores na mesma ordem em que devem aparecer.

Exemplo de resultado:

```text
A soma entre 5 e 3 é igual a 8.
```

---

## Métodos para testar uma string

O Python possui alguns métodos que permitem analisar o conteúdo de um texto.

```python
valor = input("Digite alguma coisa: ")
```

### É numérico?

```python
print(valor.isnumeric())
```

### Possui somente letras?

```python
print(valor.isalpha())
```

### Possui letras ou números?

```python
print(valor.isalnum())
```

### Possui somente espaços?

```python
print(valor.isspace())
```

### Está completamente em letras maiúsculas?

```python
print(valor.isupper())
```

### Está completamente em letras minúsculas?

```python
print(valor.islower())
```

### Está capitalizado?

```python
print(valor.istitle())
```

Esses métodos retornam `True` ou `False`.

---

# 🎯 Desafios da aula

## Desafio 03 — Somando dois números

Criar um programa que leia dois números e mostre a soma entre eles.

```python
numero1 = int(input("Digite o primeiro número: "))
numero2 = int(input("Digite o segundo número: "))

soma = numero1 + numero2

print("A soma entre {} e {} é igual a {}.".format(numero1, numero2, soma))
```

---

## Desafio 04 — Analisando um valor

Criar um programa que leia alguma coisa pelo teclado e apresente todas as informações possíveis sobre o valor digitado.

```python
valor = input("Digite alguma coisa: ")

print("O tipo primitivo desse valor é:", type(valor))
print("Possui somente espaços?", valor.isspace())
print("É um número?", valor.isnumeric())
print("Possui somente letras?", valor.isalpha())
print("Possui letras ou números?", valor.isalnum())
print("Está em letras maiúsculas?", valor.isupper())
print("Está em letras minúsculas?", valor.islower())
print("Está capitalizado?", valor.istitle())
```

---

## Executando no Codespaces

Salvei o programa em um arquivo com a extensão `.py`.

Exemplo:

```text
aula06.py
```

Para executá-lo pelo terminal do GitHub Codespaces:

```bash
python3 aula06.py
```

Também posso abrir o arquivo e clicar no botão `▶️`.

---

## O que aprendi nesta aula?

Nesta aula, entendi que o Python precisa saber qual tipo de dado está sendo utilizado.

Aprendi os quatro tipos primitivos básicos:

```python
int
float
bool
str
```

Também aprendi a utilizar `type()` para descobrir o tipo de um valor e fazer conversões utilizando funções como `int()` e `float()`.

A parte mais importante foi entender que o `input()` sempre recebe o valor como texto. Portanto, quando eu quiser fazer um cálculo, preciso converter esse texto para um tipo numérico.