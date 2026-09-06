# 📝 Aula 04 — Primeiros comandos em Python

Nesta aula, finalmente comecei a escrever meus primeiros códigos em Python. Aprendi como mostrar mensagens na tela, guardar informações em variáveis e receber dados digitados pelo usuário.

---

## Mostrando uma mensagem na tela

Para mostrar uma mensagem na tela, utilizamos a função `print()`.

```python
print("Olá, mundo!")
```

Resultado:

```text
Olá, mundo!
```

Quando queremos mostrar um texto, precisamos colocá-lo entre aspas. Podemos utilizar aspas simples ou duplas.

```python
print('Estou aprendendo Python!')
print("Estou aprendendo Python!")
```

Os dois comandos apresentam o mesmo resultado.

---

## Textos e números

No Python, textos e números são tratados de maneiras diferentes.

Para mostrar um texto, utilizamos aspas:

```python
print("7 + 4")
```

Resultado:

```text
7 + 4
```

Para realizar uma operação matemática, não devemos utilizar aspas:

```python
print(7 + 4)
```

Resultado:

```text
11
```

Quando colocamos os números entre aspas, o Python passa a tratá-los como textos:

```python
print("7" + "4")
```

Resultado:

```text
74
```

Nesse caso, o Python não realizou uma soma. Ele apenas juntou os dois textos. Esse processo é chamado de **concatenação**.

---

## Variáveis

As variáveis são utilizadas para guardar informações na memória do computador.

```python
nome = "Robert"
idade = 25
peso = 75.8
```

Nesse exemplo, criei três variáveis:

- `nome` guarda um texto;
- `idade` guarda um número inteiro;
- `peso` guarda um número com casas decimais.

O sinal de `=` deve ser entendido como **recebe**.

```python
nome = "Robert"
```

Podemos ler essa linha da seguinte maneira:

> A variável `nome` recebe o texto `"Robert"`.

Para mostrar os valores guardados, podemos utilizar:

```python
print(nome, idade, peso)
```

---

## Recebendo informações do usuário

A função `input()` permite que o usuário digite alguma informação.

```python
nome = input("Qual é o seu nome? ")
```

O texto digitado será guardado dentro da variável `nome`.

Depois, podemos utilizar essa informação em uma mensagem:

```python
nome = input("Qual é o seu nome? ")

print("Olá,", nome)
print("Prazer em conhecer você!")
```

---

## Criando meu primeiro programa

```python
nome = input("Qual é o seu nome? ")
idade = input("Quantos anos você tem? ")
peso = input("Qual é o seu peso? ")

print("Nome:", nome)
print("Idade:", idade)
print("Peso:", peso)
```

Esse programa solicita três informações e depois apresenta tudo o que foi digitado.

---

## Criando e executando um arquivo no Codespaces

Como estou utilizando o GitHub Codespaces, não preciso usar o IDLE apresentado na aula.

Para criar um programa, basta criar um arquivo com a extensão `.py`.

Exemplo:

```text
aula04.py
```

Depois de escrever o código, posso executá-lo clicando no botão `▶️` ou utilizando o terminal:

```bash
python3 aula04.py
```

Sempre que eu quiser testar novamente, basta salvar as alterações e clicar outra vez no botão de executar.

---

## Diferença entre `print()` e `input()`

As duas funções possuem objetivos diferentes:

- `print()` mostra uma informação na tela;
- `input()` solicita e recebe uma informação do usuário.

Exemplo:

```python
nome = input("Digite seu nome: ")
print("Olá,", nome)
```

O `input()` pergunta o nome, enquanto o `print()` apresenta a mensagem com a resposta digitada.

---

# 🎯 Desafios da aula

## Desafio 01 — Mensagem de boas-vindas

Criar um programa que leia o nome de uma pessoa e mostre uma mensagem de boas-vindas.

```python
nome = input("Qual é o seu nome? ")

print("Olá,", nome, "prazer em conhecer você!")
```

---

## Desafio 02 — Data de nascimento

Criar um programa que solicite o dia, o mês e o ano de nascimento de uma pessoa. Depois, o programa deve mostrar a data completa.

```python
dia = input("Em qual dia você nasceu? ")
mes = input("Em qual mês você nasceu? ")
ano = input("Em qual ano você nasceu? ")

print("Você nasceu no dia", dia, "de", mes, "de", ano + ".")
```

---

## Desafio 03 — Soma de dois números

O desafio pede dois números e tenta realizar uma soma.

```python
primeiro_numero = input("Digite o primeiro número: ")
segundo_numero = input("Digite o segundo número: ")

print("A soma é:", primeiro_numero + segundo_numero)
```

Porém, existe um problema: a função `input()` recebe as informações como texto.

Se eu digitar `6` e `3`, o resultado será:

```text
63
```

Isso acontece porque o Python está juntando dois textos em vez de somar dois números.

A conversão desses valores será estudada na próxima aula.

---

## O que aprendi nesta aula?

Nesta aula, aprendi a utilizar meus primeiros comandos em Python:

```python
print()
input()
```

Também entendi como criar variáveis, guardar informações e diferenciar textos de números.

A principal diferença é que os textos ficam entre aspas, enquanto os números utilizados em cálculos não devem ficar.

Com esses conhecimentos, já consigo criar pequenos programas que recebem informações do usuário e mostram resultados na tela.